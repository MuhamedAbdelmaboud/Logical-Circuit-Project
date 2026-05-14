# Parking Lot Counter

> **Course-Based Repo for CS 221 - Logical Circuits**  
> Taken at Spring 2026 with **Professor Osama Khoziem**  
> at **Sadat Academy for Management Sciences**

---

## Team 6 Members

| Name |
|------|
| Muhamed Abdelmaboud |
| Mohamed Hassen |
| Yousseif Mansour |

---

## What Is This Project?

This is a **digital logic circuit** built in **Logisim Evolution** that simulates a real parking lot entrance/exit system.

The idea is simple:
- A car **enters** → counter goes **up**
- A car **exits** → counter goes **down**
- The number of cars currently inside is shown on a **Hex Display**
- When the lot hits max capacity **(10 cars)**, a red **FULL** light turns on and the entrance is **automatically locked**
- A green **Available** light stays on whenever there is still space

---
## How the Logic Works

1. **UP/DOWN Counter (4-bit)**
   Counts from 0 to 15. The UP input connects to ENTER (through an AND gate). DOWN connects directly to EXIT.

2. **AND Gate + NOT Gate (entry control)**
   The FULL signal is inverted by a NOT gate and fed into the AND gate.
   This means: ENTER only works when the lot is NOT full. When full so entrance locked automatically.

3. **Hex Display**
   Wired directly to the counter output. Always shows the live car count.

4. **LEDs**
   - 🔴 Red LED — lights up when lot is full
   - 🟢 Green LED — lights up when space is available (NOT of FULL signal)

---

## Components Used

| Component | Library in Logisim | Purpose |
|---|---|---|
| Button × 3 | Base | ENTER / EXIT / RESET |
| Counter (4-bit) | Memory | Tracks number of cars |
| Comparator | Arithmetic | Checks if count ≥ 10 |
| Constant = 10 | Base | Maximum capacity value |
| AND Gate | Gates | Blocks entry when full |
| NOT Gate | Gates | Inverts the FULL signal |
| Hex Digit Display | Base | Shows current car count |
| LED × 2 | I/O | Red = Full, Green = Available |

---

## How to Run

1. Download **Logisim Evolution** (free): https://github.com/logisim-evolution/logisim-evolution
2. Open `parking_counter.circ`
3. Switch to **Simulation Mode** (the hand icon )
4. Click **ENTER** to simulate a car entering
5. Click **EXIT** to simulate a car leaving
6. Watch the Hex Display update and the LEDs respond
7. Click **RESET** to bring the counter back to zero

---

## Concepts Demonstrated

- **Sequential Logic** Up/Down Counter with enable and reset
- **Combinational Logic** AND/NOT gates for entry control
- **I/O Interfacing** Hex display + LED visual outputs

---

## Files in This Repo

| File | Description |
|---|---|
| `parking counter.circ` | Main Logisim circuit file - open this in Logisim |
| `README.md` | This file |
