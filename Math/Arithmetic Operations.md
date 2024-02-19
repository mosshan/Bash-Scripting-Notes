- Non decimal values
- enclose arithmetic expression in (()) so it evaluates

``` bash
echo 1 + 1
1 + 1

num1=20
num2=5

# this causes error
# computes but then is not directly printable
echo (( num1 + num2 ))
echo (( $num1 + $num2 ))

# also cannot do this
# need to use $ before (( to reference value and assign to num3
num3=(( num1 + num2 ))

# correct version
# computes and then replaces with the value
# $ before vars is unneeeded because it is implicit in arithmetic expressions bc word will be coerced to int value
echo $(( num1 + num2 ))
echo $(( $num1 + $num2 ))
echo $(( $num1 % $num2 ))
echo $(( $num1 * $num2 ))
echo $(( $num1 - $num2 ))
echo $(( $num1 / $num2 ))
```
- With expr command
``` bash
#! /bin/bash 
# can also use expr command
# requires $ before vars
echo $( expr $num1 + $num2 )
echo $( expr $num1 % $num2 )
# for multiplication expr needs escape char for **
echo $( expr $num1 \* $num2 )
echo $( expr $num1 - $num2 )
echo $( expr $num1 / $num2 )
```
