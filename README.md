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


![Screenshot from 2025-04-25 18-37-42](https://github.com/user-attachments/assets/3bdfa2ff-aae9-48e4-9676-c896f9584986)

cat < file2
## OUTPUT

![Screenshot from 2025-04-25 18-37-04](https://github.com/user-attachments/assets/af393f30-562b-459a-a506-b6636ae8ef73)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2025-04-25 18-38-23](https://github.com/user-attachments/assets/2280dbd2-062f-46c0-9713-0e8256cd5389)

comm file1 file2
 ## OUTPUT
![Screenshot from 2025-04-25 18-38-56](https://github.com/user-attachments/assets/915fc648-306f-45ba-9d3c-4d8bf7bc5860)

 
diff file1 file2
## OUTPUT
![Screenshot from 2025-04-25 18-39-21](https://github.com/user-attachments/assets/2c162c44-2331-4484-be17-24ee7de3eaa6)


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

![Screenshot from 2025-04-25 18-41-58](https://github.com/user-attachments/assets/dd66df9e-c855-4d54-8ef5-b6c8eaabac1d)



cut -d "|" -f 1 file22
## OUTPUT

![Screenshot from 2025-04-25 18-42-55](https://github.com/user-attachments/assets/cc0a34a8-3206-4976-87c3-dd516d2f6be2)


cut -d "|" -f 2 file22
## OUTPUT

![Screenshot from 2025-04-25 18-43-18](https://github.com/user-attachments/assets/07a9fea5-2f6b-403c-85e6-3afcad424bd5)

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



grep hello newfile 
## OUTPUT


![Screenshot from 2025-04-25 18-45-19](https://github.com/user-attachments/assets/72b4cae9-4716-4171-877d-d1c479902c29)


grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-04-25 18-45-44](https://github.com/user-attachments/assets/8563b624-f3ff-4b03-b1ef-3408646dff32)


cat newfile | grep -i "hello"
## OUTPUT


![Screenshot from 2025-04-25 18-46-46](https://github.com/user-attachments/assets/52d8b101-4ee2-4256-be9d-fff9f97938bd)


cat newfile | grep -i -c "hello"
## OUTPUT


![Screenshot from 2025-04-25 18-46-23](https://github.com/user-attachments/assets/b99caa4d-54da-47f4-872a-5532ed9bcc0c)


grep -R ubuntu /etc
## OUTPUT

![Screenshot from 2025-04-25 18-47-43](https://github.com/user-attachments/assets/32462e29-2612-4e62-8a04-c5380e9eaf46)


grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-04-25 18-48-28](https://github.com/user-attachments/assets/e4b93b2b-0ef1-41e4-992a-f763a46d9880)

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
![Screenshot from 2025-04-25 19-01-47](https://github.com/user-attachments/assets/e1f86f83-2319-478d-80db-700241f0f4af)



egrep -w '(H|h)ello' newfile 
## OUTPUT

![Screenshot from 2025-04-25 19-01-31](https://github.com/user-attachments/assets/dfe22c7d-e206-42d8-b728-b05982e6d64a)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![Screenshot from 2025-04-25 19-03-13](https://github.com/user-attachments/assets/821299ba-abbf-40aa-a103-29e7889efced)


egrep '(^hello)' newfile 
## OUTPUT

![Screenshot from 2025-04-25 19-04-02](https://github.com/user-attachments/assets/05a31db5-dcc1-43d1-95a7-4c91d105035c)


egrep '(world$)' newfile 
## OUTPUT


![Screenshot from 2025-04-25 19-04-37](https://github.com/user-attachments/assets/4350bbdb-c483-4a9e-a078-7cc66765cbb5)

egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 19-05-08](https://github.com/user-attachments/assets/e55c7058-7ea3-4166-98ae-8bdd952f2e77)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2025-04-25 19-07-06](https://github.com/user-attachments/assets/c2c00bf5-fc69-46c3-a928-b0014ec3b22b)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-04-25 19-07-55](https://github.com/user-attachments/assets/b8b09f7d-2e5f-46e0-9a4b-062967ae9990)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-25 19-08-26](https://github.com/user-attachments/assets/6e2e6a13-356a-48bb-a901-7e09ef4e56c4)


egrep 'Linux.*World' newfile 
## OUTPUT

![Screenshot from 2025-04-25 19-08-58](https://github.com/user-attachments/assets/87f77de4-ed53-442b-943f-1ef209486db0)

egrep l{2} newfile
## OUTPUT

![Screenshot from 2025-04-25 19-09-58](https://github.com/user-attachments/assets/a37ebe8d-9872-4032-9b76-f6c76473a271)


egrep 's{1,2}' newfile
## OUTPUT 

![Screenshot from 2025-04-25 19-10-35](https://github.com/user-attachments/assets/54852ad3-824b-49d2-8c1f-dd8637fbeb43)

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
![1](https://github.com/user-attachments/assets/0b75c716-5f17-43d3-b333-58e50142df07)



sed -n -e '$p' file23
## OUTPUT
![2](https://github.com/user-attachments/assets/a2cd0d2e-7e0d-4225-89de-3502241ed234)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![3](https://github.com/user-attachments/assets/827055f7-d83e-4d35-a153-23badeda6fd6)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT


![4](https://github.com/user-attachments/assets/98185b26-0a93-43cd-80d0-02adb4acfd86)

sed  '/tom/s/5000/6000/' file23
## OUTPUT


![5](https://github.com/user-attachments/assets/3fc7721e-7fed-498d-be9d-3c2bab773221)

sed -n -e '1,5p' file23
## OUTPUT

![6](https://github.com/user-attachments/assets/e2d186c7-bc87-4d4f-96ca-fd74dee0ea46)


sed -n -e '2,/Joe/p' file23
## OUTPUT


![7](https://github.com/user-attachments/assets/71be1184-ed6b-4964-8c33-28424752b3b9)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![8](https://github.com/user-attachments/assets/ce9ca8bf-3f6c-43eb-8185-68e0a1dff120)


seq 10 
## OUTPUT

![9](https://github.com/user-attachments/assets/cc96b5a5-02f6-44e3-bdd1-710072bffd62)


seq 10 | sed -n '4,6p'
## OUTPUT

![10](https://github.com/user-attachments/assets/5851ad1f-c402-421d-826b-a6ff7c51ff7e)


seq 10 | sed -n '2,~4p'
## OUTPUT

![11](https://github.com/user-attachments/assets/eb0b1e60-a6f0-4bfe-98fe-cb9d618730b6)


seq 3 | sed '2a hello'
## OUTPUT

![12](https://github.com/user-attachments/assets/2379f38b-4feb-45e1-b512-9bb32771e599)


seq 2 | sed '2i hello'
## OUTPUT
![13](https://github.com/user-attachments/assets/833c6a31-2e44-4e27-bb04-947d398b02ca)


seq 10 | sed '2,9c hello'
## OUTPUT
![14](https://github.com/user-attachments/assets/651c305a-2930-49da-9d6e-b34b7182bd1f)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![15](https://github.com/user-attachments/assets/62cdb5a6-2934-4a98-bf05-bad0ad55408a)


sed -n '2,4{s/$/*/;p}' file23
![16](https://github.com/user-attachments/assets/f1321769-245a-4d40-9ee3-3da7ae6e4ef3)


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

![17](https://github.com/user-attachments/assets/261e7f30-415e-4d2d-a05b-a0ba608160b0)

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
![18](https://github.com/user-attachments/assets/7b6917bf-3b1f-4cb0-9010-34cfdaf13e7c)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![19](https://github.com/user-attachments/assets/ae489164-3769-482c-9b72-4c7e4443bee9)

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


 ![20](https://github.com/user-attachments/assets/b44e0bca-e78e-4175-aeae-6bc10af122ee)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![21](https://github.com/user-attachments/assets/24930336-70ff-49f5-8bde-5e65610ad2d2)


![22](https://github.com/user-attachments/assets/4c7ba8e0-d84b-4ad5-828a-48d4614476e4)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![23](https://github.com/user-attachments/assets/8efda15e-5ced-4ce2-a992-3cddeef81b80)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![24](https://github.com/user-attachments/assets/bdddfcc7-78b1-4d8b-926d-85872cfeca44)

tar -xvf backup.tar
## OUTPUT

![25](https://github.com/user-attachments/assets/6244eb8d-980e-4ee6-b872-e0e1c19c288f)

gzip backup.tar

ls .gz
## OUTPUT

 ![26](https://github.com/user-attachments/assets/d2d3bc71-0aca-4c7b-9eaf-7ac52395bd64)

gunzip backup.tar.gz
## OUTPUT

![27](https://github.com/user-attachments/assets/0ee0e9e5-1613-43f2-8e5c-7062c7631a08)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![28](https://github.com/user-attachments/assets/d43e1c06-4292-4f0d-91d0-79389355bfe8)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


![29](https://github.com/user-attachments/assets/880f5adc-41d9-4385-bdb0-85eec925813b)

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
![30](https://github.com/user-attachments/assets/02e98cb0-0823-4a6d-9841-1a7213aef79b)

 
ls file1
## OUTPUT
![31](https://github.com/user-attachments/assets/2e852b13-1588-45e0-a9b1-ec8e48fab55c)

echo $?
## OUTPUT 
![32](https://github.com/user-attachments/assets/2d221705-b0a6-4cff-9c7a-63d35e181b21)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 ![33](https://github.com/user-attachments/assets/920d7501-867e-4eaf-bf9d-a01369f9f077)

echo $?
 ## OUTPUT

![33](https://github.com/user-attachments/assets/6e3ff907-6662-465b-b873-3caf3a85d86c)

 
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

![34](https://github.com/user-attachments/assets/68445397-8903-455a-8944-05a9c743bb77)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![35](https://github.com/user-attachments/assets/8b0a1ae7-8ee9-4d8c-a6da-e0b19d34effc)


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
![36](https://github.com/user-attachments/assets/a6269750-5552-40c1-a460-c0102d92478b)

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


![37](https://github.com/user-attachments/assets/7bc5d0e0-8ef8-47b6-9be5-1cb0cb322bf9)

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
![38](https://github.com/user-attachments/assets/bd3fa98c-918f-4fe9-87e8-83aa78955a55)

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
![39](https://github.com/user-attachments/assets/0b1ec023-85da-4ffb-bd59-bb43312cfe95)

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

![40](https://github.com/user-attachments/assets/e13003ae-4cf7-4e8a-a9c8-23f36be3cd84)

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
![41](https://github.com/user-attachments/assets/ba3cd1c8-2e21-42aa-ad1f-7e201567440e)

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
 ![42](https://github.com/user-attachments/assets/611dd7e7-6094-4ed4-bbc2-dc699bfbec7e)

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
 ![43](https://github.com/user-attachments/assets/766969d6-cdba-4352-b458-bc18ddd0f0d4)

 
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
 
 ![44](https://github.com/user-attachments/assets/82ca8200-02c3-4f86-b3af-56fb87280f7c)

 
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
 ![45](https://github.com/user-attachments/assets/09a67174-2cc7-46ba-bc9e-2045100834c6)

 
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
 ![46](https://github.com/user-attachments/assets/63454b29-1600-4e43-864f-c532f36c497a)

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
![47](https://github.com/user-attachments/assets/a73c67cd-2597-46f9-abef-d0b4ae0703bf)

 
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
![48](https://github.com/user-attachments/assets/b80b5ac5-8376-4764-8099-a472f57eccc0)

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
![49](https://github.com/user-attachments/assets/dc4bb67d-df6c-4df8-99f1-6adb34909db2)

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

 ![50](https://github.com/user-attachments/assets/22bb8726-77f3-4928-902a-53312da037e3)

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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![51](https://github.com/user-attachments/assets/57b3ca85-f61c-4600-9db7-4488bcabb26e)

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
 ![52](https://github.com/user-attachments/assets/54fc3698-e66d-4238-9dd7-4eea6acd66b3)

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
![53](https://github.com/user-attachments/assets/d518a631-c2f0-4a8c-99aa-99bb59b92783)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![54](https://github.com/user-attachments/assets/739e8f84-e5ce-4d44-9376-d9fdb6620001)



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

 ![55](https://github.com/user-attachments/assets/7a77ec0f-e0c6-4f97-95f3-1bc04bc59320)

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
 
 ![56](https://github.com/user-attachments/assets/49d19cc0-df8d-4b55-9b44-8850ea589337)

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
 ![57](https://github.com/user-attachments/assets/41c21647-4337-4f8f-8ed9-8c252dd99873)

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
![58](https://github.com/user-attachments/assets/bc055139-9155-41b5-a25f-8ba5e785fda1)


# RESULT:
The Commands are executed successfully.
