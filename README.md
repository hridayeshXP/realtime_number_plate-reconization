# realtime_number_plate-reconization
This project implements a complete deep learning pipeline for detecting vehicles and recognizing their license plate numbers from video footage.It combines object detection and optical character recognition (OCR) to create an accurate, real-world system for traffic monitoring and automation.
________________________________________
Project Workflow
The system is divided into three stages, each handled by a separate model:
File	Description
car_detect.pt	YOLOv8 model trained to detect vehicles from video input.
plate_image_trained.pt	Custom-trained YOLOv8 model for detecting license plates in cropped car images.
final_detection.pt	Combined YOLOv8 model that performs both car and license plate detection together.
After license plate localization, EasyOCR is used to extract the alphanumeric text.
________________________________________
Project Files
File	Type	
main.py	Python script containing the full integrated detection and OCR pipeline.	
car_detect.pt	YOLOv8 model for car detection.	
plate_image_trained.pt	YOLOv8 model for license plate detection.	
final_detection.pt	Final integrated model for car and plate detection.	
output_car_plate_ocr.mp4	Output video showing detected vehicles and recognized license numbers.	
detections.xlsx	Log file storing recognized plate numbers, frame numbers, and timestamps.	
________________________________________
Technologies Used
•	Language: Python
•	Environment: Google Colab
•	Frameworks & Libraries:
o	PyTorch
o	Ultralytics YOLOv8
o	OpenCV
o	EasyOCR
o	Pandas, NumPy, Matplotlib
________________________________________
How It Works
1.	The car detection model identifies vehicles in each frame of the uploaded video.
2.	Cropped car images are passed into the license plate detection model.
3.	The OCR module (EasyOCR) extracts text from the detected license plate.
4.	The recognized numbers are displayed on-screen and stored in detections.xlsx.
5.	The system saves an annotated video showing all detections.
________________________________________
Outputs
•	Annotated video: output_car_plate_ocr.mp4
•	Detection log: detections.xlsx
Each log entry includes:
o	Detected plate number
o	Confidence score
o	Frame number or timestamp
________________________________________
Use Cases
•	Automated Number Plate Recognition (ANPR)
•	Smart Parking and Access Control Systems
•	Traffic Law Enforcement
•	Toll Booth Automation
•	Vehicle Tracking
________________________________________
Future Enhancements
•	Real-time detection using live webcam feed
•	Improved OCR accuracy through image enhancement
•	Multi-country plate format recognition
•	Integration with vehicle registration databases


