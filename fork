#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main() {
   fork();
   printf("Called fork() system call\n");
   return 0;
}



#include <sys/wait.h>
#include <unistd.h>
#include <sys/types.h>
#include <stdio.h>
int main( ){
   pid_t child_pid;
   child_pid = fork (); // Create a new child process;
   if (child_pid < 0)
   {
      printf("fork failed");
      return 1;
   }
    else if (child_pid == 0)
  {
      printf ("child process successfully created!");
      printf ("child_PID = %d,parent_PID = %d",
      getpid(), getppid( ) );
   }
    else {
      wait(NULL);
  printf ("parent process successfully created!");
      printf ("child_PID = %d, parent_PID = %d", getpid( ), getppid( ) );
   }
   return 0;
}

#include <stdio.h>
#include <sys/types.h>
#include <unistd.h>

int main() {
   pid_t pid, mypid, myppid;
   pid = getpid();
   printf("Before fork: Process id is %d\n", pid);
   pid = fork();

   if (pid < 0) {
      perror("fork() failure\n");
      return 1;
   }


   if (pid == 0) {
      printf("This is child process\n");
      mypid = getpid();
      myppid = getppid();
      printf("Process id is %d and PPID is %d\n", mypid, myppid);
   } else { // Parent process
      sleep(2);
      printf("This is parent process\n");
      mypid = getpid();
      myppid = getppid();
      printf("Process id is %d and PPID is %d\n", mypid, myppid);
      printf("Newly created process id or child pid is %d\n", pid);
   }
   return 0;
}

#include <stdio.h>
#include <unistd.h> 

int main() {
    int pid;

    pid = fork();
    if (pid < 0) {
        // Fork failed
        perror("Fork failed");
        return 1;
    }

    if (pid == 0) {
        printf("I am child. The value of variable pid is %d\n", pid);
        printf("I am child and my process id is %d\n", getpid());
        printf("I am child and my parent process id is %d\n", getppid());
    } else {
        printf("I am parent. The value of pid is %d\n", pid);
        printf("I am parent and my process id is %d\n", getpid());
        printf("I am parent and my parent process id is %d\n", getppid());
    }

    return 0;
}




