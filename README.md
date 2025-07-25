# 🧠 Real-Time Face Recognition Attendance System

![Banner](Samples_Images_For_Testing/face-scanning-technology-vector.jpg)

This project is a **real-time face recognition-based attendance system** built using **OpenCV** and **MediaPipe**. It captures video from your webcam, detects and recognizes faces, and logs attendance automatically into dated CSV files.

---

## 🧪 Sample Images Used for Testing

These are the reference images used for testing and configuring the face recognition system. They should be placed in the `images/` directory.

**Folder:** `Samples Images For Testing/`

Example files:
- `satya_nadella.jpg`
- `jeff_bezos.jpg`
- `elon_musk.jpg`
- `kajal_aggarwal.jpg`

---

## 💡 Features

- ✅ Real-time face detection & recognition using MediaPipe Face Mesh
- ✅ Pose normalization to improve accuracy
- ✅ CLAHE lighting correction for robust recognition
- ✅ Adaptive threshold for face matching
- ✅ Attendance automatically saved to a dated CSV file
- ✅ Live confidence score and recognition overlay on webcam feed

---

## 📂 Folder Structure

```

Face-Recognition-Attendance/
│
├── images/                          # Place known face images here
├── Samples Images For Testing/      # Sample images used for development
├── Results Shots/                  # Screenshots of actual program output
├── main.py                         # Main Python script
└── README.md                       # This documentation

````

---

## 🛠️ Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/face-recognition-attendance.git
   cd face-recognition-attendance


2. **Install Python Dependencies**
   Make sure you have Python 3.7+ installed. Then install the required packages:

   ```bash
   pip install opencv-python mediapipe numpy
   ```

3. **Add Reference Face Images**
   Put the face images of people you want to recognize in the `images/` folder. File names should match the person's name (e.g., `elon_musk.jpg`).

4. **Run the Script**

   ```bash
   python main.py
   ```

---

## 📸 Result Screenshots

Here are some actual result screenshots taken from live testing of the system.

**Folder:** `Results Shots/`

What you’ll find:

* Webcam feed with name overlay
* Attendance logs in the terminal
* CSV files saved with time and names

---

## 📝 How Attendance Works

* When a face is recognized:

  * It checks if the person has already been marked present.
  * If not, it logs the name and current time into a CSV file for the day.
  * CSVs are saved to:
    `~/Documents/Attendance/YYYY-MM-DD.csv`
* Only one entry per person per session is recorded.

---

## ⚙️ Configurable Parameters

| Parameter                  | Description                                | Default |
| -------------------------- | ------------------------------------------ | ------- |
| `FACE_IMAGE_SIZE`          | Standard height of processed face images   | `500`   |
| `ROI_EXPANSION`            | Extra space around detected face (padding) | `0.35`  |
| `MIN_DETECTION_CONFIDENCE` | Face detection confidence threshold        | `0.4`   |

---

## 📈 Future Enhancements

* Add GUI for face registration
* Replace MediaPipe with FaceNet or Dlib for higher accuracy at scale
* Save/load precomputed encodings to reduce startup time
* Use database instead of CSV for attendance storage
* Add support for multi-face detection and group recognition

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🤝 Contributing

Contributions and suggestions are welcome!
Please open an issue or submit a pull request with improvements or bug fixes.

---

## 📧 Contact

Created by **\[Surya Prakash Subudhiray]**
For queries or collaboration, feel free to reach out!


