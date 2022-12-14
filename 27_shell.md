# What is Shell scripting ?


* Shell script consist of set of commands to perform a task.
* All the commands execute sequentially.
* Some task like file manipulation, program execution, user interaction, automation of task etc can be done.

#### Scripting Format
```bash
#!/bin/bash
```
- Bourne Shell(sh)
- Bourne Again Shell(Bash)
- Korn shell
- C shell
- TCsh Shell

### Types of operators:
```bash
Equal                    |      -eq/==
-------------------------|---------------
Greaterthanorequalto     |      -ge
-------------------------|--------------
Lessthanorequalto        |      -le
-------------------------|------------
Not Equal                |       -ne/!=
-------------------------|-------------
Greater Than             |      -gt
-------------------------|-----------
Less Than                |      -lt
```

### Variable in script
##### Variable:
```bash
#!/bin/bash
name=Paul
age=20
echo $name $age
```
```bash
chmod u+x variable.sh
ls -ltr
./variable.sh
```

##### How to take input from user ?
- if-else:
```bash
if [$age -eq 18]
then
    echo "You are eligible to vote"
else
    echo "Sorry you are not eligible to vote"
fi
```
###### example:

user input:
```bash
#!/bin/bash
echo what is your age ?
read $age
if [$age -ge 18]
then
    echo you can!
else
    echo you cannot
fi
```
```bash
chmod u+x input.sh
ls -ltr
./input.sh
```

##### switch:
```bash
#!/bin/bash
echo Press any option
echo 1=Show date
echo 2=List files
echo 3=Show current path

read choice

case $choice in
   1) date;;
   2) ls -ltr;;
   3) echo Invalid input;;
esac
```
```bash
chmod u+x switch.sh
ls -ltr
./switch.sh
```

##### forloop:
```bash
#!/bin/bash
for num in {1..10} or for num in $@
do
   echo Number is $num or echo "is $num"
done
```
```bash
chmod u+x forloop.sh
ls -ltr
./forloop.sh
```
##### while:
```bash
#!/bin/bash
num=10
count=0
while [$count -le $num]
do
  echo $count
  let count++
done
```
```bash
chmod u+x while.sh
ls -ltr
./while.sh
```

#### Iterate values from file:
```bash
name:     =   vi filter_iterate.sh 
----       =   -------------------
Paul       =    #!/bin/bash
Pierre     =    names="/home/user/script/name"
John       =    for name in $(cat $names)
Hicham     =    do
Boiro      =       echo character of $name
           =    done
```
```bash
chmod u+x filter_iterate.sh
./filter_iterate.sh
ls -ltr
ls -ltr | awk '{print $9}'
alias dir="ls -ltr | awk '{print | $9}'"
```
##### alias:
```bash
alias <short_name>="<your_command>"
```
###### example:
```bash
alias dir="ls -ltr | awk '{print | $9}'"
alias pchron="ps -ef | grep"
dir
pchron
```
