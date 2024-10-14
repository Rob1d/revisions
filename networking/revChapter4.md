# Chapter 4 Revision Sheet: Digital Transmission (Part 1)

## Digital to Digital Conversion

### Key Concepts

- **Digital Signals**: Both data and signals can be digital or analog. Digital data can be represented by digital signals.
- **Line Coding**: The process of converting digital data (e.g., text, numbers, audio, etc.) into digital signals.

### Definitions
- **Data Element**: The smallest unit of information (the bit) that can represent digital data.
- **Signal Element**: The unit of a digital signal that carries data elements over time.

#### Key Ratios
- **Ratio (r)**: Number of data elements per signal element.
- **Data Rate (N)**: Number of data elements sent per second (bps).
- **Signal Rate (S)**: Number of signal elements sent per second (baud).

### Important Concepts

1. **Baseline Wandering**: A phenomenon where a long sequence of continuous 0s or 1s causes the receiver's baseline (a running average of received signal power) to drift, complicating the decoding process.
   
2. **DC Components**: A consistent voltage level over time that can introduce very low frequencies into a digital signal, which is problematic in certain transmission mediums (like telephone lines that filter below 200 Hz).

3. **Self-Synchronization**: Important for ensuring that the bit intervals at the receiver match those of the sender, aiding in proper signal interpretation.

### Line Coding Schemes

- **Unipolar Encoding**: All signal levels are on one side of the time axis (e.g., NRZ: Non-Return-to-Zero).
  
- **Polar Encoding**: Signal levels exist on both sides of the time axis, with the potential introduction of two distinct voltage levels to represent binary data (e.g., NRZ-L and NRZ-I).

- **Return-to-Zero (RZ)**: Utilizes three signal levels—positive, negative, and zero. The signal returns to zero in the middle of the bit time, though it requires more bandwidth due to increased signal changes.

- **Biphase Encoding (e.g., Manchester)**:
  - **Manchester Encoding**: Transition occurs in the middle of each bit, aiding synchronization.
  - **Differential Manchester**: Transition at the middle of the bit, with values determined based on previous bits.

- **Bipolar Schemes**: Involves three voltage levels (positive, negative, and zero), specifically through a method called Alternate Mark Inversion (AMI).

### Potential Exam Questions

1. Explain what is meant by baseline wandering and how it affects digital transmission.
2. What problems do DC components cause in digital signals, and how can they be mitigated?
3. Describe the differences between the various encoding techniques discussed, noting their advantages and disadvantages.
4. What is the significance of self-synchronization in digital signal transmission?

### Diagrams and Illustrations
- [Include diagrams that visualize line coding, different encoding schemes, and the characteristics of signals over time.]

### Study Tips
- Familiarize yourself with the characteristics and applications of each line coding scheme for better retention.
- Practice encoding and decoding examples to internalize how different coding techniques affect data transmission.
- Review definitions and key concepts regularly to reinforce understanding.

# Chapter 4 Revision Sheet: Digital Transmission (Part 3)

## Analog to Digital Conversion

### Key Concepts

- **Analog to Digital Conversion (ADC)**: The process of converting an analog signal (e.g., from a microphone or camera) into a digital signal.
- **Pulse Code Modulation (PCM)**: The most common technique for digitizing an analog signal. It involves three main steps:
  1. **Sampling**: The analog signal is sampled at regular intervals.
  2. **Quantization**: The sampled values are converted into discrete levels.
  3. **Encoding**: The quantized values are translated into binary code.

### Pulse Code Modulation (PCM)

1. **Sampling**:
   - The signal is sampled over time, with the sampling period denoted by \( T_s \).
   - The sampling frequency \( f_s \) must be at least twice the highest frequency of the original signal (Nyquist Theorem).
   - Types of sampling methods:
     - Ideal Sampling
     - Natural Sampling
     - Flat-Top Sampling

2. **Quantization**:
   - The infinite range of signal amplitudes is divided into quantization levels, often denoted as \( L \).
   - The choice of levels affects the precision of the representation. Lower levels can increase quantization error.

3. **Quantization Error**:
   - The difference between the actual amplitude and the quantized value creates an approximation error.

### Delta Modulation (DM)

- **Delta Modulation**: A simpler alternative to PCM that encodes only the change between samples instead of the absolute sample value.
  - **Modulator**: Records the direction of the change (positive or negative) and represents it as binary 1 or 0.
  - **Demodulator**: Reconstructs the analog signal by using a staircase approximation based on recorded changes.

### Transmission Modes

- **Parallel Transmission**: Multiple bits are sent simultaneously, requiring more wires but resulting in higher speeds.
- **Serial Transmission**: Bits are transmitted sequentially over a single channel.

#### Types of Serial Transmission:
1. **Asynchronous**:
   - Each byte is preceded by a start bit and followed by stop bits. Timing is not tightly controlled.
   - The Start bit alerts the receiver to the arrival of new data.

2. **Synchronous**:
   - Data is sent continuously with a consistent timing mechanism.
   - Often utilizes frames for grouping bits.

3. **Isochronous**:
   - Guarantees data arrives at predefined intervals, crucial for real-time audio and video applications.

### Potential Exam Questions

1. Explain the steps involved in Pulse Code Modulation (PCM) and the importance of each step.
2. Discuss the advantages and disadvantages of delta modulation compared to PCM.
3. What are the differences between asynchronous, synchronous, and isochronous transmission?
4. Define the Nyquist theorem and its relevance to sampling rates in analog to digital conversion.

### Diagrams and Illustrations
- [Include diagrams illustrating the sampling process in PCM, the concept of quantization, and the differences across various transmission modes.]

### Study Tips
- Create flowcharts to visualize the processes of PCM and delta modulation.
- Practice calculating the required sampling frequency using the Nyquist theorem with different scenarios.
- Discuss examples of serial and parallel transmission to solidify understanding of their applications and trade-offs.

# Chapter 4 Revision Sheet: Digital Transmission (Part 3)

## Analog to Digital Conversion

### Key Concepts

- **Analog to Digital Conversion (ADC)**: The process of converting an analog signal (e.g., from a microphone or camera) into a digital signal.
- **Pulse Code Modulation (PCM)**: The most common technique for digitizing an analog signal. It involves three main steps:
  1. **Sampling**: The analog signal is sampled at regular intervals.
  2. **Quantization**: The sampled values are converted into discrete levels.
  3. **Encoding**: The quantized values are translated into binary code.

### Pulse Code Modulation (PCM)

1. **Sampling**:
   - The signal is sampled over time, with the sampling period denoted by \( T_s \).
   - The sampling frequency \( f_s \) must be at least twice the highest frequency of the original signal (Nyquist Theorem).
   - Types of sampling methods:
     - Ideal Sampling
     - Natural Sampling
     - Flat-Top Sampling

2. **Quantization**:
   - The infinite range of signal amplitudes is divided into quantization levels, often denoted as \( L \).
   - The choice of levels affects the precision of the representation. Lower levels can increase quantization error.

3. **Quantization Error**:
   - The difference between the actual amplitude and the quantized value creates an approximation error.

### Delta Modulation (DM)

- **Delta Modulation**: A simpler alternative to PCM that encodes only the change between samples instead of the absolute sample value.
  - **Modulator**: Records the direction of the change (positive or negative) and represents it as binary 1 or 0.
  - **Demodulator**: Reconstructs the analog signal by using a staircase approximation based on recorded changes.

### Transmission Modes

- **Parallel Transmission**: Multiple bits are sent simultaneously, requiring more wires but resulting in higher speeds.
- **Serial Transmission**: Bits are transmitted sequentially over a single channel.

#### Types of Serial Transmission:
1. **Asynchronous**:
   - Each byte is preceded by a start bit and followed by stop bits. Timing is not tightly controlled.
   - The Start bit alerts the receiver to the arrival of new data.

2. **Synchronous**:
   - Data is sent continuously with a consistent timing mechanism.
   - Often utilizes frames for grouping bits.

3. **Isochronous**:
   - Guarantees data arrives at predefined intervals, crucial for real-time audio and video applications.

### Potential Exam Questions

1. Explain the steps involved in Pulse Code Modulation (PCM) and the importance of each step.
2. Discuss the advantages and disadvantages of delta modulation compared to PCM.
3. What are the differences between asynchronous, synchronous, and isochronous transmission?
4. Define the Nyquist theorem and its relevance to sampling rates in analog to digital conversion.

### Diagrams and Illustrations
- [Include diagrams illustrating the sampling process in PCM, the concept of quantization, and the differences across various transmission modes.]

### Study Tips
- Create flowcharts to visualize the processes of PCM and delta modulation.
- Practice calculating the required sampling frequency using the Nyquist theorem with different scenarios.
- Discuss examples of serial and parallel transmission to solidify understanding of their applications and trade-offs.