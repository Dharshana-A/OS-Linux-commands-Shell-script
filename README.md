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

<img width="339" height="86" alt="image" src="https://github.com/user-attachments/assets/4620b558-ab4a-4ca3-9849-6f2c2836d785" />


cat < file2
## OUTPUT

<img width="467" height="191" alt="image" src="https://github.com/user-attachments/assets/761f4c28-b540-4caa-b6a5-e8b46ea973cf" />






# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="381" height="97" alt="image" src="https://github.com/user-attachments/assets/980c72bc-e0e4-4b9d-8485-73eee75f7e2e" />

comm file1 file2
 ## OUTPUT
<img width="506" height="212" alt="image" src="https://github.com/user-attachments/assets/02b15856-c23b-4d0f-9a3b-d61163af247d" />



 
diff file1 file2
## OUTPUT
<img width="393" height="190" alt="image" src="https://github.com/user-attachments/assets/79c1f3c4-43ef-4011-aeb8-3cb403c5bceb" />


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

<img width="361" height="66" alt="image" src="https://github.com/user-attachments/assets/3b783174-a24b-4377-bf0a-225c870db09d" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="417" height="137" alt="image" src="https://github.com/user-attachments/assets/3e03c158-7c39-41ab-982c-a3aec2ab2065" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="461" height="127" alt="image" src="https://github.com/user-attachments/assets/eba4124c-4d61-45e8-bd9a-efec0757f61a" />



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
<img width="441" height="60" alt="image" src="https://github.com/user-attachments/assets/127b4d34-4902-4806-bfc4-7c1692aa84af" />



grep hello newfile 
## OUTPUT
<img width="418" height="46" alt="image" src="https://github.com/user-attachments/assets/6d034a46-56e0-4a13-b0bc-cce05ffdcd0e" />




grep -v hello newfile 
## OUTPUT
<img width="415" height="97" alt="image" src="https://github.com/user-attachments/assets/eb07224c-af8e-4cea-bc36-b4098ae3d766" />




cat newfile | grep -i "hello"
## OUTPUT

<img width="550" height="57" alt="image" src="https://github.com/user-attachments/assets/4d2f6d05-9b2d-4af8-ba52-5dbe7d4ad701" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="460" height="67" alt="image" src="https://github.com/user-attachments/assets/6cef6901-898a-459e-82e1-9e0cc44b0ec7" />




grep -R ubuntu /etc
## OUTPUT
<img width="722" height="612" alt="image" src="https://github.com/user-attachments/assets/e6dc4ce2-4b34-48b0-9069-5ca7745a4e3d" />



grep -w -n world newfile   
## OUTPUT
<img width="447" height="51" alt="image" src="https://github.com/user-attachments/assets/c07cfeb4-9e2e-4464-b6ca-24abace9f973" />


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

<img width="467" height="70" alt="image" src="https://github.com/user-attachments/assets/100522d2-d08a-4418-bc51-0b2ef5facf92" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="497" height="65" alt="image" src="https://github.com/user-attachments/assets/97802813-acb4-4e3d-810f-30ee6fbab5d9" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="541" height="90" alt="image" src="https://github.com/user-attachments/assets/00ba2c6e-5b0c-45a1-b205-13ffe97bf5d6" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="367" height="87" alt="image" src="https://github.com/user-attachments/assets/269051ae-c89a-46c8-86dd-169129057d7f" />



egrep '(world$)' newfile 
## OUTPUT
<img width="452" height="77" alt="image" src="https://github.com/user-attachments/assets/ad9b8977-07ee-450b-8cb1-ba46b4aaed90" />



egrep '(World$)' newfile 
## OUTPUT
<img width="362" height="102" alt="image" src="https://github.com/user-attachments/assets/43ccec7b-c2e5-4f91-80cd-da70d4bb18d1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="512" height="80" alt="image" src="https://github.com/user-attachments/assets/63970e0c-08ed-49a6-bd29-eaf6a42316ea" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="433" height="52" alt="image" src="https://github.com/user-attachments/assets/37a6ea3b-030c-4dba-9c5f-b712bdf22439" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="327" height="62" alt="image" src="https://github.com/user-attachments/assets/289fb3b8-0697-44cb-b821-af0fd649eb07" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="470" height="37" alt="image" src="https://github.com/user-attachments/assets/506943b8-c64c-42b6-b839-6fc3d75bdb47" />


egrep l{2} newfile
## OUTPUT
<img width="410" height="63" alt="image" src="https://github.com/user-attachments/assets/0513fe7a-8020-4c90-bc87-57ff5a27348b" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="392" height="93" alt="image" src="https://github.com/user-attachments/assets/0e09f50d-bc06-49e2-8538-00590721a511" />


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
<img width="433" height="72" alt="image" src="https://github.com/user-attachments/assets/c565811d-1c37-4689-b734-aa5adca92be9" />



sed -n -e '$p' file23
## OUTPUT
<img width="402" height="41" alt="image" src="https://github.com/user-attachments/assets/a0e9f7bf-0c20-4458-9a8a-5f520db64a7e" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="455" height="153" alt="image" src="https://github.com/user-attachments/assets/e4217dcc-5b52-4010-8518-422559ddb88e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="467" height="140" alt="image" src="https://github.com/user-attachments/assets/7f0be3b6-31fb-42ad-9904-0b79ccd64820" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="520" height="153" alt="image" src="https://github.com/user-attachments/assets/7e5e9196-7e13-4d1f-ae50-0d34de51f64b" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="478" height="102" alt="image" src="https://github.com/user-attachments/assets/80df3ed7-95ad-427b-882d-e50b2fa55856" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="455" height="82" alt="image" src="https://github.com/user-attachments/assets/abf6e68c-9599-4c11-8b73-7540f716c02f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="481" height="62" alt="image" src="https://github.com/user-attachments/assets/5cf4c0ed-4b8a-4e87-aee8-a6acfeaf8ef5" />



seq 10 
## OUTPUT
<img width="377" height="190" alt="image" src="https://github.com/user-attachments/assets/b373a24a-aeab-457d-97ae-c28ba63b7d41" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="567" height="47" alt="image" src="https://github.com/user-attachments/assets/1a25f712-0753-483e-85fb-795ff0742cd3" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="512" height="66" alt="image" src="https://github.com/user-attachments/assets/df4d359c-1180-4627-bc22-ce76f05e4876" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="390" height="77" alt="image" src="https://github.com/user-attachments/assets/8eaf2c1a-a48b-4d24-b901-af9f13b4b9ce" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="427" height="72" alt="image" src="https://github.com/user-attachments/assets/97c1cb01-f304-40c7-95aa-f57cb3348d2f" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="418" height="70" alt="image" src="https://github.com/user-attachments/assets/040d7a3e-adc1-4ffc-ad6c-4a82ad8be01b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="473" height="77" alt="image" src="https://github.com/user-attachments/assets/b341baa1-0f94-4e0e-9105-41ed4ac2daa4" />



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
<img width="571" height="103" alt="image" src="https://github.com/user-attachments/assets/34de0cf4-99d7-4fc5-964e-28e0788f8d4b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="562" height="106" alt="image" src="https://github.com/user-attachments/assets/620c1c06-8c61-4c07-9aad-babfc51368c9" />

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
<img width="460" height="77" alt="image" src="https://github.com/user-attachments/assets/8ec9b374-5807-46b3-a9e2-7722c6f3dc85" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="522" height="73" alt="image" src="https://github.com/user-attachments/assets/bef99670-d3e4-4bd5-8b0c-9dfb04b37246" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="532" height="67" alt="image" src="https://github.com/user-attachments/assets/1bb4932b-1efc-46a4-869b-475f47cb61b9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="651" height="250" alt="image" src="https://github.com/user-attachments/assets/bc1258de-a674-4290-98bd-666035cbec53" />


tar -xvf backup.tar
## OUTPUT
<img width="522" height="148" alt="image" src="https://github.com/user-attachments/assets/1b1ee6fe-7b00-477f-bf4c-4aab7014a334" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="597" height="86" alt="image" src="https://github.com/user-attachments/assets/df663d2a-671b-4a2b-8d8f-c8dea70c7d73" />

gunzip backup.tar.gz
## OUTPUT
<img width="520" height="53" alt="image" src="https://github.com/user-attachments/assets/774152e2-8a92-4835-88b7-5397de5b8c53" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="706" height="60" alt="image" src="https://github.com/user-attachments/assets/1b7f4982-207e-4c16-b9fc-7d67942f952f" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="520" height="97" alt="image" src="https://github.com/user-attachments/assets/312f72b2-86d9-4634-adad-bd16a400af5e" />


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
<img width="377" height="222" alt="image" src="https://github.com/user-attachments/assets/3b655cfa-4625-46b6-9df3-6e4796675b42" />

 <img width="373" height="41" alt="image" src="https://github.com/user-attachments/assets/ab59b71c-6cb9-4129-b005-252319471e1c" />

ls file1
## OUTPUT
<img width="201" height="42" alt="image" src="https://github.com/user-attachments/assets/e9935eb9-5ffc-4b42-99f7-0ac25ad56506" />
<img width="433" height="45" alt="image" src="https://github.com/user-attachments/assets/ce82c792-aafc-4794-8382-9cf7ed72cb8c" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="507" height="57" alt="image" src="https://github.com/user-attachments/assets/ec6fda62-a0e8-49d9-82df-2ee0d5a4e973" />

abcd
 
echo $?
 ## OUTPUT
<img width="342" height="46" alt="image" src="https://github.com/user-attachments/assets/398f53e5-97f2-4c12-ab68-ee453ddbe42b" />


 
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
<img width="482" height="203" alt="image" src="https://github.com/user-attachments/assets/33acdd2f-debb-4af5-9a91-978d260c07f8" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="667" height="48" alt="image" src="https://github.com/user-attachments/assets/899b8e89-3bd2-4f18-baaf-8e280dc0d543" />


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

<img width="527" height="60" alt="image" src="https://github.com/user-attachments/assets/8afc372a-0082-4058-83a1-42b0949296c8" />

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
<img width="706" height="120" alt="image" src="https://github.com/user-attachments/assets/4bd72b58-a0aa-4747-81e3-0352bf6b6a35" />




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

<img width="637" height="102" alt="image" src="https://github.com/user-attachments/assets/1a1f2b57-992b-49cc-918d-a239ef495cfd" />

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
<img width="585" height="117" alt="image" src="https://github.com/user-attachments/assets/b750248a-5857-49ca-a334-c290cc194d18" />

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
<img width="630" height="93" alt="image" src="https://github.com/user-attachments/assets/83901e9a-0f46-4e8e-90c5-7fd79d231128" />


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
<img width="686" height="62" alt="image" src="https://github.com/user-attachments/assets/db572214-23d8-400f-9b5e-602fdad18ae9" />

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
 ## output
 <img width="431" height="42" alt="image" src="https://github.com/user-attachments/assets/c800a842-0993-4137-b3ba-3c04baf238a8" />

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
 <img width="577" height="102" alt="image" src="https://github.com/user-attachments/assets/9dbc3073-a0c6-4571-8856-ffe77b0c6132" />

 
 
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
 ## output
 <img width="532" height="177" alt="image" src="https://github.com/user-attachments/assets/7ebf12e3-584e-47ae-9fb0-54c596f4539f" />

 
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
## output
<img width="610" height="113" alt="image" src="https://github.com/user-attachments/assets/327b618d-cc5f-4ab7-a7a9-4561c5ca8026" />

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
## output
<img width="607" height="185" alt="image" src="https://github.com/user-attachments/assets/d41d14c5-2e3f-4a08-bfc4-283d853fe137" />

 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

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
