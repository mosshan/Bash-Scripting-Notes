- break
	``` bash
	#! /bin/bash
	for (( i=1 ; i<=10 ; i++ ))
	do
	  if [ $i -gt 5 ]
	  then
	    break
	  fi
	  echo "$i"
	done
	```

- continue
``` bash
#! /bin/bash
for (( i=1 ; i<=10 ; i++ ))
do
  if [ $(( $i % 2)) -eq 0 ]
  then
    continue
  fi
  echo "$i"
done
```