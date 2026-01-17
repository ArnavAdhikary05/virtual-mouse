# Virtual Mouse - Hand Gesture Control

Control your computer mouse using hand gestures captured through your webcam.

## Overview

This project uses computer vision and machine learning to detect hand landmarks and translate hand movements into mouse control. It allows you to move your cursor and click by using simple hand gestures.

## Features

- **Mouse Movement**: Move your cursor by moving your index finger (landmark 8)
- **Clicking**: Click by bringing your thumb (landmark 4) close to your index finger
- **Hand Detection**: Real-time hand detection and landmark recognition using MediaPipe
- **Live Visualization**: See the detected hand landmarks on the video feed

## Requirements

- Python 3.6+
- Webcam/Camera
- Windows/Linux/Mac

## Installation

1. Clone or download this project to your local machine.

2. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

   Or manually install:
   ```bash
   pip install opencv-python mediapipe pyautogui
   ```

## Usage

Run the script:
```bash
python mouse_control_using_hands.py
```

### Controls

- **Move Cursor**: Move your index finger in front of the camera to move the mouse pointer
- **Click**: Pinch your thumb and index finger together (close distance) to perform a left-click
- **Exit**: Press **ESC** key to exit the application

## How It Works

1. **Hand Detection**: Uses MediaPipe to detect hand landmarks in real-time from the webcam
2. **Landmark Tracking**: Identifies key points on the hand:
   - Landmark 8: Index finger tip (used for cursor movement)
   - Landmark 4: Thumb tip (used for clicking)
3. **Screen Mapping**: Converts hand positions from the camera frame to screen coordinates
4. **Mouse Control**: Uses PyAutoGUI to control the system mouse

## Dependencies

- **OpenCV** (`opencv-python`): Computer vision library for image processing
- **MediaPipe**: Machine learning framework for hand detection and landmark recognition
- **PyAutoGUI** (`pyautogui`): Python library for programmatic mouse and keyboard control

## Tips for Best Performance

- Ensure adequate lighting for better hand detection
- Place your hand clearly in front of the camera
- Keep your hand within the camera frame
- Use steady hand movements for precise cursor control
- Fine-tune the click distance threshold if needed

## Troubleshooting

- **Hand not detected**: Ensure you have adequate lighting and your hand is visible to the camera
- **Jerky mouse movement**: Try keeping your hand steady and within a consistent distance from the camera
- **Camera not opening**: Verify that your webcam is connected and not in use by another application
- **Inaccurate clicking**: Adjust the distance threshold in the code if needed

## License

This project is open source and available for personal use.

## Future Improvements

- Add gesture recognition for different actions (right-click, drag, scroll)
- Implement multi-hand support for advanced gestures
- Add settings for sensitivity adjustment
- Support for different camera calibrations
- Performance optimization for smoother movement
