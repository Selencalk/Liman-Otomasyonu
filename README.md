Port Cargo Loading Simulation
A Python-based simulation that models cargo operations in a port environment.
The project focuses on unloading trucks (TIRs), managing storage areas, and loading cargo onto ships according to destination and capacity constraints.
This repository is intended for educational and academic use.

📌 Overview
The simulation represents a simplified port system where:
Trucks arrive carrying cargo containers
Cargo is temporarily stored in storage areas
Ships are loaded based on destination country
Capacity limits and time progression are respected
Ships leave the port once they reach 95% of their maximum capacity.

📂 Project Structure
.
├── main.py
├── olaylar.csv
├── gemiler.csv
└── README.md

🧩 Main Components
Truck (TIR)
Each truck includes:
License plate
Destination country
20-ton container count
30-ton container count

Ship
Each ship has:
Ship ID / name
Destination country
Maximum capacity
Current load
A ship departs when it reaches 95% of its capacity.

Port
The port is responsible for:
Managing truck and ship queues (priority queues using heapq)
Handling two storage areas
Managing crane capacity
Simulating time progression
Coordinating cargo transfers between trucks, storage areas, and ships

📄 Input Files
olaylar.csv — Truck Events
Contains incoming truck data.
Fields:
tir_plakasi
ulke
20_ton_adet
30_ton_adet

gemiler.csv — Ships
Contains incoming ship data.
Fields:
arrival_time
ship_name
capacity
destination_country

⚙️ Simulation Flow
Trucks are read from olaylar.csv and added to the truck queue
Ships are read from gemiler.csv and scheduled by arrival time
Trucks unload cargo into Storage Area 1
Cargo is:
Loaded onto a ship with a matching destination, or
Moved to Storage Area 2 if no suitable ship is available
Crane capacity limits the operations per time unit
Ships depart once sufficiently loaded

▶️ How to Run
Make sure Python 3 is installed.
python main.py
The program outputs:
Time-based simulation steps
Cargo unloading and transfer operations
Ship departure events

🛠 Technologies Used
Python 3
csv module
heapq (priority queue)
Object-Oriented Programming (OOP)

📝 Notes
This is a simulation, not a real-time system
Parameters such as capacities and limits can be adjusted easily
Suitable for coursework and academic demonstrations
