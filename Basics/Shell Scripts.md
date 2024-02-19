
- intepreted, not compiled
- start with shebang -> #! path to interpreter
```bash
#! /bin/bash
#! /usr/bin/env bash

```
- comments start with #
- Make script executable:
	- chmod +x script_name.sh
###### Run script
	- ./script_name.sh arguments
		- works if script is in current location
	- /full_file_path/script_name.sh arguments
		- absolute path works regardless of current location
	- sh script_name.sh arguments
	- bash script_name.sh arguments
		- if not in current directory, need to use path
