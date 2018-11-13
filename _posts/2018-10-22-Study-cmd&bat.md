---
title: Stydy cmd
key: 20181015
tags: study study-cmd
---

``` batchfile
if "%PROCESSOR_ARCHITECTURE%"=="x86" goto x86     :: 冒号后的%%仍然识别为引用变量值
if %PROCESSOR_ARCHITECTURE%==AMD64 goto x64       :: 不加引号实际也可以
exit
:x64
explorer.exe http://www.baidu.com/
exit

:x86
explorer.exe //www.jb51.net/
```

```batchfile
@echo off
if exist %winDir%\SYsWOW64 (    :: 变量和路径，大小写不敏感
 start http://www.baidu.com
)else (
 start //www.jb51.net
)
```

```batchfile
@echo off
::从系统文件中获取系统版本信息
for /f "tokens=1* delims=[" %%a in ('ver') do set b=%%b
::将版本信息赋值给变量b
set b=%b:* =%
::输出指定值
echo %b:~0,4%
echo %PROCESSOR_ARCHITECTURE:~-1%
echo %b:~0,4%%PROCESSOR_ARCHITECTURE:~-1%
::调用指定值对应的cmd命令行
call:%b:~0,4%%PROCESSOR_ARCHITECTURE:~-1%
pause&exit
:5.1.6
echo 系统版本： winxp_32位
goto:eof
:5.2.6
echo 系统版本： win2003_32位
goto:eof
:5.2.4
echo 系统版本： win2003_64位
goto:eof
:6.1.6
echo 系统版本：win7_32位
goto:eof
:6.1.4
echo 系统版本：win7或win2008_64位
```

```batchfile
systeminfo |find "x64"        :: 通道符前面必须空格 后面可以不空格，find后面的字符串参数必须加引号，匹配时不匹配引号
```

```batchfile
IF PROCESSOR_ARCHITECTURE == amd64 or          :: if ... then ...else... end if ，这种形式的if cmd也支持
PROCESSOR_ARCHITEW6432 == amd64 THEN
// OS is 64bit
ELSE
// OS is 32bit
END IF

Another way to test for the same thing is:

IF PROCESSOR_ARCHITECTURE == x86 AND
PROCESSOR_ARCHITEW6432 NOT DEFINED THEN
// OS is 32bit
ELSE
// OS is 64bit

END IF
```
