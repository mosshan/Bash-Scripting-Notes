#### With While loops
``` bash
#! /bin/bash

# bad options!!! might be messed up by special chars

	#with file redirection
	while read p
	do
		echo "$p"
	done < hello.sh
	
	# read file content into one var then print
	# use cat and piping
	# use cat output as input to while loop
	cat hello.sh | while read p
	do
	  echo $p
	done

# good options:

	# first 2 methods might be messed up by special chars
	# use IFS (internal field splitter) helps recognize word boundaries internally
	# assigning space to IFS
	# -r prevents backslash escapes from being interpreted
	# each line is read into line and then printed out
	while IFS=' ' read -r line
	do 
		echo $line
	done < hello.sh
```