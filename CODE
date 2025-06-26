# ThreadCounter-Automated-Thread-Counting-Using-Camera-and-Image-Processing
import cv2
import numpy as np

# Set this to your image file
image_path = "yarn_test.jpg"
use_webcam = False

def process_frame(frame):
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    blur = cv2.GaussianBlur(gray, (5, 5), 0)
    edges = cv2.Canny(blur, 50, 150, apertureSize=3)

    lines = cv2.HoughLinesP(edges, 1, np.pi / 180, threshold=100, minLineLength=100, maxLineGap=10)
    thread_count = 0

    if lines is not None:
        for line in lines:
            x1, y1, x2, y2 = line[0]
            angle = np.arctan2(y2 - y1, x2 - x1) * 180 / np.pi
            if 80 < abs(angle) < 100:
                cv2.line(frame, (x1, y1), (x2, y2), (0, 255, 0), 2)
                thread_count += 1

    cv2.putText(frame, f"Thread Count: {thread_count}", (10, 30),
                cv2.FONT_HERSHEY_SIMPLEX, 1, (0, 0, 255), 2)
    return frame

if not use_webcam:
    frame = cv2.imread(image_path)
    if frame is None:
        print("Error loading image. Check file name or path.")
    else:
        output = process_frame(frame)
        cv2.imshow("Thread Detection - Image", output)
        cv2.waitKey(0)
        cv2.destroyAllWindows()
