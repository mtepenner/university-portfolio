## **Lab 1 Reflection: Firmware Flashing & Radio Testing**

### **1. Hardware Troubleshooting**
Initial attempts to test the board led to some concern regarding the quality of my solder joints. However, after a thorough inspection, I identified the culprit: a faulty USB-C cable. Swapping the cable resolved the power issues and confirmed that the board's physical connections were sound.

<div style="display: flex; gap: 10px; align-items: center;">
  <img src="download.png" alt="Hardware suspicion" style="width: 15%; height: auto;" />
  <img src="bigbrain.png" alt="Cable solution" style="width: 15%; height: auto;" />
</div>

### **2. Flashing Challenges: Security Constraints**
The primary hurdle during the software phase was an environmental one. My work laptop, which I use for class, employs strict security protocols that mount all USB devices as **read-only**. This prevented me from flashing the necessary software to the microcontroller.

<img src="trigger.png" alt="USB frustration" style="width: 15%; height: auto; display: block; margin-top: 10px;" />

### **3. Peer Testing and Radio Verification**
To bypass the security restrictions, I collaborated with a fellow student and utilized her machine for the flashing process. During the partner testing phase, we successfully verified the radio's functionality:
* **Transmitting:** When pressing the "Boot" button on my radio, the indicator light on the peer device responded immediately.
* **Consistency:** We swapped roles and observed identical results, confirming that both radios were communicating effectively.

<img src="20251015_140515.jpg" alt="Successful test" style="width: 15%; height: auto; display: block; margin-top: 10px;" />

### **4. Terminal Output and Packet Validation**
When my device was configured as the receiver, I successfully captured incoming data. The terminal output confirmed that packets were being received and parsed correctly by the system.

<img src="Screenshot_from_2025-10-20_13-16-04.png" alt="Terminal reception" style="width: 25%; height: auto; display: block; margin-top: 10px;" />

### **5. Final Logic Test (October 20th)**
On Monday, I performed a final validation by swapping the receiver and sender code. By spamming the boot button, I confirmed that other computers in the lab were receiving my packets. While my personal machine had difficulty displaying the "Send Success" confirmation in the terminal—likely due to the aforementioned driver or security restrictions—the connection was verified through the system's hardware interface.

<img src="Screenshot_from_2025-10-20_13-54-40.png" alt="Connection verified" style="width: 25%; height: auto; display: block; margin-top: 10px;" />

