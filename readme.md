#  Flighty Flight Controller

**Flighty** is my very first custom-designed flight controller! I built this to be a versatile "brain" for just about anything that flies, from standard quadcopters and fixed-wing UAVs to high-power model rockets.

I am currently using this board to power my personal RC VTOL project. It’s designed to be easy to solder (THT components), easy to repair, and a great hands-on project for anyone interested in PCB assembly.

##  Key Features

* **7x Servo/PWM Channels:** Plenty of outputs for complex RC planes, hexacopters, or VTOL transitions.
* **Rocketry Ready:** Two dedicated channels can be configured as electronic igniters (pyro-channels) for rocket motor ignition or parachute deployment.
* **Blackbox Data Logging:** Integrated **MicroSD slot** to record high-speed flight data, allowing you to re-analyze crashes or tune PID loops with precision.
* **Reliable Power Management:** Designed for **2S LiPo/Li-ion** setups with an integrated charging and protection circuit.
* **Repair-Friendly Design:** Focused on Through-Hole Technology (THT) for connectors and key components, making it durable and easy to fix in the field.

##  Hardware

* **Brain (MCU): STM32F405RGT6** – This is the heart of the board. It’s a powerful chip that handles high-frequency flight loops and complex navigation without breaking a sweat.
* **Gyro/Accel: MPU6500** – To keep things stable, I'm using the MPU6500 over I2C. It supports fast refresh rates (up to 500Hz on the bus) to keep the flight feeling smooth and responsive.
* **Altitude (Baro): BMP580** – This sensor is a beast. It’s incredibly precise, detecting altitude changes down to a few centimeters. It's perfect for a rock-steady hover or timing a rocket's parachute deployment at exactly the right moment.
* **Power: TPS63070 (Buck-Boost)** – I wanted to avoid brownouts. This regulator keeps a rock-solid 5V supplied to the sensors and MCU, even if the battery voltage drops during a hard maneuver.
* **Charging: BQ25883** – I added a built-in 2S balancer/charger. This is super convenient because you can top up your batteries directly through the board using the USB port.
* **Plug: USB Type-C** – Because nobody wants to carry around old Micro-USB cables anymore. One cable for your phone, your laptop, and your flight controller.

##  Software & Firmware

Flighty is compatible with **Ardupilot**, **INAV**, and **Betaflight**. 

> **Note:** Because this is a custom hardware layout, you will need to define a custom target (mapping the SPI/UART/PWM pins) in your chosen firmware.

---

##  Gallery

### Schematics
<img width="916" height="652" alt="Flighty Schematic" src="https://github.com/user-attachments/assets/cfa197a2-18ce-4974-83fe-b3c4003e0c29" />

### PCB Design
![PCB Layout](https://github.com/user-attachments/assets/8e834cd9-f544-48fb-815a-6ca0cd7bc62c)

### 3D Visuals
![3D PCB View](https://github.com/user-attachments/assets/7f54e00f-af63-49e9-a9a5-9661707b93ec)
<img width="827" height="779" alt="Board Render" src="https://github.com/user-attachments/assets/7e4a7a07-e1bb-4409-9a50-0d61d968046a" />

---

##  Bill of Materials (BOM)

| Item | Description | Quantity | Unit Price |
| :--- | :--- | :--- | :--- |
| **Flight Controller PCB** | Bare PCB from JLCPCB | 5 | $2.00 |
| **Flight Controller PCBA** | Fully Assembled Board | 2 | $130.71 |

**Project Total: $159.21**
