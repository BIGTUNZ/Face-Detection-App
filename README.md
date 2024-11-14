# Face Detection App

This project is a Face Detection App built using OpenCV and Streamlit. It allows users to detect faces in real-time video captured from a webcam and customize various detection settings. The app provides an easy-to-use web interface to adjust detection parameters, select rectangle colors, and save detected face images.

## Features

- **Real-Time Face Detection**: This method uses OpenCV's Haar Cascade Classifier to detect faces from a live webcam feed.
- **Interactive Web Interface**: Built with Streamlit, providing a user-friendly experience for adjusting settings.
- **Customizable Detection Parameters**:
  - `scaleFactor`: Controls the scale at which the image is resized during detection, affecting detection sensitivity.
  - `minNeighbors`: Sets the minimum number of neighbors required for a rectangle to be considered a face, which adjusts detection accuracy.
- **Adjustable Rectangle Color**: Users can pick a color for the rectangle that highlights detected faces.
- **Image Saving**: Capture and save frames with detected faces directly from the app.

## Requirements

- Python 3.x
- Libraries:
  - `opencv-python`
  - `streamlit`
  - `numpy`
  - `Pillow`

Install the necessary libraries using:
```bash
pip install opencv-python streamlit numpy pillow
```

## How It Works

1. **Face Detection**: The app uses OpenCV’s pre-trained Haar Cascade Classifier (`haarcascade_frontalface_default.xml`) for face detection. This classifier identifies faces in grayscale frames, so the video feed is converted to grayscale for optimal detection.
2. **Webcam Capture**: The app captures live video from the default webcam using `cv2.VideoCapture(0)`.
3. **Detection and Visualization**: Detected faces are marked with customizable rectangles. Users can control `scaleFactor` and `minNeighbors` to refine detection sensitivity.
4. **Interactive Controls**: The Streamlit interface includes sliders and color pickers for easy adjustments and buttons to start detection or save images.
5. **Save Detected Faces**: Users can capture frames with detected faces as images, which are saved to the local directory.

## Usage Instructions

1. **Run the App**: Start the Streamlit app with the following command:
   ```bash
   streamlit run app.py
   ```
2. **Adjust Parameters**: 
   - Use the **slider** to adjust `scaleFactor` for controlling detection scale and `minNeighbors` to fine-tune sensitivity.
   - Choose the **rectangle color** from the color picker to customize the display.
3. **Start Face Detection**: Press the "Detect Faces" button to begin detecting faces in real-time from your webcam.
4. **Save Image with Detected Faces**: Click "Save Image with Detected Faces" to save the current frame with rectangles around detected faces.
5. **Stop Detection**: Use the checkbox to stop face detection.

## Code Structure

- **`app.py`**: Main application file containing all code for initializing the Streamlit interface, handling webcam video capture, detecting faces, and saving images.
- **`haarcascade_frontalface_default.xml`**: Haar Cascade XML file for face detection (this should be included or downloaded separately if not present).

## Example

When the app is running, you should see a real-time video feed from your webcam with faces highlighted by rectangles. Adjust parameters and color as needed, then save any frame with detected faces by clicking the save button.

## Future Enhancements

Potential additions to this app:
- Adding support for multiple face detection models.
- Allowing video file uploads for offline face detection.
- Adding additional facial feature detection (eyes, nose, etc.).
- Incorporating other machine learning techniques for enhanced accuracy.

## License

This project is licensed under the MIT License.

## Acknowledgements

- OpenCV for providing tools for computer vision.
- Streamlit for enabling easy and interactive web app creation.
