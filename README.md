@echo off
set BC_PATH="C:\Program Files\Beyond Compare 4\BCompare.exe"  // Update this path to the Beyond Compare executable location
set ZIP1="C:\Path\to\your\first.zip"                     // Update with the path to your first zip file
set ZIP2="C:\Path\to\your\second.zip"                    // Update with the path to your second zip file
set OUTPUT_PATH="C:\Path\to\output\folder"               // Update with the desired output folder

"%BC_PATH%" @c:\path\to\script.bcs %ZIP1% %ZIP2% %OUTPUT_PATH%

criteria binary
load %1 %2
expand all
folder-report layout:side-by-side options:display-mismatches output-to:%3\orphans_report.txt
