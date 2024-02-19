- Make sure to put spaces before and after condition in brackets
	- can cause issues if you don't
- Put double quotes around variables to prevent word splitting and pathname expansion
``` bash
#! /bin/bash
if [ condition ]
then
	statement
fi

# or
if [ condition ]; then statement; fi


# comparison operators for integers
count=10
if[ "$count" -gt 20 ]
then 
	statement
fi


word = a
if [[ "$word" < "b" ]]
then
	echo "condition is true"
else
	echo "condition is false"
fi

# or (ternary operator)
if [[ "$word" < "b" ]] && echo "condition is true" || echo "condition is false"


if [[ "$word" == "b" ]]
then
	echo "equal"
elif [[ "$word" < "b" ]]
then
	echo "smaller"
else
	echo "bigger"
fi

```
Integer comparison operators
-eq , -ne, -gt, -ge, -lt, -le, <, <=, >, >=
- if you want to use <, <=, >, or >= must use (( )) for conditional instead of square brackets
String comparison operators
=, == , !=, < (less than in ASCII alphabetical order), >, -z (string is null/has 0 length)
- if using < or > must use double square brackets instead of single 
