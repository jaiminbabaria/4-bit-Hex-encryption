# 4-Bit Hex Encryption & Decryption

## Project Overview
This project demonstrates the encryption and decryption of a 4-bit hexadecimal message using a **public key** and **private key** infrastructure. The encryption and decryption processes are implemented using digital logic circuits, including encoders, decoders, negation blocks, and binary-to-grey code converters.

The project is divided into two main parts:
1. **1-Bit Encryption-Decryption Model**: A single-bit encryption and decryption circuit.
2. **4-Bit Encryption-Decryption Model**: A scaled-up version of the 1-bit model, capable of handling 4-bit hexadecimal messages.

---

## Features
- **Encryption**:
  - Converts a 4-bit hexadecimal message into encrypted data using a public key and private key.
  - Uses a 16:4 encoder, negation block, binary-to-grey code converter, and private key generator.
- **Decryption**:
  - Decrypts the encrypted data back into the original 4-bit hexadecimal message.
  - Uses a 4:16 decoder, negation block, grey-to-binary code converter, and private key.
- **Scalable Design**:
  - The 1-bit encryption-decryption model is integrated four times to handle 4-bit hexadecimal messages.

---

## Components Used
### Encryption Circuit
- **16:4 Encoder**: Converts hexadecimal input to binary.
- **Negation Block**: Complements the binary input.
- **Binary-to-Grey Code Converter**: Converts binary to grey code.
- **Private Key Generator**: Generates a private key based on the grey code.
- **4-Bit Register**: Stores the private key.
- **XOR Gates**: Used for encryption with the public key.

### Decryption Circuit
- **4:16 Decoder**: Converts binary back to hexadecimal.
- **Negation Block**: Complements the binary output.
- **Grey-to-Binary Code Converter**: Converts grey code back to binary.
- **XOR Gates**: Used for decryption with the public and private keys.

---

## How It Works
### 1-Bit Encryption-Decryption Model
1. **Encryption**:
   - The user sets a public key.
   - A 1-bit hexadecimal input (0-F) is passed through a 16:4 encoder to convert it to binary.
   - The binary input is complemented using a negation block.
   - The complemented binary is converted to grey code.
   - A private key is generated from the grey code and stored in a 4-bit register.
   - The message is XORed with the private key and then with the public key to produce the encrypted data.

2. **Decryption**:
   - The encrypted data is XORed with the public key and then with the private key.
   - The result is converted back to binary using a grey-to-binary converter.
   - The binary is complemented using a negation block.
   - Finally, the binary is passed through a 4:16 decoder to retrieve the original hexadecimal message.

### 4-Bit Encryption-Decryption Model
- The same process as the 1-bit model is applied, but 4 bits are processed simultaneously using a single pair of public and private keys.

---

## Tools and Technologies
- **Digital Logic Design**: Used for designing the encryption and decryption circuits.
- **Simulation Tools**: Logisim

---

## Future Scope
- Expand the project to handle larger bit sizes (e.g., 8-bit or 16-bit encryption).
- Implement the design on an FPGA (Field-Programmable Gate Array) for real-time applications.
- Add a user interface for easier interaction with the encryption and decryption processes.

---

## Contributors
- Jaimin Babaria (https://github.com/jaimimbabaria) - Project Developer

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments
- Special thanks to our guide and mentors for their support and guidance.
- Inspired by cryptographic principles and digital logic design.

---

## How to Use
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/4-Bit-Hex-Encryption-Decryption.git
