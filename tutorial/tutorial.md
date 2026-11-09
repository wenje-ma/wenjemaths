# 交接文档: 在本机搭好 wenje-ma 仓库的阅读环境

读者是操作这台电脑的 AI. 按 S1 到 S6 的顺序执行, 每步跑完判据再进下一步, 判据不过就按该步的失败分支处理, 不要凭猜继续. 全程只读: 不改仓库文件, 不 commit, 不 push.

## 0 验收标准

六条全部满足才算交付完成.

| 编号 | 达到的状态 | 判据 | 期望结果 |
| --- | --- | --- | --- |
| 1 | GitHub 账号可登录 | 打开 `https://github.com/settings/profile` | 页面显示用户名 |
| 2 | Git 可用 | `git --version` | `git version 2.x` |
| 3 | VSCode 可用 | `code --version` | 输出一行版本号 |
| 4 | MPE 插件已装 | `code --list-extensions` | 含 `shd101wyy.markdown-preview-enhanced` |
| 5 | 能克隆任意仓库 | `git -C <路径> rev-parse --abbrev-ref HEAD` | `main` |
| 6 | 全量 md 齐且能渲染 | 第 6.4 节两条计数命令, 加第 7 节抽样预览 | `25` 与 `942`, 公式排版正常 |

## 1 前提与事实

- 系统: Windows 10 或 11, x64, 有管理员权限, 网络能到 `github.com`.
- 存放根目录: 有 D 盘用 `D:\wenje-ma`, 只有 C 盘用 `C:\wenje-ma`. 全英文, 无空格. 下面的命令用 `$root` 指代它, 每段命令执行前先在当前终端里 `$root = "D:\wenje-ma"` 赋值, 或直接把 `$root` 换成真实路径.
- 每个仓库是独立的 git 仓库, 远端统一 `https://github.com/wenje-ma/<仓库名>.git`, 默认分支一律 `main`.
- 可以匿名克隆的公开仓库共 25 个, 合计 942 个 md.
- 这 942 个 md 全部 UTF-8 无 BOM, 行尾 CRLF. 公式只有 `$...$` 与 `$$...$$` 两种, 表格是标准 GFM, 没有 mermaid 与自定义容器.
- 目录惯例: `<仓库>\homework-cn\weekN.md` 中文习题, `homework-en\weekN.md` 英文版, `textbooks\` 教材与讲课稿, 部分仓库另有 `figures\`, `codes\`, `tex\`.
- 参考库: `wenjemaths\forced\` 是条目库, 术语与符号口径以它为准.

## 2 S1 注册 GitHub 账号

这三项必须由本人完成: 邮箱验证码, 人机验证, 密码. AI 只负责把页面打开并说明要点.

1. 打开 `https://github.com/signup`.
2. 用户名用全小写英文字母加数字, 不要中文和空格.
3. 邮箱收验证码并填回, 完成人机验证.
4. 登录后访问 `https://github.com/settings/profile`.

判据: 页面显示用户名, 右上角有头像.

说明: 公开仓库匿名就能克隆, 账号不是克隆的前提, 注册的用途是登录后访问需要授权的仓库, 提 issue, 加星.

失败分支: 页面超时或打不开 → 换网络后重试, 不要用第三方代注册服务; 收不到验证码 → 先查垃圾邮件目录, 再核对邮箱是否填错; 用户名占用 → 加数字重试.

## 3 S2 安装 Git

```powershell
winget install --id Git.Git -e --source winget --accept-package-agreements --accept-source-agreements
```

备选: 打开 `https://git-scm.com/download/win` 下载安装包, 全部选项保持默认, PATH 那一页选 `Git from the command line and also from 3rd-party software`.

判据: 新开一个终端窗口, 运行 `git --version`, 输出 `git version 2.x`.

失败分支:

- 提示 `不是内部或外部命令` → 终端是安装前开的, 关掉重开; 仍旧 → 确认 `C:\Program Files\Git\cmd` 在 PATH; VSCode 里可另设 `git.path` 指向 `C:\Program Files\Git\cmd\git.exe`.
- 找不到 winget → 在 Microsoft Store 更新 `应用安装程序`.

可选, 仅提交时需要: `git config --global user.name "名字"` 与 `git config --global user.email "邮箱"`.

## 4 S3 安装 VSCode

```powershell
winget install --id Microsoft.VisualStudioCode -e --source winget --accept-package-agreements --accept-source-agreements
```

备选: `https://code.visualstudio.com/` 下 User Installer, 安装时保持默认勾选.

判据: `code --version` 输出一行版本号. 若先出现 `crashpad ... TransactNamedPipe` 之类的报错行, 那是 Windows 下的噪声, 不算失败.

失败分支:

- 提示 `code` 不是命令 → 在 VSCode 里按 `Ctrl+Shift+P` 执行 `Shell Command: Install 'code' command in PATH`; 或用完整路径 `"%LOCALAPPDATA%\Programs\Microsoft VS Code\bin\code.cmd"`.
- 装到了自定义目录时, 同上, 用实际 `bin\code.cmd` 的路径.

非 Windows: macOS 用 `brew install --cask visual-studio-code`, Linux 用包管理器装 code, 之后 `code` 命令相同, 根目录改成 `~/wenje-ma`.

## 5 S4 安装 MPE 插件

```powershell
code --install-extension shd101wyy.markdown-preview-enhanced
```

判据: `code --list-extensions --show-versions` 里出现 `shd101wyy.markdown-preview-enhanced@0.8.x`.

必要前置: 该插件未声明支持未信任工作区, 在 Restricted Mode 下会被禁用, 表现是按预览没反应或白屏. 两个解法, 任选其一:

- 打开文件夹时弹窗问信任, 选 `Yes, I trust the authors`.
- 把用户设置 `security.workspace.trust.enabled` 改为 `false`.

快捷键注意: `Ctrl+K V` 与 VSCode 自带预览冲突, 可能打开的是自带那个. 要确定用的是 MPE, 走命令面板 `Ctrl+Shift+P` → `Markdown Preview Enhanced: Open Preview to the Side`.

自测: 新建 `test.md`, 写入下面两行, 用上面的 MPE 命令打开预览.

```markdown
行内公式 $\frac{1}{2}$, 行间公式:
$$x^{2}+y^{2}=1$$
```

判据: 预览里是带横线的分式与带上标的公式, 不是 `\frac` 原文. 验证完删掉 `test.md`.

失败分支: 预览空白 → 按上面的信任两条处理; 公式仍是原文 → 你在看左侧编辑区, 预览窗格未开, 重跑 MPE 命令; 若公式区显示红色报错, 说明 KaTeX 不认某个宏, 把 `markdown-preview-enhanced.mathRenderingOption` 改为 `MathJax` 再开预览, 注意 MathJax 首次渲染要从 CDN 拉脚本, 需联网.

## 6 S5 克隆仓库

### 6.1 单个仓库

```powershell
New-Item -ItemType Directory -Force -Path "$root" | Out-Null
git clone --depth 1 "https://github.com/wenje-ma/probability.git" "$root\probability"
```

判据三行:

```powershell
git -C "$root\probability" rev-parse --abbrev-ref HEAD
git -C "$root\probability" log -1 --format="%h %ad %s"
(Get-ChildItem -LiteralPath "$root\probability" -Recurse -Filter *.md -File).Count
```

期望: `main`, 一行提交信息, `24`.

### 6.2 换成任意仓库

地址规律只有一条: `https://github.com/wenje-ma/<仓库名>.git`. 仓库名现取, 不必另找清单:

```powershell
Invoke-RestMethod "https://api.github.com/users/wenje-ma/repos?per_page=100" -Headers @{ "User-Agent" = "curl" } |
  Select-Object name, size, @{ n = 'mb'; e = { [math]::Round($_.size / 1024) } }
```

`--depth 1` 只取最新提交, 不含历史, 体积小, 只读够用; 要完整历史就去掉这个参数.

### 6.3 更新

```powershell
git -C "$root\probability" pull --ff-only
```

### 6.4 全量克隆

```powershell
$root = "D:\wenje-ma"
$list = Invoke-RestMethod "https://api.github.com/users/wenje-ma/repos?per_page=100" -Headers @{ "User-Agent" = "curl" }
foreach ($r in $list) {
  $dst = Join-Path $root $r.name
  if (Test-Path -LiteralPath $dst) { "skip $($r.name)"; continue }
  git clone --depth 1 $r.clone_url $dst
  if ($LASTEXITCODE -ne 0) { "FAILED $($r.name)" }
}
```

判据两条, 期望 `25` 与 `942`:

```powershell
(Get-ChildItem -LiteralPath $root -Directory).Count
(Get-ChildItem -LiteralPath $root -Recurse -Filter *.md -File -Force | Where-Object { $_.FullName -notmatch "\\.git\\" } | Measure-Object).Count
```

逐仓库核分支:

```powershell
Get-ChildItem -LiteralPath $root -Directory | ForEach-Object { "$($_.Name) " + (git -C $_.FullName rev-parse --abbrev-ref HEAD 2>$null) }
```

体量提醒: 有三个仓库单个超过 200 MB, 最大的一个约 714 MB. 按 6.2 的 API 输出看 `size`, 用 `Sort-Object size -Descending` 挑最大的三个跳过即可, 只要大学数学就用不着它们.

### 6.5 连不上 github.com

处理顺序, 逐级尝试, 不要跳到关系统安全设置:

1. 换网络, 手机热点优先.
2. 有现成代理时 `git config --global http.proxy http://127.0.0.1:7890`, 用完 `--unset http.proxy`.
3. 镜像前缀 `https://gitclone.com/github.com/wenje-ma/<仓库名>.git`, 第三方服务, 可用性自行探测.
4. 都失败就让交接方打包 zip.

判据: 报错原文里出现 `Failed to connect to github.com port 443` 或长时间无输出, 即按上面顺序处理; 出现 `destination path already exists` 说明已克隆过, 跳过即可; 出现 `Permission denied (publickey)` 说明地址写成了 SSH, 换成 `https://` 开头.

## 7 S6 渲染与阅读

### 7.1 打开

```powershell
code "$root\wenjemaths"
```

首次打开会要求信任作者, 选信任, 否则 MPE 不激活.

### 7.2 预览判据

打开任意一个含 `$$` 的 md, 用 MPE 的 `Open Preview to the Side`. 逐项核对:

- 行内公式是斜体变量, 下标落在基线以下;
- 行间公式有分式横线, 矩阵有方括号, 编号靠右;
- 中文无方块与乱码;
- 表格有表头与竖线.

### 7.3 抽样清单

不点名具体文件, 按语法特征各抽一份. 先列出候选:

```powershell
Get-ChildItem -LiteralPath $root -Recurse -Filter *.md -File |
  Select-String -Pattern '\$\$' -List -Encoding utf8 |
  Select-Object -First 5 -ExpandProperty Path
```

把 `-Pattern` 换成下表的关键词, 就得到对应类型的候选文件. 每个类型抽一份打开预览.

| 抽什么 | 关键词 | 看到什么算过 |
| --- | --- | --- |
| 行间公式 | `$$` | 分式有横线, 编号靠右, 不是 `\frac` 原文 |
| 矩阵 | `begin{bmatrix}` 或 `begin{pmatrix}` | 方括号或圆括号包住, 元素不错位 |
| 分段函数 | `begin{cases}` | 左侧大括号, 右侧两行对齐 |
| 表格 | `^\x7c` | 表头与竖线在, 列不塌 |
| 图片 | `!\[` | 有图就过; 裂图先按第 10 节确认是否为已知例外 |
| 中文段落 | 任选一个含中文的 | 无方块, 无乱码 |

六类都过, 可认为 942 个 md 整体可读.

### 7.4 读全文

预览只用于验渲染, 942 个文件不要逐个开预览, 读文本即可.

```powershell
Get-Content -LiteralPath "$root\<仓库>\homework-cn\week1.md" -Encoding utf8 -TotalCount 60
```

必须显式写 `-Encoding utf8`: 文件是 UTF-8 无 BOM, PowerShell 5.1 默认按 ANSI 解码会出乱码.

按主题检索:

```powershell
Get-ChildItem -LiteralPath $root -Recurse -Filter *.md -File | Select-String -Pattern "<要检索的词>" -Encoding utf8
```

顺序建议: 先读含 `forced\` 目录的条目库建立术语口径, 再按 `<仓库>\homework-cn\weekN.md` 顺读. `textbooks\` 里的 `.pdf` 是教材扫描件, 用 PDF 阅读器打开, 不在 md 渲染范围内.

## 8 可选设置

需要时把下面合并进用户 `settings.json` (命令面板 `Preferences: Open User Settings (JSON)`).

```json
{
  "files.encoding": "utf8",
  "editor.wordWrap": "on",
  "security.workspace.trust.enabled": false,
  "markdown-preview-enhanced.mathRenderingOption": "KaTeX",
  "markdown-preview-enhanced.breakOnSingleNewLine": true,
  "markdown-preview-enhanced.scrollSync": true
}
```

说明: KaTeX 是插件内置的, 离线可用; `breakOnSingleNewLine` 保持 `true`, 因为仓库行文是一句一行; `wordWrap` 因为公式行很长.

## 9 故障排查

| 现象 | 原因 | 处理 |
| --- | --- | --- |
| `git` 或 `code` 不是命令 | 未装好, 或终端是装前开的 | 关掉终端与 VSCode 重开 |
| 预览空白或无反应 | 工作区未信任, 插件被禁用 | 见 5 节两条解法 |
| 公式显示源码 | 看的是编辑区, 预览未开 | 走 MPE 命令面板 |
| 公式区红字报错 | KaTeX 不认该宏 | 改 `mathRenderingOption` 为 `MathJax` |
| 中文乱码 | 编码按 ANSI 解码 | 编辑器右下角改 UTF-8; 命令加 `-Encoding utf8` |
| 图片裂图 | 图片缺失或需联网 | 见第 10 节 |
| 克隆转圈或报 443 | 网络 | 见 6.5 节 |
| `already exists` | 已克隆过 | 跳过 |
| `Permission denied (publickey)` | 用了 SSH 地址 | 换 https |
| 安装包被 SmartScreen 拦 | 未知程序拦截 | 更多信息, 仍要运行 |

## 10 已知例外

这些不是环境问题, 写进交付说明里, 不要当故障处理.

- `primary-mathematics\homework-cn\week116.md` 与 `primary-mathematics\homework-en\week116.md`: 有一处写成 `$1$$m$`, 两个行内公式紧贴, 后续内容可能被当成公式块, 该文件渲染异常.
- `states-python\3-报告\论文.md`: 引用 4 张 `figures\fig_*.png`, 仓库里实际是同名 `.pdf`, 4 张裂图.
- `wenje-ma\README.md`: shields.io 徽章需联网.
- `metropolis\README.md`: 代码块内是整段 LaTeX 源码, 属正常展示.
- `anki-mdmath` 无 md, 目录为空属正常.

## 11 边界

- 不执行 `git push`, `git reset`, `git clean`, 不删 `.git` 目录.
- 不把 md 转成 docx 或 pdf 交付.
- 不为连通 github.com 而关杀毒或防火墙, 不装来源不明的加速器.
- 路径只用英文与数字, 中文或空格会让部分命令失败.

## 12 回报格式

完成后回三行, 每行都要有可核对的数字或输出:

1. 版本: Git 版本号, VSCode 版本号, MPE 版本号.
2. 数量: 仓库目录数, md 总数, 以及第 6.4 节两条计数命令的原始输出.
3. 渲染: 第 7.2 节四条判据是否全过, 第 7.3 节六类抽样是否有异常, 有异常就按第 10 节对号入座.
