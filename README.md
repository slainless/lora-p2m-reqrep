# LoRa Pseudo P2M Communication using Simple ZeroMQ Req/Rep Implementation

Pretty crazy project for my undergraduate thesis, microcontroller program fully written in typescript. Should have been written in C++ atleast, but oh well.

Uploaded to source control to persist the project.

## Aim

It's pretty much a simple communication system built to handle communication between multiple node using LoRa while also preventing collision. Very naive implementation using custom ZeroMQ Request/Reply. Ideally, should implement a full-blown CSMA/CR (**Carrier Sense Multiple Access with Collision Resolution**), but that protocol being too complex to implement, and i'm being constrained by time and budget, prevented me from even attempting it.

## Components

- Raspberry Pi Pico
- KalumaJS as microcontroller framework and interface
- LoRa device E32-900T30D
- LED, LCD, and Button

## Development

1. Kaluma flashed to Pico
2. Program developed in typescript
3. Program transformed and bundled into javascript via `esbuild`
4. Javascript bundle flashed to Pico via serial communication (USB)

The hard part is when developing data-link layer, mainly in designing and implementing data communication protocol.
