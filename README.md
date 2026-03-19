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
![2a5342bc-121c-4d77-8476-4d6e5539b883](https://github.com/user-attachments/assets/b9f51f48-ff13-4c08-8433-17a82564bc2a)

cat < file2
## OUTPUT
![70620b45-8a46-467e-b0b2-6e11ed8f6809](https://github.com/user-attachments/assets/d10234b5-c45c-4824-b71f-1c9af704518a)

# Comparing Files
cmp file1 file2
## OUTPUT
 ![01041a8b-f0c7-4cde-b776-46178d831db1](https://github.com/user-attachments/assets/e0aefba6-581d-462b-b7b0-9f835a0c15c4)

comm file1 file2
 ## OUTPUT
![538a4666-2de7-40c0-b0ba-18b984cf6232](https://github.com/user-attachments/assets/6e33d0f6-bb21-4a1c-85ca-1214a098caff)

diff file1 file2
## OUTPUT
<img width="492" height="238" alt="unnamed" src="https://github.com/user-attachments/assets/671ce2fc-32ca-4973-9acb-17dee0d155e3" />

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
<img width="492" height="77" alt="unnamed" src="https://github.com/user-attachments/assets/408a4a36-17a3-405c-8eb2-92141c77a9b9" />

cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT


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
<img width="546" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/cf0de806-d487-4f75-93b8-da79b178867e" />

grep hello newfile 
## OUTPUT

grep -v hello newfile 
## OUTPUT
<img width="546" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/8dbe2474-fd97-4c93-a748-5dba926bfbe6" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="603" height="81" alt="unnamed" src="https://github.com/user-attachments/assets/6f8c9a74-776b-4c64-b091-46c609cd0513" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="635" height="62" alt="unnamed" src="https://github.com/user-attachments/assets/18b78e36-8132-4824-9d5b-73936ef9c5b7" />


grep -R ubuntu /etc
## OUTPUT
<img width="1199" height="465" alt="unnamed" src="https://github.com/user-attachments/assets/a732da23-3a4d-4fcb-b0e5-fcc045311045" />

grep -w -n world newfile   
## OUTPUT
<img width="620" height="61" alt="unnamed" src="https://github.com/user-attachments/assets/8061320f-6d20-4947-a701-4d845e95b521" />


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
<img width="628" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/cee3ca73-a2d3-4737-be37-10d0e977643b" />


egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="628" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/98e18227-7788-4ece-aaee-096d51a918c7" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="628" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/2882d146-ba2e-4891-ae14-35e2e018aad4" />



egrep '(world$)' newfile 
## OUTPUT
<img width="632" height="79" alt="unnamed" src="https://github.com/user-attachments/assets/2488772a-c9ae-47ce-9972-ea95c143452d" />




egrep '(World$)' newfile 
## OUTPUT
<img width="631" height="58" alt="unnamed" src="https://github.com/user-attachments/assets/a74f5a7a-e9ca-44bf-9753-968172cfd97e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="631" height="74" alt="unnamed" src="https://github.com/user-attachments/assets/9ded7987-f322-46ab-af9b-1b599ccab51a" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="635" height="46" alt="unnamed" src="https://github.com/user-attachments/assets/539ea417-cf05-4946-8b27-6717d15370d5" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="635" height="46" alt="unnamed" src="https://github.com/user-attachments/assets/b92e1962-101c-487a-9e6f-55dfdc3f9c74" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="635" height="46" alt="unnamed" src="https://github.com/user-attachments/assets/bd56bf46-8d96-4721-993a-ac374e0a84fd" />

egrep l{2} newfile
## OUTPUT
<img width="637" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/28fd30a6-6957-41fd-8c01-af233bb777c9" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="637" height="82" alt="unnamed" src="https://github.com/user-attachments/assets/e0bc3181-817b-4d76-9543-afb0a037b911" />


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
<img width="554" height="44" alt="unnamed" src="https://github.com/user-attachments/assets/f2a5d1bd-7d18-4345-98be-db956fadf1a0" />



sed -n -e '$p' file23
## OUTPUT
<img width="554" height="44" alt="unnamed" src="https://github.com/user-attachments/assets/ae3d48a2-5092-4149-aa50-76c33c0ee83f" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="590" height="166" alt="unnamed" src="https://github.com/user-attachments/assets/2a1af9ca-f1a8-40ad-abce-19c9aa9defbc" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="590" height="166" alt="unnamed" src="https://github.com/user-attachments/assets/9a5dc3ea-00a9-40d5-bbd0-5596124ce3f0" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="619" height="166" alt="unnamed" src="https://github.com/user-attachments/assets/45f8e258-1135-45db-88ca-d9478b206703" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="600" height="114" alt="unnamed" src="https://github.com/user-attachments/assets/8a689285-37b7-4772-8e4f-366f0b598bce" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="604" height="153" alt="unnamed" src="https://github.com/user-attachments/assets/030defb8-cfd9-450f-a08b-0e5a21e7fd43" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="629" height="133" alt="unnamed" src="https://github.com/user-attachments/assets/2aa84478-efc1-47cf-8cc3-3a3ca5a7f040" />



seq 10 
## OUTPUT
<img width="618" height="205" alt="unnamed" src="https://github.com/user-attachments/assets/82f788ad-3212-437e-9750-ceda9d05f183" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="632" height="99" alt="unnamed" src="https://github.com/user-attachments/assets/d316c557-0309-4ad8-977a-f3cc589b3b64" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="632" height="99" alt="unnamed" src="https://github.com/user-attachments/assets/734c9ce5-0659-4209-b94f-1d6dc3b0aff1" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="637" height="115" alt="unnamed" src="https://github.com/user-attachments/assets/254271d8-ba56-47db-9506-73c5f326c9ca" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="638" height="98" alt="unnamed" src="https://github.com/user-attachments/assets/e6aef7c2-614f-4711-ac32-dae952a8ad44" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="638" height="98" alt="unnamed" src="https://github.com/user-attachments/assets/5860212d-b288-4a9b-a42f-10d3ef4d869b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="638" height="98" alt="unnamed" src="https://github.com/user-attachments/assets/fedfc791-8be3-4633-876c-ccb5d200e265" />



sed -n '2,4{s/$/*/;p}' file23
<img width="638" height="98" alt="unnamed" src="https://github.com/user-attachments/assets/04417753-8e7a-4fa9-b097-6ebc339866c9" />


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
<img width="457" height="110" alt="unnamed" src="https://github.com/user-attachments/assets/bd093d78-587c-4066-bc85-7e8d0d3500c2" />


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
<img width="602" height="154" alt="unnamed" src="https://github.com/user-attachments/assets/b08e2257-57c8-430c-ae31-c468979e1018" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="677" height="78" alt="unnamed" src="https://github.com/user-attachments/assets/8277c1ca-f715-42ea-b939-42c83c3e9195" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT


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
<img width="745" height="89" alt="unnamed" src="https://github.com/user-attachments/assets/26b995f8-5a91-40f2-b53c-eab0c300fdf9" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="730" height="190" alt="unnamed" src="https://github.com/user-attachments/assets/1f0d17f0-19bf-4b7d-9c59-5289c097266c" />


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
<img width="700" height="312" alt="unnamed" src="https://github.com/user-attachments/assets/8b7bcb33-7132-4ca7-95d0-9590ed90ea94" />

 
ls file1
## OUTPUT
<img width="676" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/efa895d2-c149-4d88-96f3-73fdb0e8871e" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="667" height="59" alt="unnamed" src="https://github.com/user-attachments/assets/ec5bae0b-5eb9-47e6-af99-1a72ce670ba2" />

echo $?
## OUTPUT 
<img width="653" height="206" alt="unnamed" src="https://github.com/user-attachments/assets/7ff3317a-b9b7-49d8-b498-b47e9ee24b1a" />
 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="651" height="113" alt="unnamed" src="https://github.com/user-attachments/assets/a0d32188-bec5-4baf-a680-d1867206e902" />


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
<img width="647" height="98" alt="unnamed" src="https://github.com/user-attachments/assets/9133604d-094f-4342-b716-d4bdae87b433" />

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


# RESULT:
The Commands are executed successfully.
