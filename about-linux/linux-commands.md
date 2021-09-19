echo hello
whoami (current user)
echo $0 (location of current program)
history (command executed history)
!2 (second commend executed in history)

apt (advanced package tool) (package manager)
apt list
apt update
apt install nano
apt remove nano

directories
  /bin (binaries/programs)
  /boot (program related to booting)
  /dev (program related to devices)
  /etc (editable text configuration files)
  /home (home directory for different user)
  /root (home directory for root user)
  /lib (library files for software)
  /var (log files/ application data so on)
  /proc (running processes)

pwd (print working directory)
ls
ls -1 (one item per line)
ls -l (long listing)

cd
cd ..
cd ~
cd /one/two

mkdir (create folder)
mv (rename file/folder or move to other directory)
touch (to create file)
touch file1.txt file2.txt file3.txt
rm (remove one/more files)
rm file*
rm -r (remove directory and all its content recursively)

nano (basic text editor for linux)
cat (concatenate) (show content of file)
more (show file content with page wise (spacebar to change page)) (only down possible)
less (replace more command, to allow scroll up and down)
head -n 5 (to show first five line of file)
tail -n 5 (to show last five line of file)

cat file1.txt file2.txt file3.txt > combined.txt (combine 3 file to one file)
echo hello > file1.ext

grep (global regular expression print)
grep -i searchterm file.txt
grep -i searchterm /etc/passwd
grep -i searchterm file1.txt file2.txt
grep -i -r searchterm . (directory search)
grep -ir searchterm . (directory search)

find (finding file/folder (show hidden also))
la -a (show hidden file/folder)
find -type d (only folders)
find -type f (only files)
find -type f -name "f*" (all file name start with f)
find -type f -iname "f*" (case insensitive name)

mkdir test ; cd test ; echo done (chainging command) (execute every command irrespective if other fail(s))
mkdir test && cd test && echo done 
mkdir test || echo "Directory exist"

pipping
ls /bin | less
ls /bin | head 

long command break
mkdir test;\
cd test; \
echo "DONE"

printenv (pint all environment variables)
printenv PATH
echo $PATH
export MY_ONE=sumit
echo $MY_ONE

echo MY_ONE=sumit >> ~/.bashrc (append content to .bashrc to make Environment variable available when terminal start)
source ~/.bashrc (to reload bashrc file to make effect)

ps (list current running process)
sleep 3
sleep 100 &
kill PID

manage users
useradd (add user)
usermod (modify user)
userdel (delete user)

useradd -m sumit
cat /etc/passwd
usermod -s /bin/bash sumit

cat /etc/shadow (password stored in encrypted format)

$ in terminal path => normal user 
#in terminal path => root user  

useradd => original api
adduser => more interactive (use useradd under the hood)

managing groups
groupadd
groupmod
groupdel

(user have one primary group & multiple secondary group)

groupadd developers 
cat /etc/group
usermod -G developers one (set secondary group)
usermod -g developers one (set primary group(--gid))
cat /etc/passwd | grep one
groups one (list of groups user is in)  


file permissions

my-test-script.sh (shell script)
echo echo hello > deploy.sh
chmod u+x deploy.sh (Add execution permission for user)
chmod u-x deploy.sh (remove execution permission for user)
chmod o+x deploy.sh (add execution permission for other users)
chmod og+x+w-r deploy.sh deploy2.sh (others and groups that owns this file, add execute & write permission and remove read)






 

