
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
<img width="621" height="155" alt="01-cat-file1" src="https://github.com/user-attachments/assets/1668e500-464f-4463-a448-dfe94d2bb80f" />

cat < file2
## OUTPUT
<img width="624" height="164" alt="02-cta-file2" src="https://github.com/user-attachments/assets/2b8781ac-8154-4630-981c-1137a813880a" />

# Comparing Files
cmp file1 file2
## OUTPUT
<img width="628" height="68" alt="03  cmp" src="https://github.com/user-attachments/assets/4afd4c9c-cd92-40b8-b2d1-c20eb8945e0a" />

comm file1 file2
## OUTPUT
<img width="1225" height="372" alt="img04" src="https://github.com/user-attachments/assets/20e0c72f-48d4-4723-9fb0-4ee4782f4cc7" />

diff file1 file2
## OUTPUT
<img width="1156" height="450" alt="img 05" src="https://github.com/user-attachments/assets/6595a5fe-cfd5-4800-8342-ee1623490b01" />

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
## output
<img width="1217" height="165" alt="img 06" src="https://github.com/user-attachments/assets/7f041603-4c3b-4792-b2db-32821f0100a7" />
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
## output
<img width="1145" height="210" alt="img 07" src="https://github.com/user-attachments/assets/458a44b5-6dab-45d6-a504-cbacffcf3028" />


cut -c1-3 file11
## OUTPUT
<img width="1158" height="153" alt="img 08" src="https://github.com/user-attachments/assets/dfda25d2-0a5e-4ca2-a458-a6296cd0c23d" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="1141" height="210" alt="img 09" src="https://github.com/user-attachments/assets/7b5137c3-beb4-4e39-a0cb-9027f8525958" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="1170" height="208" alt="img 10" src="https://github.com/user-attachments/assets/9855d620-0261-470f-99b7-278bb86b2b7b" />


cat < newfile 
```
Hello world
hello world
^d
````
```
cat > newfile 
Hello world
hello world
 ```

grep Hello newfile 
## OUTPUT
<img width="1212" height="117" alt="img 11" src="https://github.com/user-attachments/assets/8faa9ac1-c0d3-402f-a3e7-8a3d4274eb1d" />

grep hello newfile 
## OUTPUT
<img width="1125" height="110" alt="img 12" src="https://github.com/user-attachments/assets/922ac035-8719-4671-a142-59b9c3ccaf9e" />

grep -v hello newfile 
## OUTPUT
<img width="1163" height="125" alt="img 13" src="https://github.com/user-attachments/assets/017a080b-ca49-4015-a335-9031b18ed14b" />

cat newfile | grep -i "hello"
cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1163" height="124" alt="img 14" src="https://github.com/user-attachments/assets/2c570303-5f00-42e4-b992-371c24a34c89" />



grep -R ubuntu /etc
## OUTPUT
<img width="1467" height="883" alt="img 15" src="https://github.com/user-attachments/assets/ca9c8fc6-a5ef-408b-bab8-d25492899937" />


grep -w -n world newfile   
## OUTPUT
<img width="1260" height="159" alt="img 16" src="https://github.com/user-attachments/assets/29292b3f-3bae-4204-ba13-1a2cb77bce2d" />


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
<img width="1140" height="171" alt="img 17" src="https://github.com/user-attachments/assets/fac357aa-4781-4cb7-88b2-2b04d69604fc" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="987" height="161" alt="img 18" src="https://github.com/user-attachments/assets/5e71fe3e-3119-414c-bcf3-85a6c3923524" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1156" height="150" alt="img 19" src="https://github.com/user-attachments/assets/2b509d25-01a1-4f1c-865e-04d2b6852886" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="1158" height="120" alt="img 20" src="https://github.com/user-attachments/assets/28133afa-9430-44e5-ba79-27817121b2c7" />

egrep '(world$)' newfile 
## OUTPUT
<img width="1161" height="150" alt="img21" src="https://github.com/user-attachments/assets/69b43cca-2de0-476e-90c5-1618780fc4d4" />

egrep '(World$)' newfile 
## OUTPUT
<img width="1172" height="123" alt="img22" src="https://github.com/user-attachments/assets/e8a0a871-0150-433f-a9b3-2a7f9bd2999c" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1162" height="199" alt="img23" src="https://github.com/user-attachments/assets/552c1ac0-3986-4428-98b1-5733bca2f92a" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="1162" height="127" alt="img24" src="https://github.com/user-attachments/assets/46b199a0-07f2-43bc-87a7-7e0abf85ebda" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1167" height="129" alt="img25" src="https://github.com/user-attachments/assets/d288074a-fe2c-4dff-8208-cae39c1d18be" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1150" height="129" alt="img26" src="https://github.com/user-attachments/assets/e3b43bcc-9cb3-4f32-be38-1faf395be0e5" />

egrep l{2} newfile
## OUTPUT
<img width="1149" height="158" alt="img27" src="https://github.com/user-attachments/assets/7bd696a9-dd48-4c73-8d54-1c05ab3d1d52" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="1146" height="192" alt="img28" src="https://github.com/user-attachments/assets/12b7e4b7-8914-4bf0-b2bb-e75631a4ea22" />

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
<img width="1156" height="120" alt="img29" src="https://github.com/user-attachments/assets/5c75ea04-5be0-4219-bc8c-1a9aced747ac" />

sed -n -e '$p' file23
## OUTPUT
<img width="1151" height="127" alt="img30" src="https://github.com/user-attachments/assets/abfd0d56-3705-4f69-96a7-e464ed5c1965" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1133" height="406" alt="img31" src="https://github.com/user-attachments/assets/e0c8e708-5af6-4831-b6fe-4f9f9ac8eeb7" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1162" height="420" alt="img32" src="https://github.com/user-attachments/assets/adf2849e-d163-480f-8426-1ad5725ea078" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1147" height="414" alt="img33" src="https://github.com/user-attachments/assets/c98f1954-b02e-4cc5-8779-273c758d14fe" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="1170" height="290" alt="img34" src="https://github.com/user-attachments/assets/6ac7bf8d-9f94-4ec4-abc2-ce90295dbf7e" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1160" height="190" alt="img35" src="https://github.com/user-attachments/assets/e1305568-a2a7-4dd6-8b38-479706ab9590" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1147" height="153" alt="img36" src="https://github.com/user-attachments/assets/fd62a6de-d154-41bf-af0f-7186a2acfa68" />

seq 10 
## OUTPUT
<img width="1162" height="492" alt="img 37" src="https://github.com/user-attachments/assets/eb30b967-62ed-4918-92ea-176e89eed2cd" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1146" height="210" alt="img38" src="https://github.com/user-attachments/assets/5e2cdb0c-5400-4f0c-a1d5-398f57252246" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1166" height="209" alt="img39" src="https://github.com/user-attachments/assets/1069ae92-a36d-491c-915b-ec110dd16481" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="1161" height="245" alt="img40" src="https://github.com/user-attachments/assets/e9abae19-8d8d-474f-a2ac-f0cad660d2dc" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="1152" height="205" alt="img41" src="https://github.com/user-attachments/assets/fde042fb-135d-4268-b2e1-b8914e9bbdfe" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1162" height="211" alt="img42" src="https://github.com/user-attachments/assets/b4efc1fd-3ba7-4a33-b757-523b0612714b" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1150" height="214" alt="img43" src="https://github.com/user-attachments/assets/a83066fc-a6cf-4bd7-9f4c-79bb9b63766d" />

sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="1162" height="206" alt="img44" src="https://github.com/user-attachments/assets/7b15a5ea-e088-4e59-9524-32144af6685d" />

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
<img width="1143" height="282" alt="img45" src="https://github.com/user-attachments/assets/b40059b9-cb70-4211-bcd3-d948f98120d2" />

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

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1156" height="296" alt="img46" src="https://github.com/user-attachments/assets/632e6450-130b-4778-a1bc-2a3a1be99e95" />


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
<img width="1170" height="413" alt="img47" src="https://github.com/user-attachments/assets/ddbe0d2f-0242-425e-bc6b-8e4d86b46ff7" />


cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1175" height="197" alt="img48" src="https://github.com/user-attachments/assets/c84a281d-7f7e-41a4-8e77-44dadf3ed5f9" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1163" height="198" alt="img49" src="https://github.com/user-attachments/assets/7616e628-0355-4014-aa97-ccec1d0074af" />

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1182" height="774" alt="img50" src="https://github.com/user-attachments/assets/b0113812-85a2-4fd4-ac95-7b3fc7d60453" />

tar -xvf backup.tar
## OUTPUT
<img width="1187" height="630" alt="img51" src="https://github.com/user-attachments/assets/66870367-9fe3-4cfe-a2bc-f55757d06f27" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="864" height="250" alt="img52" src="https://github.com/user-attachments/assets/8a927607-37a6-4f9f-b388-e25d6511fc6e" />
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
<img width="528" height="125" alt="img53png" src="https://github.com/user-attachments/assets/161ff695-5f0d-4d2e-98d2-cb0f0941e041" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="409" height="123" alt="img54" src="https://github.com/user-attachments/assets/a0296fc6-12e0-4565-8d21-6ae81b8f63db" />


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
<img width="660" height="405" alt="img55" src="https://github.com/user-attachments/assets/57021dcb-3f18-4a4b-9f77-4c9b7129f991" />

 
ls file1
## OUTPUT
<img width="278" height="70" alt="img56" src="https://github.com/user-attachments/assets/9327b523-6bd4-4f43-8601-9f4a8ef37775" />



echo $?
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="266" height="76" alt="img57" src="https://github.com/user-attachments/assets/49caf6d6-644c-4e74-b563-731036839d56" />



abcd
 
echo $?
 ## OUTPUT
<img width="417" height="150" alt="img58" src="https://github.com/user-attachments/assets/0422a8bc-63e0-47ae-be1f-302b26a7a06a" />
 
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
## OUTPUT
<img width="443" height="270" alt="img59" src="https://github.com/user-attachments/assets/0095d8be-f5f3-411a-b81b-fe432c1c4d20" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="391" height="106" alt="img60" src="https://github.com/user-attachments/assets/507e0ddf-6108-4352-aa76-c9453909340a" />



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
<img width="657" height="218" alt="img61" src="https://github.com/user-attachments/assets/e5a94e31-845f-4adf-9acc-73e5b0f33204" />


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
<img width="705" height="439" alt="img62" src="https://github.com/user-attachments/assets/d3b07606-bfb3-49eb-af7f-2dbb39e9fe68" />


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
## OUTPUT
<img width="681" height="355" alt="img63" src="https://github.com/user-attachments/assets/1dd9c883-bc5e-4d8a-91f1-cad4e19ccc27" />

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
<img width="687" height="444" alt="img64" src="https://github.com/user-attachments/assets/310dc1b8-2a68-4680-b95f-438bd95c2fa1" />


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
<img width="712" height="150" alt="img65" src="https://github.com/user-attachments/assets/4f6984f4-9d09-47f5-a61e-fdb677ed04ae" />


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
<img width="730" height="142" alt="img66 (1)" src="https://github.com/user-attachments/assets/54f89e93-ca24-47a5-95e5-5969cfb9560e" />


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
<img width="738" height="275" alt="img67" src="https://github.com/user-attachments/assets/4e22c96e-bcf2-4baf-8a26-1541afdc87a6" />

 
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
<img width="746" height="322" alt="img68" src="https://github.com/user-attachments/assets/5594c80b-7eda-4f4c-9e36-0ccf29c27c5d" />

 
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
<img width="732" height="275" alt="img69" src="https://github.com/user-attachments/assets/9fe7144b-d0b5-431b-a5a1-4aa1ac764389" />


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
<img width="475" height="335" alt="img70" src="https://github.com/user-attachments/assets/ef13802c-6992-406f-a75f-1e148e734970" />

 
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
<img width="452" height="295" alt="img71" src="https://github.com/user-attachments/assets/c2fcf4b4-201a-430a-a192-8273b43bd2fe" />

 
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
<img width="465" height="292" alt="img72" src="https://github.com/user-attachments/assets/0b5e4796-ae8a-4250-b2f3-f5bcdf2ee2e7" />

 
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
<img width="491" height="542" alt="img73" src="https://github.com/user-attachments/assets/ee3a86fb-6359-4083-8482-41ad5b075659" />

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
<img width="452" height="337" alt="img74" src="https://github.com/user-attachments/assets/a8c73adc-592a-488b-a21a-f5f14f6ca444" />


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
<img width="412" height="388" alt="img75" src="https://github.com/user-attachments/assets/bf40ab27-fd5d-41b7-a1b2-75e467e5c9ac" />

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
<img width="426" height="179" alt="img76" src="https://github.com/user-attachments/assets/ad18700a-7f5a-4896-b6b8-35a154d312fc" />


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
<img width="485" height="141" alt="img77" src="https://github.com/user-attachments/assets/a4a53cbd-642c-41e5-84dc-cf85a8e53114" />

 
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
<img width="599" height="345" alt="img78" src="https://github.com/user-attachments/assets/cd4a1b5f-e956-49e9-951f-14a74e73e585" />

 
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
<img width="547" height="281" alt="img79" src="https://github.com/user-attachments/assets/7d9b1100-91a0-46ef-9275-2acc38a31d71" />

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
## OUTPUT
<img width="547" height="281" alt="img79" src="https://github.com/user-attachments/assets/9c0868aa-e938-433c-a50b-248e7a5f21c4" />

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
<img width="597" height="336" alt="img80" src="https://github.com/user-attachments/assets/d258a050-633a-4038-80be-d816bce80225" />


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
<img width="687" height="405" alt="img81" src="https://github.com/user-attachments/assets/a235ec9d-85b9-45d0-a732-068b3ca17724" />

 
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
<img width="485" height="180" alt="img82" src="https://github.com/user-attachments/assets/10fb6530-4c64-4473-8c4c-691e5cf3f92c" />

# RESULT:
The Commands are executed successfully.
