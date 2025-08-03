# Dress Size & Body Measurement Estimation from Video 🎥👕👖
Run the ipynb file in colab , and upload the dresscombo.mp4 file in colab .  Then you need to enter the height of the person .

This project estimates a man's **shirt size, trouser size, trouser length, and weight** from a video.  
It uses **YOLOv12**, **MediaPipe**, and **OpenCV** to analyze the person’s posture and proportions, along with a manually entered height.

---

## 🔍 Key Features

- 📏 **Body Measurement Estimation**:
  - Predicts **shirt size** (e.g., M, L, XL)
  - Predicts **trouser size** and **length**
  - Estimates **body weight** in kg

- 📹 **Video Output with Overlay**:
  - The result video shows the detected person with bounding boxes
  - Annotations include predicted weight, shirt & trouser size

- 📐 **Uses Manual Height Input**:
  - The user's height (in cm) is provided as input
  - All other dimensions are calculated proportionally using pose landmarks

---

## 🧠 Tech Stack

- **Python**
- **OpenCV** – for video reading, writing, and drawing
- **MediaPipe** – for pose detection and body landmark extraction
- **YOLOv12 (Ultralytics)** – for person detection
- **Google Colab** – for experimentation

---

## 🚀 How It Works

1. **Input**: A video of the person walking or standing
2. **Height Input**: Manually entered by the user (in centimeters)
3. **Pose Estimation**: MediaPipe detects body keypoints
4. **Proportional Estimation**:
   - Body part lengths (torso, limbs) are measured in pixel scale
   - Converted to real-world measurements using height ratio
5. **Final Prediction**:
   - Uses rule-based approximation to predict sizes
   - Weight estimated using rough anthropometric assumptions

---

## 🧪 Example

```bash
video_path = "/content/dresscombo.mp4"
person_height_cm = 178  # user enters manually
