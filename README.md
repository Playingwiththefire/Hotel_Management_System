# Hotel-Management-System
Developed a hotel management system in POSIX-compliant C-OS /IPC/Pipes
Hotel Management System

This repository contains the source code for a hotel management system implemented in POSIX-compliant C for Ubuntu 22.04. The system simulates various entities within a hotel environment, including Admin, Hotel Manager, Tables, Customers, and Waiters, each implemented as distinct processes.

Project Structure:

admin.c: Manages the hotel closure process based on user input.
table.c: Creates table processes, manages customer orders, and coordinates with waiter processes.
waiter.c: Receives orders from tables, validates orders, calculates bills, and communicates earnings to the hotel manager.
hotelmanager.c: Oversees total earnings, calculates wages and profits, and communicates with other processes using shared memory.
menu.txt: Contains the predefined menu items with their corresponding prices.
earnings.txt: Output file recording earnings from different tables of the hotel.
