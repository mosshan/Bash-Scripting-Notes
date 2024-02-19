
Arrays
```bash
# declare array
	arr=(1 2 3)
	os=('ubuntu' 'windows' 'kali')

	# can treat vars not explicitly declared as arrays as arrays
	#assigns value to 0th index though and array has length of 1
	string=abc
	echo "${string[@]}"
	#value is assigned to 0th index
	echo "${string[0]}" #output: abc
	echo "${string[1]}" #output:  
	

# accessing/ referencing
	# reference array -> requires curly brackets (not required for most other vars)
	${arr}
	# access array element at index 0 
	${arr[0]}
	# access each element in array
	${arr[@]}
	# get indices of array
	${!arr[@]}
	# get length of array
	${#arr[@]}

#changing array
	# add elements
	os[3]='mac'
	# can add element at ANY index
	#gaps in array are okay
	os[17]='mac'
	
	# replace elements
	os[0]='mac'
	
	#remove element at index from array
	unset os[2]

#printing
	# print first item in array
	echo "${arr}"
	#print whole array
	echo "${os[@]}"
	#print indices of array
	echo "${!os[@]}"
	#print length of array
	echo "${#os[@]}"

# looping through
	# loop through array
	for num in ${arr[@]}; do
		echo $num
	done

	# prints only first item in array
	for num in ${arr}

	# loop through indices of array
	# ! indicates accessing indices of array, not elements themselves
	for i in ${!arr[@]}; do
		echo "element $i is ${arr[$i]}"
	done
```