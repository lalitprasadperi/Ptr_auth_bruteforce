# Bruteforce Attack on Pointer Authentication Codes (PAC)

This repository demonstrates a brute-force attack on Pointer Authentication Codes (PAC), a feature used in ARMv8.3+ architectures to enhance security by adding authentication to pointers. PAC is designed to prevent certain types of exploits like Return-Oriented Programming (ROP) and Code Reuse Attacks (CRA). This project also draws insights from the research conducted in the PACMAN project, which analyzed vulnerabilities in PAC implementations by combining speculative execution attacks with brute-forcing.

---

## Table of Contents
1. [Introduction](#introduction)  
2. [Features](#features)  
3. [Setup](#setup)  
4. [Usage](#usage)  
5. [Example Output](#example-output)  
6. [Limitations](#limitations)  
7. [References](#references)  
8. [Disclaimer](#disclaimer)  
9. [Contributing](#contributing)  

---

## Introduction

Pointer Authentication Codes (PAC) use cryptographic methods to sign pointers, making unauthorized modifications detectable. While PAC significantly improves security, research such as the **PACMAN** project has highlighted potential weaknesses. This repository builds on those insights to demonstrate a brute-force attack in controlled environments, focusing on:
- Key management weaknesses
- Limited key space in constrained setups
- Timing and speculative execution vulnerabilities as demonstrated in PACMAN.

### Insights from PACMAN
The PACMAN project, presented at [ISCA 2022](https://pacmanattack.com), combined speculative execution attacks with brute-forcing PACs. It showcased that PACs could be bypassed under specific conditions by leveraging microarchitectural behaviors and timing side channels. This repository does not implement speculative execution attacks but explores brute-force attacks in isolation.

---

## Features

- **PAC Basics**: Demonstrates pointer signing and verification.  
- **Brute-Force Simulation**: Implements a brute-force attack on PACs under constrained key ranges.  
- **Insights from PACMAN**: Incorporates key findings and limitations from PACMAN research.  
- **Customizable**: Configure attack parameters like key size, timing constraints, and pointers.  

---

## Setup

### Prerequisites
- **Hardware**: ARMv8.3+ CPU with PAC enabled.  
- **Operating System**: Linux-based OS with GCC or Clang compiler supporting PAC.  
- **Dependencies**: 
  - GCC/Clang
  - Python 3 (for helper scripts)
  - `make` (build tool)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/pac-bruteforce-attack.git
   cd pac-bruteforce-attack


