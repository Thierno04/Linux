* Bash Variable like ( RANDOM, UID)
* Use of 'basename'
* Function in script (Passing arguments in a function)
* Arguments passing and accessing in script
* Shift
* iterate arguments using for loop
* I/O redirect in script
* Use of /dev/null
* Sleep Command
* How to exit a script on failure
* How to make a variable constant
* User of logger to log message to syslog under var/log/messages


  ## Display or get the name of the script
```bash
  echo "The name of the script is: ${0}"
  ```
  ##### basename:
  Print name with any leading directory components removed.
  ```bash
  #basename /home/user/folder1/folder2/myscript.sh
  Output: myscript.sh
  ```
  ##### Functions:

  * Block of code which perform some task and run when it is called.
  * Can be reuse many times in our program which lessen our lines of code.
  * We can pass arguments to the method.
  
  ###### example:
  ```bash
  #!/bin/bash
  scriptName() {
      echo
      echo "Name of the script is ${basename $0}"
      echo
  }
  scriptName
```
```bash
chmod u+x scriptName.sh
./scriptName.sh
```
```bash
#!/bin/bash
scriptNameDetail() {
    echo "My name is $1"
    echo "My age is $2"
    echo
}
scriptNameDetail paul 20
scriptNameDetail pierre 45
```
```bash
chmod u+x scriptNameDetail.sh
./scriptNameDetail.sh
```
```bash
#!/bin/bash
addition() {
  local num1=$1
  local num2=$2
  le sum = $num1 + $num2
  echo "sum $num1 and $num2"
}
addition 20 30
```
```bash
#!/bin/bash
echo ===========check internet=============
ping -c1 www.google.com &> /dev/null
if [$? -eq 0]
then
     echo "Connection successfull"
else
     echo "Connection failed"
fi
```
  ##### Shell Variables:

  RANDOM: A random integer between 0 and 32767 is generated.
  UID: User ID of the user logged in.
  
  vi user_check.sh
```bash
    #!/bin/bash
    if [[ $UID -eq 0 ]]
    then
       echo "You are root"
    else
       echo "You are not root"
    fi
```
```bash
  chmod 777 user_check.sh
  ./user_check.sh
  su - root
  /home/user/user_check.sh
```
  
