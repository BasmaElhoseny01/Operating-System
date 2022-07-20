# Operating-System
It is a simple OS to perform selection algorithms among different processes and a Memory allocation algorithm(Buddy sort).

Linux based project

The main file to run is process_generator.c after putting the processes info in the make file.

-------------------------------------------------------------------------------------------------------------------------------------------------------------
Scheduling Algorithms:
 1. Non-preemptive Highest Priority First (HPF).
 2. Shortest Remaining time Next (SRTN).
 3. Round Robin (RR)

-------------------------------------------------------------------------------------------------------------------------------------------------------------
Memory allocation Algorithms:
 1.Buddy sort

-------------------------------------------------------------------------------------------------------------------------------------------------------------
processes.txt format:

#id arrival runtime priority memsize
1 1 6 5 200
2 3 3 3 170

-------------------------------------------------------------------------------------------------------------------------------------------------------------
scheduler output (scheduler.log) format:

#At time x process y state arr w total z remain y wait k
At time 1 process 1 started arr 1 total 6 remain 6 wait 0
At time 3 process 1 stopped arr 1 total 6 remain 4 wait 0
At time 6 process 2 finished arr 3 total 3 remain 0 wait 0 TA 3 WTA 1
At time 6 process 1 resumed arr 1 total 6 remain 4 wait 3
At time 10 process 1 finished arr 1 total 6 remain 0 wait 3 TA 10 WTA 1.67

-------------------------------------------------------------------------------------------------------------------------------------------------------------
Memory allocation output (memory.log) format:

#At time x allocated y bytes for process z from i to j
At time 1 allocated 200 bytes for process 1 from 0 to 255
At time 3 allocated 200 bytes for process 2 from 256 to 383
At time 6 freed 200 bytes from process 2 from 256 to 383
At time 10 freed 200 bytes from process2 from 256 to 383

-------------------------------------------------------------------------------------------------------------------------------------------------------------
