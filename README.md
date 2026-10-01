# 🏦 Core ATM Simulation Engine

A lightweight, high-precision console-based ATM banking simulator built in pure Java. This project demonstrates enterprise-grade backend coding standards, strict data encapsulation, and mathematically bulletproof financial transaction tracking.

---

## 🎯 Project Core Objectives
* **Absolute Financial Accuracy:** Employs `java.math.BigDecimal` to eradicate floating-point rounding bugs entirely.
* **Interface-Driven Architecture:** Utilizes a strict decoupling pattern separating core business specifications from functional implementation layers.
* **Secure Data Management:** Implements private instance scopes to protect account data models from unauthorized state mutations.

---

## 🛠️ Architecture & Design Layers

The application is structured into four highly isolated components following professional software engineering tiers:

1. **`Atm` (The Data Model):** A passive, encapsulated POJO data shell managing account parameters (`balance`, `depositAmount`, `withdrawAmount`).
2. **`AtmInterface` (The Contract Layer):** An abstract system blueprint establishing structural behavior boundaries for banking operations.
3. **`AtmInterfaceFiller` (The Business Service):** The processing core responsible for executing ledger operations, balance validations, and math arithmetic.
4. **`AtmMain` (The Orchestrator):** The runtime command center managing secure PIN validation loops, application state execution, and interactive console input streams via `BufferedReader`.

---

## 📊 Why BigDecimal? (The Math Guardrail)
Standard primitive variables (`double`, `float`) utilize binary floating-point calculations which introduce trailing fractional errors (e.g., `1.00 - 0.90` dynamically evaluating to `0.09999999999999998`). 

This project strictly utilizes `BigDecimal` string constructors and explicit object methods (`.add()`, `.subtract()`, `.compareTo()`) to guarantee absolute base-10 calculation precision—ensuring compliance with standard corporate banking ledger requirements.

---

## 🚀 Execution & Quick Start

### Prerequisites
* Java Development Kit (JDK) 8 or higher
* An IDE (IntelliJ IDEA, Eclipse) or standard terminal CLI

### Running the App
1. Clone this repository to your local workspace.
2. Compile the source directory files.
3. Run the master orchestration file:
```bash
java com.reagan.atmsimulation.AtmMain
```

### Default Credentials
* **Secure Demo PIN:** `1234`
