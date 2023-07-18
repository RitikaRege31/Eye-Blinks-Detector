# Eye-Blinks-Detector


# Blink Detection using Facial Landmarks

This repository contains Python code for detecting blinks in a video using facial landmarks. The blink detection algorithm is based on the eye aspect ratio (EAR) computed from the coordinates of specific facial landmarks.

## Dependencies

To run the code, you need the following dependencies:

- Python 3.6+
- imutils
- scipy
- dlib
- OpenCV (cv2)

You can install the dependencies using the following command:

```
pip install imutils scipy dlib opencv-python argparse
```

## Usage

To detect blinks in a video, follow these steps:

1. Download or clone this repository to your local machine.

2. Download the shape predictor file named `shape_predictor_68_face_landmarks.dat` from the dlib website: http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2. Extract the file and place it in the same directory as the Python script.

3. Prepare a video file that contains faces. You can use any video file you have or download a sample video for testing.

4. Open a terminal or command prompt, navigate to the directory where the Python script is located, and run the following command:

   ```
   python detect_blinks.py --shape-predictor shape_predictor_68_face_landmarks.dat --video video.mp4
   ```

   Replace `video.mp4` with the path to your video file.

5. The video stream will start, and a window will appear displaying the processed video frames. The blink count and eye aspect ratio will be displayed on the video frames.

6. Press 'q' to stop the video stream and exit the program.

## Customization

You can modify the following constants in the code according to your requirements:

- `EYE_AR_THRESH`: The eye aspect ratio threshold to determine a blink.
- `EYE_AR_CONSEC_FRAMES`: The number of consecutive frames the eye must be below the threshold to count as a blink.

## Acknowledgments

The blink detection algorithm is based on the work of [Tereza Soukupova](https://github.com/teresasoukupova) and [Jan Cech](https://github.com/jeceka) on the [dlib](http://dlib.net/) library.

## References

- Soukupova, T., & Cech, J. (2016). Real-time eye blink detection using facial landmarks. In Proceedings of the 2016 ACM Companion on Interactive Surfaces and Spaces (pp. 37-40).
