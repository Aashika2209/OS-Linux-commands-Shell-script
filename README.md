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
![Screenshot from 2025-03-03 11-18-46](https://github.com/user-attachments/assets/24e0004f-f578-4c01-abff-ef9347482d24)





cat < file2
## OUTPUT
![Screenshot from 2025-03-03 11-19-43](https://github.com/user-attachments/assets/5fdd90aa-17ad-4570-b8e1-af4f5d31ae0d)



# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-03 11-26-51](https://github.com/user-attachments/assets/a02822c3-96f2-49a2-ba8b-447ba0474700)

 
comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-03-03 11-27-09](https://github.com/user-attachments/assets/e1b7e408-ce72-43e4-9261-0f9802dd5402)


 
diff file1 file2
## OUTPUT
![Screenshot from 2025-03-03 11-27-48](https://github.com/user-attachments/assets/101c2b9a-984f-4cce-ada8-f94c1d57bfe7)


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
![Screenshot from 2025-03-03 11-42-48](https://github.com/user-attachments/assets/e982bac5-3b3f-4a2d-a466-fde1e186c48f)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-03 11-43-03](https://github.com/user-attachments/assets/0b683c9d-757a-4e07-9275-c9624e4692fb)





cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-03 11-43-17](https://github.com/user-attachments/assets/2d2fe845-5208-4a0b-aff7-5384fc7e7713)



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

![Screenshot from 2025-03-05 08-26-01](https://github.com/user-attachments/assets/64dc9bf6-61f8-4e4e-aafc-5b711bfa0a6b)






grep hello newfile 
## OUTPUT

![Screenshot from 2025-03-05 08-26-16](https://github.com/user-attachments/assets/c8d0df57-65a9-4720-afcc-8bcf00aa55c5)





grep -v hello newfile 
## OUTPUT

![Screenshot from 2025-03-05 08-26-31](https://github.com/user-attachments/assets/b153fb6e-db0a-4505-8924-0810a7e1451b)




cat newfile | grep -i "hello"
## OUTPUT

![Screenshot from 2025-03-05 08-26-46](https://github.com/user-attachments/assets/6153eced-eccf-498d-a697-a66edf0d3ce9)





cat newfile | grep -i -c "hello"
## OUTPUT

![Screenshot from 2025-03-05 08-28-04](https://github.com/user-attachments/assets/1a26ba94-ae06-4a19-b653-146fd90c786a)






grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT

![Screenshot from 2025-03-05 08-29-42](https://github.com/user-attachments/assets/e905606a-5e73-4e78-bd8d-51643109e8b6)



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
![Screenshot from 2025-04-23 08-58-58](https://github.com/user-attachments/assets/df6b351b-a89f-4870-acc0-f7def402e0f5)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-00-49](https://github.com/user-attachments/assets/7cab9ead-ed3e-410c-83d2-f3fd9f6574eb)




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2025-04-23 08-59-38](https://github.com/user-attachments/assets/e46fd823-825f-4867-b30d-ba6693b417d4)





egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-00-08](https://github.com/user-attachments/assets/a6b5020a-cb3e-47cd-99e2-51c4d2888bb0)




egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-06-28](https://github.com/user-attachments/assets/b775d249-d684-472f-8660-037453e6669f)




egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-06-44](https://github.com/user-attachments/assets/5950c7a0-8774-4d28-bfbf-6f2ef260c9c8)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-06-44](https://github.com/user-attachments/assets/cf6a4d51-9cec-4099-9c57-6e19a5a4ec84)





egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-06-57](https://github.com/user-attachments/assets/6d262696-1020-48a7-9573-3436184328f9)




egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-07-03](https://github.com/user-attachments/assets/2571c825-9258-4ff7-a3a1-aa2b4a8218ca)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2025-04-23 09-10-03](https://github.com/user-attachments/assets/27dd7e21-333c-4a64-a7cb-931d3f19b784)



egrep l{2} newfile
## OUTPUT
![Screenshot from 2025-04-23 09-10-11](https://github.com/user-attachments/assets/15ff5fae-ab78-4806-a0a7-a76441003e02)




egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2025-04-23 09-10-22](https://github.com/user-attachments/assets/7e2eb950-edea-42ce-8b3a-127de9ac3aec)


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
![Screenshot from 2025-04-23 09-13-40](https://github.com/user-attachments/assets/2d58e95d-0681-4304-8411-2bed8464cecc)




sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2025-04-23 09-13-45](https://github.com/user-attachments/assets/e9ff0708-212c-4bac-98c2-09c0540f7ad2)





sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-23 09-13-58](https://github.com/user-attachments/assets/14396666-9bd6-4336-bda9-7e5c8e51377a)




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2025-04-23 09-14-13](https://github.com/user-attachments/assets/4cb72f68-9fbb-4e25-a22d-deb4644641c9)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![Screenshot from 2025-04-23 09-16-34](https://github.com/user-attachments/assets/539b34d4-7b0a-46ce-b411-ef3d0b8b9ea0)





sed -n -e '1,5p' file23
## OUTPUT

![Screenshot from 2025-04-23 09-16-43](https://github.com/user-attachments/assets/2c3470cf-53cf-4e4f-94df-aa7cf670bc25)




sed -n -e '2,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-23 09-16-53](https://github.com/user-attachments/assets/0093ae6a-49dd-4496-ad10-bf30dbaaa509)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![Screenshot from 2025-04-23 09-17-04](https://github.com/user-attachments/assets/5cbf2912-251e-44cf-b488-1853288b4f04)




seq 10 
## OUTPUT

![Screenshot from 2025-04-23 09-17-24](https://github.com/user-attachments/assets/1f0cfa30-a5ef-42dd-a9fd-b8ca0e52742e)





seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2025-04-23 09-20-43](https://github.com/user-attachments/assets/937f5f85-4739-4194-93fd-3e2a86daca6f)





seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2025-04-23 09-20-50](https://github.com/user-attachments/assets/f47f1dca-07e2-4277-9a28-915d2ca92fac)




seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2025-04-23 09-21-01](https://github.com/user-attachments/assets/e0f59c5d-cb39-49d1-ab72-94e99b0a985d)




seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2025-04-23 09-21-15](https://github.com/user-attachments/assets/57d1caa4-6aba-477f-8697-c9434854d4b7)



seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2025-04-23 09-21-20](https://github.com/user-attachments/assets/a9d73662-cfa7-42e5-8f9b-fffadce61e72)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2025-04-23 09-21-42](https://github.com/user-attachments/assets/b7ebf226-093d-46d0-abc1-4c7c6ccb33a4)




sed -n '2,4{s/$/*/;p}' file23
## OUTPUT 
![Screenshot from 2025-04-23 09-24-29](https://github.com/user-attachments/assets/f64a4c1a-288c-4b0e-80a1-37c4aab192fb)



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
![Screenshot from 2025-04-23 09-26-21](https://github.com/user-attachments/assets/699f0984-2eb3-4341-92bf-66c2e45a8c4f)


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
![Screenshot from 2025-04-23 09-27-32](https://github.com/user-attachments/assets/3817b6d3-361b-4e4f-b75a-1343cb9198f2)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 ![Screenshot from 2025-04-23 09-28-25](https://github.com/user-attachments/assets/6b6a25a3-17cd-494c-abbe-4236f3492abd)


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
 ![Screenshot from 2025-04-23 09-31-20](https://github.com/user-attachments/assets/c67882cc-0504-4053-881a-a4349632a3c9)



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2025-04-23 09-31-32](https://github.com/user-attachments/assets/9513e984-044d-46e1-a023-842041019d33)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot from 2025-04-23 09-32-01](https://github.com/user-attachments/assets/3ae553dc-779a-4af6-aa09-e134e73c033a)



mkdir backupdir
 
mv backup.tar backupdir
 
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
