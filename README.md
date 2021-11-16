
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



#include <errno.h>
#include <sys/stat.h>
#include <stdio.h>
#include <stdlib.h>
​
int main(void)
{
struct stat statbuf;
​
if (stat("abc", &statbuf) < 0)
perror("stat error for file.txt");
​
if (chmod("abc", (statbuf.st_mode | S_IXGRP )) < 0)
perror("chmod error for abc");
​
/* set absolute mode to "rw-r--r--" */
if (chmod("newfile.txt", S_IRUSR | S_IWUSR | S_IRGRP | S_IROTH) < 0)
perror("chmod error for newfile.txt");
​
if(chmod("xyz", 0777)<0)
perror("chmod error for nxyz");
return 0;
}




utting all the changes together yields:

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <errno.h>
#include <sys/stat.h>

int main(int argc, char **argv)
{
    char mode[] = "0777";
    char buf[100] = "/home/hello.t";
    int i;
    i = strtol(mode, 0, 8);
    if (chmod (buf,i) < 0)
    {
        fprintf(stderr, "%s: error in chmod(%s, %s) - %d (%s)\n",
                argv[0], buf, mode, errno, strerror(errno));
        exit(1);
    }
    return(0);
}





#include<sys/types.h>
#include<sys/stat.h>
#include<stdio.h>
#include<fcntl.h>
main( int argc,char *argv[3] )
{
int fd,i;
char buf[2];
fd=open(argv[1],O_RDONLY,0777);
if(fd==-argc)
{
printf("file open error");
}
else
{
while((i=read(fd,buf,1))>0)
{
printf("%c",buf[0]);
}
close(fd);
}
}




