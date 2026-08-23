| 功能描述 | 完整命令 | 简写/别名 | 使用示例 | 补充备注 |
| ---- | ---- | ---- | ---- | ---- |
| 查看当前所在路径 | Get‑Location | pwd | pwd | 输出当前所在文件夹完整路径 |
| 切换目录 | Set‑Location &lt;路径&gt; | cd | cd D:\project<br>cd .. | cd .. 返回上一级目录 |
| 列出目录内文件 | Get‑ChildItem | dir / ls / gci | dir<br>dir ‑Recurse | ‑Recurse 递归查看所有子目录文件 |
| 新建文件/文件夹 | New‑Item [-ItemType] &lt;类型&gt; &lt;名称&gt; | ni | ni readme.md<br>ni code ‑ItemType Directory | 创建文件夹添加 ‑ItemType Directory，‑Force 可创建多级目录 |
| 删除文件/文件夹 | Remove‑Item &lt;目标&gt; | del / rm | del readme.md<br>Remove‑Item code ‑Recurse ‑Force | 删除文件夹必须加 ‑Recurse ‑Force 递归强制删除 |
| 复制文件/文件夹 | Copy‑Item &lt;源&gt; &lt;目标&gt; | copy / cp | copy readme.md ./code/<br>Copy‑Item code ./backup ‑Recurse | 复制文件夹时，末尾添加 ‑Recurse 参数 |
| 移动 / 重命名 | Move‑Item &lt;源&gt; &lt;目标&gt; | move / mv | move readme.md new.md<br>move new.md ./code/ | 同目录为重命名，跨目录为移动文件 |
| 读取文件内容 | Get‑Content &lt;文件&gt; | cat / type | cat readme.md<br>Get‑Content readme.md ‑Encoding utf8 | ‑Encoding utf8 参数避免中文乱码 |
| 清空控制台屏幕 | Clear‑Host | cls | cls | 清空界面显示，不会删除历史命令记录 |

补充说明

**常用路径符号说明**
- `~`：家目录
- `/`：根目录
- `..`：上一级目录
- `./`：当前目录

**终端快捷操作**
- 上下方向键：快速调取之前输入过的历史命令，重复执行无需重新输入
- Tab 键：文件名、文件夹名、路径自动补全，输入开头后按 Tab 可自动补全名称，减少手动输入与拼写错误

<br>

| 功能描述 | Git命令 | 使用示例 | 备注 |
| ---- | ---- | ---- | ---- |
| 查看工作区状态 | git status | `git status` | 查看哪些文件被修改、暂存 |
| 添加全部修改到暂存区 | git add "文件名" | `git add .` | `.`代表当前目录全部文件 |
| 提交版本 | git commit -m "描述" | `git commit -m "写清楚这次改了什么"` | `-m`后双引号填写提交说明 |
| 查看简洁提交日志 | git log --oneline | `git log --oneline` | 简短展示每一次提交记录 |
| 切换分支 | git checkout "编号"| `git checkout main` | 切换到main分支 |
| 推送到远程仓库 | git push | `git push` | 将本地分支提交推送到远程origin对应分支 |
| 获取远程最新信息(不合并) | git fetch | `git fetch` | 更新本地 origin/* 远程分支记录，不改动本地代码 |
| 拉取远程代码并合并 | git pull | `git pull` | = git fetch + git merge，拉取远程代码合并到本地 |
