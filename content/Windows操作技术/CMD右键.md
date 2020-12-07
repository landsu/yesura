# 添加 "Run CMD Here" 到鼠标右键 

>**info**  **复制下面的代码到一个txt文档，改扩展名为：XXX.reg，双击添加到注册表即可**

```
Windows Registry Editor Version 5.00

[HKEY_CLASSES_ROOT\Directory\shell\OpenCmdHere]
@="Run CMD Here"
"Icon"="cmd.exe"

[HKEY_CLASSES_ROOT\Directory\shell\OpenCmdHere\command]
@="cmd.exe /s /k pushd \"%V\""

[HKEY_CLASSES_ROOT\Directory\Background\shell\OpenCmdHere]
@="Run CMD Here"
"Icon"="cmd.exe"

[HKEY_CLASSES_ROOT\Directory\Background\shell\OpenCmdHere\command]
@="cmd.exe /s /k pushd \"%V\""

[HKEY_CLASSES_ROOT\Drive\shell\OpenCmdHere]
@="Run CMD Here"
"Icon"="cmd.exe"

[HKEY_CLASSES_ROOT\Drive\shell\OpenCmdHere\command]
@="cmd.exe /s /k pushd \"%V\""

[HKEY_CLASSES_ROOT\LibraryFolder\background\shell\OpenCmdHere]
@="Run CMD Here"
"Icon"="cmd.exe"

[HKEY_CLASSES_ROOT\LibraryFolder\background\shell\OpenCmdHere\command]
@="cmd.exe /s /k pushd \"%V\""
```

