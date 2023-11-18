# Presentation_control_using_handgestures
The Presentation Control Using Hand Gesture project is a novel approach to enhance the interaction with presentation . Leveraging computer vision and gesture recognition, this system allows users to seamlessly navigate through presentation slides, start/stop presentations, and perform other actions using intuitive hand movements.


## Installation

1. **Clone the repository:**
    git clone https://github.com/vashu1409/Presentation_control_using_handgestures.git
    

2. **Create Images Folder:**

    Create a folder named `Images` in the same directory as the Python file (`main.py`). This is where you'll place the PowerPoint images.

3. **Upload PowerPoint Images:**

    Place your presentation slides as individual images in the `Images` folder. Ensure the images are named sequentially (e.g., slide1.jpg, slide2.jpg).

    ```plaintext
    your-project/
    ├── main.py
    └── Images/
        ├── slide1.jpg
        ├── slide2.jpg
        └── ...
    ```
    This step ensures that the images are in the correct order for the presentation.

4. **Install Dependencies:**

    Install required Python dependencies

5. **Run the Application:**

    ```bash
    python main.py
    ```

    This will start the application, and you can now perform the predefined gestures to control the presentation. Refer to the documentation for a list of supported gestures.



   **Hand Gestures and Their Uses:**
The application recognizes various hand gestures to perform specific actions. Here are the
finger gestures and their corresponding uses:
➢ **Index Finger Extended**: 
In the Presentation Control mode, extending the index finger is used to draw on the
slides.
➢ **Thumb Raised:** 
In the Presentation Control mode, raising the thumb allows you to navigate to the
previous slide/image.
➢ **Pinky Finger Raised:** 
In the Presentation Control mode, raising the pinky finger allows you to navigate to the next
slide/image.
➢ **Two Fingers Raised**(index & middle): 
In the Presentation Control mode, raising the two fingers acts as pointer to point on the
slide/image.
➢ **Three Fingers Raised:** 
In the Presentation Control mode, raising the three fingers is used to delete the most recent
annotation or drawing made on the presentation slide/image.


# Presentation-Control-System
This project is about creating a simple presentation control system using hand gestures captured by your computer's webcam. It allows you to navigate through a series of images (slides) and even draw on them using your hand movements.

## Breakdown of how the project works:

#### Importing Libraries and Setting Up Parameters:
The code starts by importing necessary libraries like cv2 (OpenCV) and cvzone (a computer vision library). It also defines some parameters like the dimensions of the camera frame, a gesture threshold, the folder path where presentation images are stored, etc.

#### Camera Setup:
It initializes the webcam (camera) and sets its width and height to capture frames of a specific size.

#### Hand Detection Setup:
The code sets up a hand detection object using the HandDetector class from the cvzone library. This detector will help identify hands in each frame captured by the webcam.

#### Variables Initialization:
Various variables are initialized to manage the functionality of the presentation control system. These include lists to store images, counters, flags for different actions, and more.

#### Loading Presentation Images:
The code retrieves a list of image file names from the specified folder path. These images will be used as slides for the presentation.

#### Main Loop:
The program enters a continuous loop where it captures frames from the webcam and processes them.

#### Hand Detection and Gesture Interpretation:
Within the loop, it detects hands in the frame using the HandDetector object. If a hand is detected and specific finger configurations are recognized (like a "thumbs up" or "index finger up"), certain actions are triggered.

#### Slide Navigation:
If the hand is raised above a certain threshold (indicating it's at face level), and specific finger configurations are detected, the program interprets these gestures as commands to navigate through the presentation images. For example, if you raise your index finger, it might go to the next slide; if you raise your pinky finger, it might go to the previous slide.

#### Drawing on Slides:
If certain fingers are raised in a particular way, the program enters a drawing mode. You can draw on the current slide by moving your index finger around. The finger's position is tracked, and lines are drawn between consecutive positions, creating a simple drawing effect.

#### Annotations:
You can also make annotations by raising your index and middle fingers. This creates a series of points that are connected with lines, simulating drawing shapes or lines on the slide.

#### Displaying the Interface:
The code continuously updates the display to show the current slide and any annotations or drawings made on it. It also displays a smaller version of the webcam feed in the corner for real-time visualization of your hand gestures.

#### Exiting the Program:
To exit the program, you can press the 'q' key. This will break the loop and close the application.

In summary, this project uses hand gestures captured by the webcam to control a presentation, navigate through slides, and even draw on the slides in real-time.
