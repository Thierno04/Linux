# What is a wildcard in Linux?

A wildcard is a character that can be used as a substitute for any of a class of characters in a search.
```bash
* - zero or more character
? - single character
[] - range of character
```
touch file.sh
```bash
ls -l *.sh
```
touch file1 file2 file3
```bash
ls -l file*
```
```bash
rm file*
```
vi names.txt
(John)
```bash
cat names.txt | grep ^J
cat names.txt | grep ^n
```
