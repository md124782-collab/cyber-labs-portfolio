Step 1: Create a Day 10 folder inside your repo
cd ~/cyber-labs-portfolio       # move into your main repo
mkdir day10_linux_commands       # new folder for Day 10
cd day10_linux_commands
Step 2: Create sample files to practice commands
touch secret.txt notes.txt log.txt
echo "This is a secret password" > secret.txt
echo "Some notes about Day 10" > notes.txt
echo "Log entries 1 2 3" > log.txt
ls -l
Step 3: Practice permissions
chmod 640 secret.txt
ls -l secret.txt
Change ownership (if testing is possible):
sudo chown bandit3:bandit2 notes.txt
ls -l notes.txt
Reset ownership to your current user. You can change the owner back to yourself:
sudo chown $USER:$USER notes.txt
ls -l notes.txt
Step 4: Practice searching inside files
grep "password" secret.txt
grep -R "Day 10" .
Step 5: Other useful commands
awk → print the 3rd column of log.txt
awk '{print $3}' log.txt
sed → replace text
sed 's/Log/Entry/' log.txt
tar → archive files
tar -cvf day10.tar *.txt
scp → copy file to another machine (if you have one)
scp day10.tar user@host:/path
nano day10_cheatsheet.md
nano day10_cheatsheet.md
