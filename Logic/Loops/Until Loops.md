``` bash
#! /bin/bash
until [ condition ]
do 
	command1
	command2
	...
	commandn
done

#example print 1 - 10
n=1
until [ $n -gt 10 ]
do
	echo "$n"
	n=$(( n+1 ))
done
```