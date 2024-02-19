- iterates over list and allows user to select item
	- press ctr + c to exit
- often used with case statement

``` bash
#! /bin/bash

# basic syntax
select varName in list
do
  command1
  command2
  ..
  commandN
done

# example
select name in mark john tom ben
do
  echo "$name"
done

# 
select name in mark john tom ben
do
  case "$name" in
    mark )
      echo "mark is selected"
      ;;
    john )
      echo "john is selected"
      ;;
    tom )
      echo "tom is selected"
      ;;
    ben )
      echo "ben is selected"
      ;;
    * )
	  echo "Error, please provide a number between 1-4"
	  ;;
  ecase
done

```