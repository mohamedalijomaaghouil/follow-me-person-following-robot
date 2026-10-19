# 🤖 Autonomous Person-Following Robot (MediaPipe + RealSense)

A real-time robot tracking system that follows a person using skeletal detection and depth sensing, built by a team of engineering students at ENISo.

🎓 Project by: [Mohamed Ali Jomaa Ghouil](https://www.linkedin.com/in/mohamed-ali-jomaa-ghouil), Yasmine Saad, Yahya Ben Turkia  
🧑‍🏫 Supervised by: **Dr. Lamine Houssein** — Engineer in Mechatronics, PhD in Robotics, Assistant Professor at ENISo

---

## 🎯 Objective

Design and implement a robot capable of:

- Detecting a **person** using real-time pose estimation  
- Reacting to a **hand gesture** to start/stop following  
- Maintaining a **safe distance (~2 meters)** using depth camera  
- Sending movement commands via **Modbus TCP**

---

## 🛠️ Technologies Used

- 📷 **Intel RealSense D435i** — Color + Depth Camera  
- 🧍‍♂️ **MediaPipe Holistic** — Real-time skeleton & gesture tracking  
- 🧠 **Python 3.11** with:
  - `opencv-python` (video processing)  
  - `numpy`  
  - `pyrealsense2`  
  - `mediapipe`  
  - `pyModbusTCP`  
- 🧰 **Ubuntu/Linux** + **VS Code**
- ⚙️ **Modbus TCP** for robot control

---

## 🚦 How It Works

- Detects **shoulders** → calculates chest center
- Uses **depth data** to determine distance
- Calculates:
  - `Vx` (linear speed) → forward/backward
  - `Wz` (angular speed) → left/right rotation
- **Gesture Recognition**:  
  - Raise right hand (with open hand gesture) → toggle following  
  - Robot stops if target lost > 10 seconds

---

## ⌨️ Controls

- Press `f` — Manually toggle follow mode  
- Press `c` — Activate gesture mode (to start/stop with hand)  
- Press `u` — Deactivate gesture mode  
- Press `q` — Quit the program  

---

## 🧪 Demo

🎥 **Demo** – Robot following a person, and wheel speed changing when turning  
[▶️ Watch on YouTube](https://youtu.be/bcdjbf4g2AU) · [Screen recording on Google Drive](https://drive.google.com/file/d/13Uw83MHfXj6rsvhU6wesWhnttASEJpLC/view?usp=sharing)


---

## 📁 Project Structure

```
├── person_following.py                                  # Main Python program
├── requirements.txt                                     # Dependencies
└── Documentation Complète du prjet Follow me Robot.pdf # Full technical documentation (in French)
```

---

## 🚀 Installation & Setup

### Prerequisites:
- Ubuntu 20.04+ with Python 3.11  
- Intel RealSense SDK installed  
- A working Modbus-compatible robot (or run in simulation)

### 1. Clone the repo
```bash
git clone https://github.com/mohamedalijomaaghouil/Autonomous-vision-based-person-following-robot-using-YOLO-and-Realsense.git
cd Autonomous-vision-based-person-following-robot-using-YOLO-and-Realsense
````

### 2. Set up virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Modbus simulator (optional)

```bash
python3 -m pymodbus.server --host 127.0.0.1 --port 1502
```

### 5. Run the robot

```bash
python3 person_following.py
```

---

## 📬 Contact

📧 [mohamedalijomaaghouil@gmail.com](mailto:mohamedalijomaaghouil@gmail.com)
🔗 [LinkedIn – Mohamed Ali Jomaa Ghouil](https://www.linkedin.com/in/mohamed-ali-jomaa-ghouil)

---

## 🏫 Developed at

**National Engineering School of Sousse (ENISo)**
Mechatronics Department – Semester 2 Project – May 2025
