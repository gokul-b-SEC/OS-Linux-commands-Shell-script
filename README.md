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
<img width="341" height="102" alt="image" src="https://github.com/user-attachments/assets/243959ea-3e69-4219-9bcc-b723423cbf92" />



cat < file2
## OUTPUT
<img width="328" height="162" alt="image" src="https://github.com/user-attachments/assets/dd1263f0-dc14-4cac-a5ac-a63bb6ded908" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="362" height="44" alt="image" src="https://github.com/user-attachments/assets/05a15035-03e9-4698-b339-d5b4e6b0ebbe" />

comm file1 file2
 ## OUTPUT
<img width="375" height="198" alt="image" src="https://github.com/user-attachments/assets/636746bf-cf4a-47e2-88e0-bbfffa4a8777" />

 
diff file1 file2
## OUTPUT
<img width="428" height="305" alt="image" src="https://github.com/user-attachments/assets/a30ae306-6ee0-4296-9e7b-9aedc3be3db6" />


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
<img width="383" height="84" alt="image" src="https://github.com/user-attachments/assets/548fc9bf-e24d-4098-9f04-15c57229a5a6" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="433" height="109" alt="image" src="https://github.com/user-attachments/assets/dbf30f17-fad5-4da0-94f8-a2b822f24c0f" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="442" height="110" alt="image" src="https://github.com/user-attachments/assets/66ce1f86-0187-469c-9d34-9f1ed14bc5a0" />


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
<img width="409" height="56" alt="image" src="https://github.com/user-attachments/assets/1cd8d0b5-ff68-4187-a71f-cc0b48d9ad75" />



grep hello newfile 
## OUTPUT
<img width="400" height="58" alt="image" src="https://github.com/user-attachments/assets/aa9d06fd-801e-40b2-81aa-dbcff1262827" />




grep -v hello newfile 
## OUTPUT

<img width="430" height="59" alt="image" src="https://github.com/user-attachments/assets/be2cc20a-bc17-4df4-a9dc-acc90ad46cd8" />


cat newfile | grep -i "hello"
## OUTPUT
<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/ad6b0c91-9502-4d73-aac9-8183c2da0d83" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="578" height="52" alt="image" src="https://github.com/user-attachments/assets/668f9b4f-998e-46ba-bc9e-aadc1f33cdae" />



grep -R ubuntu /etc
## OUTPUT
<img width="609" height="218" alt="image" src="https://github.com/user-attachments/assets/1a31620b-cfbd-4812-8b21-fc905390d3de" />



grep -w -n world newfile   
## OUTPUT
<img width="474" height="80" alt="image" src="https://github.com/user-attachments/assets/de39a51d-3e24-4337-877c-2d80ec64923b" />


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
<img width="563" height="78" alt="image" src="https://github.com/user-attachments/assets/08559dfd-cb97-4b21-9c9f-a7d1a380e74c" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/06adac7f-dd12-475f-b517-aa355c2673f4" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="605" height="81" alt="image" src="https://github.com/user-attachments/assets/733df390-e639-4d62-bcff-d09d6a789077" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="489" height="58" alt="image" src="https://github.com/user-attachments/assets/ae70cbe1-d568-41ae-9422-57bf9d7b227a" />


egrep '(world$)' newfile 
## OUTPUT
<img width="495" height="54" alt="image" src="https://github.com/user-attachments/assets/817198dc-c354-4622-8475-d623c50dedc6" />



egrep '(World$)' newfile 
## OUTPUT
<img width="485" height="49" alt="image" src="https://github.com/user-attachments/assets/a85aa4f2-dd23-4296-adb6-667e95636b19" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="559" height="76" alt="image" src="https://github.com/user-attachments/assets/3c59798a-3f6f-43c2-9222-40e6def7ef61" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="475" height="62" alt="image" src="https://github.com/user-attachments/assets/62433422-721b-4141-b779-d244f9e6d1b2" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="446" height="52" alt="545721026-26ef3e32-ae83-4d77-b0ab-bedd76bd06e3" src="https://github.com/user-attachments/assets/5165d4b3-56a0-4cd7-8245-f65fa77bc6f0" />
<img width="540" height="57" alt="image" src="https://github.com/user-attachments/assets/39b749a8-0b7b-46da-9caf-f47a703300e3" />



egrep l{2} newfile
## OUTPUT
<img width="549" height="76" alt="image" src="https://github.com/user-attachments/assets/bae0976c-fd5a-4d1a-a642-1447b2d2712c" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="492" height="116" alt="image" src="https://github.com/user-attachments/assets/2bfdc5f2-c108-48ec-93d1-76f4504388ed" />


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
<img width="446" height="52" alt="image" src="https://github.com/user-attachments/assets/7ca5d2d2-7f42-477d-90b3-8e9dc2dcd031" />



sed -n -e '$p' file23
## OUTPUT
<img width="463" height="58" alt="image" src="https://github.com/user-attachments/assets/f7a8ab3a-ceca-44dd-8deb-0eff42050d20" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="520" height="243" alt="image" src="https://github.com/user-attachments/assets/a9fb1a08-cefb-409e-bdce-ad810b656099" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="521" height="237" alt="image" src="https://github.com/user-attachments/assets/8d4080b3-58ad-447e-8178-8565ef2aecf4" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="555" height="245" alt="image" src="https://github.com/user-attachments/assets/a14622fa-e184-4218-be6f-1449d074859f" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="481" height="169" alt="image" src="https://github.com/user-attachments/assets/f3ee37b2-d44f-4c5d-8282-d0c6695fc6f5" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="520" height="108" alt="image" src="https://github.com/user-attachments/assets/26cf7df5-dda7-4e82-92e1-d00b08934312" />






sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="560" height="83" alt="image" src="https://github.com/user-attachments/assets/63d09adc-4f1b-47d8-844b-fe8aedc54588" />




seq 10 
## OUTPUT
<img width="470" height="241" alt="image" src="https://github.com/user-attachments/assets/d8d92406-797f-4388-8ca0-841247f1bcda" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/73548424-c87d-4ec5-b3e0-3eabb348d659" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="468" height="97" alt="image" src="https://github.com/user-attachments/assets/8179cf2d-f375-445c-9375-7ec884cb2163" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="476" height="116" alt="image" src="https://github.com/user-attachments/assets/7ece0b26-ef9b-4c59-9038-f98a3d6e381d" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/7eafca73-08ea-4507-8b0b-ba2e1fd3c3cf" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="478" height="94" alt="image" src="https://github.com/user-attachments/assets/6f5473d5-d13d-4842-a9eb-b831dda60f5c" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="542" height="102" alt="image" src="https://github.com/user-attachments/assets/7fec3233-3d89-4c3a-af2f-d7cd187fd232" />



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
<img width="343" height="156" alt="image" src="https://github.com/user-attachments/assets/f19c9a56-71f5-489b-98ff-01a954564348" />


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
<img width="363" height="160" alt="image" src="https://github.com/user-attachments/assets/e8613215-22a2-4a5a-a6f0-6d91ff7d9127" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="652" height="243" alt="image" src="https://github.com/user-attachments/assets/ed3263b2-48bc-44bc-9e62-b264dd964d27" />

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
<img width="536" height="113" alt="image" src="https://github.com/user-attachments/assets/58a372cf-348c-4817-8076-8761ddc33047" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="137" height="69" alt="image" src="https://github.com/user-attachments/assets/aaa79d40-1544-471b-b902-671caeb792d0" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="137" height="69" alt="image" src="https://github.com/user-attachments/assets/6521e83e-fb50-4b87-a9e2-99a4925c84cf" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="137" height="69" alt="image" src="https://github.com/user-attachments/assets/5f03c6a4-c242-46fd-b35c-3f3efce9f0d5" />


tar -xvf backup.tar
## OUTPUT
<img width="137" height="69" alt="image" src="https://github.com/user-attachments/assets/7273675b-8cf6-40b8-acf5-93654a57a8e7" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="691" height="94" alt="image" src="https://github.com/user-attachments/assets/8dd6ab7c-260a-4103-93c8-e2efac58b431" />

gunzip backup.tar.gz
## OUTPUT
<img width="858" height="258" alt="image" src="https://github.com/user-attachments/assets/0c43308e-643a-45bd-b36e-635e8e7eac4c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="710" height="301" alt="image" src="https://github.com/user-attachments/assets/7eac5dd9-b1ff-47ab-87bc-75acc3164c41" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/ab214170-edf5-4b72-bf0e-12c1292771b5" />


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
<img width="430" height="331" alt="image" src="https://github.com/user-attachments/assets/39542fcf-9a88-4a00-bfed-d7c9e11f0859" />

 
ls file1
## OUTPUT
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/b25b8c2c-d5fb-459e-8562-f47e43e17b50" />

echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/b3218470-0553-4184-8d75-d61ab4ca4a80" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="285" height="54" alt="image" src="https://github.com/user-attachments/assets/2682b0e4-5b94-44ce-9030-360e82250037" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="469" height="221" alt="image" src="https://github.com/user-attachments/assets/1c0b0e11-4178-4767-9f57-080d65eb8357" />


 
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
<img width="476" height="243" alt="image" src="https://github.com/user-attachments/assets/ec519dcb-cf4b-48da-9608-9d9f778d8828" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="image" src="https://github.com/user-attachments/assets/6e2352b0-f708-43b6-b817-d4c4d168280f" />


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
<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/b5822d57-bddb-4efb-87ad-f9b4ecc958c2" />

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

<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/3f977bfe-f2ec-4af6-a185-77d53695f37d" />




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

<img width="524" height="391" alt="image" src="https://github.com/user-attachments/assets/8b562093-bd09-4d7b-86d4-8decb6840218" />



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

<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/4148eb07-2829-46f6-963a-70b4c076e038" />

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

<img width="573" height="471" alt="image" src="https://github.com/user-attachments/assets/29dcfb94-e3af-4725-9297-c8cc68c49732" />


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

<img width="541" height="248" alt="image" src="https://github.com/user-attachments/assets/c158fc70-6625-4675-b605-a2091dc13cf2" />

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

<img width="504" height="160" alt="image" src="https://github.com/user-attachments/assets/33090468-d216-4c27-a016-f1e129876b22" />

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

<img width="446" height="201" alt="image" src="https://github.com/user-attachments/assets/f51d790c-710b-4eb2-8d6e-e95463a45434" />


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

<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/58a72d63-0fe4-47cd-988c-3badb7edd573" />

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

<img width="397" height="204" alt="image" src="https://github.com/user-attachments/assets/6be21cda-37ef-40fe-8d15-7ae588cd3c59" />

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

 <img width="412" height="201" alt="image" src="https://github.com/user-attachments/assets/10bef7d9-29a0-4fe9-91dd-1cb149fb10f9" />


 
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

<img width="785" height="304" alt="image" src="https://github.com/user-attachments/assets/0acabd04-c0df-49ba-822b-3ce243404e1d" />


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

<img width="756" height="275" alt="image" src="https://github.com/user-attachments/assets/44a8976b-56d1-459f-a3ad-849dd6685dce" />

 
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

<img width="481" height="144" alt="image" src="https://github.com/user-attachments/assets/05c6c423-21f5-4731-a3a2-e9098ef6be44" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="774" height="137" alt="image" src="https://github.com/user-attachments/assets/c92db8ec-cc57-45c3-b083-a305f11c8148" />



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

<img width="755" height="44" alt="image" src="https://github.com/user-attachments/assets/2ef94fa8-2bb1-4cfb-8467-40eb7b328fa2" />

 
 ./funcex.sh 1 2

<img width="762" height="38" alt="image" src="https://github.com/user-attachments/assets/4d230b69-6aca-48b3-ad98-6dd7c4abd8bd" />

 
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

 <img width="758" height="63" alt="image" src="https://github.com/user-attachments/assets/25dd1153-8cba-43b0-9176-eda338cdf91c" />

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

<img width="762" height="87" alt="image" src="https://github.com/user-attachments/assets/25b264df-4a71-45b6-982d-cce0c5ad4e04" />

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

 <img width="765" height="327" alt="image" src="https://github.com/user-attachments/assets/e5b4f629-4803-45cb-abcc-3f937c2196b8" />

 
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

<img width="783" height="218" alt="image" src="https://github.com/user-attachments/assets/9a5760da-4eab-496b-a95b-079a21f6e3a1" />

 
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

<img width="772" height="70" alt="image" src="https://github.com/user-attachments/assets/dbb2606c-2341-4e47-af8f-9412fa89eb41" />


# RESULT:
The Commands are executed successfully.
