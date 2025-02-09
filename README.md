# Plannning
Planner used : https://popf-cloud-solver.herokuapp.com

## Tricky switch domain
- A switch can be toggled.
- There are five switches.
- A switch can only be switched on if it has a neighbour that is already on.
- The five switches are in a row so that each switch has two neighbours, except the two at the ends of the row which only have one.
- The five switches are in initial positions: {off, off, on, off, off}.
- Make all switches turn on

Generate plan:  
<img width="551" alt="plan_2_2" src="https://user-images.githubusercontent.com/14234116/201556849-593179c2-91cd-4969-8915-9d1883c46c90.png">


## Tricker switch domain
- There are 10 switches
- The ten switches are in initial positions: {on, off, on, off, off, on, off, off, on, off}.
- A switch can only be switched on if it has exactly one neighbour that is already on.

Generated plan:  
<img width="583" alt="plan_2_2_bonus" src="https://user-images.githubusercontent.com/14234116/201556883-f1d680bd-3c08-40ca-851f-07fdcff6a5c1.png">


## Basic logistics domain
Diagram below gives set of locations and paths.

<img width="631" alt="Screenshot 2022-11-13 at 6 19 02 PM" src="https://user-images.githubusercontent.com/14234116/201556296-92add82c-d2f7-405c-ad3b-b6775d75aeb5.png">

Actions:
- Packages can be loaded into and out of trucks (a driver does not have to be present).
- Drivers can walk between connected locations.
- Drivers can get into and out of trucks.
- A truck with a driver inside can move between connected locations.

Objects:
- Two drivers
- Two trucks
- Four packages
- Eleven locations

Initial state:
- The drivers are in locations {wp1, wp4}
- The trucks are in locations {wp6, wp9}
- The packages are in locations {wp2, wp3, wp5, wp11}

Goal state:
- Both drivers must be home in wp1.
- The packages must be in their destination locations:
- package 1 and 3 in location wp9
- package 2 and 4 in location wp2

Generated plan:  
[Link to plan pdf](Logistics/plan.pdf)

## Logistics domain now with durative ations and added vehicles like plane and boat.

<img width="1027" alt="Screenshot 2022-11-15 at 1 51 07 PM" src="https://user-images.githubusercontent.com/14234116/202022800-c0721caa-a0be-48eb-9329-f6ddca5f169f.png">

- Packages can be loaded into and unloaded from trucks (10 time units).
- Drivers can walk between connected waypoints (at a speed of 0.5).
- Drivers can get into and out of trucks (10 time units).
- Trucks with drivers can drive between connected waypoints (at a speed of 1).
- The boat and the plane don’t need drivers to move.
- They can only travel over the blue and yellow edges (connected to the lighthouse and the sky). Trucks can only travel on roads.
- The boat travels at a speed of 1.5.
- The plane travels at a speed of 2

Generated Plan:
[Link to plan pdf](Logistics%20with%20durative%20actions/plan.pdf)

## Logistics domain with dealines for delivery modelled with TImed initial literals

Generated plan:
[Link to plan pdf](Logistics%20with%20Timed%20Initial%20Literal/plan.pdf)



