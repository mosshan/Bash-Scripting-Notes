-  by default not supported using echo $(()) or echo ( expr)
- Use bc
	- language for basic calculations
	- usually auto installed but if needed install with 
		- sudo apt-get install bc
``` bash
#! /bin/bash
num1=20.5
num2=5

# echo text is treated as input for bc command
echo "20.5+5" | bc
echo "20.5-5" | bc
echo "20.5%5" | bc
echo "20.5*5" | bc
# this doesn't give us the correct value
echo "20.5/5" | bc #outputs: 4
# need to set variable scale for output
# give us up to 2 decimal places
echo "scale=2;20.5/5" | bc

# bc with vars
echo "$num1+$num2" | bc

# square root
num=27

#this will not work! need math library
echo "scale=2;sqrt($num)" | bc

# call math library where sqrt lives
echo "scale=2;sqrt($num)" | bc -l

#power
echo "3^3" | bc
echo "$num^3" | bc
```

- bc reference
	- man bc