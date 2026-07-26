# EXP-2-Image-Capture-and-Video-Processing-Using-OpenCV

## Aim
To write a Python program using OpenCV to capture an image from the webcam and perform the following operations:

1 . Write the frame as a JPG file
2 . Display the video
3 . Display the video by resizing the window
4 . Rotate and display the video

## Software Used
- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
  
## Algorithm
### Step 1:
Import the required libraries and initialize the webcam using cv2.VideoCapture().

### Step 2:
Capture frames continuously from the webcam.

### Step 3:
Save a frame as a JPG image using cv2.imwrite().

### Step 4:
Display the live video stream using cv2.imshow().

### Step 5:
Resize the frame and rotate it using OpenCV functions, then display the processed frames.

## Program
### Developed By: 
#### Name : SAADHANA A
#### Register No : 212225240126

### i) Write the frame as JPG file
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("pic 1.jpg", frame)
cap.release()
captured_image = cv2.imread('pic 1.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```
### ii) Display the video
```
cap = cv2.VideoCapture(0)
for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
cap.release()
```
### iii) Display the video by resizing the window
``` cap = cv2.VideoCapture(0)
for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
cap.release()
```
### iv) Rotate and display the video
```
cap = cv2.VideoCapture(0)
for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)
cap.release()
```

## Output
### i) Write the frame as JPG image
Captured image is saved as captured_image.jpg

<img width="427" height="264" alt="Screenshot 2026-07-26 163125" src="https://github.com/user-attachments/assets/084d6013-1039-40b1-a8c8-c3d53e21986d" />

### ii) Display the video
Live webcam video is displayed

<img width="423" height="245" alt="Screenshot 2026-07-26 163135" src="https://github.com/user-attachments/assets/dedda2c1-d17b-4b85-9dab-b1671fcae5f1" />

### iii) Display the video by resizing the window
Video is shown in resized resolution (640 × 480)

<img width="227" height="320" alt="Screenshot 2026-07-26 163459" src="https://github.com/user-attachments/assets/20a5946a-6722-4132-8e64-efdde14ad695" />

### iv) Rotate and display the video
Video is displayed after rotation (90° clockwise)

<img width="205" height="320" alt="Screenshot 2026-07-26 163153" src="https://github.com/user-attachments/assets/af751e98-efd2-4ee6-ab9c-b1062bc7baeb" />

## Result

Thus, the image is successfully captured from the webcam and various video processing operations such as saving, displaying, resizing, and rotating are performed using OpenCV.


