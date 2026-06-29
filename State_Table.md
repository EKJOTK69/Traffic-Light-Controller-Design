# Finite State Machine (FSM) State Table

This document describes the state transitions and output logic of the Smart Traffic Light Control System Finite State Machine (FSM).

## State Description

- State 001 : Main Road 1 Green
- State 010 : Main Road 2 Green
- State 011 : Transition from Main Road 2
- State 100 : Turn Road Green
- State 101 : Side Road Green
- State 110 : Transition from Side Road
- State 111 : Reset/Error State

---

## State Transition Table

| Present State (ABC) | Input | Next State (A⁺B⁺C⁺) | M1 (RYG) | M2 (RYG) | T (RYG) | S (RYG) |
|---------------------|-------|----------------------|----------|----------|---------|---------|
| 001 | TN̅G | 001 | 001 | 001 | 100 | 100 |
| 001 | TNG | 010 | 001 | 001 | 100 | 100 |
| 010 | T̅Y | 010 | 001 | 010 | 100 | 100 |
| 010 | TY | 011 | 001 | 010 | 100 | 100 |
| 011 | TT̅G | 011 | 001 | 100 | 001 | 100 |
| 011 | TTG | 100 | 001 | 100 | 001 | 100 |
| 100 | F̅Y | 100 | 010 | 100 | 010 | 100 |
| 100 | FY | 101 | 010 | 100 | 010 | 100 |
| 101 | TS̅G | 101 | 100 | 100 | 100 | 001 |
| 101 | TSG | 110 | 100 | 100 | 100 | 001 |
| 110 | T̅Y | 110 | 100 | 100 | 100 | 010 |
| 110 | TY | 001 | 100 | 100 | 100 | 010 |
| 111 | — | 000 | 000 | 000 | 000 | 000 |

---

## Output Encoding

| Code | Light Status |
|------|--------------|
| 100 | Red ON |
| 010 | Yellow ON |
| 001 | Green ON |
| 000 | All OFF |
