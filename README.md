# **WildGuardAlert: Automated Wild Animal and Fall Detection System with Instant Alerts**

**FarmSafeGuard** is an AI-powered solution designed to safeguard farms from wild animal intrusions while also ensuring human safety by detecting falls. The system employs advanced object detection, motion tracking, and real-time alert mechanisms. It helps farmers proactively manage wildlife threats and respond to emergencies on the farm. The project integrates the **YOLO model** for accurate object detection and uses **Twilio** for instant SMS notifications. Additionally, it features **text-to-speech** functionality to provide immediate auditory alerts.

## **Features**
- **Wild Animal Detection**: Identifies animals like elephants, bears, horses, cows, and others that may enter the farm premises.
- **Human Fall Detection**: Recognizes when a person falls and automatically triggers an alert.
- **Auto Alert System**: Sends SMS notifications using Twilio when a wild animal or fall is detected.
- **Text-to-Speech Announcements**: Provides real-time vocal alerts for detected objects, helping ensure quick responses.
- **Motion Detection with Alarms**: Monitors farm surroundings for abnormal movements and triggers an alarm for potential threats.

## **Technologies Used**
- **Python**: Core programming language for system development.
- **OpenCV**: Handles video input and processes motion detection.
- **YOLOv8 (Ultralytics)**: Utilized for high-precision object detection of animals and humans.
- **Twilio API**: Sends SMS alerts to notify users of wild animal intrusions or falls.
- **pyttsx3**: Implements text-to-speech functionality to enhance awareness.
- **Winsound**: Triggers sound alarms for detected movements or intrusions.
- **Imutils**: Assists with image processing and optimizing video frames.

## **How It Works**
1. **Object Detection**: The system captures a live video feed using a camera through OpenCV, with the YOLOv8 model identifying objects, focusing on wild animals and humans.
2. **Fall Detection**: Measures the dimensions of a detected person. If the ratio of height to width suggests a fall, the system sends an alert.
3. **Motion Detection**: Continuously monitors for unusual motion in the video feed and triggers alarms if significant movement is detected.
4. **Alerting**: When a fall or wild animal is detected, the system:
   - Activates an alarm sound.
   - Sends an SMS alert using Twilio.
   - Announces the detected event using text-to-speech for immediate action.
