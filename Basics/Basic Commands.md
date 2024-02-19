- determine which shells are supported by system
	- /etc/shells
- bash location
	- which bash
- echo
	- you don't need single/double quotes in echo unless you're using it to show a character shouldnt be interpreted (ie a backslash)
	- if you're using echo with a variable, don't use double quotes
	``` bash
	today=Saturday
	echo "today is $today"
	today is Saturday
	echo 'today is $today'
	today is $today
	echo today is $today
	today is Saturday
```
- cat
	- append to file or overwrite file
	- press ctrl + d to leave cat
	``` bash
	# append to file
	cat >> $file_name
	
	# overwrite file
	cat > $file_name
	```

- sleep
	- sleep 1
	- gives pause of however many seconds you specify
- open new terminal
	- terminal_name &
- get version of bash
	- echo ${BASH_VERSION}
- pwd
	- get present working directory
- date
	- get date
	-

- rm 
	- remove file
- mkdir