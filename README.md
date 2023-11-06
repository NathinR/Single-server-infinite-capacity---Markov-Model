# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![278441841-bd1bbd98-d4c5-4be1-b305-7ef9e1c14771](https://github.com/NathinR/Single-server-infinite-capacity---Markov-Model/assets/118679646/c7237c68-8c08-4f39-9385-1d2d32a6510f)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :
![278441888-d0b2c7ae-8fa7-4bff-96f3-af0fc16e4725](https://github.com/NathinR/Single-server-infinite-capacity---Markov-Model/assets/118679646/fa9c3e02-fe7a-405c-bd21-77aec3a41d80)

## Experiment:
![278441742-9e6a1fa3-f6e4-411d-a6e1-7aa812e3ca81](https://github.com/NathinR/Single-server-infinite-capacity---Markov-Model/assets/118679646/a4f3a9fb-df86-4b35-a054-267f9f55c153)
![278441768-cd7773a7-4791-4292-9ac1-8be698e7d944](https://github.com/NathinR/Single-server-infinite-capacity---Markov-Model/assets/118679646/11b4f50c-71d9-4a95-8548-e6b1066e0b26)

## Program
Developed by: NATHIN R

Register no.:212222230090
```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```

## Output :
![image](https://github.com/NathinR/Single-server-infinite-capacity---Markov-Model/assets/118679646/a72575f4-ab98-4d01-a6a8-2fc3d6a05d63)

## Result :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
