- check if file exists, if it's a regular/block/character special file
``` bash
#! /bin/bash
echo -e "enter the name of the file: \c" #\c keeps cursor on same line after echo but must use -e to allow interpretation of back slack so it doesnt print \c 
read file_name

# check if file exists -> use -e
if [ -e "$file_name" ]
then
	echo "File $file_name found"
else
	echo "File $file_name not found"
fi



```
File Test Operators -> don't chain like -rw
- check if file exists: 
	- -e file_name
- check if file exists and is a regular file
	- -f file_name
- check if directory exists
	- -d dir_name
- check if file is block special file
	- binary, picture, video, music file
	- -b
- check if file is character special file
	- normal txt file which contains some extra data
	- -c
- check if file is empty
	- -s
- check if file has read permission
	- -r
- check if file has write permission
	- -w
- check if file has execute permission
	- -x