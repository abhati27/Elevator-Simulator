# Elevator-Simulator
This project is a multi-threaded simulation of an elevator system. It is intended to provide a realistic model of how elevators and passengers would interact in a multi-floor building, with each elevator and passenger operating in their own threads.


## Files
### elevator.h
This header file contains constant definitions and function prototypes for the elevator simulation. Constants include the maximum capacity of each elevator, the total number of elevators, the total number of floors in the building, the number of passengers, and the number of trips each passenger makes.

The function prototypes are as follows:

`scheduler_init()`: Initializes the scheduler.

`passenger_request()`: Called when a passenger requests an elevator. Signals the passenger when their elevator has arrived.

`elevator_ready()`: Called when an elevator is ready to take an action. Signals passengers when the elevator is ready.

### elevator.c
This is the main source file for the elevator simulation. It contains the implementation of the functions declared in `elevator.h`. The elevator and passenger states are managed using POSIX threads and conditions, ensuring proper synchronization in the system.

### main.c
This file contains the main function which drives the elevator simulation. It creates the necessary threads for each passenger and elevator, then joins all the threads to ensure they have completed their execution.



