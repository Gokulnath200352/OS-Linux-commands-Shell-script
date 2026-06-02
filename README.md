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
<img width="351" height="163" alt="image" src="https://github.com/user-attachments/assets/31a33e3e-49fd-4042-8274-cef09271ab1a" />



cat < file2
## OUTPUT
<img width="323" height="207" alt="image" src="https://github.com/user-attachments/assets/7022b2e8-7517-4bdf-a755-23d4c362d65a" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="485" height="78" alt="image" src="https://github.com/user-attachments/assets/c585e815-cd12-4f5e-ab34-d9e0fe4ea950" />

comm file1 file2
 ## OUTPUT
<img width="407" height="259" alt="image" src="https://github.com/user-attachments/assets/5fd1ad79-4370-46ca-9880-16af76eee0be" />

 
diff file1 file2
## OUTPUT
<img width="410" height="315" alt="image" src="https://github.com/user-attachments/assets/38ffd268-fd4a-44f8-914b-7589c72dacea" />


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
<img width="376" height="105" alt="image" src="https://github.com/user-attachments/assets/d9642f6e-02ed-4fc3-861d-7ca0a8a6de18" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="409" height="130" alt="image" src="https://github.com/user-attachments/assets/33d25e7a-fc70-4376-a89d-5624ff965af7" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="431" height="146" alt="image" src="https://github.com/user-attachments/assets/dd2eb6d2-7b80-4290-9145-8733643d1198" />


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
<img width="410" height="81" alt="image" src="https://github.com/user-attachments/assets/9799ec0e-d52b-47b0-a165-5038e68f9224" />



grep hello newfile 
## OUTPUT
<img width="311" height="110" alt="image" src="https://github.com/user-attachments/assets/82ef6e5e-ec65-4e81-a7bd-9592889845bc" />




grep -v hello newfile 
## OUTPUT

<img width="345" height="77" alt="image" src="https://github.com/user-attachments/assets/e3796a23-ff8c-4a5f-963e-8477f7c4ffaa" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="432" height="97" alt="image" src="https://github.com/user-attachments/assets/dfbdde66-ab0e-4c37-b167-b036317210a4" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="502" height="77" alt="image" src="https://github.com/user-attachments/assets/bec6cd18-3ec6-4377-83f2-293b0cb0d2d6" />



grep -R ubuntu /etc
## OUTPUT

<img width="801" height="231" alt="image" src="https://github.com/user-attachments/assets/46257962-8312-474b-b504-0dddf0e9dbee" />


grep -w -n world newfile   
## OUTPUT
<img width="443" height="117" alt="image" src="https://github.com/user-attachments/assets/047f65e7-f342-40eb-ab7c-41b4ce49412b" />


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

<img width="480" height="99" alt="image" src="https://github.com/user-attachments/assets/67ae0163-7821-4856-bcf9-625642c1a82a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="392" height="107" alt="image" src="https://github.com/user-attachments/assets/2f62aeba-7335-425c-8fbc-2e2eabd19b7a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="501" height="105" alt="image" src="https://github.com/user-attachments/assets/82d26352-d1f8-4298-80da-38a23fe03991" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="337" height="97" alt="image" src="https://github.com/user-attachments/assets/ef6dd209-acd8-40d3-8f6d-7ca8686e4f58" />


egrep '(world$)' newfile 
## OUTPUT

<img width="329" height="131" alt="image" src="https://github.com/user-attachments/assets/c96c1fa8-8991-410e-97a6-19e969726c2e" />


egrep '(World$)' newfile 
## OUTPUT
<img width="374" height="94" alt="image" src="https://github.com/user-attachments/assets/ba43c14e-aae3-4bc4-8cef-da896569bb87" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="488" height="134" alt="image" src="https://github.com/user-attachments/assets/61e2ccfb-021d-4b05-beb6-061ce1f54b6f" />



egrep '[1-9]' newfile 
## OUTPUT



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="475" height="73" alt="image" src="https://github.com/user-attachments/assets/338e9817-6717-4a19-876b-998c6bf497f4" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="520" height="75" alt="image" src="https://github.com/user-attachments/assets/f4c0f6de-1f90-4482-8525-30a37d10397c" />

egrep l{2} newfile
## OUTPUT
<img width="363" height="100" alt="image" src="https://github.com/user-attachments/assets/f0102a7c-642f-42fa-b9bc-82bc0ac6651a" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="430" height="137" alt="image" src="https://github.com/user-attachments/assets/b135d08d-8bad-47c4-9a05-6d7dbb5c3953" />


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
<img width="421" height="80" alt="image" src="https://github.com/user-attachments/assets/57358f15-327f-4859-91a5-977de366b23a" />



sed -n -e '$p' file23
## OUTPUT
<img width="582" height="285" alt="image" src="https://github.com/user-attachments/assets/479362a7-c40b-4df8-9e5a-97fe140f7c55" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="569" height="290" alt="image" src="https://github.com/user-attachments/assets/5a77d5f8-d2d0-4148-91e6-3279b4117b27" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="524" height="291" alt="image" src="https://github.com/user-attachments/assets/123476f9-06a6-4e2a-bc23-7df165c10597" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="578" height="287" alt="image" src="https://github.com/user-attachments/assets/d8cd44e3-827e-45f0-974e-0319ec40b90e" />



sed -n -e '1,5p' file23
## OUTPUT

<img width="528" height="193" alt="image" src="https://github.com/user-attachments/assets/52e8c585-afc8-41f5-97da-599aa9f35ce0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="479" height="136" alt="image" src="https://github.com/user-attachments/assets/31b27bfe-f16e-47f5-8d13-762349e5678e" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="544" height="106" alt="image" src="https://github.com/user-attachments/assets/b16a8155-170f-4be5-b1cd-74081c864063" />


seq 10 
## OUTPUT
<img width="240" height="351" alt="image" src="https://github.com/user-attachments/assets/556a65a2-97de-4201-aebf-c5997b2f200c" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="430" height="135" alt="image" src="https://github.com/user-attachments/assets/66704d9a-a647-4676-9b38-39814b6f8881" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="451" height="129" alt="image" src="https://github.com/user-attachments/assets/840b424c-b6f1-4b26-8ec9-149f84864443" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="438" height="167" alt="image" src="https://github.com/user-attachments/assets/72bafdf8-3388-40fe-8660-28361bf0f158" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="383" height="125" alt="image" src="https://github.com/user-attachments/assets/a5f9d63f-94bb-4752-9d85-d8ab436c6ce6" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="491" height="123" alt="image" src="https://github.com/user-attachments/assets/d219af64-d804-4236-ab4a-ff79f7f05255" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="497" height="129" alt="image" src="https://github.com/user-attachments/assets/b1de3635-d097-458d-86b5-dcfc2ea4f61a" />



sed -n '2,4{s/$/*/;p}' file23
<img width="497" height="126" alt="image" src="https://github.com/user-attachments/assets/4f30b85e-2a5b-40f5-9f32-45d9d227b90f" />


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
<img width="447" height="188" alt="image" src="https://github.com/user-attachments/assets/27ddff8d-70a9-4bcf-a414-3309f09ad27a" />


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

<img width="436" height="195" alt="image" src="https://github.com/user-attachments/assets/8d614428-6461-480a-b654-6b378ec68a1b" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="593" height="282" alt="image" src="https://github.com/user-attachments/assets/e810cdc0-1986-4157-b7b9-d928a9d9a923" />

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
<img width="417" height="139" alt="image" src="https://github.com/user-attachments/assets/7d484a81-c272-4c58-8a4b-3ae0256493c3" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="530" height="160" alt="image" src="https://github.com/user-attachments/assets/420dbaff-66d8-4cfa-be6e-9829801776ee" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="679" height="261" alt="image" src="https://github.com/user-attachments/assets/d4b948e4-0142-47be-8651-584e5ef44fd9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="640" height="88" alt="image" src="https://github.com/user-attachments/assets/6005c5cb-2ae1-4bed-b686-409660898a78" />
 

tar -xvf backup.tar
## OUTPUT
<img width="559" height="73" alt="image" src="https://github.com/user-attachments/assets/12e84bdc-1a4e-4004-81e2-80cc4719be2e" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="717" height="71" alt="image" src="https://github.com/user-attachments/assets/84b899d3-0a59-446b-a3fa-204defe70782" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="574" height="81" alt="image" src="https://github.com/user-attachments/assets/1e086536-ab05-4317-aafe-00cc5a4bff39" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="285" height="75" alt="image" src="https://github.com/user-attachments/assets/7898bf8b-3295-4b2c-9e97-8038cf3ef8e2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="390" height="134" alt="image" src="https://github.com/user-attachments/assets/ff869f92-9df0-49a2-9068-eb608640ed30" />


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
<img width="542" height="441" alt="image" src="https://github.com/user-attachments/assets/96577e37-f460-4dbb-a9f6-a06ca2d3f4a9" />

 
ls file1
## OUTPUT
<img width="291" height="67" alt="image" src="https://github.com/user-attachments/assets/74ea65f7-0859-4a8e-8a40-664b6f8602d4" />

echo $?
## OUTPUT 
<img width="244" height="64" alt="image" src="https://github.com/user-attachments/assets/c15fa773-0b82-459e-9510-656edcf86e8d" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="237" height="65" alt="image" src="https://github.com/user-attachments/assets/9ed6b628-14fb-4ab9-99b4-c508e9955a90" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="211" height="66" alt="image" src="https://github.com/user-attachments/assets/68e7f07e-5ddf-4c29-8660-312b07690ce3" />


 
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

<img width="363" height="255" alt="image" src="https://github.com/user-attachments/assets/792fb741-15c1-4d30-b7b4-030da94a6f8d" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="388" height="67" alt="image" src="https://github.com/user-attachments/assets/60f94660-fe3d-4564-a742-ebab34a412d8" />


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
<img width="650" height="65" alt="image" src="https://github.com/user-attachments/assets/fecb33bc-06dd-4f9c-8165-713ed757d63c" />

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
<img width="508" height="98" alt="image" src="https://github.com/user-attachments/assets/d17ea124-a572-4ccc-b6c9-c61c69a8459f" />

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

<img width="462" height="73" alt="image" src="https://github.com/user-attachments/assets/e5180e6e-9ce4-450b-b519-84bba588de81" />

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
<img width="528" height="75" alt="image" src="https://github.com/user-attachments/assets/d493ae1b-6e23-47a9-b222-370a45dd9865" />

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
<img width="565" height="161" alt="image" src="https://github.com/user-attachments/assets/d23bc60e-f2a7-4779-967f-52b32ae3fcd7" />

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
<img width="331" height="183" alt="image" src="https://github.com/user-attachments/assets/34bc915f-a45f-4707-91e6-d88f43cb9096" />

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

<img width="333" height="227" alt="image" src="https://github.com/user-attachments/assets/3b266c4c-a1bd-4283-b227-f8f04adfdddb" />

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
<img width="335" height="189" alt="image" src="https://github.com/user-attachments/assets/ed258cb8-8b48-49f4-9df0-9635a4900f91" />

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
<img width="398" height="187" alt="image" src="https://github.com/user-attachments/assets/6611f7ab-55b6-4f6f-8d37-6865e7c28213" />

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
<img width="459" height="323" alt="image" src="https://github.com/user-attachments/assets/04b44bdc-1d13-4118-af56-5a2706ecf137" />

 
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
<img width="699" height="109" alt="image" src="https://github.com/user-attachments/assets/63bd0c96-4919-4b35-af93-1259814576b1" />

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
<img width="781" height="173" alt="image" src="https://github.com/user-attachments/assets/a2c06085-1c88-459b-bfe2-e0c488af2929" />
 
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

## OUTPUT



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
<img width="353" height="124" alt="image" src="https://github.com/user-attachments/assets/a8a084bb-feeb-41ae-845e-3d9fec9c944f" />

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
<img width="353" height="124" alt="image" src="https://github.com/user-attachments/assets/abf7e745-7a10-423e-aa4e-da2669357d2c" />

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
<img width="380" height="446" alt="image" src="https://github.com/user-attachments/assets/100e3bbd-3639-47a5-96bc-6e09b7a3545e" />

 
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
<img width="427" height="347" alt="image" src="https://github.com/user-attachments/assets/a7b4ebd1-7606-4351-8e99-becbc1dcdb5e" />
 
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
<img width="355" height="127" alt="image" src="https://github.com/user-attachments/assets/c53187df-d989-40a6-bafb-1fd49efc1f27" />


# RESULT:
The Commands are executed successfully.
