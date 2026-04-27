# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
<img width="793" height="243" alt="image" src="https://github.com/user-attachments/assets/620ce4c0-def8-4d49-960b-15bc882684bf" />



cat < file2
## OUTPUT

<img width="698" height="245" alt="image" src="https://github.com/user-attachments/assets/e2fe1b30-04f6-43f4-8858-2cb6547585c3" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="785" height="94" alt="image" src="https://github.com/user-attachments/assets/0402ded8-0f46-4fee-a853-5e63df7ce326" />

comm file1 file2
 ## OUTPUT

 <img width="862" height="388" alt="image" src="https://github.com/user-attachments/assets/db663cac-6b19-4678-9b43-070a3dd02c3f" />

diff file1 file2
## OUTPUT
<img width="841" height="529" alt="image" src="https://github.com/user-attachments/assets/742c85fe-4088-4bee-a9b6-d22ce356edfb" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT

<img width="714" height="141" alt="image" src="https://github.com/user-attachments/assets/818fe6bc-2ff4-4029-8c20-9941a86e461e" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="805" height="175" alt="image" src="https://github.com/user-attachments/assets/3ad60eab-c129-4771-b2d7-dd1034408edc" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="812" height="190" alt="image" src="https://github.com/user-attachments/assets/b33019b2-8e69-42a9-abf8-61c8e043e910" />


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

<img width="623" height="98" alt="image" src="https://github.com/user-attachments/assets/a484512d-f0a2-4e54-864f-76513ad1eafd" />


grep hello newfile 
## OUTPUT

<img width="708" height="97" alt="image" src="https://github.com/user-attachments/assets/3efb0829-593a-4a56-8247-19d10b2ee20f" />

grep -v hello newfile 
## OUTPUT

<img width="806" height="151" alt="image" src="https://github.com/user-attachments/assets/3031b098-4a06-4327-a57b-1fb3bdbf2b1b" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="739" height="103" alt="image" src="https://github.com/user-attachments/assets/b27fd200-2230-4f57-a9d2-b110957517f4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="943" height="95" alt="image" src="https://github.com/user-attachments/assets/0b8fcf3d-4fad-412d-bda0-8537906b2c93" />



grep -R ubuntu /etc
## OUTPUT

<img width="1159" height="493" alt="image" src="https://github.com/user-attachments/assets/ca34c292-8f7f-4bd4-b46b-626bde987e85" />


grep -w -n world newfile   
## OUTPUT
<img width="545" height="99" alt="image" src="https://github.com/user-attachments/assets/6905e532-7f84-4b1d-a86f-16c44ae1824b" />


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT

<img width="579" height="108" alt="image" src="https://github.com/user-attachments/assets/ec323cdc-8d91-4289-afce-991f8876e08d" />


egrep -w '(H|h)ello' newfile 
## OUTPUT


<img width="584" height="100" alt="image" src="https://github.com/user-attachments/assets/0868d5e1-6a93-43f2-9892-339f323bc1c7" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="677" height="103" alt="image" src="https://github.com/user-attachments/assets/70fe88af-6344-439a-a2d8-be66734d8c6a" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="531" height="78" alt="image" src="https://github.com/user-attachments/assets/6c357dc4-a2d2-4e4a-b690-ec93678939c5" />



egrep '(world$)' newfile 
## OUTPUT
<img width="497" height="101" alt="image" src="https://github.com/user-attachments/assets/b377d317-151e-4039-8330-b7c3d089b641" />



egrep '(World$)' newfile 
## OUTPUT
<img width="574" height="93" alt="image" src="https://github.com/user-attachments/assets/1f0f5df5-183e-4d6b-90e2-a0332af096ff" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="583" height="134" alt="image" src="https://github.com/user-attachments/assets/8dd70c5b-fe3a-4870-84d0-32c578e61780" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="475" height="71" alt="image" src="https://github.com/user-attachments/assets/673d53e7-1cd7-4483-b097-f64b30c9ff11" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="567" height="67" alt="image" src="https://github.com/user-attachments/assets/e0f31e58-f730-4df8-9035-7839b2da5421" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="545" height="86" alt="image" src="https://github.com/user-attachments/assets/bd5da4b9-2fef-4f2a-bf78-357baefe3900" />


egrep l{2} newfile
## OUTPUT

<img width="481" height="124" alt="image" src="https://github.com/user-attachments/assets/85355261-6a64-482b-99b1-e01b0df30163" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="583" height="126" alt="image" src="https://github.com/user-attachments/assets/9d12bd6e-db48-4493-ad55-6d5131d64dce" />

cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT

<img width="465" height="69" alt="image" src="https://github.com/user-attachments/assets/f4fba2bf-efc7-4f0a-9c73-1080e7e156db" />


sed -n -e '$p' file23
## OUTPUT
<img width="461" height="77" alt="image" src="https://github.com/user-attachments/assets/6c32bf07-78f6-4a8a-a6b4-bc52211daff0" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="619" height="302" alt="image" src="https://github.com/user-attachments/assets/dd6e1a8d-6458-4e41-a510-335ca7a5437f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="648" height="294" alt="image" src="https://github.com/user-attachments/assets/2a31f086-4b66-4eea-acf8-52b9ca404aae" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="688" height="309" alt="image" src="https://github.com/user-attachments/assets/cf312344-6ecd-41b8-a48c-55a321c8f112" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="615" height="211" alt="image" src="https://github.com/user-attachments/assets/49d284f8-cd50-4a11-b278-0658d98d8aa1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="537" height="149" alt="image" src="https://github.com/user-attachments/assets/84e376d6-e8b5-499f-90fa-2444e8b6a0c2" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="589" height="106" alt="image" src="https://github.com/user-attachments/assets/372c748e-810e-44ef-a95d-1bb7b3e5bcdb" />


seq 10 
## OUTPUT

<img width="485" height="376" alt="image" src="https://github.com/user-attachments/assets/3f7dc19a-d58b-4408-89f2-67901fc50039" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="508" height="138" alt="image" src="https://github.com/user-attachments/assets/7d78c8ad-b4f8-4adf-a129-5c1665beddf7" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="477" height="135" alt="image" src="https://github.com/user-attachments/assets/59dcc23e-73ba-45d4-89a2-599a2acfe832" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="456" height="162" alt="image" src="https://github.com/user-attachments/assets/04b5e591-9f97-4add-8fe8-b20a7203cbc2" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="469" height="144" alt="image" src="https://github.com/user-attachments/assets/6de71d94-4de1-482c-a51a-0025d9919060" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="518" height="133" alt="image" src="https://github.com/user-attachments/assets/95fffe3f-d4f7-4804-a3ea-7475e3ac6a19" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="609" height="141" alt="image" src="https://github.com/user-attachments/assets/53d49d03-1ea1-458c-b719-b246b1d95108" />

<img width="585" height="134" alt="image" src="https://github.com/user-attachments/assets/638ea039-31ce-4edb-9682-7d7416e1510e" />


sed -n '2,4{s/$/*/;p}' file23


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
<img width="478" height="210" alt="image" src="https://github.com/user-attachments/assets/ad597a29-5419-4305-8147-2017f8c5709e" />


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

<img width="475" height="208" alt="image" src="https://github.com/user-attachments/assets/e0b87248-f5d4-4e64-8957-36d726ba3960" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="786" height="352" alt="image" src="https://github.com/user-attachments/assets/ddcfef6c-9319-482e-acff-5432747c363d" />

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="541" height="131" alt="image" src="https://github.com/user-attachments/assets/ffd8115f-8e14-48f6-ac84-e63940924610" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="693" height="129" alt="image" src="https://github.com/user-attachments/assets/3e644cce-df51-455a-bfbe-55b093e54c25" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="822" height="802" alt="image" src="https://github.com/user-attachments/assets/5bd15125-4070-4f7a-b6d0-2d3f3bfcd9a6" />

<img width="858" height="797" alt="image" src="https://github.com/user-attachments/assets/71506101-32ef-4a8f-a3d0-efca033457f6" />

<img width="866" height="806" alt="image" src="https://github.com/user-attachments/assets/18f263b8-c03e-4037-bef9-fd66d4619a9c" />

<img width="850" height="815" alt="image" src="https://github.com/user-attachments/assets/4f099dfc-ce8f-4ac4-baf6-30054eb79e60" />

<img width="940" height="832" alt="image" src="https://github.com/user-attachments/assets/1fb4e0cc-9c88-412e-aca2-d504171eb221" />

<img width="852" height="759" alt="image" src="https://github.com/user-attachments/assets/4a68a362-174f-44fd-8d00-4164283eeb61" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="914" height="793" alt="image" src="https://github.com/user-attachments/assets/51d31014-dfc2-420e-af96-2f7faab34a2d" />

<img width="931" height="791" alt="image" src="https://github.com/user-attachments/assets/14f105d4-130c-4489-9d19-a56df77e04db" />

<img width="932" height="141" alt="image" src="https://github.com/user-attachments/assets/c6f843f7-d833-420b-9fb6-52b95f204c44" />

tar -xvf backup.tar
## OUTPUT
<img width="751" height="794" alt="image" src="https://github.com/user-attachments/assets/5f3e5923-4cda-4560-8346-828456876eab" />

<img width="930" height="838" alt="image" src="https://github.com/user-attachments/assets/3744f5ac-51ca-42c1-8e16-4e166c3ee768" />

<img width="792" height="825" alt="image" src="https://github.com/user-attachments/assets/a0bfe38e-4007-478a-ad45-dfa53e1ca5c8" />

<img width="847" height="708" alt="image" src="https://github.com/user-attachments/assets/ce669504-623e-45c7-b4ca-ea4e3901ac0e" />


gzip backup.tar

ls .gz
## OUTPUT
gunzip backup.tar.gz
## OUTPUT
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="497" height="120" alt="image" src="https://github.com/user-attachments/assets/b91f8c81-3f8d-4764-9fd1-3d21e38f337e" />


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
<img width="850" height="463" alt="image" src="https://github.com/user-attachments/assets/6e95c014-98af-4c17-829c-42206854bd47" />

 
ls file1
## OUTPUT
<img width="417" height="65" alt="image" src="https://github.com/user-attachments/assets/7fac6aff-c3e0-45ff-aa87-7017b42027eb" />

echo $?
## OUTPUT 

<img width="415" height="64" alt="image" src="https://github.com/user-attachments/assets/3381e2ff-d080-4b0e-940e-519eb7fa2410" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
##OUTPUT
<img width="561" height="274" alt="image" src="https://github.com/user-attachments/assets/6ceab59a-3709-4708-975e-2ad6e78151ef" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT

<img width="810" height="95" alt="image" src="https://github.com/user-attachments/assets/5cc1d324-074d-47ed-8ffc-dc92201d7cc7" />


# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="752" height="129" alt="image" src="https://github.com/user-attachments/assets/75e454d4-d3f6-43fd-baa9-451ea429211a" />

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="770" height="100" alt="image" src="https://github.com/user-attachments/assets/a94bef28-36ad-43cd-88ae-5879027b8db4" />

# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="843" height="93" alt="image" src="https://github.com/user-attachments/assets/2f6e91e1-ecfa-4ad0-8168-e828edb8add4" />

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 <img width="518" height="58" alt="image" src="https://github.com/user-attachments/assets/1e728586-9e86-4aa0-bb36-e5c5491f21a9" />

$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 
 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 
 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 <img width="818" height="171" alt="image" src="https://github.com/user-attachments/assets/127a9f40-670a-4c1a-af89-4eef9583a0f8" />

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="532" height="410" alt="image" src="https://github.com/user-attachments/assets/577ca23a-05fc-4258-a972-a36dd834f196" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
<img width="868" height="117" alt="image" src="https://github.com/user-attachments/assets/c35917e2-950e-4903-a61d-35395fc63df2" />

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
 <img width="466" height="162" alt="image" src="https://github.com/user-attachments/assets/08e179ec-fce9-4318-96df-2b0114aca21b" />

cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

<img width="476" height="108" alt="image" src="https://github.com/user-attachments/assets/ac71971e-6106-40ec-b15f-981c92cef64a" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="403" height="64" alt="image" src="https://github.com/user-attachments/assets/ff881df6-4688-4579-9540-4d4f17c20866" />



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
 ./funcex.sh 

 <img width="449" height="58" alt="image" src="https://github.com/user-attachments/assets/ad88468a-30fa-4a4a-aeca-62ebeee98541" />

 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 
 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 <img width="479" height="116" alt="image" src="https://github.com/user-attachments/assets/db56b778-8de6-4bef-b1d4-c0c8b0d84737" />

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 <img width="496" height="438" alt="image" src="https://github.com/user-attachments/assets/1ec09795-46e2-4e94-82b9-29dd5a7ec9f6" />

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="448" height="123" alt="image" src="https://github.com/user-attachments/assets/8f1bfd5a-8294-42d5-b40d-caddeb5105b6" />


# RESULT:
The Commands are executed successfully.
