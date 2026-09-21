# Jaundice-Detection-Using-Raspberry-Pi-and-Machine-Learning
Raspberry Pi-based ML &amp; image processing for jaundice detection

 Award: First Prize Winner – Hackathon
 
This project focuses on early jaundice detection using image processing and machine learning. A live image of the human eye is captured and processed on a Raspberry Pi, where a pre-trained machine learning model analyzes eye coloration. Based on trained datasets, the system accurately identifies the presence of jaundice and provides quick diagnostic results for early screening.

Jaundice is a medical condition characterized by yellowing of the skin and the sclera (whites of the eyes) caused by elevated bilirubin levels. Early detection is critical, especially in neonates and vulnerable patients.

This project implements an automated, non-invasive screening tool using a Deep Learning Convolutional Neural Network (CNN) integrated with a Telegram Bot hosted on a Raspberry Pi. Users can upload an image of a patient's eye or skin directly through Telegram to receive an instant, automated preliminary analysis and staging of jaundice.


The system operates on an edge-computing architecture where the Telegram application acts as the user interface, communicating via webhook/polling with a Python backend running locally on a Raspberry Pi.

[ User (Telegram App) ] 
       │ (Sends Photo /start)
       ▼
[ Telegram Bot API ] 
       │ (Polling Updates)
       ▼
[ Raspberry Pi Backend (Python) ] 
       ├─► 1. Downloads & Preprocesses Image (Pillow/NumPy)
       ├─► 2. Performs Inference via CNN Model (.h5)
       └─► 3. Evaluates Thresholds & Classifies Stage
       │
       ▼
[ Formatted Markdown Response Sent Back to Telegram ]
