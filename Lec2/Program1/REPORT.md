#Report for the first program

This program creates an array of the specified length
```
printf("Enter length of array: ");
scanf("%d", &length);
```

After that, memory allocation for this array should occur,
and if this does not happen, the "malloc" function returns NULL
```
if ((array = (int * ) malloc(length * sizeof(int))) != NULL)
```

Then the number of allocated bytes should be output
```
printf("Allocated %lu bytes\n", length * sizeof(*array));
```

If there were no failures at all stages of the program execution, 
the program will clear the allocated memory
```
if (array != NULL)
{
free(array);
}
```
