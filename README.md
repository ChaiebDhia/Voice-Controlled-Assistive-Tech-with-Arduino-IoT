
# 🚀 Prototyping Innovation: Voice-Controlled Assistive Tech with Arduino & Python

## Project Overview

Excited to share a recent project where I developed a voice-controlled system using an Arduino-based prototype (simulating a wheelchair) paired with a custom Python GUI and voice assistant. While initially designed to enhance patient autonomy in healthcare, this solution has far broader applications—demonstrating how IoT and voice recognition can revolutionize multiple domains!

## 🔍 Key Features & Flexibility

* **Modular Design:** The Arduino prototype can be replaced with a real wheelchair, smart home devices, or even industrial equipment—making it adaptable for healthcare, smart cities, logistics, and more.
* **Voice Control:** Users can intuitively navigate environments, control PCs, or manage IoT devices (e.g., lights, appliances) via voice commands.
* **Scalable Architecture:** Built with layered IoT principles (perception, network, application) for seamless integration with diverse hardware.

## 💡 Beyond Healthcare - Potential Applications

This project isn’t just about assistive tech—it’s a proof-of-concept for voice-driven automation in:

* **Smart Homes:** Control systems for elderly/disabled individuals.
* **Industrial IoT:** Hands-free operation in warehouses or factories.
* **Education:** Assistive learning tools for students with mobility challenges.

## 🛠️ Tech Stack

* **Hardware:** Arduino (4WD robot car as prototype), various sensors (specifics depend on implementation), Bluetooth modules (HC-05/06 recommended).
* **Software:** Python (for GUI and voice assistant logic), UML-designed workflows, IoT protocols (e.g., Serial communication over Bluetooth).
* **User-Centric:** Prioritized accessibility with voice + GUI fallback options.

---

## 🚀 Getting Started

To get this project up and running, you'll need to configure both the Arduino hardware and the Python software.

### 1. Prerequisites

* **Hardware:**
    * Arduino board (Uno)
    * 4WD Robot Car Chassis (or similar mobile platform)
    * L298N Motor Driver Module
    * HC-05 or HC-06 Bluetooth Module
    * Power supply for Arduino and motors (e.g., 18650 batteries + holder)
    * Jumper wires
* **Software:**
    * Arduino IDE (for uploading code to the Arduino)
    * Python 3.x (recommended 3.8+)
    * `pip` (Python package installer)

### 2. Arduino Setup

1.  **Navigate to the Arduino Code:**
    Change directory to the Arduino project folder:
    ```bash
    cd Arduino code of the robot prototype
    ```
    *(Note: Ensure your main Arduino sketch file is named `arduino code.ino` within this folder).*

2.  **Open in Arduino IDE:**
    Open the `arduino code.ino` file using the Arduino IDE.

3.  **Install Libraries (if any):**
    If the sketch uses any external libraries (e.g., for specific sensors or motor control), install them via `Sketch > Include Library > Manage Libraries...` in the Arduino IDE. Common libraries might include `SoftwareSerial` (for HC-05/06) or specific motor control libraries.

4.  **Hardware Connections:**
    * Connect the HC-05/HC-06 Bluetooth module's `TX` to Arduino `RX` (e.g., Digital Pin 10), and `RX` to Arduino `TX` (e.g., Digital Pin 11, *use a voltage divider for 5V Arduino to 3.3V Bluetooth RX*).
    * Connect the L298N motor driver to Arduino digital pins for motor control (refer to your specific robot car's wiring diagram).
    * Power the Arduino and motor driver appropriately.

    *(**Important:** Disconnect the Bluetooth module's RX/TX during code upload to avoid interference.)*

5.  **Upload Code:**
    * Select your Arduino Board (`Tools > Board > Arduino Uno/Nano`).
    * Select the correct Port (`Tools > Port`).
    * Click the "Upload" button to flash the code to your Arduino.

### 3. Python Voice Assistant & GUI Setup

1.  **Navigate to the Python Code:**
    Change directory to the Python project folder:
    ```bash
    cd Lina voice assistant GUI/
    ```

2.  **Create a Virtual Environment (Recommended):**
    It's good practice to create a virtual environment to manage dependencies:
    ```bash
    python -m venv venv
    ```
    Activate the virtual environment:
    * On Windows:
        ```bash
        .\venv\Scripts\activate
        ```
    * On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```

3.  **Install Dependencies:**
    Install all required Python libraries using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
    *(If `requirements.txt` is missing, you'll need to create it. Common libraries might include `SpeechRecognition`, `PyAudio`, `pyserial`, `tkinter` (usually built-in), `pyttsx3`.)*

4.  **Configure Bluetooth Port:**
    * Ensure your HC-05/HC-06 Bluetooth module is paired with your PC.
    * Identify the COM Port (Windows) or `/dev/tty` path (macOS/Linux) assigned to your Bluetooth module. You can usually find this in your operating system's device manager or Bluetooth settings.
    * **Open `main.py`** (or relevant configuration file) and **update the `SERIAL_PORT` variable** to match your Bluetooth module's COM port.

5.  **Run the Application:**
    Once dependencies are installed and the port is configured, run the main Python script:
    ```bash
    python main.py
    ```

    This will launch the GUI and activate the voice assistant.

---

## 🌟 Future Vision

Exploring AI-driven multilingual support (Arabic/FR/EN), 360° obstacle detection, and cloud integration to bypass throttling limits. The ultimate goal is to evolve this into a universal voice-control platform adaptable to any domain!

---

## 💬 Let’s Connect!

How could this approach solve challenges in your industry? Drop a comment or DM—I’d love to collaborate or hear your thoughts.

For more information, please visit my LinkedIn and review this post:
[https://www.linkedin.com/posts/dhia-shayeb_dhiashayebprojectreportpdf-activity-7340068522724675584-oN66?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFrTPq8BsAUhmHWHUbuCqXT-g9R2budTmaY](https://www.linkedin.com/posts/dhia-shayeb_dhiashayebprojectreportpdf-activity-7340068522724675584-oN66?utm_source=share&utm_medium=member_desktop&rcm=ACoAAFrTPq8BsAUhmHWHUbuCqXT-g9R2budTmaY)

