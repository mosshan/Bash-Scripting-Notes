basics
``` bash
#! /bin/bash

while [ condition ]
do 
	command1
	command2
	command3
done

#example print 1- 10
n=1
while [ $n -le 10 ]
do
	echo "$n"
	n=$(( n+1 ))
	#or
	(( n+1 ))
	#or (post increment)
	(( n++ ))
done

#or
while (( $n <= 10 ))
```


 sleep with while loops 
- use delay
``` bash
#! /bin/bash
n=1
while [ $n -le 10 ]
do
	echo "$n"
	(( n++ ))
	sleep 1
done
```

open new terminal
- open a new terminal in a loop
``` bash
#! /bin/bash
n=1
while [ $n -le 3 ]
do
	echo "$n"
	(( n++ ))
	gnome-terminal &
	xterm &
done
```