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
![image](https://github.com/user-attachments/assets/d9a9b5a0-ce98-4463-8694-de5968f830dd)



cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/a08c46f1-661d-42eb-8b46-0cdf2d83cbd6)


# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/22dd609e-0754-4645-9d61-4b313c467a31)


 
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/f2e8afd8-fb05-4db5-986c-72423fda2e67)


 
diff file1 file2=
## OUTPUT
![image](https://github.com/user-attachments/assets/9afe8ebc-a7cc-461f-9560-63fcf4c6e671)



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
![image](https://github.com/user-attachments/assets/2842c57f-ed08-4e2d-a57d-223864f709ed)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/9b7b3ef6-dc5d-4a09-9451-f43f5f8744e1)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/42885571-2f9c-4190-9eee-8ae3c7ec2ad9)



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
![image](https://github.com/user-attachments/assets/353cecb6-7957-4834-a674-65dae20b4577)



grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/d8fff637-a75a-4c70-a04b-582becec3c1f)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/86229310-4404-48e4-9fd7-c3d163b2a5a4)



cat newfile | grep -i "hello"
## OUTPUT
catcay![image](https://github.com/user-attachments/assets/f9c1859a-89a2-4c7e-9f95-40365a0ef593)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/0a39a9cc-38cf-4971-ab99-ad8e117ff923)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/3318c4c5-df1d-4daa-b2fd-cd4040c988f3)




grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/28c99648-7b86-471f-bba7-ce2616622de3)


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
![image](https://github.com/user-attachments/assets/06d09963-6c29-42b9-87be-0161f9bb9565)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/991b34d0-14f7-43c4-bea7-60d12fca1a29)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a12a0579-0bfc-44f6-91e6-4110cd7d0dbf)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/23eebaf9-7a5e-4064-8e3e-aa186e77ab2c)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7e709133-5cb9-456e-943a-96d858083607)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/7fc123fc-a21e-428c-8752-0b1a42476953)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/505780a4-847d-4cbb-98ed-6cebde640fc5)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/bde4baa4-46a2-4a9a-8840-2a2bd0f359cf)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e06d0975-b629-4d5d-824a-0fbce8ecf1a5)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/fade5397-358a-4524-a620-3f2c99724ca3)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/69905dbb-0162-4c24-8e71-0247261c4ff1)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/97f1302a-2895-45e7-b609-d09527052f91)


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
![image](https://github.com/user-attachments/assets/cd96e4b5-e262-4995-b8d2-db38f2652aa9)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/3bd8cb4a-b773-4c9f-82fa-ae98766e3e7f)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/60b6abb5-a2d1-4322-8a0d-01f03cda3a42)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6cb53acf-cf7e-4ec4-ad96-6c00a0010a85)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/a6d10a2d-8275-478b-9640-095b2a749731)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/5bfc80a0-399e-45a0-9ccc-ad1046d478d3)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/3ff4f743-80c0-4463-b374-b035ed0ca29e)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/42778dc3-9278-4bf4-a9b0-cbcd9628d5f9)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/90dbe783-eb48-4a96-ad5a-44721b6cf243)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/9d250bb6-35c9-4458-92fb-5697f20e138a)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/33e99f31-6cba-4bbc-bcbd-a82352b8ad7b)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/2e176a7e-952e-4176-bd0f-0b561f6848df)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/c194f650-1936-40c1-ba4d-f2b27c1fb185)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/0f5a0df1-2c0b-4143-8bca-1c638095d311)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/27246303-bf6e-48bd-9543-ebb3e81f7627)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/f9bbde87-894a-4667-9adf-474a464c0f46)


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
![image](https://github.com/user-attachments/assets/78947bc9-23ac-4fa6-aee0-896d571e81d4)


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
![image](https://github.com/user-attachments/assets/6cd9039c-a3cc-4948-bcae-7e1022494d38)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c4a972a3-66c4-4f55-96a6-98f50000ce16)

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
![image](https://github.com/user-attachments/assets/bec165b5-622d-4f59-9529-24e1b4cd2822)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/381d954c-4b3f-4c17-a68d-7a39554d11d8)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/034b64c3-ca94-4368-8558-10e9f3518bb6)


mkdir backup
 
mv backup.tar backup
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/bf7111a0-a133-4d5c-be1c-184aa1e815c6)



tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/28829fe0-ec0b-41c8-b729-40679e8da395)


gzip backup/backup.tar

ls backup/
## OUTPUT
 ![image](https://github.com/user-attachments/assets/7c5b593d-0d02-4278-8bdf-42e167a624d3)

gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/423f648e-8c46-45fb-9111-8cc72e9a6a44)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/ef8a8449-d7ba-4b31-992b-091635ec28e8)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/1b7f090b-fe10-4e1c-b5d0-138a58527faf)


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
![image](https://github.com/user-attachments/assets/39562f27-6faf-481f-a181-b8125834d720)


 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/4d59591a-ff89-420e-bfe2-ab1361afb1ea)

echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/1daa1145-765b-42dc-b4e1-f9ad55365efc)

./file1
bash: ./file1: Permission denied
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/3e02c5b8-1190-4ee5-af99-63e929effcf4)

echo $?
## OUTPUT 
 ![image](https://github.com/user-attachments/assets/75670820-d8ae-4d4c-b63b-13af8a34fda4)

abcd
## OUTPUT
![image](https://github.com/user-attachments/assets/03b4a231-283b-4fa6-a6cf-f7cc20b845a8)

 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/cfad55eb-bb4e-4fea-9d79-93de3b284eb2)


 
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
![image](https://github.com/user-attachments/assets/3a58bbdd-7593-421d-b91b-48f0d52ea544)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/c3a1cae6-a0df-4f5d-929a-3f79d6be2d1e)


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
![image](https://github.com/user-attachments/assets/5694f78b-c471-4b75-91c9-03d0fd4b01ce)

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
![image](https://github.com/user-attachments/assets/5d2c9cce-9c92-4531-b91e-9f11ba34966b)



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
![image](https://github.com/user-attachments/assets/2079102e-ae5d-457b-8f39-498cc18f55e9)

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
![image](https://github.com/user-attachments/assets/be562898-7222-44ec-85ab-42e2f6e95248)

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
![image](https://github.com/user-attachments/assets/08d2db37-df44-4f9f-afe3-3a27406eb613)


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
![image](https://github.com/user-attachments/assets/0a022f7e-adb8-4a82-8164-f69c72c933b0)

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
![image](https://github.com/user-attachments/assets/9ac3c36b-c057-4ba5-b333-4a317aaa6848)

 
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
## OUTPUT 
![image](https://github.com/user-attachments/assets/68680c45-5ddb-42a7-ba00-bc15c2d5eb56)

 
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
$ ./untiltest.sh
## OUTPUT 
![image](https://github.com/user-attachments/assets/2d875ead-c045-49d5-b455-eff8dfb7ba7d)

 
 
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
$ ./forin1.sh
## OUTPUT 
![image](https://github.com/user-attachments/assets/8bbec228-68c6-4abd-a4aa-c0d2db55e55a)

 
 
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
![image](https://github.com/user-attachments/assets/84dc7e89-192a-4656-b6dd-72e7620caac2)

 
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
![image](https://github.com/user-attachments/assets/08f0d32e-1f48-4ae2-ba0d-7339ca9bd4b7)

 
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
![image](https://github.com/user-attachments/assets/ed3cc4c1-74a9-48b4-b32c-436bb4c7f68c)

 
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
$ ./forin1.sh
## OUTPUT 
![image](https://github.com/user-attachments/assets/8c5ee40b-a82d-4289-a99a-7abc9c9ee17c)



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
![image](https://github.com/user-attachments/assets/d383a492-cfae-4479-854f-5eff53159869)


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
![image](https://github.com/user-attachments/assets/96196f88-c530-442f-8de8-c7a59bd4e40f)


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
![image](https://github.com/user-attachments/assets/d1ab3130-265c-42f4-98b8-cd8583f03429)


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
![image](https://github.com/user-attachments/assets/e7348aa3-21f4-44d7-8238-f1e43046adc9)

 
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
![image](https://github.com/user-attachments/assets/b9647a72-f7de-46a8-93c5-209675d5f7f9)


cat forcontinue.sh 
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
![image](https://github.com/user-attachments/assets/7f724f3f-b2f6-4551-90fa-ab2e8a2f3078)

 
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
![image](https://github.com/user-attachments/assets/34bcf00b-1c4b-4f9a-a72d-f06ec57daf93)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/8f713a51-f20c-4342-a5ae-7b78f4dbe97c)



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

 ./funcex.sh 

 
 ./funcex.sh 1 2
## OUTPUT
![image](https://github.com/user-attachments/assets/aa1f1a2c-8f97-4406-b682-f45b02cece48)


 
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
![image](https://github.com/user-attachments/assets/246d3342-6470-448f-af60-905729d90538)
 
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
![image](https://github.com/user-attachments/assets/71797238-37bf-4f9c-a43b-240e70bff8b4)

 
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
 ./argshift.sh 1 2 3
 ## OUTPUT
![image](https://github.com/user-attachments/assets/6cf3f0e9-e59c-4ec9-8bcf-9d60b45ca2d9)

 
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
![image](https://github.com/user-attachments/assets/76658a84-eca3-401a-b9a4-ccf134b14884)

 
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
![image](https://github.com/user-attachments/assets/984226e9-09e3-400f-a06c-8fb5393a1fe2)



# RESULT:
The Commands are executed successfully.
