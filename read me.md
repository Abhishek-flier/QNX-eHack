# &#x20;Smart Traffic Signal Simulator (Multithreaded C Project)

## &#x20;Overview

This project simulates a smart traffic management system using C programming with pthreads.  
It dynamically selects traffic lanes based on:

* Vehicle density
* Emergency vehicle priority
* Multithreaded execution

\---**Features**

* Priority-based lane selection:

  * Ambulance (highest)
  * Fire
  * Disaster
  * Police
  * Normal traffic
* Vehicle-based timing calculation
* Continuous traffic cycle simulation
* Multithreaded lane execution using pthread
* Movement split (Straight / Left / Right / U-turn)
* Thread-safe synchronization using mutex + condition variables

\---**Input Format**

vehicles type

Example:
12 none  
15 ambulance  
8 fire  
20 none

\--- **How It Works**

1. Input traffic data for 4 lanes:
North, South, East, West
2. System selects highest priority lane
3. Emergency vehicles override normal traffic
4. Among same priority → higher vehicle count wins
5. Lane runs in its own thread
6. Cycle repeats continuously

\--- Compilation \& Execution

Compile:
gcc main.c -o traffic -lpthread

Run:
./traffic

\--- **Technologies Used**

* C Language
* POSIX Threads (pthread)
* Mutex \& Condition Variables
* Linux / Unix environment

\--- **Future Improvements**

* Raspberry Pi integration
* OpenCV vehicle detection
* AI traffic prediction
* Real-time camera feed support

\--- 

