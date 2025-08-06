
@echo off
title Tidal for Roblox
color 0A
cls

echo Initializing Tidal Download...
setlocal EnableDelayedExpansion
set "bar="
set /a progress=0

:loop
set /a progress+=5
set "bar=!bar!-"
cls
title Tidal for Roblox - Downloading [%progress%%%]
echo Downloading Tidal for Roblox...
echo.
echo [!bar!                                                  ] !progress!%%
ping localhost -n 1 >nul
if !progress! lss 100 goto loop

echo.
echo Download complete!
echo Creating file...
echo https://github.com/exislow/tidal-dl-ng > "%USERPROFILE%\Desktop\Tidal.txt"
echo File "Tidal.txt" created on Desktop.
pause
