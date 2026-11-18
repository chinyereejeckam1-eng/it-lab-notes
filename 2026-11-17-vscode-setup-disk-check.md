VS Code setup + disk report script, Nov 17, 2026

Task: Set up VS Code, then write and run a PowerShell script showing drive space in GB and the 5 largest folders under my home folder in MB.
Prompt: I asked Claude (free chat plan) to write the script, then ran and verified it myself in VS Code's PowerShell terminal.

What it produced: Get-DiskReport.ps1. Part 1 lists each local fixed drive with total, used, and free space in GB plus free %. Part 2 measures every folder directly under $HOME, skips junctions/symlinks, and shows the top 5 by size in MB with a progress bar.
What I fixed:
•  The .ps1 download failed in the browser, so I copied the script from Claude's file panel and pasted it into VS Code.
•  The file first saved as "# Get-DiskReport.ps1" because VS Code took the name from the script's first comment line. Fixed with Save As to Get-DiskReport.ps1.
•  The first run was blocked by the execution policy. Fixed with Set-ExecutionPolicy -Scope CurrentUser RemoteSigned, then re-ran.

Verified output, top 5 folders under my home folder:
•  AppData: 10,108.65 MB
•  Music: 2,899.54 MB
•  Downloads: 484.26 MB
•  Pictures: 17.71 MB
•  .copilot: 0.01 MB


What I learned: how to read an error and fix the actual cause. File-not-found meant the name was wrong, and the security error meant the execution policy needed changing, not the script. 
<img width="500"  alt="image" src="https://github.com/user-attachments/assets/cbab9805-7e52-4384-a4ff-ba66a3c5277d" />
<img width="500"  alt="image" src="https://github.com/user-attachments/assets/63b2a292-12cf-4799-a097-8d1e4a19cbf1" />
<img width="500" alt="image" src="https://github.com/user-attachments/assets/5848a87b-023a-4d9d-83e1-1bdcfd34f6f4" />
<img width="500"  alt="image" src="https://github.com/user-attachments/assets/fdd3a2c6-894f-4940-83be-bf9d3577bb26" />


