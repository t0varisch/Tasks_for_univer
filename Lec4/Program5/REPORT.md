#Report for the fifth program

Initially, the program receives the signal entered by the user and processes it, after which it creates a global variable-a counter
```
int counter = 0;

```

There are also two processing functions in the program
First:
```
void handler1(int sig)
{
counter++;
printf("counter = %d\n", counter);
/* Flushes the printed string to stdout */
fflush(stdout);
kill(pid, SIGUSR1);
}
```
And second

```
void handler2(int sig)
{
counter += 3;
printf("counter = %d\n", counter);
exit(0);
}
```
Processing occurs, during which the program binds the first processing function to the current process.
Further, if the process turns out to be a child, the handler2 function will process the signal.

