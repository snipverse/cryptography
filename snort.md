1) Installation
Install:

Snort
Snort Rules
Npcap

Restart the system.

2) Verify Installation
Open Command Prompt → go to:
C:\Snort\bin

Run:
snort -V

3) Replace Rules
Open:

rules folder
preproc_rules folder

Delete old files → paste new rules.

4) Configure Snort
Open:
C:\Snort\etc\snort.conf

Set HOME_NET = your IP
Set EXTERNAL_NET = !$HOME_NET
Set rule paths
Set log directory
Create WHITE_LIST file

5) Find Interface
Run:
snort -W

Note interface number (e.g., 5).

6) Test Setup
Run Snort → check for no errors.

7) Custom Rule
Open:
C:\Snort\rules\local.rules

Add your rule.

8) Run Snort
snort -i 5 -c C:\Snort\etc\snort.conf -A console
