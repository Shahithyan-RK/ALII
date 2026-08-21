# Advanced Light Intensity Indicator (ALII)

An analog and discrete digital electronics system that senses, processes, and displays light intensity — built entirely **without microcontrollers**.

## Overview

ALII accurately measures ambient light intensity while handling real-world noise and stability issues, using only analog circuitry and discrete digital logic. The project demonstrates end-to-end mixed-signal system design: from raw sensor signal conditioning through to a stable, averaged digital display.

## System Architecture

The system is divided into four main stages:

### 1. Signal Conditioning (Active Filtering)
A 2nd-order Sallen-Key low-pass filter with a 10 Hz cutoff frequency reduces 50 Hz mains interference picked up by the LDR sensor, cutting noise by approximately 28 dB and producing a clean, stable analog signal.

### 2. Quantization (Flash ADC)
A custom 3-bit Flash ADC built from a parallel comparator ladder converts the analog voltage into a digital thermometer code in real time, representing light intensity across 8 levels (0–7) with no conversion delay.

### 3. Digital Stability Logic
A stability timer built from discrete logic gates and counters prevents display flicker caused by momentary shadows or transients. The display only updates once the light level has remained stable for a predefined period.

### 4. Digital Averaging Logic
Average light intensity over a set time period is computed using a timer, a counter, flip-flops, and 4-bit adders — all implemented in discrete digital logic.

## Repository Contents

- Simulation files
- Circuit designs (schematics)
- Project demonstration videos

## Tech / Concepts Used

- Analog active filter design (Sallen-Key topology)
- Flash ADC / comparator-based quantization
- Discrete sequential logic (counters, flip-flops, timers)
- 4-bit binary adder circuits
- Mixed-signal system integration

## Key Learnings

This project provided hands-on experience in analog circuit design, digital logic design, and system-level problem-solving, and deepened our understanding of hardware-based thinking in mixed-signal systems.
