---

# Smart Light Bulb Security Analysis

## Overview

This repository contains the research and findings from our project on **Smart Light Bulb Security Analysis**, conducted at Carnegie Mellon University. The study explores the security vulnerabilities in smart light bulbs from various brands, including Philips, Merkury, and Cync, using comprehensive static and dynamic analysis methods.

The goal of this project is to identify security weaknesses, assess their impact, compare the security postures across brands and price ranges, and provide actionable recommendations to improve IoT security standards.

---

## Key Features

- **Static Analysis Tools**: 
  - Merkury: DeGuard, MobSF
  - Cync: APKLab, MobSF, Ghidra
  - Philips Hue: APKdeguard, JADX, dex2jar, JD-GUI

- **Dynamic Analysis Tools**:
  - Merkury: BurpSuite, WireShark
  - Cync: WireShark, custom scripts
  - Philips Hue: Frida for code injection

- **Testing Highlights**:
  - Reverse engineering smart bulb applications.
  - Analyzing network traffic to uncover vulnerabilities.
  - Identifying insecure cryptographic implementations and permissions misuse.
  - Exploring security differences across brands and price points.

---

## Findings

1. **Merkury**:
   - Hardcoded secrets and encryption vulnerabilities.
   - Insecure WebView implementations prone to MITM attacks.
   - Use of ESP32 hardware with exploitable vulnerabilities.

2. **Cync**:
   - Weak cryptographic algorithms (e.g., use of MD5 and AES ECB mode).
   - Deprecated library usage (e.g., `memcpy` and `memalign` leading to buffer and heap overflow risks).
   - Support for outdated SSL/TLS protocols.

3. **Philips Hue**:
   - Misuse of permissions (e.g., undocumented camera permissions).
   - Use of deprecated hashing algorithms (MD5, SHA-1).
   - Proper brightness boundary controls.

---

## Challenges

- Geographic separation across Pittsburgh and Silicon Valley.
- Limited prior experience in hacking and mobile security systems.
- High learning curve for understanding IoT security systems.

---

## Tools and Frameworks

- **Static Analysis**: DeGuard, MobSF, APKLab, Ghidra, JADX, dex2jar, JD-GUI
- **Dynamic Analysis**: Frida, BurpSuite, WireShark
- **Hardware**: Rooted Google Pixel devices for deeper analysis.

---

## Recommendations

- Strengthen cryptographic implementations (replace MD5 and weak AES modes).
- Securely manage secrets by avoiding hardcoded keys.
- Implement proper SSL certificate validation.
- Regularly audit app permissions to ensure compliance with privacy policies.
- Foster collaboration between consumers, manufacturers, and regulators for continuous IoT security improvement.

---

## Future Work

- Develop proof-of-concept exploits for identified vulnerabilities.
- Conduct further analysis on firmware and additional reverse engineering.
- Expand testing to other IoT devices to generalize findings.

---

## Contributors

- **Aayush Dhanotiya**  
  Heinz College, CMU   

- **Supriya Nittoor**  
  Heinz College, CMU  

- **Nicholas Park**  
  INI, CMU  

- **Wendy Chen**  
  ECE, CMU   

- **Sterling McTee**  
  Heinz College, CMU  

---

## Acknowledgments

Special thanks to **Professor Patrick Tague** for his invaluable guidance and support, as well as our peers for their constructive feedback and encouragement throughout the project.

---
