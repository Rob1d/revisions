
# Part One

## 1. Basics of Data Transmission

Definition: The process of sending digital or analog data signals between two or more devices across a network medium.
### Types:

Digital Transmission: Discrete signals are used (e.g., binary 0s and 1s).
Analog Transmission: Continuous signals are used (e.g., sound waves).

## 2. Transmission Modes

### Simplex:

Definition: One-way communication.
Example: Television broadcasting where the signal flows from the station to the viewer.

### Half-Duplex:

Definition: Two-way communication but only one direction at a time.
Example: Walkie-talkies; users cannot speak and listen simultaneously.

### Full-Duplex:

Definition: Two-way communication simultaneously.
Example: Telephone conversations, both parties can speak and listen at the same time.

## 3. Transmission Medium

### Wired Media:

Twisted Pair Cable: Commonly used for Ethernet networks; copper wires twisted into pairs.
Coaxial Cable: Used for cable television; provides better shielding from interference.
Fiber Optic Cable: Uses light to transmit data, offering higher bandwidth and longer distances.

### Wireless Media:

Radio Waves: Used in Wi-Fi and mobile networks.
Microwaves: Utilized in point-to-point communication links.
Infrared: Used in remote controls and some short-range communications.

## 4. Signal Transmission Techniques

### Modulation:

Purpose: Encoding information into a carrier wave for transmission.
Types:

Amplitude Modulation (AM): Modifies the amplitude of the carrier wave.
Frequency Modulation (FM): Alters the frequency of the carrier wave.
Phase Modulation (PM): Changes the phase of the carrier wave.

### Multiplexing:

Purpose: Combining multiple signals over a single medium.
Types:
Frequency Division Multiplexing (FDM): Multiple signals are assigned different frequencies.
Time Division Multiplexing (TDM): Different signals share the same frequency but are assigned unique time slots.
Wavelength Division Multiplexing (WDM): Used in fiber optics; different data streams transmit light at different wavelengths.

## 5. Signal Quality Considerations

### Noise: 
Unwanted interference that distorts the signal.

Example: Electrical appliances causing static on a radio.

### Attenuation:
Signal loss over distance.

Example: A signal becoming weaker as it travels over long stretches of cable.

### Distortion:
Alteration of the original signal shape.

Example: Echo on phone lines.
### 6. Error Detection and Correction

Purpose: Ensures data integrity in transmission.
Techniques:
### Parity Check:
Adds a parity bit to the data for error detection.

### Checksums:
Generates a value from the data set; checked at the receiver for consistency.

### Cyclic Redundancy Check (CRC):
More robust than checksums and widely used in network communication.


# Chap one revised

## 1. Understanding Data Transmission
Definition: The delivery of data and information via signals across a communication channel.

## 2. Transmission Types

### Serial Transmission:

Definition: Data bits are sent sequentially over the same channel.
Example: USB (Universal Serial Bus) connections transfer data serially.

### Parallel Transmission:

Definition: Multiple data bits are transmitted simultaneously across multiple channels.
Example: Older printer cables (Centronics connection) used parallel transmission.

## 3. Signal Encoding Methods

### Unipolar Encoding:

Definition: Uses a single voltage level to represent binary data.
Example: A 5V level represents a '1', while 0V represents a '0'.

### Polar Encoding:

Definition: Uses two voltage levels above and below a zero line.
Example: NRZ (Non-Return to Zero) and RZ (Return to Zero) are examples.

### Bipolar Encoding:

Definition: Uses three voltage levels: positive, negative, and zero.
Example: AMI (Alternate Mark Inversion) encodes '0' as 0V and alternates '1' between positive and negative voltages.

## 4. Factors Affecting Transmission

### Bandwidth:

Definition: The range of frequencies a transmission medium can support.
Example: Fiber optic cables offer higher bandwidth than copper cables.

### Noise:

Definition: Random electrical signals that interfere with data transmission.
Reduction Techniques: Shielded cables, twisted pairs, filtering.

## 5. Data Rate vs. Signal Rate

### Data Rate:

Definition: Number of data bits transmitted per second (bps).
Example: A data rate of 1 Mbps indicates 1 million bits transmitted per second.

### Signal Rate:

Definition: Number of signal elements transmitted per second.
Relates to Baud Rate: Where Baud rate measures the number of signal units.

## 6. Transmission Impairments

### Attenuation:

Definition: Gradual loss of signal strength as it travels over the medium.
Example: Fiber optic repeaters counteract attenuation by amplifying the signal.

### Distortion:

Definition: Any change in the form or shape of the signal.
Example: Echo on a phone line is a form of distortion.

### Latency:

Definition: Delay before a transfer of data begins following an instruction for its transfer.
Example: Satellite communications often have higher latency due to distance.

## 7. Error Detection Mechanisms

### Parity Bits:

Purpose: Error detection by counting the number of set bits.
Types: Even parity and odd parity.

### Checksum:

Purpose: A simple way to check integrity by summing up the data units.
Example: Used in IP and TCP protocols.

### Cyclic Redundancy Check (CRC):

# Chapter 2 & rev2

## 1. Advanced Transmission Techniques

### Pulse Code Modulation (PCM):

Definition: Method of converting an analog signal into a digital signal.
Steps: Sampling, Quantizing, and Encoding.
Example: Commonly used in digital telephony and audio recordings.

### Differential Manchester Encoding:

Definition: A method of encoding where the presence of a transition denotes a binary '0' or '1'.
Uses: Ensures clock synchronization by guaranteeing a transition every bit period.

## 2. Line Configuration

### Point-to-Point Configuration:

Definition: Direct link between two devices.
Example: Connecting two computers using a single Ethernet cable.

### Multipoint Configuration:

Definition: Multiple devices share a single link.
Example: Multiple devices connected on a bus topology network.

## 3. Synchronization

### Synchronous Transmission:

Definition: Blocks of data are sent at regular intervals.
Example: Used in high-speed data transfer systems like mainframe computers.

### Asynchronous Transmission:

Definition: Data is sent at irregular time intervals.
Example: Keyboards and mouse devices typically use asynchronous transmission.

## 4. Flow Control Mechanisms

### Stop-and-Wait:

Definition: Sender waits for an acknowledgment after every message before sending the next.
Impact: Simple but inefficient for long-distance or high-speed networks.

### Sliding Window Protocol:

Definition: Allows multiple packets to be sent before needing an acknowledgment.
Example: Used in TCP (Transmission Control Protocol) for efficient and reliable data transfer.

## 5. Error Control Techniques

### Automatic Repeat reQuest (ARQ):

Types:
Stop-and-Wait ARQ: Retransmits every packet until acknowledgment.
Go-Back-N ARQ: Sender transmits several packets but can only deal with the next acknowledgment.
Selective Repeat ARQ: Only the erroneous packets are resent, improving efficiency.

## 6. Transmission Media Characteristics

### Throughput:

Definition: Actual rate at which bits are sent over a network.
Factors: Affected by network traffic and error rates.

### Propagation Speed:

Definition: Speed at which a signal travels through a medium.
Example: Generally, light speed in fiber optics, slower in electrical wires.

### Propagation Time:

Formula: Distance / Propagation speed.

## 7. Bandwidth Utilization

Time Division Multiplexing (TDM):

Definition: Divides time into slots and allocates each slot to different signals.
Example: Used in digital telephony.

### Frequency Division Multiplexing (FDM):

Definition: Different signals are transmitted over different frequency bands.
Example: Analog television broadcasting.

### Statistical Time Division Multiplexing (STDM):

Definition: Dynamically allocates time slots based on demand.
Advantage: More efficient than standard TDM.
