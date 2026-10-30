# 云保标桌面端 0.2.9

适用于 Windows 10 / 11 x64，两个安装包均可离线安装。

1. 安装 Yunbaobiao-Base-0.2.9-windows-x64-setup.exe（139.65MB）。仅安装基准包即可打开程序、调整设置、登记文件及管理项目。未安装模型时不会解析子文件，也不能发起比对。
2. 需要比对时，安装 Yunbaobiao-Models-0.2.9-windows-x64-setup.exe（472.50MB）。安装器自动寻找同版本的基准程序。
3. 回到程序点击“重新检测”，即可发起比对，无需重启程序。

升级时请先退出程序，依次安装同版本的两个包。模型包包括文本及图片模型、中文 OCR、Word 转换、经济清标及其离线运行环境。经济标只做本地规则及原组件检查，不进行 AI 复核；其他模块按各自 AI 配置运行。

0.2.9 修复了安装版错误沿用旧版运行时路径，导致文件解析出现 ENOENT 的问题。

## 完整性校验

下载 SHA256SUMS.txt，使用 PowerShell 计算安装包的哈希并与文件内容比对：

~~~powershell
Get-FileHash .\Yunbaobiao-Base-0.2.9-windows-x64-setup.exe -Algorithm SHA256
Get-FileHash .\Yunbaobiao-Models-0.2.9-windows-x64-setup.exe -Algorithm SHA256
~~~
