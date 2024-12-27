# Unit 2: Communication Methodologies

**2.1 Need for Modulation in Communication System:**
- **Modulation** is the process of varying a carrier signal in order to transmit data over a communication medium.
- The need for modulation arises because:
  - **Signal Strength and Range**: Low-frequency signals (like audio or video) have limited range and cannot travel over long distances. Modulation allows these signals to be carried by high-frequency carriers, improving range.
  - **Antenna Size**: To transmit signals effectively, the size of the antenna is proportional to the wavelength of the signal. Higher frequency signals require smaller antennas, making them more practical for communication systems.
  - **Multiplexing**: Modulation allows multiple signals to be combined and transmitted simultaneously over a single channel (multiplexing), reducing interference and optimizing bandwidth use.

**2.2 Concepts of AM, FM, PM, FSK, TSK, PCM (No Mathematical Model):**
- **AM (Amplitude Modulation)**: The amplitude (strength) of the carrier signal is varied in accordance with the information signal. Commonly used in radio broadcasting.
  
- **FM (Frequency Modulation)**: The frequency of the carrier signal is varied based on the information signal. FM is more resistant to noise than AM and is commonly used in high-fidelity radio broadcasting.

- **PM (Phase Modulation)**: The phase of the carrier signal is varied in accordance with the information signal. PM is closely related to frequency modulation but focuses on changes in phase rather than frequency.

- **FSK (Frequency Shift Keying)**: A form of frequency modulation used in digital communication, where the frequency of the carrier signal changes between a set of discrete frequencies to represent binary data (0s and 1s).

- **TSK (Time Shift Keying)**: Involves the modulation of time intervals to represent data. This is a less common technique compared to other forms of keying like FSK or PSK.

- **PCM (Pulse Code Modulation)**: A method used to digitally represent analog signals by converting the amplitude of the analog signal into a series of coded pulses. This is used in digital audio and telecommunication systems.

**2.3 Concept of Bandwidth and Channel Capacity of Different Communication Systems:**
- **Bandwidth**: The range of frequencies that a communication system can transmit. It is usually measured in Hertz (Hz) and represents the amount of data that can be transmitted in a given time period. Higher bandwidth generally allows faster data transfer.
  
- **Channel Capacity**: The maximum amount of data that can be transmitted over a communication channel. It is determined by factors such as bandwidth, signal-to-noise ratio (SNR), and the modulation technique used. The Shannon-Hartley theorem is often used to calculate the theoretical channel capacity.

- **Communication Systems and Channel Capacity**:
  - **Radio**: The bandwidth in radio communication depends on the frequency band used (e.g., AM radio uses a different bandwidth than FM radio).
  - **Microwave**: Microwaves offer higher bandwidth compared to radio waves and are used in point-to-point communication systems, including satellite communication and data transmission over long distances.
  - **Fiber Optics**: Offers extremely high bandwidth and is used for high-speed internet and telecommunications.
  - **Satellite**: The channel capacity is influenced by the bandwidth of the satellite transponder and the distance between the satellite and the Earth.

**2.4 Multiplexing Techniques:**
- **TDM (Time Division Multiplexing)**: Involves dividing the available bandwidth of a communication channel into time slots. Each signal is assigned a specific time slot during which it can transmit, allowing multiple signals to share the same channel without interference. TDM is used in both analog and digital systems.
  
- **FDM (Frequency Division Multiplexing)**: Involves dividing the bandwidth of the communication channel into several frequency bands. Each signal is assigned a different frequency band to transmit its data, allowing simultaneous transmission of multiple signals over the same channel.
  
- **WDM (Wavelength Division Multiplexing)**: A technique used in fiber optic communication where the available bandwidth is divided into different wavelengths (or channels) of light. Each signal is transmitted at a different wavelength, allowing for high-capacity data transmission over a single fiber optic line.
  
- **CDMA (Code Division Multiple Access)**: A method where multiple signals are transmitted simultaneously on the same frequency band but are differentiated by unique codes. Each signal is encoded with a specific code, and the receiver uses the same code to decode the signal. CDMA is widely used in mobile communications and GPS.