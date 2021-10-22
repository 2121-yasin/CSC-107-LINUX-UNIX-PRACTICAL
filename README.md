
Solutions:-

1.	#!/bin/bash read 2113 read word
if [ $(grep -c "$word" "$2113") -gt 0 ]; then
echo "Success" else
echo "Fail"
fi


2.	#!/bin/bash

read oldfile read newfile
mv "$oldfile" "$newfile"

3.	echo "Enter Phone Number as XXXXXXXX: " read PhoneNumber
pat="^[0-9]{8}$"
while [[ ! $PhoneNumber =~ $pat ]] do
echo "Please enter phone number as XXXXXXXX: " read PhoneNumber
done
echo $PhoneNumber
