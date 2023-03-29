---
tags: bat
---

```cmd
@echo off
echo 游戏列表： 
:menu
echo.
echo. 1.2048  2.神庙逃亡  3.穿越火线 
echo.
set /p num=请输入你要运行的游戏编号： 
if %num%==1 (start Obsidian.txt) else if %num%==2 (start git代码.bat) else if %num%==3 (start crossfire) else echo 输入错误
goto menu
```

