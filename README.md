# 🍽️ Hotel Management System (POSIX-Compliant C)

This repository contains the source code for a **Hotel Management System** implemented in **POSIX-compliant C** on **Ubuntu 22.04**. The system simulates various entities in a hotel environment — such as Admin, Hotel Manager, Tables, Customers, and Waiters — each running as separate processes. Communication between these processes is handled via **pipes** and **shared memory**.

---

## 📁 Project Structure

- **`admin.c`**  
  Handles hotel shutdown logic and ensures clean termination of all child processes.

- **`table.c`**  
  Creates and manages table processes. Takes customer orders and forwards them to waiter processes.

- **`waiter.c`**  
  Receives and validates customer orders from tables, calculates bills, and sends earnings data to the Hotel Manager.

- **`hotelmanager.c`**  
  Aggregates total earnings, calculates staff wages and profits, and manages shared memory communication.

- **`menu.txt`**  
  Contains the predefined menu items and their corresponding prices.

- **`earnings.txt`**  
  Output file that records earnings from different tables in the hotel.

---

## 🔧 Technologies Used

- **Language**: C (GCC)
- **Operating System**: Ubuntu 22.04
- **IPC Mechanisms**:
  - **Pipes**: For inter-process communication between tables and waiters
  - **Shared Memory**: For communication between waiters and the hotel manager
- **POSIX APIs**:
  - `fork()`
  - `pipe()`
  - `read()`, `write()`
  - `shmget()`, `shmat()`, `shmdt()`
  - `kill()`, `wait()`, etc.

---

## 🚀 How It Works

1. **Admin** initializes and controls the start/stop of the hotel system.
2. **Tables** simulate customers placing orders.
3. **Waiters** handle incoming orders, compute bills, and forward revenue data.
4. **Hotel Manager** computes total income and wages using shared memory.
5. Output is stored in `earnings.txt`, and the menu is read from `menu.txt`.

---

## 📌 Key Concepts Demonstrated

- Multi-process programming using `fork()`
- Inter-process communication via **pipes**
- Shared memory usage with proper synchronization
- Real-time coordination between concurrent processes
- File I/O and structured logging
- Clean resource management and termination handling

---


