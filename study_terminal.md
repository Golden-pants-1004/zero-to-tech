<table border="1" cellpadding="6" cellspacing="0"> <thead> <tr> <th>功能描述</th> <th>完整命令</th> <th>简写/别名</th> <th>使用示例</th> <th>补充备注</th> </tr> </thead> <tbody> <tr> <td>查看当前所在路径</td> <td>Get-Location</td> <td>pwd</td> <td>pwd</td> <td>输出当前所在文件夹完整路径</td> </tr> <tr> <td>切换目录</td> <td>Set-Location &lt;路径&gt;</td> <td>cd</td> <td>cd D:\project<br>cd ..</td> <td>cd .. 返回上一级目录</td> </tr> <tr> <td>列出目录内文件</td> <td>Get-ChildItem</td> <td>dir / ls / gci</td> <td>dir<br>dir -Recurse</td> <td>-Recurse 递归查看所有子目录文件</td> </tr> <tr> <td>新建文件/文件夹</td> <td>New-Item [-ItemType] &lt;类型&gt; &lt;名称&gt;</td> <td>ni</td> <td>ni readme.md<br>ni code -ItemType Directory</td> <td>创建文件夹添加 -ItemType Directory，-Force 可创建多级目录</td> </tr> <tr> <td>删除文件/文件夹</td> <td>Remove-Item &lt;目标&gt;</td> <td>del / rm</td> <td>del readme.md<br>Remove-Item code -Recurse -Force</td> <td>删除文件夹必须加 -Recurse -Force 递归强制删除</td> </tr> <tr> <td>复制文件/文件夹</td> <td>Copy-Item &lt;源&gt; &lt;目标&gt;</td> <td>copy / cp</td> <td>copy readme.md ./code/<br>Copy-Item code ./backup -Recurse</td> <td>复制文件夹时，末尾添加 -Recurse 参数</td> </tr> <tr> <td>移动 / 重命名</td> <td>Move-Item &lt;源&gt; &lt;目标&gt;</td> <td>move / mv</td> <td>move readme.md new.md<br>move new.md ./code/</td> <td>同目录为重命名，跨目录为移动文件</td> </tr> <tr> <td>读取文件内容</td> <td>Get-Content &lt;文件&gt;</td> <td>cat / type</td> <td>cat readme.md<br>Get-Content readme.md -Encoding utf8</td> <td>-Encoding utf8 参数避免中文乱码</td> </tr> <tr> <td>清空控制台屏幕</td> <td>Clear-Host</td> <td>cls</td> <td>cls</td> <td>清空界面显示，不会删除历史命令记录</td> </tr> </tbody> </table>
补充说明<br>
常用路径符号说明<br>
~：家目录<br>
/：根目录<br>
..：上一级目录<br>
./：当前目录<br><br>
终端快捷操作<br>
上下方向键：快速调取之前输入过的历史命令，重复执行无需重新输入<br>
Tab 键：文件名、文件夹名、路径自动补全，输入开头后按 Tab 可自动补全名称，减少手动输入与拼写错误