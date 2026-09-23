# GitHub资料库零基础使用说明

这份说明用于把“375 nm位移塔尔伯特光刻文献学习资料”放进自己的GitHub仓库，并在网页上阅读、记笔记和保存修改。只用Edge就能开始，不需要先学编程或命令行。

## 一 先分清三个东西

GitHub是在线保存和协作的平台；repository（仓库）是一个项目的文件夹；Git是记录修改历史的工具。你目前先使用GitHub网页即可。

README.md是仓库首页说明。md是Markdown文本文件，GitHub会把它显示成有标题、表格和链接的文档。PDF适合在WPS里阅读、批注和打印。

这次交付的ZIP是已整理好的上传包，不是已经上线的GitHub仓库。解压后里面有README.md、docs、downloads和notes。在线仓库地址只有在你登录GitHub并创建成功后才会产生。

## 二 第一次建库

1. 在Edge中打开 https://github.com 并登录自己的账号。如果没有账号，先自行完成注册与验证。
2. 打开 https://github.com/new ，也可以点击右上角加号后选择New repository。
3. Owner选择自己的账号。Repository name填写talbot-375nm-reading；如果提示重名，可改成talbot-reading-notes。
4. Description可以填：375 nm位移塔尔伯特光刻照明系统文献学习与笔记。
5. 初次学习建议选择Private（私有），先把它当自己的学习资料夹。Public（公开）表示其他人也可能查看。
6. 不勾选自动添加README，也暂时不选License和.gitignore模板，因为上传包已有首页，文献引用也有各自的来源归属。
7. 点击Create repository。看到仓库页就说明建库完成，随后还需要上传内容。

官方说明：https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository

## 三 上传这次资料

1. 把交付的talbot-375nm-reading.zip解压。
2. 进入解压后的talbot-375nm-reading文件夹，确认这一层直接能看到README.md、docs、downloads、notes。
3. 在空仓库页面点击uploading an existing file。如果仓库已包含文件，选择Add file → Upload files。
4. 将上一步这一层里面的文件和文件夹拖入上传区域。不要直接上传ZIP，也不要把外层talbot-375nm-reading文件夹一起套进去，否则首页导航会多一层目录。
5. 等待上传完成。检查列表里有README.md、docs/下的章节、downloads/下的PDF以及notes/下的笔记模板。
6. Commit message填写：添加六篇文献辅助读本与学习说明。
7. 对自己的新建空仓库，若允许直接提交到main，可选择该项并点击Commit changes。若页面只允许Propose changes，则按页面创建分支和Pull request，再将自己的请求合并；受保护分支的设置可能不同。
8. 返回仓库首页，确认出现中文导航，并点击第一篇导读测试链接。

GitHub网页上传单文件限制为25 MiB，一次最多100个文件。本资料包在这些限制内。网页上传不会自动执行本地.gitignore规则，因此只拖入这次整理的包内文件。

官方说明：https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository

## 四 平时怎样使用

阅读：打开仓库首页 → 点击阅读路线或某篇论文 → 按学习单元阅读。英文部分目前包含四篇摘要对照，正文逐段精读后续继续补充。

记笔记：打开notes/学习笔记.md → 点击铅笔形编辑按钮（有时在编辑菜单中）→ 在对应论文下面填写 → 点击Preview预览 → Commit changes保存。这里的commit就是“保存一个带说明的版本”。

更新进度：打开notes/学习进度.md，编辑时把某一项的[ ]改成[x]，然后提交。完成导读不等于完成原文精读，所以两项分开打勾。

查看旧版本：在文件页面寻找History，选择一条修改记录，查看当时的内容或差异。开始阶段不需要学习分支、合并等全部术语。

下载全部：仓库首页点Code → Download ZIP。下载的是当时版本的快照，不会自动跟随线上更新，也不包含完整Git历史。

在WPS批注：从downloads下载PDF，打开后划线和写批注。批注只保存在你的本地文件里，不会自动传回GitHub；如果需要同步，要另行上传批注版。

官方编辑说明：https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files

官方下载说明：https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives

## 五 最少记住的词

| 页面词语 | 对你意味着什么 |
|---|---|
| Repository / Repo | 一个资料库 |
| README | 首页说明和入口 |
| Commit changes | 保存一次修改，并留下说明 |
| main | 当前资料的主版本所在分支 |
| History | 修改历史 |
| Private / Public | 私有 / 公开 |
| Upload files | 上传本地文件 |
| Download ZIP | 下载当前版本的整个文件包 |

## 六 文件怎样分工

docs是分章节导读，适合在GitHub上读和修改；downloads是本次导出的完整PDF；notes是你自己的进度和笔记；README是导航。

PDF是导出的阅读版本。以后改了Markdown，PDF不会自动重新排版。为了避免两份文字不一致，建议优先修改docs中的对应章节，需要新PDF时再统一导出。

当前包没有设置GitHub Pages，也不需要打开Actions运行程序。资料上传后，GitHub本身就能阅读Markdown；它不是部署好的一套独立网站。

六篇原论文PDF仍保留在你本机。本包包含导读、引用与摘要翻译，不把六篇论文原文件整包上传。若以后分享原论文，应先确认相应来源允许的传播方式。

## 七 一次完整的学习操作

今天打开第一篇导读 → 在WPS阅读对应原文 → 在学习笔记中写“光刻胶记录什么” → 给这一条修改写说明“补充第一篇光刻流程理解” → 保存。

下次打开仓库时，先看学习进度，再继续下一单元。这样GitHub就成为你的科研阅读档案，而不仅是一个放文件的地方。

## 八 常见疑问

不会编程能用吗？能。上述流程只需要网页、文件上传和简单文字编辑。

上传ZIP后为什么不能直接看到章节？因为GitHub把它当成一个压缩文件；请解压并上传里面的目录和文件。

网页改了文件，电脑文件会一起改吗？不会。初期用“网页编辑，必要时重新下载”的方式即可。

能把GitHub链接发给老师吗？公开仓库可以分享访问链接；私有仓库需要给老师的GitHub账号访问权限，或直接把PDF发给老师。是否开放仓库由你决定。

后面要继续翻译怎么做？在笔记里注明论文、节号、页码和不懂的句子，再把对应内容交给辅助阅读工具。新内容整理进相应章节即可。
