# What are Linux Environment Variables?

Linux environment variable is a dynamic-named value, which may be used by one or more programs running.
Set of defined Rules & Values to build an environment.

### How to unset environment variables?

To set the environment variable temporary
```bash
        export TESTVAR=1
```
To set the environment variable permanently 
```bash
        vi .bashrc
        TESTVAR='123'
        export TESTVAR  
```
To set the global environment variable  permanently 
```bash
        vi /etc/profile 
        TESTVAR='123'
        export TESTVAR
```
###### ex:
```bash
vi .bashrc ===> ( export TESTVAR="abc" )
source .bashrc
echo $TESTVAR
```
