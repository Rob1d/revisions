# Chapter 1 Revision Sheet

## Digital to Digital Conversion

### Key Concepts

- **Digital Signals**: Represent data in either digital or analog form. Digital data converted into digital signals for transmission.
- **Line Coding**: The process of converting digital data into digital signals.
  - Involves encoding bits into electrical signals for transmission.

### Line Coding Schemes

#### 1. **Unipolar Scheme**
- All signal levels on one side of the time axis.
- **NRZ (Non-Return-to-Zero)**: Positive voltage denotes bit 1; a zero voltage denotes bit 0.

#### 2. **Polar Scheme**
- Signal voltages on both sides of the time axis.
- Variants:
  - **NRZ-L (Level)**: Voltage level represents the bit value.
  - **NRZ-I (Invert)**: Changes or lack of changes dictate the bit value.

#### 3. **Return-to-Zero (RZ)**
- Uses three values: positive, negative, and zero.
- Signal returns to zero in the middle of each bit.
- Requires greater bandwidth due to two changes per bit.

#### 4. **Biphase Coding**
- **Manchester Encoding**: 
  - Voltage level shifts in the middle of the bit to maintain synchronization.
  - Signal rate doubles that of NRZ.
- **Differential Manchester**: 
  - Always transitions in the middle of the bit; bit value determined at the beginning.
  
#### 5. **Bipolar Schemes**
- Involve three voltage levels: positive, negative, and zero.
- **Bipolar Alternate Mark Inversion (AMI)**:
  - Zero voltage indicates bit 0; binary 1s alternate between positive and negative voltages.

### Important Considerations
- **Baseline Wandering**: A long sequence of bits (especially zeros) can lead to receiver misinterpretation due to the drift in the baseline reference.
- **DC Components**: Adapt line coding schemes to avoid constant voltage levels over time, which can lead to misinterpretations by receivers.

## Potential Exam Questions

1. What are the main differences between NRZ-L and NRZ-I encoding methods?
2. Explain the advantages and disadvantages of the Manchester encoding scheme.
3. Describe the AMI encoding method and its synchronization issues.
4. Define baseline wandering and discuss its impact on digital signal transmission.

## Diagrams and Illustrations
- [Include diagrams of different line coding schemes, signal transitions in Manchester and Differential Manchester, and examples of bipolar encoding.)

## Study Tips
- Focus on understanding the advantages and disadvantages of each line coding scheme.
- Practice drawing the waveforms for different encoding methods to visualize how they are represented over time.
- Test yourself with the potential exam questions and try explaining concepts aloud or to a study partner.

# Chapter 2 Revision Sheet

## Network Models

### Key Concepts

- **Protocol**: Rules that govern communication between sender, receiver, and intermediary devices.
- **Protocol Layering**: Division of communication tasks into layers, where each layer has specific functions and communicates with the layers above and below it.
  
#### Principles of Protocol Layering
1. **Two Opposite Tasks**: Each layer should perform tasks in both transmitting and receiving directions.
2. **Logical Connections**: Communication appears as though there is a direct connection at each layer.

### TCP/IP Protocol Suite

- **Transmission Control Protocol/Internet Protocol (TCP/IP)**: A set of protocols used for the Internet which is organized in a layered architecture.
- **Layer Functions**:
  - **Application, Transport, Network Layers**: Handle end-to-end communication.
  - **Data Link, Physical Layers**: Handle hop-to-hop communication across devices.
  
- **Encapsulation and Decapsulation**: The processes of wrapping and unwrapping protocols around data as it travels through the layers.

### Addressing in Networks
- Every communication requires a source and destination address.
- Physical layer does not require any addressing; it only deals with bits.

## Potential Exam Questions

1. Explain the importance of protocol layering in network communication.
2. Describe the functions of each layer in the TCP/IP protocol suite.
3. What are the processes of encapsulation and decapsulation? Provide examples.
4. How does addressing work in network models, particularly within the TCP/IP framework?

## Diagrams and Illustrations
- [Include a diagram illustrating the TCP/IP model layers and describing the duties of each layer.]
- [Include an illustration of encapsulation/decapsulation processes.]

## Study Tips
- Create flashcards for each layer of the TCP/IP suite and their respective functions.
- Practice drawing the layered model and the relationships between layers.
- Discuss potential exam questions with peers to enhance understanding and retention of the material.