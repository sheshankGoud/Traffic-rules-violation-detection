# Traffic Rules Violation Detection

A Python desktop application concept for reviewing traffic footage and recording potential traffic-rule violations. The project uses a PyQt5 graphical interface, OpenCV-based video/image processing, and SQLite for records.

> **Attribution:** This repository is based on the open-source project by Rahat Zaman and Sakib Reza: https://github.com/rahatzamancse/Traffic-Rules-Violation-Detection. The original project README describes it as an initial, incomplete release. Preserve the original GPL-3.0 license and attribution. Do not present the original implementation as entirely your own. Document any changes you personally make below.

## Features described by the original project

- Desktop interface built with PyQt5
- SQLite database for vehicles, rules, cameras, and violation records
- Video/image processing using OpenCV
- Workflows for signal, parking, and wrong-direction violation scenarios
- Search and archive interfaces for stored records

**Important:** These are features described by the source project; they have not all been independently tested in this packaged copy. Treat detection results as experimental, not as proof of an actual legal violation.

## Technology stack

- Python
- OpenCV (`opencv-python`)
- PyQt5
- SQLite
- imutils
- QDarkStyle (listed in the original requirements)

## Project structure

```text
.
├── main.py
├── MainWindow.py
├── Database.py
├── Archive.py
├── SearchWindow.py
├── DetailLogWindow.py
├── ViolationItem.py
├── add_windows/
├── processor/
├── UI/
├── database/
│   ├── ddl.sql
│   └── traffic.db
├── images/
├── requirements.txt
└── LICENSE.txt
```

## Setup

Use a virtual environment. The dependency pins in the original project are old and may not install cleanly on current Python versions, so test in a compatible environment and update dependencies deliberately rather than blindly upgrading them.

### Windows (PowerShell)

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install --upgrade pip
pip install -r requirements.txt
python main.py
```

If PowerShell blocks activation, use Command Prompt and run `.venv\Scripts\activate.bat`, or invoke `.venv\Scripts\python.exe` directly.

## Known limitations / next steps

- This is a legacy desktop application; verify installation and runtime behavior before claiming it works on your machine.
- The original release is marked incomplete.
- Large demo video files were omitted from this GitHub-ready package to keep the repository lightweight. Add only videos you own or are licensed to redistribute, preferably using Git LFS or external hosting for large files.
- Add screenshots from a successful local run, tests, and a record of your own contributions.
- Review data and database contents before making the repository public. Do not upload personal data, credentials, or private footage.

## My contributions

Add only work you personally complete. For example:

- [ ] Set up and tested the project locally
- [ ] Fixed documented installation/runtime issues
- [ ] Added or improved a feature: _describe it_
- [ ] Added tests or sample results: _describe them_

## License and attribution

The source project states that it is licensed under GNU GPL v3. See [`LICENSE.txt`](LICENSE.txt) and the original repository for the full context and attribution.
