#### syntax options
``` bash
#! /bin/bash

# syntax options
	for VARIABLE in 1 2 3 .. N
	do
		command1
		command2
		...
		commandN
	done
	#OR---------------------------------
	for VARIABLE in file1 file2 file3
	do
		command1 on $VARIABLE
		command2
		...
		commandN
	done
	#OR---------------------------------
	for OUTPUT in $(Linux-Or-Unix-Command)
	do
		command1 on $OUTPUT
		command2 on $OUTPUT
		...
		commandN
	done
	#OR---------------------------------
	for (( EXP1; EXP2; EXP3 ))
	do
	  command1
	  command2
	  command3
	done
```

#### basic examples
``` bash
#! /bin/bash
#examples

# iterate over nums and print
for num in 1 2 3 4 5
do
	echo "$num"
done

# works in bash version > 3
#output: 1 2 3 4 
for num in {1..5}
do 
	echo "$num"
done

# works in bash version > 4
# give increment for value
for num in {START..END..INCREMENT} # loops over 
for num in {1..10..2} #output: 1 3 5 7 9

for (( i=0; i<5; i++ ))
do
  echo $i
done

```
#### for loops to execute commands
``` bash
#! /bin/bash

#execute commands
for command in ls pwd date
do
  echo "----------------$command--------------"
  $command
done

# for all items in the directory, print the name if they are a directory
for item in *
do
  if [ -d "$item" ]
  then
    echo "$item is a directory"
  fi
done
```
