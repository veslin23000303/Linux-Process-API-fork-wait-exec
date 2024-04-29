# Linux-Process-API-fork-wait-exec-
Ex02-Linux Process API-fork(), wait(), exec()
# Ex02-OS-Linux-Process API - fork(), wait(), exec()
Operating systems Lab exercise


# AIM:
To write C Program that uses Linux Process API - fork(), wait(), exec()

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Write the C Program using Linux Process API - fork(), wait(), exec()

### Step 3:

Test the C Program for the desired output. 

# PROGRAM:
DEVELOPED BY:VESLIN ANISH A REGISTER NUMBER:212223240175

## C Program to print process ID and parent Process ID using Linux API system calls
```
#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>
int main(void)
{	//variable to store calling function's process id
	pid_t process_id;
	//variable to store parent function's process id
	pid_t p_process_id;
	//getpid() - will return process id of calling function
	process_id = getpid();
	//getppid() - will return process id of parent function
	p_process_id = getppid();
	//printing the process ids

//printing the process ids
	printf("The process id: %d\n",process_id);
	printf("The process id of parent function: %d\n",p_process_id);
	return 0; }
```















##OUTPUT
![WhatsApp Image 2024-04-29 at 23 24 54_9624c54c](https://github.com/veslin23000303/Linux-Process-API-fork-wait-exec/assets/151148539/ca0439ca-eb63-47b7-8bf5-ea6a018ebb55)














## C Program to create new process using Linux API system calls fork() and exit()
```
#include <stdio.h>
#include<stdlib.h>
int main()
{ int pid; 
pid=fork(); 
if(pid == 0) 
{ printf("Iam child my pid is %d\n",getpid()); 
printf("My parent pid is:%d\n",getppid()); 
exit(0); } 
else{ 
printf("I am parent, my pid is %d\n",getpid()); 
sleep(100); 
exit(0);} 
}
```












##OUTPUT
![WhatsApp Image 2024-04-29 at 23 25 25_153c054e](https://github.com/veslin23000303/Linux-Process-API-fork-wait-exec/assets/151148539/327f2872-9f3f-4da8-97a8-dcb0929a0282)








## C Program to execute Linux system commands using Linux API system calls exec() family

```
#include <unistd.h>
#include <stdio.h>
#include <stdlib.h>
int main()
{
	printf("Running ps with execlp\n");
	execlp("ps", "ps", "ax", NULL);
	printf("Done.\n");
	exit(0);
}
```
























##OUTPUT

![WhatsApp Image 2024-04-29 at 23 25 57_f968be2b](https://github.com/veslin23000303/Linux-Process-API-fork-wait-exec/assets/151148539/1731023c-6ccb-4a9b-a868-7368d4b82850)

















# RESULT:
The programs are executed successfully.
