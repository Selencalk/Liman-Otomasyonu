🚢 Port Loading Simulation
This project is a Python-based simulation that models the process of unloading trucks (TIRs) at a port and loading their cargo onto ships according to destination countries, storage areas, and capacity constraints.
The simulation focuses on logistics management, data structures, and object-oriented programming concepts.
🎯 Project Purpose
The main goals of this project are:
Simulating cargo flow from trucks to ships in a port
Managing storage areas and crane capacity
Assigning cargo to ships based on destination country
Demonstrating the use of priority queues (heap) and OOP
Modeling a time-based logistics simulation
📂 Project Structure
.
├── main.py
├── olaylar.csv
├── gemiler.csv
└── README.md
main.py
The main Python file that controls the simulation logic.
It includes the following classes:
Tir
License plate
Destination country
Number of 20-ton and 30-ton containers
Total cargo and cost calculation
Ship
Ship ID
Capacity
Destination country
Current load status
Port
Truck and ship queues (implemented using heap)
Two storage areas
Crane capacity and time management
Cargo unloading and ship loading operations
📄 CSV Files
olaylar.csv – Truck Events
Contains information about trucks arriving at the port.
Fields:
tir_plakasi
ulke
20_ton_adet
30_ton_adet
Total cargo calculation:
total_load = (20_ton_count × 20) + (30_ton_count × 30)
gemiler.csv – Ships
Contains information about ships arriving at the port.
Fields:
arrival_time
ship_name
capacity
destination_country
A ship leaves the port when 95% of its capacity is filled.
⚙️ Simulation Workflow
Trucks are read from olaylar.csv and added to the queue
Ships are read from gemiler.csv
Trucks unload cargo into Storage Area 1
Cargo is:
Loaded onto a ship heading to the same country, or
Moved to Storage Area 2 if no suitable ship is available
Crane capacity and time advance step by step
Ships depart once they reach sufficient capacity
▶️ How to Run
Make sure Python 3 is installed.
python main.py
During execution, the program prints:
Minute-by-minute events
Cargo unloading and transfer operations
Ship departures
🛠 Technologies Used
Python 3
csv module
heapq (priority queue)
Object-Oriented Programming (OOP)
📝 Notes
This is a simulation, not a real-time system
Capacities and limits can be easily adjusted
Suitable for academic projects and assignments
