@echo off
setlocal

set BC_PATH="C:\Program Files\Beyond Compare 4\BComp.exe"  -- Modify this path to point to your Beyond Compare executable.

set FIRST_ZIP="C:\path\to\first.zip"  -- Replace with the path to your first ZIP file.
set SECOND_ZIP="C:\path\to\second.zip"  -- Replace with the path to your second ZIP file.

set ORPHANS_REPORT="C:\path\to\orphans.txt"  -- Replace with the path where you want to save the orphans report.

"%BC_PATH%" "%FIRST_ZIP%" "%SECOND_ZIP%" /fileviewer=Text /solo /lefttitle="First ZIP" /righttitle="Second ZIP" /savetarget="%ORPHANS_REPORT%" /filefilter="*.*" /criteria=orphan

echo Comparison complete. Orphaned files have been saved to "%ORPHANS_REPORT%"

endlocal
