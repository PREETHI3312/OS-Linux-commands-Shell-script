## NAME:Preethi A K
## REGISTER NUMBER: 212223230156

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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/87ac0d6a-1446-457d-86a1-988721ea01af)




cat < file2
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/8fccc8a1-d8c7-490c-954c-8d12780ad55d)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/faf7be7f-368e-4972-a142-bdb707f5ef60)

 
comm file1 file2
 ## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a7a105ea-6765-4fd6-b997-014bbd767c2a)

 
diff file1 file2
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/01ad1a86-1512-4ffd-9dd0-33ad1b981581)




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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a0cce53d-e73e-455e-9340-72b81f67ad6d)





cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/e7a008d1-3e4c-40d2-a3a5-44ba333b2e4f)





cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/c5735266-0638-486c-a756-e6b0340deb48)




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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/b702dd82-0b07-4005-b957-0cc15c1d3d23)




grep hello newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/08ea546b-76f1-4eda-9e0f-f203f280e2a6)





grep -v hello newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/45040c17-58c3-446f-aa3f-077eb70a68f3)




cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/d193581f-02b6-4555-b088-7b05d7461148)





cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/65a8474e-cc02-4c2d-9e67-8e76ee6c4584)





grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/22fdcf81-932f-4b8d-8525-a64e0ec2f425)




grep -w -n world newfile   
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/3e1bda9a-6ea0-4db2-a568-fbc718c37a19)


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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/25d0fec3-0f33-4029-bb7a-8b6dc3d9f165)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/949add15-11a4-4fe7-84e8-440126aaa9a4)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/30add5da-a3a2-4363-a53a-130b58db8320)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/55b62521-ae26-4c21-a7ef-76af4069aca8)




egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/6231c0d4-c8b0-4331-80ab-b50c2c750dfa)





egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/54bd99ae-8395-4423-a4d5-33985e59bf47)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f34d417b-508e-4569-8d0e-e8a3ad4d6b45)




egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/d39364c0-71da-42bc-844d-be536727a70f)




egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/7149b0f0-5880-435e-8c34-0114f0fa3f94)



egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a1558cfd-123d-4d04-a072-edf7f8e194de)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/919d40e4-c1ea-42e1-9645-de17925281f8)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/cea59baf-267b-419f-aee4-2673da56d2d5)


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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/98b8fafa-04d2-41ed-ad0a-f1230817d95a)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/b660c572-1734-40ce-be88-9252a60d9aa3)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/dbb7abdd-1f69-4e0f-8433-2953261eb789)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/6aa29cfd-6b07-4d27-b36e-1b14d1cb2e7e)




sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/30f5c5a9-9c75-43f0-8ad1-38df5d8c8177)




sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/0257c450-9623-4f9c-a9fa-376e59ea41eb)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/13bd70de-b1df-4d66-91f4-400ca29f4092)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f4130ac3-9533-4d96-8f07-cabd48ddeb4b)




seq 10 
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/6878d8f6-6916-4079-9662-041241ba0fb7)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/81bde4e8-4de7-46ae-a6ab-91a67224ad05)




seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/fd8471e6-bc9a-43b1-aa5d-573add27fa89)




seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/444759b0-3989-40f1-add9-59938cbb27f1)




seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f725afb5-e8b8-4694-b49c-b8a0c813a692)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a00f2a8c-4b7d-4822-99cf-83263a691c6a)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/d04ee7c2-46ee-43ac-93b2-0ea156edc231)



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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/0fa515bd-81b8-4cb3-8d49-4e050065141e)



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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/47a9031a-70e8-4290-ab78-aee3b3336700)




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/3a8b94a3-b62c-4e2d-ba61-6b952493ee12)


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
 ![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/bfeb1938-f6da-4d70-a305-87724b6f9b66)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a0a2671d-6f19-4682-bd0d-36e82d2a7048)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/4c9a04e6-dfe5-4928-af8f-b4f35f38d37c)



mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/ccbc4154-17d8-4dc5-bbaf-0896a668b8a5)



tar -xvf backup.tar
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/0d5efaa0-863c-4b17-9ed8-3e9dd6f09955)


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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/8b571dc0-2f93-4ab2-a314-0055d7559ee3)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f05197ce-9a61-4432-8677-06f9a3f2074d)



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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/66ce463b-a769-4ce7-9701-472a735ec84e)


 
ls file1
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/6d43e64c-5b38-4b4c-953d-15306e4f0962)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/e207d92e-1b49-4f24-bf5e-6b509e151ca3)

 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/84516bf6-930b-4545-8031-e8922ded7758)


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f5691f96-7fb8-405b-aca8-99b245694866)

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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/9e14508f-e06b-48bd-8335-24ab45869507)

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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a3bbfe31-a584-41fa-bb8e-34f6a8c71c2d)



# using numeric test comparisons
cat >  iftest.sh 
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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/f0324dc3-e174-4c13-9e62-2b8e12f0ece8)


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

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/4d51cbe0-75a7-4c8b-9897-31d80e242b23)


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

![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/b23da05d-9057-4155-a3b3-e0d5e1658424)

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


![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/dd2856b3-6746-4001-9bb5-64248d70cbf2)

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
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/2089b93c-f8f4-4aa2-9a14-7ad18c022649)

 
cat > whiletest
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```bash
#!/bin/bash

```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/01d121de-472d-4dbd-b7b9-3b02b5273151)


 
 
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

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/37852111-38c2-4d5b-b02e-db081bb55911)


 
 
 
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

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/5db0aa23-2b65-47be-845b-d27e71d1cf0e)

 
 
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

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/e871a57b-eba5-4f24-beaa-b50a1cc05f9d)


 
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

## OUTPUT

![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/3e502c00-aa25-42d7-94f4-c1cf42abbeb0)



 
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

![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/57eb9b7e-55ed-4f8a-b04f-299ca7312d54)



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

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/a2fc3dd0-6460-481c-93c6-644032cf66bf)



$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/23e57dee-3012-407b-a599-187a55addb7b)



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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/2811cf5c-8f23-497a-8175-1e53557b62ab)


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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/25c8eba9-2ae6-4b0d-aee8-0f5bdc40756f)



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
 ![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/7ff92879-790a-4e10-b53d-b3f846385518)


 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/605c7e2c-66cc-4915-b199-f4a7fe1f3dc7)


 
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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/85d238ab-8b91-4dd4-a8a6-6b840499c3ba)



 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/321f81e4-81c7-499b-b9f5-1cab56f6288f)





 
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
./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/cdfc76b5-6701-4b9d-ac3a-d01716b50612)

 

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/d16bf8f4-1339-48cf-a69f-099205f74514)


 
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
$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/71f9847b-4423-43ed-9b5a-6fe1b1902839)


 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
 ./argshift.sh 1 2 3
```



 
 
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
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/8a81067c-381e-4a78-a1f8-a6b503c919a4)
![image](https://github.com/PREETHI3312/OS-Linux-commands-Shell-script/assets/151625222/895da9ca-8150-4a82-907a-1ee93a57e361)


 
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
 


# RESULT:
The Commands are executed successfully.
