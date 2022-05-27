# Report for the third program

Initially, memory is allocated for an array with "char" elements
char * c = (char * ) calloc(100, sizeof(char));

Then the program opens the file foo.txt with parameters for reading `O_RDONLY` and creating `O_CREAT`
```
int fd = open("foo.txt", O_RDONLY | O_CREAT);
```

Then the value of the file descriptor is output
```
printf("fd = %d/n", fd);
```

Next, the information is calculated from 10 bytes and its volume is written to the variable "sz"
```
sz = read(fd, c, 10);
```

A terminal zero will be written to the end of the array and the program will close the file
```
if (close(fd) < 0)
{
perror("close file error:");
exit(1);
}
```
