🚦 Density-Based 4-Way Traffic Light Control System
📌 Project Overview

This project implements a traffic light control system using an ATmega32 microcontroller, programmed in Assembly language. The system dynamically controls traffic signals based on traffic density, optimizing vehicle flow at a 4-way intersection.
🛠 Features

✅ Traffic Density Detection: Uses sensor inputs on PORTA (PA0-PA3) to detect vehicle presence.
✅ Dynamic Light Control: Traffic lights on PORTC (PC0-PC5) & PORTD (PD0-PD5) switch based on density.
✅ Fixed Time Mode: If no density is detected, the system follows a normal cyclic sequence.
✅ Efficient Delay Function: Implements an optimized delay function (DelayMEGA).

⚙ Assembly Code Overview
🔹 Port Configuration

    PORTA (PA0 - PA3): Inputs for traffic density detection.
    PORTC & PORTD: Outputs controlling traffic light signals.

🔹 Control Flow

    Traffic Sensor Check:
        Each lane is checked for traffic density.
        If a vehicle is detected (PAx = 1), the corresponding traffic light sequence is executed.

    Signal Control Logic:
        Green Light is ON for detected lanes.
        Red Lights stop other lanes.
        Yellow Light ensures transition.

    Fixed Mode Execution:
        If no density is detected, the system cycles through a predefined sequence.

    Delay Function (DelayMEGA)
        Generates necessary delays using registers R16, R17, R18.

🚀 Installation & Usage

    Clone the repository:

    git clone https://github.com/your-username/repo-name.git

    Open in AVR Studio / Atmel Studio.
    Assemble and Compile the Code.
    Simulate using Proteus / Upload to ATmega32.

⚡ Challenges Faced & Solutions
🔴 Traffic Density Detection Issues

✅ Solution: Used SBIS (Skip If Bit is Set) & SBIC (Skip If Bit is Cleared) for real-time sensor reading.
🔴 Timing & Delays

✅ Solution: Optimized DelayMEGA function using nested subtraction loops to maintain consistent timing.
📜 License

This project is open-source and available under the MIT License.
🤝 Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request.
