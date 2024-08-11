Overview
The Fall Detection System is a MATLAB-based project that utilizes mobile sensors (accelerometer and gyroscope) to detect falls. It can send an alert via SMS with the location of the fall using Twilio's API. The system is designed to be used with the MATLAB Mobile app, which allows the collection of sensor data from a mobile device.

Features
- Real-Time Fall Detection: The system monitors accelerometer and gyroscope data in real-time to detect falls based on pre-defined thresholds.
- SMS Notification: When a fall is detected, the system sends an SMS to a predefined number, including a Google Maps link with the location of the incident.
- Graphical User Interface: The project includes a simple GUI for starting/stopping the detection process and visualizing the sensor data.

Requirements
- Software
  MATLAB (with Mobile Sensor Connectivity)
  MATLAB Mobile app installed on a mobile device
  Twilio account for sending SMS

Hardware
- A mobile device with accelerometer, gyroscope, and GPS sensors.

Installation
1. Clone the Repository:
   git clone https://github.com/Savani-Manvi/Fall-Detection-System-Simulation-on-MATLAB.git
   cd Fall-Detection-System-Simulation-on-MATLAB
2. Twilio Setup:
   - Create a Twilio account and obtain your accountSid, authToken, and a Twilio phone number.
   - Replace the placeholders in the fallDetectionSystem function with your Twilio credentials and the recipient's phone number.
3. MATLAB Setup:
   - Ensure that MATLAB is installed on your machine.
   - Open the MATLAB script fallDetectionSystem.m in MATLAB.
   - Make sure the MATLAB Mobile app is set up on your mobile device and connected to MATLAB.

Usage
1. Run the Script:
   - Start MATLAB and run the script fallDetectionSystem.m.
   - The GUI will open, displaying the accelerometer and gyroscope data.

2. Start Detection:
   - Press the "Start" button to begin monitoring.
   - The system will start logging sensor data and display it in real-time.

3. Fall Detection:
   - If a fall is detected (based on the set thresholds), the system will display a message in the MATLAB command window and send an SMS with the detected fall's location.

4. Stop Detection:
   - Press the "Stop" button to stop monitoring.

Configuration
- Thresholds
  The system uses predefined thresholds to detect falls:
    Acceleration Threshold: 19.6 m/s² (approximately 2g).
    Gyroscope Threshold: 100 °/s.
  These thresholds can be adjusted in the fallDetectionSystem function according to your specific needs.
- SMS Notification
  The SMS notification is sent using Twilio's API.
  Make sure your mobile device has an active GPS signal to include accurate location data in the SMS.

Limitations
- The system depends on accurate sensor data from the mobile device, and poor sensor quality or lack of GPS signal might affect its performance.
- The fall detection logic is based on simple thresholding; more advanced algorithms can be implemented for improved accuracy.

License
- This project is licensed under the MIT License. See the LICENSE file for more details.

Contribution
- Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

Contact
- For any inquiries, please reach out to manvi.savani@gmail.com.
