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

<img width="2170" height="725" alt="image1" src="https://github.com/user-attachments/assets/ebfa066a-fd79-4e75-8fdd-beb714ce438c" />


cat < file2
## OUTPUT

<img width="2171" height="724" alt="image2" src="https://github.com/user-attachments/assets/65798f4d-54e7-497a-bede-eccb634edcf1" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="2171" height="724" alt="image3" src="https://github.com/user-attachments/assets/a98cd896-8797-4941-bd6a-f25c56efc2b2" />
comm file1 file2
 ## OUTPUT

<img width="2172" height="724" alt="image4" src="https://github.com/user-attachments/assets/5832ab2c-69ab-4eb6-9ef1-10519b0a00ae" />


 
diff file1 file2
## OUTPUT
<img width="1537" height="1023" alt="image5" src="https://github.com/user-attachments/assets/c928bdc6-00ef-4924-83ec-7c7643e9a0ee" />
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


<img width="1859" height="846" alt="image6" src="https://github.com/user-attachments/assets/66d7dde5-60f5-41b1-ade4-b0c7f7d1df0c" />

cut -d "|" -f 1 file22
## OUTPUT


<img width="1859" height="846" alt="image7" src="https://github.com/user-attachments/assets/fd9bd5c7-82b4-403f-b536-ca710835c832" />
cut -d "|" -f 2 file22
## OUTPUT
<img width="2170" height="725" alt="image8" src="https://github.com/user-attachments/assets/e246c7a5-bb4a-4f04-93da-192da09f1586" />


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
<img width="1724" height="912" alt="image9" src="https://github.com/user-attachments/assets/c8f42d83-0435-40b0-912c-662a8770b793" />




grep hello newfile 
## OUTPUT


<img width="1827" height="861" alt="image10" src="https://github.com/user-attachments/assets/b9b26df5-837e-4425-98d4-0e229587fc59" />



grep -v hello newfile 
## OUTPUT
<img width="1863" height="844" alt="image11" src="https://github.com/user-attachments/assets/6d0d8fab-6c11-4175-9300-5659b1eb4969" />

cat newfile | grep -i "hello"
## OUTPUT


<img width="1745" height="901" alt="image12" src="https://github.com/user-attachments/assets/9b166456-a219-4fb9-a00c-63c2460400ee" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1828" height="860" alt="image13" src="https://github.com/user-attachments/assets/72f3f236-f72f-4b17-8eea-7f4a458867f1" />


grep -R ubuntu /etc
## OUTPUT

<img width="1658" height="949" alt="image14" src="https://github.com/user-attachments/assets/da85c805-2885-4e25-a63b-967840a89b96" />


grep -w -n world newfile   
## OUTPUT

<img width="1692" height="930" alt="image15" src="https://github.com/user-attachments/assets/861ddd17-a8bb-40fd-8c6d-096d24a4f62e" />
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


<img width="1488" height="1057" alt="image16" src="https://github.com/user-attachments/assets/97569206-00d7-4809-b80e-182f933c2082" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1559" height="1009" alt="image17" src="https://github.com/user-attachments/assets/d4bee7ed-fe56-453a-b460-502ff28f12e5" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1545" height="1018" alt="image18" src="https://github.com/user-attachments/assets/84b5eea9-82bd-4788-9d97-f3bcbe5fc0d2" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="1738" height="905" alt="image19" src="https://github.com/user-attachments/assets/74b05dea-8718-4d6a-a8ed-7f93af180679" />
egrep '(world$)' newfile 
## OUTPUT

<img width="1617" height="973" alt="image20" src="https://github.com/user-attachments/assets/6b41b601-9cad-40ba-a986-bae5e15ef9c7" />




egrep '(World$)' newfile 
## OUTPUT
<img width="1617" height="973" alt="image 26" src="https://github.com/user-attachments/assets/2977ea9c-baf1-4b31-938a-a2d1419aee4c" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1519" height="1035" alt="image25" src="https://github.com/user-attachments/assets/b14a2c32-afbb-401e-8631-02c0f5eb9283" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1709" height="920" alt="image27" src="https://github.com/user-attachments/assets/1cebabb9-2f0c-40d4-b3ab-382e1359abb4" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1740" height="904" alt="image28" src="https://github.com/user-attachments/assets/bca8c12c-6493-4477-a9b0-e0b6a9c3b6a9" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1691" height="930" alt="image29" src="https://github.com/user-attachments/assets/34523ae5-e1a5-4405-8597-543794ff2ae0" />


egrep l{2} newfile
## OUTPUT

<img width="1672" height="941" alt="image30" src="https://github.com/user-attachments/assets/64a3dcff-d464-409e-97d9-e172a576cd56" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1700" height="925" alt="image31" src="https://github.com/user-attachments/assets/a47b477a-961c-4d7f-a0b2-0f6fad339265" />

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
<img width="2188" height="718" alt="image32" src="https://github.com/user-attachments/assets/35c27d23-15a0-452d-84fe-09d98773be6f" />



sed -n -e '$p' file23
## OUTPUT

<img width="2172" height="724" alt="image33" src="https://github.com/user-attachments/assets/ec6130c4-ef7e-4096-a0f0-9c025777837d" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1899" height="828" alt="image34" src="https://github.com/user-attachments/assets/3addb6ce-2cd4-440f-8431-ffad2266f977" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1997" height="787" alt="image35" src="https://github.com/user-attachments/assets/a52a8751-8940-4f8d-993f-37d972766fba" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1959" height="803" alt="image36" src="https://github.com/user-attachments/assets/0dfb4dcd-1930-42e5-a861-a6a0a29a561a" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1615" height="974" alt="image37" src="https://github.com/user-attachments/assets/325b1b82-658c-4a83-934c-2fbcd0610ef1" />


sed -n -e '2,/Joe/p' file23
## OUTPUT


<img width="1736" height="906" alt="image38" src="https://github.com/user-attachments/assets/78d499b2-e142-46f6-8ad2-cf9b1cdb5609" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1956" height="804" alt="image39" src="https://github.com/user-attachments/assets/9fca89e2-0ef6-4dc3-8e91-f914db3af0a3" />



seq 10 
## OUTPUT

<img width="1407" height="1118" alt="image40" src="https://github.com/user-attachments/assets/87ef6e3c-e62f-4ba7-9130-26f373cdb688" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1805" height="871" alt="image41" src="https://github.com/user-attachments/assets/e973f50e-08d1-432a-b039-297707e2b62f" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1723" height="913" alt="image42" src="https://github.com/user-attachments/assets/e281fdd7-5691-4f7d-abec-ff70b4ade46e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="1554" height="1012" alt="image43" src="https://github.com/user-attachments/assets/f2e770cc-030f-4b92-873d-86a6afef1d0d" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1606" height="979" alt="image44" src="https://github.com/user-attachments/assets/63275bc1-3768-4c1e-8b4c-523b988a701c" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1309" height="1201" alt="image45" src="https://github.com/user-attachments/assets/2e977e4e-f974-4c44-ad84-63aee382db0b" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1960" height="802" alt="image46" src="https://github.com/user-attachments/assets/a75da8e6-42ea-4b79-b569-c096b7507e4d" />


sed -n '2,4{s/$/*/;p}' file23

<img width="1847" height="852" alt="image47" src="https://github.com/user-attachments/assets/621ec76b-faa7-4f9c-a27c-8007b2be284c" />

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

<img width="1220" height="390" alt="Screenshot 2026-08-01 200947" src="https://github.com/user-attachments/assets/ac7200df-711a-4f56-9ce3-3553d661dc94" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1859" height="846" alt="image48" src="https://github.com/user-attachments/assets/399f3c70-e4a9-4af0-a823-6179cb260c3c" />

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

<img width="1961" height="802" alt="image49" src="https://github.com/user-attachments/assets/b812fedb-f766-4d2d-b267-62a2bc61b62a" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1797" height="875" alt="image50" src="https://github.com/user-attachments/assets/3893b54b-f77a-4925-a545-4457cae8dc88" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1860" height="845" alt="image51" src="https://github.com/user-attachments/assets/7bc78f8e-a4ec-44c8-a9f8-506c6aec6afb" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1812" height="868" alt="image52" src="https://github.com/user-attachments/assets/c97e18a7-9554-450e-8b67-84dae4b3b96e" />


tar -xvf backup.tar
## OUTPUT
<img width="1693" height="929" alt="image53" src="https://github.com/user-attachments/assets/de8c45b2-1708-4947-b742-fc9019c2a09e" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1889" height="833" alt="image54" src="https://github.com/user-attachments/assets/f6bcb8f1-8188-448d-8fbc-6b3550289624" />

gunzip backup.tar.gz
## OUTPUT

 <img width="1719" height="915" alt="image55" src="https://github.com/user-attachments/assets/fb18dc06-b82f-4708-8412-d56a3eda3ed0" />

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

<img width="1852" height="849" alt="image56" src="https://github.com/user-attachments/assets/48a3ae68-f07d-428c-821d-72e02d79099f" />


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
<img width="902" height="464" alt="Screenshot 2026-08-01 210114" src="https://github.com/user-attachments/assets/88206857-7edf-48d7-a438-3fc7f9f0b8c6" />

 
ls file1
## OUTPUT
<img width="2173" height="724" alt="image58" src="https://github.com/user-attachments/assets/dc9dc240-a19a-4977-92b5-6089e7a78f7d" />

echo $?
## OUTPUT 
<img width="2168" height="725" alt="image59" src="https://github.com/user-attachments/assets/7fa958a4-c1ac-4402-91cb-b1ede0f9ee19" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="2152" height="731" alt="image60" src="https://github.com/user-attachments/assets/c6a5b5c0-df09-488e-a945-f0852e67980f" />

abcd
 
echo $?
 ## OUTPUT

<img width="2141" height="734" alt="image61" src="https://github.com/user-attachments/assets/903a6f5e-e3b8-42f1-9656-ef183bf244d9" />

 
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


<img width="1815" height="866" alt="image62" src="https://github.com/user-attachments/assets/3e7499fd-c46c-4868-b92b-3a04a5e19fcb" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1923" height="818" alt="image63" src="https://github.com/user-attachments/assets/92da7e23-5bcd-4a5e-8d17-c0bebf71dd7b" />


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
<img width="2014" height="781" alt="image64" src="https://github.com/user-attachments/assets/30cfb765-d118-4435-9ae7-02800c5a89df" />

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
<img width="1823" height="863" alt="image65" src="https://github.com/user-attachments/assets/a185686e-4432-4af2-b08c-bf0125c2cdd2" />



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
<img width="1376" height="1143" alt="image66" src="https://github.com/user-attachments/assets/958a9a24-ef1a-4586-bb4d-26f49c067196" />

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
<img width="821" height="261" alt="Screenshot 2026-08-01 214653" src="https://github.com/user-attachments/assets/aed3857c-a4b1-49df-b26c-cc4cd6132c4c" />

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

<img width="2164" height="726" alt="image67" src="https://github.com/user-attachments/assets/060c6d5f-9d2a-4341-95f5-4d68ce0eb90b" />

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
<img width="1551" height="1014" alt="image68" src="https://github.com/user-attachments/assets/62413693-38ef-4729-b2f0-c031737b6d29" />

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
<img width="2149" height="731" alt="image69" src="https://github.com/user-attachments/assets/33834194-ec5a-4d9d-9ea7-416f9a072fcf" />

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

<img width="2135" height="736" alt="image70" src="https://github.com/user-attachments/assets/a15c5134-d76b-43b9-ba74-e8d705a7ce32" />

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
<img width="2167" height="726" alt="image71" src="https://github.com/user-attachments/assets/377eb115-e938-4332-bfd4-f26aac9b87cb" />

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
<img width="1900" height="828" alt="image72" src="https://github.com/user-attachments/assets/1eb932a5-2f16-4c55-988e-666d810606c3" />

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

 <img width="2159" height="728" alt="image73" src="https://github.com/user-attachments/assets/9a60f68a-bac7-4d87-91f6-b5a3ad18053a" />

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
<img width="1780" height="884" alt="image74" src="https://github.com/user-attachments/assets/98b287f3-c72b-4bc1-b1cd-63f113712a27" />

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
 <img width="1857" height="847" alt="image75" src="https://github.com/user-attachments/assets/23035925-c482-456a-b641-cf0757960ce5" />

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
<img width="921" height="331" alt="Screenshot 2026-08-01 221013" src="https://github.com/user-attachments/assets/2d161928-924c-4d1c-a99d-42b8f8a90829" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="921" height="331" alt="Screenshot 2026-08-01 221013" src="https://github.com/user-attachments/assets/89d8611b-9b23-4e95-bb1e-05ce7ec1fb15" />


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
<img width="1877" height="838" alt="image76" src="https://github.com/user-attachments/assets/a3615ce8-826a-43b5-8308-8170711c3de6" />

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

<img width="2149" height="731" alt="image77" src="https://github.com/user-attachments/assets/82afaea9-fb84-4349-9348-7ff0683ab5dd" />

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
<img width="2105" height="747" alt="image78" src="https://github.com/user-attachments/assets/76741ff1-d50d-4110-8f27-fbc6681d00d9" />

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
 
 <img width="1850" height="850" alt="image79" src="https://github.com/user-attachments/assets/1cf455dc-103c-4aa5-a1dd-dea2679e2af4" />

 
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
 <img width="1844" height="853" alt="image80" src="https://github.com/user-attachments/assets/9445ad44-7470-4dda-a0dc-a85031b9a95d" />

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
<img width="2167" height="725" alt="image82" src="https://github.com/user-attachments/assets/39c1c6d0-aed1-4e12-8899-6e8692ff33c5" />


# RESULT:
The Commands are executed successfully.
