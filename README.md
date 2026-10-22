<div align="center">

🚦 Traffic Rules Violation Detection
Computer Vision • Python • OpenCV • PyQt5 • SQLite
<p>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=flat-square&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/GUI-PyQt5-41CD52?style=flat-square&logo=qt&logoColor=white" alt="PyQt5">
  <img src="https://img.shields.io/badge/Database-SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite">
  <img src="https://img.shields.io/badge/Status-Experimental-orange?style=flat-square" alt="Experimental">
</p>

A computer-vision project exploring how traffic footage can be processed to identify potential traffic-rule violations and display records in a desktop GUI.
</div>

👀 Project Preview
<p align="center">
  <img src="images/main.gif" alt="Project demonstration" width="82%">
</p>

<p align="center">
  <img src="images/main_black.png" alt="Application dark theme" width="46%">
  <img src="images/overall-usage.png" alt="Application overview" width="46%">
</p>

✨ Overview
This project explores a traffic-monitoring workflow using video/image processing, vehicle classification, violation rules, and a graphical user interface. The original project documentation describes three violation categories:
- 🚦 Signal violation — detecting a vehicle crossing a configured line during a red signal.
- 🅿️ Parking violation — flagging a vehicle that remains in a configured restricted area beyond a defined time.
- ↔️ Wrong-direction violation — using vehicle positions over time to identify movement against a configured direction.
⚠️ Project status: The original documentation labels this as an initial release and notes that not everything is complete. Treat it as an experimental/learning project, not a validated traffic-enforcement system. Detection accuracy and runtime behavior must be tested before making performance claims.

🧰 Tech Stack
Technology	Purpose
🐍 Python	Main application language
👁️ OpenCV	Image and video processing
🧠 TensorFlow / MobileNetV1	Vehicle-classification approach described in the original documentation
🖥️ PyQt5	Desktop graphical interface
🗃️ SQLite	Store vehicle, rule, camera, and violation records
🎨 QDarkStyle	Dark GUI styling


⚙️ How It Works
1. 🎥 Input: Read video footage from a configured camera/feed.
2. 🧹 Preprocessing: Apply grayscale conversion, Gaussian blur, background subtraction, thresholding, and contour detection.
3. 🚗 Vehicle classification: Classify detected moving objects using the model described in the source documentation.
4. 📐 Rule checks: Evaluate configured signal-line, parking-zone, or direction rules.
5. 🗄️ Record keeping: Store relevant records in an SQLite database.
6. 🖥️ Review: Use the desktop interface to inspect camera feeds and recorded violation details.
<p align="center">
  <img src="images/system.png" alt="System overview" width="75%">
</p>

🖼️ Application Screenshots
<p align="center">
  <img src="images/fig2.png" alt="Main application interface" width="46%">
  <img src="images/fig3.png" alt="Camera configuration interface" width="46%">
</p>
<p align="center">
  <img src="images/fig4.png" alt="Violation records" width="46%">
  <img src="images/detail.png" alt="Violation detail view" width="46%">
</p>

🚀 Getting Started
Prerequisites
- Python installed on your system
- Git
- The project dependencies listed in requirements.txt
- Any model files and sample video assets required by the application
Installation
1. Clone your GitHub repository (replace the URL with your repository URL):
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   cd YOUR-REPOSITORY
2. Create and activate a virtual environment.
   Windows (PowerShell):
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   macOS / Linux:
   python3 -m venv .venv
   source .venv/bin/activate
3. Install dependencies:
   python -m pip install -r requirements.txt
4. Start the application (if the entry point and required assets are present):
   python main.py
🛠️ Dependency versions, model files, and camera/video configuration may require additional setup. If startup fails, check the error message and project issues before assuming the application is fully configured.

🗂️ Main Components
- Image processing: Preprocessing and extracting moving-object contours from frames.
- Vehicle classification: The source documentation describes a MobileNetV1-based classifier trained with transfer learning.
- Violation logic: Configurable checks for signal, parking, and direction violations.
- Database: SQLite records for cars, rules, cameras/groups, and violations.
- Desktop GUI: PyQt5 interface for configuring inputs and reviewing records.
🔭 Possible Improvements
- ✅ Add automated tests for violation-detection rules.
- 📊 Measure precision, recall, and false-positive rates on a documented test set.
- 🧪 Add sample input videos and reproducible test instructions where licensing permits.
- 🔒 Improve configuration handling and avoid storing sensitive data in source code.
- 📦 Pin dependency versions and document model-weight setup.
- 📝 Record the changes and features contributed by each maintainer.
🤝 Contributing
Contributions can be made through issues and pull requests. Before submitting changes, explain the problem, describe the change, and include steps to test it.
🙏 Credits & Attribution
This README is a cleaned-up presentation of the project documentation supplied with the source. The original project credits Rahat Zaman and Sakib Reza, with supervision credited to Dr. Sk. Mohammad Masudul Ahsan. Please retain the original license and attribution notices when redistributing or modifying the code.
- 🔗 Original project: Traffic Rules Violation Detection
- 📚 The original repository documents a GNU GPLv3 license. Check the included LICENSE file to confirm the license terms for this copy.
<div align="center">

⭐ If you find this project useful for learning, consider starring the repository.

Built for learning and experimentation — not a substitute for validated traffic-enforcement technology.
</div>
