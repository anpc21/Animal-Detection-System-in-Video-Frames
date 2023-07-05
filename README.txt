Animal Detection System in Video Frames - Readme

This Python code provides a web-based Animal Detection System that uses YOLOv8, a popular object detection model, to detect animals in real-time video streams or recorded video files. The system uses Flask, a web framework, to host a web page where users can either upload a video file or use their camera for live detection.

Requirements:

- Python 3.x
- OpenCV (cv2) - Install with `pip install opencv-python`
- Ultralytics (ultralytics.YOLO) - Install with `pip install yolo`

Usage:

1. Ensure that you have installed the required libraries and modules.
2. Download the YOLOv8 model (COCO_TRAINED_MODEL.pt) from the Ultralytics repository or use any other pre-trained YOLOv8 model you prefer.
3. Save the COCO_TRAINED_MODEL.pt model file in the same directory as the Python script.
4. Run the Python script to start the Flask application.
5. The Flask application will host a webpage on http://localhost:5000/.
6. Access the webpage using your web browser.

Web Interface:

The webpage titled "Animal Detection System in Video Frames" will be displayed.
- You can select a video file to upload and click the "Upload" button to start detection in the uploaded video file.
- Alternatively, you can click the "Capture from Camera" button to enable real-time detection using your device's camera.
- To stop the real-time detection, click the "Stop" button.

Functionality:

The `generate()` function serves as a generator that continuously captures video frames from the selected source (file or camera) and performs YOLOv8 inference on each frame.
Detected animals will be annotated on the frames, and the annotated frames will be displayed on the webpage.

Note:

- The YOLO class from Ultralytics is used to load the YOLOv8 model and perform inference.
- The video stream can be started and stopped using the web interface to facilitate easy and interactive usage.

Disclaimer:

This code is intended for educational and demonstration purposes only.
The YOLOv8 model provided by Ultralytics or any other pre-trained model used is subject to the terms and licenses of the respective authors and should be used responsibly and legally.

Customizations:

- You can modify the HTML template in the `index.html` file to change the appearance of the web page and add additional functionalities.
- Adjust the model loading and detection parameters according to your specific use case or trained models.
- You may add more post-processing steps to further process the detected animal information as per your requirements.

The Animal Detection System based on YOLOv8 can detect various objects present in the COCO dataset, which includes animals and other common objects. The COCO dataset contains a wide range of object categories, and the YOLOv8 model can detect objects such as:

1. Animals: Dogs, cats, birds, horses, cows, elephants, giraffes, zebras, bears, etc.
2. Vehicles: Cars, trucks, buses, bicycles, motorcycles, airplanes, boats, etc.
3. Household Objects: Chairs, tables, beds, sofas, TVs, refrigerators, etc.
4. People: Humans of various ages, genders, and activities.
5. Electronics: Laptops, cell phones, keyboards, monitors, etc.
6. Outdoor Objects: Trees, plants, traffic lights, stop signs, fire hydrants, etc.
7. Sports Objects: Balls (soccer, basketball, baseball), tennis rackets, hockey sticks, etc.
8. Food Items: Fruits, vegetables, bottles, cups, plates, etc.

The model has been trained on a large and diverse dataset