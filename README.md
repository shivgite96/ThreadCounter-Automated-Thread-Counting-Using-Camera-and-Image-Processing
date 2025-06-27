📝 Description:

During my internship in the textile industry, I observed a common problem on the factory floor: workers manually counted threads in yarns or woven fabrics for quality checks. This manual method was not only time-consuming but also prone to human error and inconsistency. To solve this, I developed ThreadCounter, a system that uses a camera and image processing to automate the thread counting process.

This project utilizes a standard USB or laptop camera to capture images of yarn or fabric samples. These images are then processed using Python and the OpenCV library. The system applies various image processing techniques such as grayscale conversion, Gaussian blur, edge detection (like Canny), thresholding, and contour detection to accurately identify and count the number of threads present in the image.

🎯 Key Features:

📷 Real-time or static image input via camera

🔍 Automatic thread detection and counting

⏱️ Reduces manual labor and saves time

✅ Improves accuracy and repeatability

🏭 Designed for use in textile quality control


⚙️ Technologies Used:

Python

OpenCV

NumPy

Camera Module (Webcam/USB Camera)


📦 Applications:

Yarn thread counting in spinning mills

Quality inspection in weaving departments

Research and testing in textile labs


💡 Future Scope:

This system can be further enhanced by:

Integrating with Arduino or PLCs for automatic rejection of faulty fabric rolls

Using machine learning for better adaptability to different yarn types

Adding GUI for user-friendly interaction
