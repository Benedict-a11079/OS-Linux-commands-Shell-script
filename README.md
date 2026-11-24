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
<img width="456" height="110" alt="437457677-967a622c-6563-4855-ab6e-bd33f3e1a973" src="https://github.com/user-attachments/assets/7de0121b-7e00-4156-b220-d0b987d33afe" />



cat < file2
## OUTPUT
<img width="456" height="110" alt="437457779-9cb30c01-6ca1-4508-b567-920317d92ce7" src="https://github.com/user-attachments/assets/99dd7888-fb10-4b47-8ef0-9e5ed4dd5849" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="481" height="44" alt="437457912-356f08aa-5611-4bb9-bc5e-02c43c13d403" src="https://github.com/user-attachments/assets/46e6e8c4-242e-445e-97c5-fde0e6577a11" />

comm file1 file2
 ## OUTPUT
<img width="481" height="198" alt="437458025-9b4f494f-3764-4004-89a7-b6554328d7c4" src="https://github.com/user-attachments/assets/6270b11a-57d1-4868-9cd7-6ee4c655350b" />

 
diff file1 file2
## OUTPUT

<img width="481" height="198" alt="437458079-dfe29c5f-7b65-4a49-b361-9bd4c5cb9430" src="https://github.com/user-attachments/assets/3fbaad25-919d-4a24-83b9-8a915251aae1" />

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


<img width="497" height="54" alt="437458179-f1d13611-bbec-432e-b9cb-85ffb7538742" src="https://github.com/user-attachments/assets/ee080e60-3945-4a3d-80e6-13d160734475" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="531" height="75" alt="437458250-be89e8ec-8d82-46ca-90f7-516446ea7551" src="https://github.com/user-attachments/assets/ffdd3a32-8d58-47de-83d2-6d102674740c" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="531" height="75" alt="437458334-06251dfd-c2e1-4033-b83c-699161f82a7d" src="https://github.com/user-attachments/assets/ab643760-043b-4b9f-a630-320093ed3044" />


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

<img width="531" height="42" alt="437458430-027acbdf-56a3-46b0-862e-dadefb65295a" src="https://github.com/user-attachments/assets/67a58ed6-d981-4e36-ba84-49a7a10e3352" />


grep hello newfile 
## OUTPUT

<img width="531" height="42" alt="437458510-66c88133-9569-4d73-a191-9b74b320b70c" src="https://github.com/user-attachments/assets/592921ad-f1f8-45bc-8423-69434f1098a0" />



grep -v hello newfile 
## OUTPUT

<img width="531" height="42" alt="437458605-54d7af23-a79e-46cb-b549-57664f1d5c57" src="https://github.com/user-attachments/assets/4b02f820-cd95-4e0e-af71-ca7ba79f3ba5" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="597" height="57" alt="437458711-415d2950-f5c4-4d72-9a82-4eada399247b" src="https://github.com/user-attachments/assets/d4dcc9cd-d0b3-4db9-8ac1-31526799ff0e" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="630" height="49" alt="437458787-45757001-bf07-41a0-9ca0-f7d1ed2b84ab" src="https://github.com/user-attachments/assets/b7a0317c-823e-4613-9aec-bd6f0c8c2da6" />



grep -R ubuntu /etc
## OUTPUT

<img width="630" height="142" alt="437458863-41e662bb-ca4d-4dd5-94e5-10cf130c572d" src="https://github.com/user-attachments/assets/a5d2d18d-c94a-4d02-9b33-498b2a26de0f" />


grep -w -n world newfile   
## OUTPUT
<img width="630" height="59" alt="437458939-2959a482-0122-46d1-9c2b-bcf9d17cc219" src="https://github.com/user-attachments/assets/6384a053-bac1-4481-8e87-08cb0fdf4dcf" />


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

<img width="630" height="59" alt="437463455-78d128c6-04bc-40c6-bf8e-d8abbf76b086" src="https://github.com/user-attachments/assets/9e577f02-dbb1-4819-a03f-bd2fddf03ae4" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="630" height="59" alt="437463537-4bf9423d-4115-4702-b77d-652036301cc0" src="https://github.com/user-attachments/assets/9894e08a-6546-477e-b1d8-3a98479f914a" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="630" height="59" alt="437463627-14924440-952c-480e-83e3-68d0742c897f" src="https://github.com/user-attachments/assets/264378aa-04d6-438b-8b7e-708845209169" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="630" height="37" alt="437463736-1d2da7f4-7edd-4697-a5ab-08b3b15cbe93" src="https://github.com/user-attachments/assets/34ea69d5-3787-4932-b220-2498b194eeb7" />


egrep '(world$)' newfile 
## OUTPUT

<img width="630" height="58" alt="437463805-f8d8366d-ded2-41eb-83e4-ebdfba968dd2" src="https://github.com/user-attachments/assets/2f35c4f8-db57-46a0-81e1-5b0a53c9e4c7" />


egrep '(World$)' newfile 
## OUTPUT

<img width="630" height="42" alt="437463872-3c0717c6-f676-4ea9-b28f-8850ea51a52c" src="https://github.com/user-attachments/assets/3b7dfd1a-cdd4-4656-bbd0-92f4517ec05f" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="630" height="73" alt="437463953-f9c9d21b-2bc4-4b7d-8585-ac393785db8b" src="https://github.com/user-attachments/assets/b89ff065-dc26-4c99-8596-f9beaad43fdd" />


egrep '[1-9]' newfile 
## OUTPUT


<img width="630" height="44" alt="437464029-df7c6665-f757-49cb-ac27-e218c651c7fe" src="https://github.com/user-attachments/assets/1c3e3d4c-5aff-47f2-a984-044b01005b8f" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="630" height="42" alt="437464120-e6f5f5cc-1313-415b-babd-30bf5c4828b9" src="https://github.com/user-attachments/assets/4d190fda-43a0-40ab-a724-3f803b140a9a" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="630" height="42" alt="437464182-af4ce7ef-128f-4e4a-b1c9-6fe459f9cc59" src="https://github.com/user-attachments/assets/0f5d9c28-599e-4b90-a79b-4a4747ec4220" />


egrep l{2} newfile
## OUTPUT

<img width="630" height="58" alt="437464298-b8033a58-9387-4802-8ae1-e082b998bf40" src="https://github.com/user-attachments/assets/9c248aa8-78db-47ad-9585-136f27d1c30d" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="630" height="77" alt="437464408-31237cb8-66ad-42f9-a942-5bd7478096c1" src="https://github.com/user-attachments/assets/e6f75b50-5a1f-4b45-96e8-696962658613" />


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
<img width="889" height="44" alt="437489915-7b94549c-1754-4c4c-8d1c-3b4ef4057d90" src="https://github.com/user-attachments/assets/84c10292-9cff-48a9-9f7e-7cf5ebfdf868" />



sed -n -e '$p' file23
## OUTPUT

<img width="889" height="44" alt="437489999-d6c1017b-dcfe-4ba2-9968-6fd515f70ccc" src="https://github.com/user-attachments/assets/78c84a81-5723-41c7-96ed-efb38aaff087" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="940" height="169" alt="437490090-defc7fe9-c3e9-43e5-9466-e52556533f6e" src="https://github.com/user-attachments/assets/e8d8c36d-121b-4e93-9651-6c3a434d652d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="950" height="169" alt="437490189-592fe0f8-f473-480d-afae-21201455bd13" src="https://github.com/user-attachments/assets/00af85cf-dd78-460d-99f6-0390bae9cc67" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT





sed -n -e '1,5p' file23
## OUTPUT




sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT



seq 10 | sed -n '2,~4p'
## OUTPUT



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT



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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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
