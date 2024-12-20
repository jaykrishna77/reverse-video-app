# Reverse Video App

## Overview

The **Reverse Video App** allows users to upload a video, which is then processed to create a reversed version of the video. The application utilizes a Flask backend with Python for video processing, and a responsive frontend built with HTML, CSS, and JavaScript.

## Features

- Upload a video file for reversal.
- Process the video on the server side.
- Play the reversed video directly in the browser.
- Responsive design suitable for various devices.

## Technologies Used

- **Frontend:** 
  - HTML
  - CSS
  - JavaScript
- **Backend:**
  - Flask (Python)
- **Video Processing:**
  - OpenCV for video frame manipulation
  - MoviePy for audio handling and video writing
- **Other Libraries:**
  - NumPy for numerical operations

## Installation

### Prerequisites

- Python 3.x installed on your machine.
- Required Python packages (listed in `requirements.txt`).
- Ensure you have the necessary libraries for video processing.

### Clone the Repository


git clone https://github.com/Sathwik9418/reverse-video-app.git
cd reverse-video-app


### Set Up the Backend

1. Create a virtual environment (optional but recommended):


   python -m venv venv
   source venv/bin/activate  # On Windows use venv\Scripts\activate
   

2. Install the required Python packages:

   pip install -r requirements.txt
   

### Run the Application

1. Start the Flask server:

   python app.py
   

2. Open your browser and navigate to `http://localhost:5000` to access the app.

## How It Works

1. **File Upload:**
   - Users can upload a video file through a web form. The file input is styled to enhance user experience.

2. **Video Processing:**
   - Upon submission, the video file is sent to the backend where it is temporarily saved.
   - The `reverse_video` function is invoked, which performs the following:
     - Extracts audio from the uploaded video (if present).
     - Reads and reverses the video frames using OpenCV.
     - Reverses the extracted audio using the `scipy.io.wavfile` library, if applicable.
     - Combines the reversed video and audio using MoviePy and saves the final output.

3. **Result Display:**
   - The reversed video is then sent back to the frontend, where it is displayed in a video player for the user to watch.

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request.
