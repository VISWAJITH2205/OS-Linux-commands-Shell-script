# Name : VISWAJITH LALITHRAM R.V
# Reg.No : 212224240187

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
![Alt text](img/01.png)


cat < file2
## OUTPUT
![Alt text](img/02.png)


# Comparing Files
cmp file1 file2
## OUTPUT
![Alt text](img/03.png)


 
comm file1 file2
 ## OUTPUT
![Alt text](img/04.png)

 
diff file1 file2
## OUTPUT
![Alt text](img/05.png)


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
![Alt text](img/06.png)



cut -d "|" -f 1 file22
## OUTPUT
![Alt text](img/07.png)


cut -d "|" -f 2 file22
## OUTPUT
![Alt text](img/08.png)


cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![Alt text](img/09.png)

grep hello newfile 
## OUTPUT

![Alt text](img/10.png)


grep -v hello newfile 
## OUTPUT

![Alt text](img/11.png)

cat newfile | grep -i "hello"
## OUTPUT

![Alt text](img/12.png)


cat newfile | grep -i -c "hello"
## OUTPUT

![Alt text](img/13.png)


grep -R ubuntu /etc
## OUTPUT

![Alt text](img/14.png)

grep -w -n world newfile   
## OUTPUT
![Alt text](img/15.png)


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
![Alt text](img/16.png)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![Alt text](img/17.png)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Alt text](img/18.png)



egrep '(^hello)' newfile 
## OUTPUT

![Alt text](img/19.png)

egrep '(world$)' newfile 
## OUTPUT
![Alt text](img/20.png)


egrep '(World$)' newfile 
## OUTPUT
![Alt text](img/21.png)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![Alt text](img/22.png)


egrep '[1-9]' newfile 
## OUTPUT
![Alt text](img/23.png)


egrep 'Linux.*world' newfile 
## OUTPUT
![Alt text](img/24.png)

egrep 'Linux.*World' newfile 
## OUTPUT
![Alt text](img/25.png)

egrep l{2} newfile
## OUTPUT
![Alt text](img/26.png)


egrep 's{1,2}' newfile
## OUTPUT 
![Alt text](img/27.png)

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
![Alt text](img/28.png)


sed -n -e '$p' file23
## OUTPUT
![Alt text](img/29.png)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Alt text](img/30.png)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Alt text](img/31.png)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Alt text](img/32.png)


sed -n -e '1,5p' file23
## OUTPUT
![Alt text](img/33.png)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![Alt text](img/34.png)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Alt text](img/35.png)


seq 10 
## OUTPUT
![Alt text](img/36.png)


seq 10 | sed -n '4,6p'
## OUTPUT
![Alt text](img/37.png)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Alt text](img/38.png)


seq 3 | sed '2a hello'
## OUTPUT
![Alt text](img/39.png)


seq 2 | sed '2i hello'
## OUTPUT
![Alt text](img/40.png)

seq 10 | sed '2,9c hello'
## OUTPUT
![Alt text](img/41.png)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Alt text](img/42.png)


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
![Alt text](img/43.png)

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
![Alt text](img/44.png)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Alt text](img/45.png)
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
![Alt text](img/46.png)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Alt text](img/47.png)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Alt text](img/48.png)

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

![Alt text](img/49.png)
tar -xvf backup.tar
## OUTPUT
![Alt text](img/50.png)
gzip backup.tar



# RESULT:
The Commands are executed successfully.
