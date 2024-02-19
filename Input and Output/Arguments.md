
Pass Arg to bash script
- stored in default arg vars $1, $2, etc
- $0 is name of script
``` bash
echo $0 $1 $2 $3
# if I run script.sh 1 2 3 my output would be:
./script.sh 1 2 3 



# pass arguments as an array, stored as array args
args=("$@")

# print out all args sent in
for arg in ${args[@]}; do
	echo $arg
done

# or
echo $@

# print num of args passed to script
echo $#
```
