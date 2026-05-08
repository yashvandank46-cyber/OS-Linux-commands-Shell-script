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
<img width="650" height="162" alt="image" src="https://github.com/user-attachments/assets/c6414b61-834e-4835-b208-bf8c6de1ad73" />



cat < file2
## OUTPUT



# Comparing Files
cmp file1 file2
## OUTPUT
 
comm file1 file2
 ## OUTPUT
<img width="711" height="85" alt="image" src="https://github.com/user-attachments/assets/442c4218-8ff7-4d08-b0a4-1ffe68e5c3ad" />

 
diff file1 file2
## OUTPUT
<img width="701" height="308" alt="image" src="https://github.com/user-attachments/assets/6d4f2eee-f25a-488b-9aba-b9fbf9318df0" />


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

<img width="620" height="108" alt="image" src="https://github.com/user-attachments/assets/cacb9857-0d4e-4559-8616-00173c256057" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="704" height="129" alt="image" src="https://github.com/user-attachments/assets/0ea758b9-cb69-4750-a135-bba1215d0b4a" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="755" height="139" alt="image" src="https://github.com/user-attachments/assets/4a61c8fd-e8ca-453d-adb4-6bbec41c3ea0" />


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
<img width="582" height="92" alt="image" src="https://github.com/user-attachments/assets/cef89d71-2c77-4f0d-bf52-821ea22e000c" />



grep hello newfile 
## OUTPUT

<img width="720" height="79" alt="image" src="https://github.com/user-attachments/assets/7b8c49dc-0f42-42fb-9624-10b5754b5da3" />



grep -v hello newfile 
## OUTPUT
<img width="582" height="85" alt="image" src="https://github.com/user-attachments/assets/550aa056-276a-4936-9bea-5c9aa2014a2b" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="650" height="112" alt="image" src="https://github.com/user-attachments/assets/1eda83cc-91aa-4928-84b6-e0612ea62fe3" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="693" height="87" alt="image" src="https://github.com/user-attachments/assets/64b4d51e-f8b7-4da2-b3c2-3b536518f2f1" />



grep -R ubuntu /etc
## OUTPUT
<img width="942" height="253" alt="image" src="https://github.com/user-attachments/assets/e51981dd-dc8e-4096-98a5-75fc9dc7f8fa" />



grep -w -n world newfile   
## OUTPUT
<img width="658" height="103" alt="image" src="https://github.com/user-attachments/assets/d2134b04-c5ec-4e22-b677-34665b5144a0" />


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

<img width="696" height="112" alt="image" src="https://github.com/user-attachments/assets/0bf5ee3d-3ad3-4317-b241-bf72d801e81a" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="755" height="115" alt="image" src="https://github.com/user-attachments/assets/5e428677-5929-4c12-8e3c-695ac2dc0a78" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="695" height="111" alt="image" src="https://github.com/user-attachments/assets/ebe01475-a287-4732-9a3a-3b8093a5872f" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="759" height="86" alt="image" src="https://github.com/user-attachments/assets/34efb978-2062-42f1-b846-09d2ebcab147" />


egrep '(world$)' newfile 
## OUTPUT
<img width="740" height="112" alt="image" src="https://github.com/user-attachments/assets/12ef91c5-acbe-440e-b48b-75184bf8eba5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="706" height="82" alt="image" src="https://github.com/user-attachments/assets/3d7c87b5-57d8-44f5-8c97-694247ea9b8d" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="717" height="132" alt="image" src="https://github.com/user-attachments/assets/dd21f2df-e67a-4a5b-b823-b167196eba5b" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="664" height="83" alt="image" src="https://github.com/user-attachments/assets/d618093d-ab85-4437-b082-8182ac53e576" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="766" height="79" alt="image" src="https://github.com/user-attachments/assets/89eaa714-ef0c-43dd-b980-d73be8e43382" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="713" height="86" alt="image" src="https://github.com/user-attachments/assets/14830232-3e7f-4877-9b34-9cf03b655285" />


egrep l{2} newfile
## OUTPUT
<img width="672" height="118" alt="image" src="https://github.com/user-attachments/assets/57c5784e-d745-40cd-9a5d-5993b39e62f2" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="673" height="135" alt="image" src="https://github.com/user-attachments/assets/45471748-2137-4e8f-bd3b-616145d580fa" />


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

<img width="681" height="89" alt="image" src="https://github.com/user-attachments/assets/99df1968-8b66-434c-ae1f-e9c248432fda" />


sed -n -e '$p' file23
## OUTPUT
<img width="577" height="92" alt="image" src="https://github.com/user-attachments/assets/08768bbf-09ca-422f-abda-fc93bfc22b15" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="797" height="259" alt="image" src="https://github.com/user-attachments/assets/2b428d06-9bc1-4a7a-ba41-95db1b88fbb0" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="719" height="257" alt="image" src="https://github.com/user-attachments/assets/e0ef0663-97e5-48bf-bb33-16bd266e9da3" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="752" height="261" alt="image" src="https://github.com/user-attachments/assets/0d7de1c3-d323-45ab-a52e-c2ce131aa800" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="762" height="184" alt="image" src="https://github.com/user-attachments/assets/7cef1faa-2161-4f06-967a-3bf29357e864" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="729" height="138" alt="image" src="https://github.com/user-attachments/assets/dd5a4220-4fc8-41cf-885f-2a65d3363484" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="704" height="113" alt="image" src="https://github.com/user-attachments/assets/6e90cd77-4f9f-424c-8a99-f28d7e07e1b2" />



seq 10 
## OUTPUT
<img width="667" height="300" alt="image" src="https://github.com/user-attachments/assets/f3d41e5d-0271-43a9-812e-9873d37a687c" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="578" height="133" alt="image" src="https://github.com/user-attachments/assets/76386e9f-9d26-4c47-860c-79de2096ef12" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="512" height="129" alt="image" src="https://github.com/user-attachments/assets/5806a5cb-0a3b-433a-b48d-448bb110704d" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="544" height="161" alt="image" src="https://github.com/user-attachments/assets/f0bfcebf-c8eb-4a88-be45-a1355548af8a" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="527" height="123" alt="image" src="https://github.com/user-attachments/assets/209faa7f-1b2b-41f4-8283-9760ace3db68" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="622" height="127" alt="image" src="https://github.com/user-attachments/assets/9087282e-4bf4-42ee-b870-0b652d69bff8" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="678" height="139" alt="image" src="https://github.com/user-attachments/assets/52a10020-27f4-4529-9153-3924d666e7cc" />



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
<img width="628" height="181" alt="image" src="https://github.com/user-attachments/assets/6462e53f-a985-4edc-b0ec-b3efa2363a25" />


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
<img width="612" height="179" alt="image" src="https://github.com/user-attachments/assets/11cfb88b-6150-4524-9f19-e1d73fa8c627" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="688" height="246" alt="image" src="https://github.com/user-attachments/assets/b1445927-971f-489b-acde-39e2677019b9" />

cat > urllist.txt
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
<img width="609" height="133" alt="image" src="https://github.com/user-attachments/assets/96988d8e-2d80-4a90-8c72-84cf410d1c12" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="751" height="128" alt="image" src="https://github.com/user-attachments/assets/0b60b840-ecc1-4304-966e-c1498008e61b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="913" height="332" alt="image" src="https://github.com/user-attachments/assets/879e82c2-6c6a-4575-829c-3a609366221b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="900" height="229" alt="image" src="https://github.com/user-attachments/assets/e9300a47-f20f-4eb8-b8c0-b33d7dd85808" />


tar -xvf backup.tar
## OUTPUT
<img width="682" height="294" alt="image" src="https://github.com/user-attachments/assets/eccb6e05-10bf-44e7-a5df-74c5e8a3c015" />

gzip backup.tar

ls
## OUTPUT
 <img width="903" height="107" alt="image" src="https://github.com/user-attachments/assets/f70f14d6-7be3-4b63-bb48-8b51819cc8e3" />

gunzip backup.tar.gz
## OUTPUT
<img width="720" height="55" alt="image" src="https://github.com/user-attachments/assets/b0e8beb9-a331-4f70-bd12-e4967de08cdf" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="654" height="81" alt="image" src="https://github.com/user-attachments/assets/77114597-e628-4c9c-9344-67fbcb4018e2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="688" height="150" alt="image" src="https://github.com/user-attachments/assets/cc82feb3-f25b-4210-9a83-6d240dc00438" />


cat > scriptest.sh 
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
<img width="803" height="378" alt="image" src="https://github.com/user-attachments/assets/54ffc290-55da-4bdb-97c2-57e47658b2cd" />

 
ls file1
## OUTPUT
<img width="523" height="80" alt="image" src="https://github.com/user-attachments/assets/64645be2-0b97-4463-9d0c-f86fcb7ab17c" />

echo $?
## OUTPUT 
<img width="537" height="87" alt="image" src="https://github.com/user-attachments/assets/358e96e2-57db-4b1e-8667-666d1715d604" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="777" height="93" alt="image" src="https://github.com/user-attachments/assets/09ee8f83-cde0-43a1-a9b0-eda902cb1349" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="686" height="85" alt="image" src="https://github.com/user-attachments/assets/18484fe5-ba38-40aa-818c-19b62288535c" />


 
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

cat > strcomp.sh 
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

<img width="493" height="79" alt="image" src="https://github.com/user-attachments/assets/9ad1e982-1a33-4e63-bc2e-45f455412bb4" />


chmod 755 strcomp.sh
 
./strcomp.sh 


# check file ownership
cat > psswdperm.sh 
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
<img width="776" height="83" alt="image" src="https://github.com/user-attachments/assets/ce7e26a2-900e-4009-85ef-23148df0f991" />

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

<img width="722" height="115" alt="image" src="https://github.com/user-attachments/assets/35f1a66e-4b47-4d46-973e-0865c5e003d5" />


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
<img width="657" height="97" alt="image" src="https://github.com/user-attachments/assets/5504cdcb-c3de-46f5-8ecd-f6c83b45abf3" />

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
<img width="778" height="108" alt="image" src="https://github.com/user-attachments/assets/cd970e8c-ce9b-46b0-a707-da23b058be53" />


# looking for a possible value using elif
cat > elifcheck.sh 
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
<img width="628" height="80" alt="image" src="https://github.com/user-attachments/assets/da6fa596-0eff-435d-b5ca-921d38ea10a5" />


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
<img width="623" height="70" alt="image" src="https://github.com/user-attachments/assets/5adbc9e2-4ffd-487a-82ec-ac7d72f5398a" />


# using the case command
cat > casecheck.sh 
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
<img width="641" height="87" alt="image" src="https://github.com/user-attachments/assets/2eb18dbd-b3eb-4acd-8f87-443446568e84" />

 
cat > whiletest.sh
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
 <img width="702" height="300" alt="image" src="https://github.com/user-attachments/assets/9056b876-8b4e-4ef2-a9f4-5479e1f8604b" />

 
cat >untiltest.sh 
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

## OUTPUT
<img width="395" height="147" alt="image" src="https://github.com/user-attachments/assets/61e58b14-99dc-41ff-b2a1-b0fd384ab9df" />

 
 
 
cat > forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
## OUTPUT
<img width="497" height="225" alt="image" src="https://github.com/user-attachments/assets/1383c248-3f92-43bc-9452-90db181b8bbc" />
 
 
cat > forin2.sh 
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
## OUTPUT>
<img width="550" height="152" alt="image" src="https://github.com/user-attachments/assets/29d6c408-82c1-4785-a385-518d2a1f87ca" />

 
cat > forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 

 ## OUTPUT>
<img width="640" height="230" alt="image" src="https://github.com/user-attachments/assets/1b16bdb3-8f5e-426a-afd7-ac8ad1bd73ed" />

 
cat > forin1.sh 
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
<img width="483" height="204" alt="image" src="https://github.com/user-attachments/assets/5fdc8929-261f-4923-9b58-9dbd5f1ec7e9" />

cat > forinfile.sh 
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
$ cat >cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="496" height="222" alt="image" src="https://github.com/user-attachments/assets/b08bcf1f-aa71-478b-b477-e53346667ddd" />


cat > forctype.sh 
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
<img width="531" height="183" alt="image" src="https://github.com/user-attachments/assets/dc167aa4-7179-4113-828a-5233b328a3d1" />

cat > forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
<img width="565" height="176" alt="image" src="https://github.com/user-attachments/assets/079fd9f0-4f4b-4f27-83d4-7b9a50fade51" />

cat > fornested1.sh 
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
 <img width="637" height="357" alt="image" src="https://github.com/user-attachments/assets/aec6ab31-2fe7-417d-8103-5c5b316ba67c" />


 
cat > forbreak.sh 
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
<img width="738" height="135" alt="image" src="https://github.com/user-attachments/assets/a4cfefaa-fece-404e-8bd4-391fe39a0f60" />

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
 
cat > exread.sh 
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
<img width="636" height="114" alt="image" src="https://github.com/user-attachments/assets/5a6c15e3-9d98-4bd8-8731-3682636d4ba9" />


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT




$ ./exread1.sh 
 
cat > funcex.sh
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
## OUTPUT
 <img width="530" height="77" alt="image" src="https://github.com/user-attachments/assets/b9202d94-2ada-488a-8c69-d725e29381f8" />


 


 
cat > argshift.sh
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
<img width="562" height="128" alt="image" src="https://github.com/user-attachments/assets/6659187e-c1da-444c-ae84-2a9a2665e60d" />
 
 cat > argshift1.sh
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
$ chmod 777 argshift1.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="419" height="130" alt="image" src="https://github.com/user-attachments/assets/77b675b1-0113-41e2-a7e4-fd7a17d3fa7a" />

 
cat > argshift.sh
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
<img width="585" height="400" alt="image" src="https://github.com/user-attachments/assets/8a2aaedf-1fb5-4d3d-bac6-4bb48dca963c" />

 
 
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
 <img width="605" height="389" alt="image" src="https://github.com/user-attachments/assets/9d674c3a-de6a-4fcf-bdf3-15c0f142bab1" />

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
<img width="539" height="121" alt="image" src="https://github.com/user-attachments/assets/65d80ea8-1906-4631-8212-870c70b22eb6" />


# RESULT:
The Commands are executed successfully.
