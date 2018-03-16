1. List all of the main states a process may be in at any point in time on a standard Unix system. Briefly explain what each of these states mean.  

_answer_ - 
  a. _Created/New :_ When the process is created it is in the Created or New state.  

  b. _Ready :_ The process has been loaded into memory and is awaiting execution.  

  c. _Running :_ Process has been chosen and is in the process of execution  

  d. _Blocked :_ when a process is not allowed, for a variety of reasons (awaiting user input, for example), to execute. Some sort of external change in state is required before it will be allowed to run again.  

  e. _Terrminated/Exit :_either the process has completed running or it has been killed.  
  

2. What is a Zombie Process? How does it get created? How does it get destroyed?  

_answer_ 
A zombie process is one that has completed execution, but still has an entry in the process table. Generally, a child process becomes a zombie during the process of being removed from the process table. Its parent process reads and reaps the exit status of the process, and then the zombie is removed from the process table. The analogy that works best for me is a relay race in which one runner passes a baton to another. 

3. Describe the job of the Scheduler in the OS in general.  

_answer_ - The scheduler in the OS allocates system resources to handle processes that are simultaneously vying for execution time from the CPU. Scheduling algorithms used toward this end are FIFO, shortest job first, and round robin, among others.

4. Describe the benefits of the MLFQ over a plain Round-Robin scheduler.  

_answer_ - In *round robin scheduling*, each process is assigned a fixed time slot and all processes get a fixed share of CPU. *Multi-Level Feedback Queue (MLFQ)* attempts to better address turnaround time and response time constraints by "learning" the characteristics of each process as the system runs. As such, it can make more efficient scheduling decisions.