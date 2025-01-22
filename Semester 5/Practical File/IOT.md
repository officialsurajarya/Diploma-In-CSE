## **Practical 1: Installation of Arduino IDE**

---

#### **Aim**
The aim of this practical is to demonstrate the steps involved in installing the **Arduino Integrated Development Environment (IDE)**, which is used for writing and uploading code to Arduino boards.

#### **Introduction**
The **Arduino IDE** is a cross-platform application used to write and upload programs (known as sketches) to an Arduino board. It supports various programming languages like **C** and **C++**, making it easy to interface with different sensors, actuators, and other hardware.

---

### **Steps to Install Arduino IDE**

#### **Step 1: Download the Arduino IDE**
1. **Go to the Official Arduino Website**:
   - Open a web browser and visit the official Arduino website: [https://www.arduino.cc/](https://www.arduino.cc/).
  
2. **Navigate to the Download Section**:
   - On the Arduino homepage, click on the **"Software"** tab located in the top menu.
   - In the dropdown menu, select **"Download the Arduino IDE"**.

3. **Select Your Operating System**:
   - The website will show download options for different operating systems:
     - **Windows**
     - **Mac OS**
     - **Linux**
   - Choose the appropriate version based on your operating system.

#### **Step 2: Install Arduino IDE on Windows**
1. **Download the Windows Installer**:
   - Click on the **Windows** option to download the executable file.
  
2. **Run the Installer**:
   - Once the file is downloaded, locate the installer file (typically `arduino-x.x.x-windows.exe`).
   - Double-click to launch the installation process.

3. **Follow the Installation Wizard**:
   - Accept the License Agreement.
   - Choose the installation folder or leave it as default.
   - Choose whether to install additional drivers (USB drivers for Arduino boards).
   - Click **"Install"** to proceed.
   - Once the installation is complete, click **"Close"**.

4. **Launch the Arduino IDE**:
   - After installation, locate the **Arduino IDE** from the **Start menu** or the desktop shortcut and launch it.

#### **Step 3: Install Arduino IDE on macOS**
1. **Download the macOS Installer**:
   - Select the **Mac OS** version of the Arduino IDE and download the `.dmg` file.

2. **Install the Arduino IDE**:
   - Open the `.dmg` file and drag the **Arduino** application into the **Applications** folder.

3. **Launch the Arduino IDE**:
   - Go to the **Applications** folder, find the **Arduino IDE**, and double-click to open it.

#### **Step 4: Install Arduino IDE on Linux**
1. **Download the Linux Version**:
   - Select the **Linux** option for your distribution (32-bit or 64-bit).
   - Download the compressed `.tar.xz` file.

2. **Extract and Install**:
   - Extract the contents of the `.tar.xz` file.
   - Open a terminal and navigate to the extracted folder.
   - Run the `install.sh` script to install the Arduino IDE.

3. **Launch the Arduino IDE**:
   - Once installed, you can launch the Arduino IDE from the terminal or through your system’s application menu.

---

### **Step 5: Setup the Arduino IDE**
1. **Select Your Arduino Board**:
   - Connect your Arduino board (such as **Arduino Uno**) to your computer via USB.
   - Open the Arduino IDE.
   - Go to **Tools > Board** and select the appropriate board type (e.g., **Arduino Uno**).

2. **Select the Serial Port**:
   - Go to **Tools > Port** and select the port to which your Arduino is connected (e.g., COM3 on Windows or `/dev/ttyUSB0` on Linux).

3. **Install Drivers (if necessary)**:
   - If you are using Windows, make sure the necessary drivers for your Arduino board are installed. These drivers are typically included in the IDE installation, but in some cases, you might need to manually install them.

---

### **Step 6: Verify the Installation**
1. **Test the Installation**:
   - To verify that everything is set up correctly, open the **"Blink"** example from the Arduino IDE:
     - Go to **File > Examples > 01.Basics > Blink**.
     - This program makes the built-in LED on the Arduino board blink on and off.
   
2. **Upload the Sketch**:
   - Click on the **Upload** button (the right arrow icon) in the IDE. The sketch will compile and upload to the Arduino board.
   - If successful, the LED on the board will start blinking, confirming that the installation was successful.

---


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>





## **Practical 2: Interfacing Light Emitting Diode (LED) - Blinking LED**

---

#### **Aim**
To interface an **LED (Light Emitting Diode)** with an **Arduino** board and blink the LED using a simple code.

#### **Introduction**
An **LED** is a semiconductor device that emits light when current flows through it in the forward direction. It is often used as an indicator in various electronic projects. In this practical, we will interface an LED with an Arduino board and write a simple program to make it blink. The blinking of the LED will be achieved by turning it ON and OFF at regular intervals.

---

### **Required Components**
1. **Arduino Board** (e.g., Arduino Uno)
2. **LED** (Light Emitting Diode)
3. **Resistor** (220 ohms)
4. **Breadboard** (Optional)
5. **Jumper Wires**

---

### **Circuit Diagram**

Below is the circuit diagram that demonstrates how to interface an LED with an Arduino. The LED is connected to **Pin 13** (digital output pin) of the Arduino board, with a current-limiting resistor (220 ohms) in series to prevent the LED from burning out due to excess current. The negative terminal of the LED is connected to the **ground (GND)** pin of the Arduino.

---

### **Steps for Interfacing LED with Arduino**
1. **Connect the Components**:
   - Connect the **anode (longer leg)** of the LED to **Pin 13** on the Arduino board.
   - Connect the **cathode (shorter leg)** of the LED to **GND** (ground) on the Arduino board.
   - Place a **220-ohm resistor** between Pin 13 and the anode of the LED to limit the current flowing through the LED.

2. **Write the Code**:
   Open the **Arduino IDE** and write the following code to make the LED blink.

---

### **Arduino Code:**

```cpp
void setup() {
  pinMode(13, OUTPUT);  // Set Pin 13 as output
}

void loop() {
  digitalWrite(13, HIGH);  // Turn LED on
  delay(1000);              // Wait for 1 second
  digitalWrite(13, LOW);   // Turn LED off
  delay(1000);              // Wait for 1 second
}
```

#### **Explanation of the Code**:
1. **`pinMode(13, OUTPUT);`**: This line sets **Pin 13** as an output pin, which is where the LED is connected.
2. **`digitalWrite(13, HIGH);`**: This turns the LED on by supplying **5V** to Pin 13.
3. **`delay(1000);`**: This introduces a delay of **1000 milliseconds (1 second)**, keeping the LED on for 1 second.
4. **`digitalWrite(13, LOW);`**: This turns the LED off by setting Pin 13 to **LOW**, i.e., 0V.
5. **`delay(1000);`**: Another 1-second delay, keeping the LED off for 1 second.

---

### **Upload and Test the Program**
1. Connect your Arduino board to your computer via a **USB cable**.
2. Open the **Arduino IDE**, paste the code, and click on the **Upload** button (the arrow icon).
3. After the code is successfully uploaded, the LED connected to Pin 13 should start blinking, turning ON for 1 second and OFF for 1 second repeatedly.

<img src="arduino.jpg" alt="Arduino" width="500" />






Here is the rewritten document in a sequential and accurate manner:

---
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


### Practical No: 3  
**AIM:** Interfacing button and LED: LED blinking when the button is pressed.  

**Requirements:**  
- 1x Breadboard  
- 1x LED  
- 1x Button  
- 1x Resistor  
- 6x Jumper wires  

**Procedure:**  
1. Place the LED and button on the breadboard.  
2. Connect the positive terminal of the LED to the digital pin 13 of the Arduino board (output) and the negative terminal to the ground (GND) of the Arduino.  
3. Connect one terminal of the button to the digital pin 2 of the Arduino (input) and the other terminal to the 5V power pin.  
4. Connect one terminal of the resistor to the digital pin 2 and the other terminal to GND (Arduino).  
5. Connect the Arduino board to a laptop or PC using a USB cable.  
6. Write and upload the following program in the Arduino IDE, then check the output.  

**Program Code:**  
```cpp
const int BUTTON = 2;  // Pin number for the button
const int LED = 13;    // Pin number for the LED
int BUTTONState = 0;   // Variable to store button state

void setup() {
  pinMode(BUTTON, INPUT);  // Set the button pin as input
  pinMode(LED, OUTPUT);    // Set the LED pin as output
}

void loop() {
  BUTTONState = digitalRead(BUTTON);  // Read the button state and store it in BUTTONState

  if (BUTTONState == HIGH) {  // If the button is pressed
    digitalWrite(LED, HIGH);  // Turn the LED on
  } else {
    digitalWrite(LED, LOW);   // Turn the LED off
  }
}
```

---
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>







### Practical No: 4  
**AIM:** Interfacing Light Dependent Resistor (LDR) and LED for an automatic light lamp.  

**Requirements:**  
- 1x LED  
- 1x 220 Ω Resistor  
- 1x 10 kΩ Resistor  
- 1x Breadboard  
- 6x Jumper wires  

**Theory:**  
An LDR (Light Dependent Resistor) changes its resistance based on the intensity of light falling on it. In the dark, its resistance is high (up to several mega-ohms), whereas in the light, its resistance is low (a few hundred ohms). This behavior is due to the photons giving energy to electrons in the semiconductor, enabling current conduction.  

**Procedure:**  
1. Place the LDR and LED on the breadboard.  
2. Connect one terminal of the LDR to the 5V power pin and the other terminal to analog pin A0 of the Arduino. Also, connect the other terminal of the resistor to ground.  
3. Write the following program in the Arduino IDE.  
4. Connect the Arduino to a laptop or PC and upload the program. Verify the output.  

**Program Code:**  
```cpp
int ldr = A0;   // Set A0 (Analog Input) for LDR
int value = 0;  // Variable to store LDR value

void setup() {
  Serial.begin(9600);  // Start serial communication
  pinMode(3, OUTPUT);  // Set pin 3 as output (LED control)
}

void loop() {
  value = analogRead(ldr);  // Read the value from the LDR
  Serial.println("LDR value is:");
  Serial.println(value);    // Print the LDR value to Serial Monitor

  if (value < 300) {
    digitalWrite(3, HIGH);  // Turn on LED when it's dark
  } else {
    digitalWrite(3, LOW);   // Turn off LED when it's bright
  }
  delay(100);  // Optional delay for stability
}
```  

**Behavior:**  
- When there is light on the LDR, the LED turns off.  
- When there is no light, the LED turns on.  

---
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

### Practical No: 5  
**AIM:** Interfacing Temperature Sensor (LM35).  

**Requirements:**  
- Temperature Sensor (LM35)  
- LCD Display  
- 1x Resistor  
- 1x Breadboard  
- 1x Arduino  

**Theory:**  
The LM35 is a temperature sensor with a range of -55°C to 150°C. It provides an analog voltage output proportional to the temperature. This voltage is converted to digital form using an ADC for microcontroller processing.  

**Procedure:**  
1. Connect the temperature sensor to the Arduino board:  
   - GND pin of the sensor to ground on the Arduino.  
   - VCC pin of the sensor to the 5V power pin of the Arduino.  
   - VOUT pin of the sensor to analog pin A1 of the Arduino.  
2. Write the following program in the Arduino IDE.  
3. Upload the program to the Arduino and observe the output.  

**Program Code:**  
```cpp
const int lm35_pin = A1;  // LM35 output pin connected to A1

void setup() {
  Serial.begin(9600);  // Start serial communication
}

void loop() {
  int temp_adc_val;    // Variable to store raw ADC value
  float temp_val;      // Variable to store temperature in Celsius

  temp_adc_val = analogRead(lm35_pin);  // Read the analog value from LM35
  
  temp_val = temp_adc_val * 4.88;       // Convert ADC value to voltage (assuming 5V reference)
  temp_val = temp_val / 10;             // LM35 provides 10mV per degree Celsius

  Serial.print("Temperature = ");
  Serial.print(temp_val);
  Serial.println(" Degree Celsius");

  delay(1000);  // Wait for 1 second before next reading
}
```

**Result:**  
- Example output on Serial Monitor:  
  ```
  Temperature: 29°C  
  Temperature: 28°C  
  Temperature: 27.8°C  
  ```

---

Let me know if further refinements are required!