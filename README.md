<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/6e8d3c50-5dd3-4caf-bb9e-5d5ab8473d63" /># OS-Linux-commands-Shell-scripting
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
<img width="489" height="114" alt="image" src="https://github.com/user-attachments/assets/975dd680-95aa-472b-ab5a-7324f6881d50" />



cat < file2
## OUTPUT

<img width="557" height="128" alt="image" src="https://github.com/user-attachments/assets/e7dc93ed-e92c-4f42-9e51-de7bc27210d2" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="593" height="41" alt="image" src="https://github.com/user-attachments/assets/f3a13449-4062-410f-95b3-f94590d44632" />

comm file1 file2
 ## OUTPUT
<img width="593" height="156" alt="image" src="https://github.com/user-attachments/assets/ceea12f3-ff6c-48aa-bf69-b1cc9ba5a6b1" />

 
diff file1 file2
## OUTPUT
<img width="593" height="186" alt="image" src="https://github.com/user-attachments/assets/2212a7d4-b97c-46cd-becd-e7bef8ff0a97" />


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

<img width="593" height="161" alt="image" src="https://github.com/user-attachments/assets/515c793a-bea7-45c7-8ded-ffdbfce548b3" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="645" height="161" alt="image" src="https://github.com/user-attachments/assets/fcc2c3ee-ae57-4d95-a14f-52dc310334eb" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="645" height="106" alt="image" src="https://github.com/user-attachments/assets/50d3ee40-8595-4f53-a474-b719040e5998" />

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
<img width="645" height="45" alt="image" src="https://github.com/user-attachments/assets/83a6393d-f8d7-475c-8baf-8b67e7ab1b20" />



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


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
<img width="702" height="56" alt="image" src="https://github.com/user-attachments/assets/187441f5-22a7-46a3-9167-4fe10e329c3f" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="702" height="56" alt="image" src="https://github.com/user-attachments/assets/a3388b21-8605-472d-8d4f-2b5280188257" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="722" height="68" alt="image" src="https://github.com/user-attachments/assets/798a874a-d51a-4171-b161-8a702de7f698" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="722" height="59" alt="image" src="https://github.com/user-attachments/assets/f32515b5-eb88-40e9-8701-b750751baab2" />


egrep '(world$)' newfile 
## OUTPUT

<img width="722" height="59" alt="image" src="https://github.com/user-attachments/assets/d275b315-3de7-4798-ac14-6155dc373d7c" />


egrep '(World$)' newfile 
## OUTPUT
<img width="722" height="59" alt="image" src="https://github.com/user-attachments/assets/ddfdb890-8bd7-4a42-88f6-737a9ca99307" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="722" height="80" alt="image" src="https://github.com/user-attachments/assets/adbd8354-dcb9-48e6-bb0c-08cb99d196ff" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="722" height="59" alt="image" src="https://github.com/user-attachments/assets/cb816ca9-fcb4-48eb-b660-8d87eaa72cbe" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="722" height="64" alt="image" src="https://github.com/user-attachments/assets/dc7db948-d72b-4cdb-aa17-6d69bbbd293b" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="722" height="52" alt="image" src="https://github.com/user-attachments/assets/09a1ee39-562f-451a-8ddf-c86db3aba5ca" />

egrep l{2} newfile
## OUTPUT
<img width="722" height="73" alt="image" src="https://github.com/user-attachments/assets/eac7b33f-a952-44c1-bbda-85c8daf87bd3" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="722" height="93" alt="image" src="https://github.com/user-attachments/assets/1818f25b-dba6-4517-af71-5e5e2e78475c" />



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
<img width="722" height="66" alt="image" src="https://github.com/user-attachments/assets/6f82e0e7-7e7a-4262-b027-c48207456731" />



sed -n -e '$p' file23
## OUTPUT

<img width="722" height="66" alt="image" src="https://github.com/user-attachments/assets/d2264214-9451-41ac-8bec-53f1e78e74f2" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="722" height="206" alt="image" src="https://github.com/user-attachments/assets/e4c02470-b031-4d53-b1b5-f1006640cea7" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="722" height="206" alt="image" src="https://github.com/user-attachments/assets/f71aecfb-1ce3-4197-81c2-707837391e51" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="722" height="206" alt="image" src="https://github.com/user-attachments/assets/edad5acb-35b4-4b2f-91f8-756dd026c0ac" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="722" height="137" alt="image" src="https://github.com/user-attachments/assets/7c154068-c4d5-4ae2-9de4-1d9cd014efd9" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/b0892e5c-87c5-4413-8f93-0b7701e020e6" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="722" height="78" alt="image" src="https://github.com/user-attachments/assets/8cfb83a4-6f35-4225-8940-ecd55d3f4f89" />


seq 10 
## OUTPUT

<img width="722" height="222" alt="image" src="https://github.com/user-attachments/assets/eaeb6c0b-cf07-4c9a-b888-2225c04a17ef" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/9c06a1e6-2970-440f-8a1a-b6988a420ca6" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="722" height="186" alt="image" src="https://github.com/user-attachments/assets/15c30199-f218-474e-a697-1e41c160344a" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="722" height="112" alt="image" src="https://github.com/user-attachments/assets/ebaec149-df15-4337-af89-7d232581950f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/7e5eee24-60ac-40b6-9c60-82a7f2e179f1" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/fec30d69-e4b0-44a3-b7eb-44ecfb55f283" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/7e8acb79-3636-46f7-92fe-4dda9d80041f" />



sed -n '2,4{s/$/*/;p}' file23

<img width="722" height="97" alt="image" src="https://github.com/user-attachments/assets/08bd6dbc-c73c-4094-a891-cdb147db8dc2" />

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
<img width="722" height="130" alt="image" src="https://github.com/user-attachments/assets/62d4a02b-bf75-4592-9d12-1c39f14ecf4c" />


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
<img width="722" height="130" alt="image" src="https://github.com/user-attachments/assets/1eb8eb05-1616-459a-9473-0a5b2dcf1bcc" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="763" height="206" alt="image" src="https://github.com/user-attachments/assets/d699e8d4-20ce-4952-bda6-75385ecfd001" />

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

<img width="763" height="96" alt="image" src="https://github.com/user-attachments/assets/f384a6f4-d4e4-4bbf-b0aa-5d24c5c82685" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="763" height="96" alt="image" src="https://github.com/user-attachments/assets/b30cbff8-5559-4871-b907-b860a2b97c26" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="763" height="126" alt="image" src="https://github.com/user-attachments/assets/b2cb398a-386e-4195-baf3-3728f0e72db2" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="763" height="81" alt="image" src="https://github.com/user-attachments/assets/3f2a15b8-45ac-43fa-b8b7-3471cfc0a4fa" />

tar -xvf backup.tar
## OUTPUT
<img width="763" height="81" alt="image" src="https://github.com/user-attachments/assets/c09c3255-4d0b-4975-af48-bf5d21e33d33" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="763" height="81" alt="image" src="https://github.com/user-attachments/assets/04f00b3b-763a-425c-8e30-070d3c13c170" />

gunzip backup.tar.gz
## OUTPUT
<img width="763" height="81" alt="image" src="https://github.com/user-attachments/assets/b38590b2-abe4-40d3-8c54-a828adc71e5a" />

 
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
<img width="763" height="95" alt="image" src="https://github.com/user-attachments/assets/36a8bbb1-80f8-4690-8f94-5e7b31af2fb5" />


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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
