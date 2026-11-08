# 交接文档: 在本机搭好 wenje-ma 仓库的阅读环境

读者是操作这台电脑的 AI. 按 S0 到 S6 的顺序执行, 每步判据不过就停下处理, 不要凭猜继续. 全程只读: 不改仓库文件, 不 commit, 不 push.

## 0 验收标准

| 编号 | 达到的状态 | 判据 | 期望结果 |
| --- | --- | --- | --- |
| 1 | 这台机器能连上 github.com | 第 2 节两条命令 | 返回 `200`, 且列出 `refs/heads/main` |
| 2 | GitHub 账号可登录 | 打开 `https://github.com/settings/profile` | 页面显示用户名 |
| 3 | VSCode 可用且界面中文 | `code --version` 加界面检查 | 输出一行版本号, 菜单是中文 |
| 4 | Git 可用 | `git --version` | `git version 2.x` |
| 5 | MPE 插件已装 | `code --list-extensions` | 含 `shd101wyy.markdown-preview-enhanced` |
| 6 | 能克隆任意仓库 | `git -C <路径> rev-parse --abbrev-ref HEAD` | `main` |
| 7 | 全量 md 齐且能渲染 | 第 7.6 节计数命令, 加第 8.4 节抽样 | `25` 与 `942`, 公式排版正常 |

## 1 前提与事实

- 系统: Windows 10 或 11, x64, 有管理员权限.
- 开始前先按第 2 节确认能连上 github.com; 一时连不上就多重试几次, 隔几分钟再来.
- 存放目录: 先用桌面上的 `wenje-ma`, 便于查找; 全量或大仓库改用 `D:\wenje-ma`. 不要直接放在 C 盘或 D 盘根目录, 避免与其他文件混放和权限问题. 路径尽量英文, 不带空格.
- 每个仓库是独立的 git 仓库, 远端统一 `https://github.com/wenje-ma/<仓库名>.git`, 默认分支一律 `main`.
- 可匿名克隆的公开仓库共 25 个, 合计 942 个 md.
- 这 942 个 md 全部 UTF-8 无 BOM, 行尾 CRLF. 公式只有 `$...$` 与 `$$...$$`, 表格是标准 GFM, 没有 mermaid 与自定义容器.
- 目录惯例: `<仓库>\homework-cn\weekN.md` 中文习题, `homework-en\weekN.md` 英文版, `textbooks\` 教材与讲课稿, 部分仓库另有 `figures\`, `codes\`, `tex\`.
- 参考库: `wenjemaths\forced\` 是条目库, 术语与符号口径以它为准.

## 2 S0 确认网络可达

先测 API, 再测 git. 两条都通才算过关, 只过一条会在克隆时卡住.

```powershell
Invoke-WebRequest "https://api.github.com/users/wenje-ma" -TimeoutSec 10 -UseBasicParsing | Select-Object -ExpandProperty StatusCode
git ls-remote "https://github.com/wenje-ma/wenjemaths.git" | Select-Object -First 3
```

判据: 第一条输出 `200`, 第二条输出若干行 `refs/heads/main`.

连不上就多重试几次: 关掉窗口隔几分钟再跑, 换个时间段再跑, 两条命令交替试几遍. 通了再往下走, 不要在这一步反复折腾.

## 3 S1 注册 GitHub 账号

三项必须由本人完成: 邮箱验证码, 人机验证, 密码.

1. 打开 `https://github.com/signup`.
2. 邮箱优先用学校邮箱, 可能触发学生权益; QQ 邮箱也能注册, 注册后可再绑定备用邮箱.
3. 用户名避开常见词, 用昵称加数字, 否则会重名.
4. 密码自己记得住就行, 不必过复杂.
5. 完成后访问 `https://github.com/wenje-ma`, 能列出公开仓库即为正常.

判据: `https://github.com/settings/profile` 显示用户名, 右上角有头像.

说明: 公开仓库匿名就能克隆, 账号不是克隆的前提, 注册的用途是登录后访问需要授权的仓库, 提 issue, 加星.

失败分支: 页面打不开 → 回第 2 节; 收不到验证码 → 查垃圾邮件目录, 核对邮箱是否写错; 用户名占用 → 加数字重试.

## 4 S2 安装 VSCode

官网 `https://code.visualstudio.com/` 下 User Installer, 安装时保持默认并勾选"创建桌面快捷方式".

装完补两项:

```powershell
code --install-extension MS-CEINTL.vscode-language-pack-zh-hans
code --install-extension eamodio.gitlens
```

第一条是简体中文界面, 第二条是可选的 Git 增强, 装完按提示重载窗口. 若命令行 ID 失效, 直接在扩展面板搜 `Chinese` 与 `GitLens` 安装, 以面板为准.

判据: `code --version` 输出一行版本号; 重载后菜单是中文. 若先出现 `crashpad ... TransactNamedPipe` 之类的报错行, 那是 Windows 下的噪声, 不算失败.

失败分支: 提示 `code` 不是命令 → 在 VSCode 里按 `Ctrl+Shift+P` 执行 `Shell Command: Install 'code' command in PATH`; 或直接用 `"%LOCALAPPDATA%\Programs\Microsoft VS Code\bin\code.cmd"`.

## 5 S3 安装 Git

两种装法, 任选其一.

```powershell
winget install --id Git.Git -e --source winget --accept-package-agreements --accept-source-agreements
```

或到 `https://git-scm.com/download/win` 下载, PATH 那一页选 `Git from the command line and also from 3rd-party software`.

判据: 新开终端运行 `git --version`, 输出 `git version 2.x`.

装完配一次身份, 提交时才需要, 但建议一并做掉:

```powershell
git config --global user.name "<GitHub 用户名>"
git config --global user.email "<注册邮箱>"
```

失败分支: 提示 `不是内部或外部命令` → 终端是安装前开的, 关掉重开; 仍旧 → 确认 `C:\Program Files\Git\cmd` 在 PATH, 或让 VSCode 的 `git.path` 指向 `C:\Program Files\Git\cmd\git.exe`; 找不到 winget → 在 Microsoft Store 更新 `应用安装程序`.

## 6 S4 安装 MPE 插件

```powershell
code --install-extension shd101wyy.markdown-preview-enhanced
```

判据: `code --list-extensions --show-versions` 里出现 `shd101wyy.markdown-preview-enhanced@0.8.x`.

必要前置: 该插件未声明支持未信任工作区, 在 Restricted Mode 下会被禁用, 表现是按预览没反应或白屏. 两个解法, 任选其一:

- 打开文件夹时弹窗问信任, 选 `Yes, I trust the authors`.
- 把用户设置 `security.workspace.trust.enabled` 改为 `false`.

打开预览: 首选编辑器右上角的分屏图标, 一次点击即可在右侧出预览. `Ctrl+K V` 与 VSCode 自带预览冲突, 可能打开的是自带那个; 要确定用的是 MPE, 走命令面板 `Ctrl+Shift+P` → `Markdown Preview Enhanced: Open Preview to the Side`.

自测: 新建 `test.md`, 写入下面两行, 用上面的办法打开预览.

```markdown
行内公式 $\frac{1}{2}$, 行间公式:
$$x^{2}+y^{2}=1$$
```

判据: 预览里是带横线的分式与带上标的公式, 不是 `\frac` 原文. 验证完删掉 `test.md`.

失败分支: 预览空白 → 按信任两条处理; 公式仍是原文 → 你看的是左侧编辑区, 预览窗格未开; 公式区红字 → KaTeX 不认该宏, 把 `markdown-preview-enhanced.mathRenderingOption` 改成 `MathJax`, 首次渲染需联网.

## 7 S5 克隆仓库

### 7.1 准备目录

```powershell
$root = Join-Path ([Environment]::GetFolderPath("Desktop")) "wenje-ma"
New-Item -ItemType Directory -Force -Path $root | Out-Null
$root
```

最后一行打印出来的路径就是实际目录, 桌面被 OneDrive 重定向时它也会给出正确位置. 全量克隆或大仓库建议改用 `D:\wenje-ma`.

### 7.2 取仓库地址 (最容易错的一步)

在浏览器打开仓库首页, 地址栏应当形如 `https://github.com/wenje-ma/<仓库名>`, 并且页面上能看到绿色的 `Code` 按钮.

以下三种地址都不能用:

- 带 `/blob/` 或 `/tree/` 的, 那是某个文件或子目录的页面;
- 以 `.md` 结尾的, 那是文件页;
- 仓库内的相对路径, 那不是地址.

判据: 地址栏里只有两段路径, 形如 `<账号>/<仓库名>`.

### 7.3 克隆单个仓库

```powershell
git clone --depth 1 "https://github.com/wenje-ma/<仓库名>.git" "$root\<仓库名>"
```

`--depth 1` 只取最新提交, 不含历史, 体积小, 只读够用; 要完整历史就去掉这个参数.

判据三行:

```powershell
git -C "$root\<仓库名>" rev-parse --abbrev-ref HEAD
git -C "$root\<仓库名>" log -1 --format="%h %ad %s"
(Get-ChildItem -LiteralPath "$root\<仓库名>" -Recurse -Filter *.md -File).Count
```

期望: `main`, 一行提交信息, 一个大于 0 的 md 数.

失败分支: 报 443 或长时间无输出 → 多重试几次, 隔几分钟再来; `destination path already exists` → 已克隆过, 跳过; `Permission denied (publickey)` → 地址写成了 SSH, 换成 `https://` 开头; 弹窗要账号密码 → 地址写错了仓库名或该仓库需授权, 公开仓库不会弹窗.

### 7.4 clone 与 fork 的区别

| 操作 | 结果 | 什么时候用 |
| --- | --- | --- |
| clone | 仓库复制到本地, 只在你电脑上, 改动传不回原作者 | 只想读笔记, 默认选这个 |
| fork | 在你的 GitHub 账号下生成一份副本, 你可以改并推送到自己那份 | 想改内容, 或想长期保留自己的版本 |

fork 之后克隆的是你自己账号下的地址, 形如 `https://github.com/<你的用户名>/<仓库名>.git`, 原作者的库仍可只读参考.

### 7.5 更新

首选图形界面: 在 VSCode 左侧源代码管理面板点同步或拉取按钮, 一步完成.

命令行:

```powershell
git -C "$root\<仓库名>" pull --ff-only
```

失败分支: 报 `index.lock` 已存在或文件被占用 → 先关掉正在打开该目录的预览, PDF 阅读器, 终端; 确认没有 git 进程后, 删除 `.git\index.lock` 再重试.

### 7.6 全量克隆

```powershell
$root = Join-Path ([Environment]::GetFolderPath("Desktop")) "wenje-ma"
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

逐个核分支:

```powershell
Get-ChildItem -LiteralPath $root -Directory | ForEach-Object { "$($_.Name) " + (git -C $_.FullName rev-parse --abbrev-ref HEAD 2>$null) }
```

体量提醒: 有三个仓库单个超过 200 MB, 最大的一个约 714 MB. 用 `$list | Sort-Object size -Descending` 看排序, 只要大学数学就跳过最大的三个. 全量约 2 GB, 桌面盘空间不够就换到 D 盘.

## 8 S6 渲染与阅读

### 8.1 打开

```powershell
code "$root"
```

首次打开会要求信任作者, 选信任, 否则 MPE 不激活.

### 8.2 打开预览

在资源管理器里点开任意一个 md, 再点编辑器右上角的分屏图标. 要确认是 MPE 在渲染, 用命令面板的 `Markdown Preview Enhanced: Open Preview to the Side`.

### 8.3 四条判据

- 行内公式是斜体变量, 下标落在基线以下;
- 行间公式有分式横线, 矩阵有方括号, 编号靠右;
- 中文无方块与乱码;
- 表格有表头与竖线.

### 8.4 抽样清单

不点名文件, 按语法特征各抽一份. 先列候选:

```powershell
Get-ChildItem -LiteralPath $root -Recurse -Filter *.md -File |
  Select-String -Pattern '\$\$' -List -Encoding utf8 |
  Select-Object -First 5 -ExpandProperty Path
```

把 `-Pattern` 换成下表关键词, 即得该类型的候选. 每类抽一份开预览.

| 抽什么 | 关键词 | 看到什么算过 |
| --- | --- | --- |
| 行间公式 | `$$` | 分式有横线, 编号靠右 |
| 矩阵 | `begin{bmatrix}` | 方括号包住, 元素不错位 |
| 分段函数 | `begin{cases}` | 大括号包住, 两行对齐 |
| 表格 | `^\x7c` | 表头与竖线在, 列不塌 |
| 图片 | `!\[` | 有图就过; 裂图先按第 11 节判断 |
| 中文段落 | 任选一个含中文的 | 无方块, 无乱码 |

六类都过, 可认为 942 个 md 整体可读.

### 8.5 读全文

预览只用于验渲染, 不要逐个开预览, 读文本即可.

```powershell
Get-Content -LiteralPath "$root\<仓库>\homework-cn\week1.md" -Encoding utf8 -TotalCount 60
```

必须显式写 `-Encoding utf8`: 文件是 UTF-8 无 BOM, PowerShell 5.1 默认按 ANSI 解码会出乱码.

按主题检索:

```powershell
Get-ChildItem -LiteralPath $root -Recurse -Filter *.md -File | Select-String -Pattern "<要检索的词>" -Encoding utf8
```

顺序建议: 先读含 `forced\` 目录的条目库建立术语口径, 再按 `<仓库>\homework-cn\weekN.md` 顺读. `textbooks\` 里的 `.pdf` 是教材扫描件, 用 PDF 阅读器打开, 不在 md 渲染范围内.

手机端: md 不能直接看, 需要就导出 PDF 再传过去, 或用支持 Markdown 的阅读应用.

## 9 可选设置

需要时合并进用户 `settings.json` (命令面板 `Preferences: Open User Settings (JSON)`).

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

说明: KaTeX 是插件内置的, 不需要联网; `breakOnSingleNewLine` 保持 `true`, 因为仓库行文是一句一行; `wordWrap` 因为公式行很长.

## 10 故障排查

| 现象 | 原因 | 处理 |
| --- | --- | --- |
| 克隆转圈或报 443 | 一时连不上 | 多重试几次, 隔几分钟再来 |
| `git` 或 `code` 不是命令 | 未装好, 或终端是装前开的 | 关掉终端与 VSCode 重开 |
| 预览空白或无反应 | 工作区未信任, 插件被禁用 | 见第 6 节两条解法 |
| 公式显示源码 | 看的是编辑区, 预览未开 | 点右上角分屏图标 |
| 公式区红字报错 | KaTeX 不认该宏 | 改 `mathRenderingOption` 为 `MathJax` |
| 中文乱码 | 按 ANSI 解码 | 编辑器右下角改 UTF-8; 命令加 `-Encoding utf8` |
| 图片裂图 | 图片缺失或需联网 | 见第 11 节 |
| `already exists` | 已克隆过 | 跳过 |
| `index.lock` 存在 | 另一进程占用仓库 | 关预览与终端后删 `.git\index.lock` |
| 文件名从资源管理器拖进仓库失败 | 目标被占用或权限不足 | 改用复制粘贴, 不要拖拽 |
| `Permission denied (publickey)` | 用了 SSH 地址 | 换 `https://` |
| 安装程序被 SmartScreen 拦 | 未知程序拦截 | 更多信息, 仍要运行 |
| 界面还是英文 | 中文包未生效 | 重载窗口, 或扩展面板重装 Chinese |

## 11 已知例外

这些不是环境问题, 写进交付说明里, 不要当故障处理.

- `primary-mathematics\homework-cn\week116.md` 与 `primary-mathematics\homework-en\week116.md`: 有一处写成 `$1$$m$`, 两个行内公式紧贴, 后续内容可能被当成公式块.
- `states-python\3-报告\论文.md`: 引用 4 张 `figures\fig_*.png`, 仓库里实际是同名 `.pdf`, 4 张裂图.
- `wenje-ma\README.md`: shields.io 徽章需联网.
- `metropolis\README.md`: 代码块内是整段 LaTeX 源码, 属正常展示.
- `anki-mdmath` 无 md, 目录为空属正常.

## 12 边界

- 只读. 发现笔误记下来报告, 不改文件. 日后若被要求改文稿, 先读 `wenje-codes\STYLE.md`, 按那里的口径来.
- 不执行 `git push`, `git reset`, `git clean`, 不删 `.git` 目录; 不删库, 不重命名远端仓库.
- 不把 md 转成 docx 或 pdf 交付, 手机端需要时另行导出.
- 不安装来源不明的软件与破解版, 不为连通网络关杀毒或防火墙.
- 路径尽量英文与数字, 中文或空格会让部分命令失败.

## 13 回报格式

完成后回三行, 每行都要有可核对的数字或输出:

1. 环境: 网络两条命令的输出, Git 版本, VSCode 版本, MPE 版本.
2. 数量: 仓库目录数, md 总数, 以及第 7.6 节两条计数命令的原始输出.
3. 渲染: 第 8.3 节四条判据是否全过, 第 8.4 节六类抽样是否有异常, 有异常按第 11 节对号入座.
