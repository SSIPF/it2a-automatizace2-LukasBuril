@echo off

for /f "tokens=1-4 delims=," %%a in (uziv.txt) do (
    net user "%%a" "%%b" /add 
    net localgroup "%%c" /add
    net localgroup "%%c" "%%a" /add
    echo Jmeno: "%%a" Heslo: "%%b" skupina: "%%c"

    
)
