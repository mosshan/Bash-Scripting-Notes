- patterns can be strict or flexible 
	- regex patterns
	- * is for default case bc could be any text

``` bash
#! /bin/bash

# basic syntax
case expression in
	pattern1 )
		statements ;;
	pattern2 )
		statements ;;
	...
	* )
		statements ;;
esac

#example of strict pattern matching
vehicle=$1

case $vehicle in
	"car" )
		echo "rent of $vehicle is \$100" ;;
	"van" )
		echo "rent for $vehicle is \$80" ;;
	"bicycle" )
		echo "rent for $vehicle is \$5" ;;
	* )
		echo "$vehicle is unknown" ;;
esac

# example of flexible pattern matching
echo -e "Enter some character: \c"
read value

case $value in
	[a-z] )
		echo "$value is a lowercase letter" ;;
	[A-Z] )
		echo "$value is an uppercase letter" ;;
	[0-9] )
		echo "$value is a digit" ;;
	? )
		echo "$value is a special character" ;;
	* )
		echo "$value is unknown"
esac

```