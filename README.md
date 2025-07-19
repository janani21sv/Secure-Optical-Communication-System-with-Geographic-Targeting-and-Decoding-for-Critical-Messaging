# Secure-Optical-Communication-System-with-Geographic-Targeting-and-Decoding-for-Critical-Messaging
KEYWORDS: Optical Communication, Laser-Based Transmission, Secure Data Transmission, Morse Code Encoding, Image Processing, OpenCV-Based Decoding, Geographic, Targeting, Servo-Controlled System, Obstacle Avoidance, Ultrasonic Sensors, Encryption and Decryption, Real-Time Signal Processing, Android-Based Receiver, Frame Classification, Wireless Communication, Interference-Free Transmission, Disaster Communication, Military Applications

OVERVIEW:
As the increase in complexity of emergency responses, the demand for reliable and secure communication system has increased especially for the high stack environments 
like disaster management, military operations and emergency response. Our approach highlights "Secure Optical Communication System with Geographic Targeting and RealTime Decoding" serves as a solution for these challenges by the optical transmission. The integration of optical transmission, cryptographic security and real-time decoding, the system enhances security and geographically precise communication makes it ideal for critical scenario-based environments.

METHODOLOGY:
1. System Initialization:
The proposed light-based communication system integrates laser diodes, servo motors, and a user-friendly HTML-based GUI linked to an interactive map of Amrita University. Upon activation, users can select a transmission center point by clicking on the map, which automatically aligns three servo motors at 120° angular separation. This GUI setup enables intuitive configuration of the laser communication direction.

2. Transmission Modes:
The system supports two modes: Broadcast Mode and Targeted Mode.
In Broadcast Mode, all servos start at 0°, and an ultrasonic sensor detects nearby obstacles. If an obstacle is detected, servo positions adjust by 5° to avoid interference. The message is then transmitted in Morse code through simultaneous laser diode blinking.
In Targeted Mode, the user selects a specific target location via the GUI. The system identifies the nearest servo, aligns it with the target, encrypts the message using the Caesar cipher, converts it to Morse code, and transmits it via a single laser diode for precise, directed communication.

3. Message Encoding & Transmission:
Messages undergo two levels of transformation. First, they are encrypted using a Caesar cipher (a simple character shift). The encrypted text is then converted into Morse code, where a dot (.) is represented by a longer laser pulse, a dash (-) by a shorter pulse, and spaces by no laser activity for a fixed duration. This light-based pulse system enables efficient message encoding.

4. Reception & Decoding:
The receiver consists of a Flutter-based mobile app integrated with OpenCV for real-time decoding. The camera captures laser pulses as frames and processes them as follows:
Frame Capture: The system captures continuous frames, timestamps them, and converts the format from YUV420 to JPEG.
Binary Signal Extraction: Using OpenCV, images are converted to Lab color space, and a threshold is applied to detect light presence (“on” or “off”).
Morse Code Interpretation: A state machine detects signal durations to differentiate between dots, dashes, and spaces. It uses a lookup table to convert sequences into letters.
Decryption: Decoded letters are decrypted using Caesar shift to retrieve the original message.
Message Display: The final text is shown on the app, along with visual indicators (camera feed, light status graph) for user clarity.

5. Performance & Range Evaluation:
The system was tested for message accuracy, speed, and range. Transmission accuracy averaged 98%, with minor errors due to light interference or motion blur. The optimal transmission speed was "5 words per minute (WPM)" for stable decoding. Faster speeds reduced accuracy due to camera frame rate limits. The effective communication range was calculated using laser beam physics. With a 5 mW red laser (650 nm), the system achieved a reliable range of '12 cm". By increasing power or using green lasers (510 nm), the range significantly improved (up to 101 m), as green lasers are more visible and scatter less, aiding signal detection.

BLOCK DIAGRAM:

<img width="655" height="460" alt="image" src="https://github.com/user-attachments/assets/f9c5dae6-c772-46f8-98a0-99c0227110b9" />


SIMULATION OUTPUTS:

<img width="655" height="460" alt="image" src="https://github.com/user-attachments/assets/ae0ea376-44f6-410f-8df0-c722657a4357" />
<img width="655" height="460" alt="image" src="https://github.com/user-attachments/assets/32dc3a7d-60b1-4401-91ea-0f8401c42c70" />
<img width="655" height="560" alt="image" src="https://github.com/user-attachments/assets/c54f08d5-08a3-4966-b955-283aca061731" />
<img width="655" height="460" alt="image" src="https://github.com/user-attachments/assets/0f1c8bb3-7f8c-4fe5-a81d-611347af27f3" />

WORKING MODEL:

<img width="370" height="550" alt="image" src="https://github.com/user-attachments/assets/81078506-d977-48dd-9896-8768d2380ed8" />

SAMPLE OUTPUTS SCREENSHOTS:

<img width="440" height="651" alt="image" src="https://github.com/user-attachments/assets/16f64eab-6f0c-4a8d-88f0-819820a32a7b" />
<img width="440" height="651" alt="image" src="https://github.com/user-attachments/assets/bdefb71d-289c-4eaa-9d2d-2cff888a6439" />


CONCLUSION:
This laser-based optical communication system offers a secure, interference-resistant, and infrastructure-independent alternative to traditional wireless methods. Designed for military, disaster response, and remote operations, it features dual transmission modes: Broadcast and Targeted along with encryption and Morse code for secure message delivery. An interactive map interface, ultrasonic obstacle avoidance, and an Android-based OpenCV decoder ensure precise, reliable communication. Future improvements like AI-based detection and stronger encryption can further enhance its security and range, making it a robust solution for high-risk environments.



