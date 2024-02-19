
Read User Input
```bash
echo "Enter name:"
read name
echo "Name is:  $name" # make sure not to use single quotes

echo "Enter names:"
read name1 name2 name3
echo "Entered names: $name1, $name2, $name3"
# could also do 
echo Entered names: $name1, $name2, $name3

# enter input on same line you printed prompt string on
read -p 'Username: ' username_var # or "Username: "
echo "Username: $username_var"

# make input silent (don't show what user is typing like for pwd)
read -sp "Password: " password_var

# have user enter multiple inputs and save them in an array
echo "Enter names: "
read -a names
echo "Names: ${names[0]}, ${names[1]}"

# read without variable -> input goes into built in var, REPLY
echo "Enter name :"
read
echo "Name: $REPLY"


# enable interpretation of backslashed chars which do diff things
# \c allows the user to enter the char on the same line (ie it doesnt print a new line after)
echo -e "Enter a char: \c"
```
