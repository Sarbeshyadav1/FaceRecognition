# Face Recognition Attendance System

## Overview
This is an automated attendance management system that uses facial recognition technology to mark student attendance. The system captures live video feed, recognizes faces, identifies students, and automatically records their attendance in a database and CSV file.

## Key Features
- **Facial Recognition**: Automatically detects and recognizes student faces
- **Automated Attendance**: Marks attendance in real-time when a face is recognized
- **User-Friendly UI**: Graphical interface for easy navigation and operation
- **Attendance Viewing**: Dedicated interface to view and manage attendance records
- **Secure Database**: Student information and attendance records stored securely

## How to Use
1. **Launch the Application**: Run `python main.py`
2. **Face Recognition**: Click "Face Recognition" to start the camera
3. **Mark Attendance**: When your face is recognized, attendance is automatically marked
4. **View Attendance**: Click "View Attendance" to see all attendance records
5. **Exit**: Press 'q' to close the face recognition window

## Installation
1. Clone the repository
2. Install required packages: `pip install -r requirements.txt`
3. Run the application: `python main.py`

## System Requirements
- Python 3.6 or higher
- Webcam or camera device
- Required libraries: OpenCV, NumPy, PIL, tkinter

## Data Privacy
The system only stores essential student information and attendance records. All data is kept locally and is not shared with external services. 

# 🎯 Face Recognition Based Standard Attendance System

This is a Python-based desktop application that automates student attendance using face recognition technology. The system captures faces using a webcam, trains a recognizer, and marks attendance automatically by identifying known faces.

---

## 📌 Features

- Face detection using OpenCV
- Face recognition and model training
- Student registration
- Attendance logging in CSV and SQLite DB
- Login module
- Simple UI with Tkinter

---

## ⚙️ Tech Stack

| Technology     | Purpose                         |
|----------------|----------------------------------|
| Python         | Main programming language        |
| OpenCV         | Face detection and recognition   |
| SQLite         | Lightweight database             |
| Tkinter        | GUI for desktop app              |
| Haarcascade    | Face detection XML model         |

---

## 📁 Project Structure

```
FaceRecognition/
├── attendance.py               # Marks attendance in CSV
├── face_recognizer.py          # Face recognition logic
├── train.py                    # Training module
├── init_db.py / init_db.sql    # Database initialization
├── login.py                    # User login interface
├── student.py                  # Student registration
├── main.py                     # Main file to launch app
├── face_recognition.db         # SQLite database
├── attendance.csv              # Attendance log file
├── data/                       # Captured face images
├── classfier.xml               # Trained face recognizer model
├── haarcascade_frontalface... # Face detection model
├── id_mapping.json             # Mapping of student IDs
├── README.md                   # Documentation
├── TECH_STACK.md               # Tech stack details
```

---

## 🖥️ Installation

### Prerequisites

- Python 3.x installed
- Webcam
- Git (optional)

### Step-by-Step Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/sarbeshyadav1/FaceRecognition.git
   cd FaceRecognition
   ```

2. **Create a Virtual Environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Required Packages:**
   Create `requirements.txt` if not already present:
   ```bash
   pip install opencv-python numpy pillow
   ```

4. **Initialize the Database:**
   ```bash
   python init_db.py
   ```

---

## 🚀 How to Use

### 1. **Register a Student**
Run the `student.py` file to capture a new student's face images.
```bash
python student.py
```

### 2. **Train the Recognizer**
Train the model with the captured face data:
```bash
python train.py
```

### 3. **Launch the App**
Start the main app and mark attendance via camera:
```bash
python main.py
```

Attendance will be stored in `attendance.csv` and `face_recognition.db`.

---

## 🧪 Sample Data

Face images are saved under `/data/` with filenames like `user.<id>.<imagenum>.jpg`.

---

## ⚠️ Notes

- Avoid bright or dark lighting when capturing faces.
- Add `.gitignore` to exclude sensitive files like:
  ```
  *.db
  *.csv
  /data/
  *.xml
  ```

---

## 🙋‍♂️ Author

**Sarbesh Yadav**  
B.Tech CSE | SRM University - AP  
`AP22110011510`

---

## 📄 License

This project is open-source and free to use under the MIT License.
