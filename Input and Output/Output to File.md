 Append output to end of text file
``` bash
#! /bin/bash

echo -e "enter the name of the file: \c"
read file_name
# must check if file exists and we can write to file
if[ -f "$file_name" ]
then
	if[ -w "$file_name" ]
	then
		# ctrl + d allows you to go out of cat command
		echo "type text to append. To quit press ctrl+d"
		
		cat >> $file_name
		
	else
		echo "you do not have write permissions for $file_name "
	done
else
	echo "$file_name does not exist"
done

#or
if [ -f "$file_name" ] && [ -w "$file_name" ]
then 
	cat >> $file_name
else
	echo "$file_name does not exist or you do not have write permissions for it"
done


```
- Append text
	- cat >> $file_name
- overwrite file
	- cat > $file_name