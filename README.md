# **Virtualization Quiz App** 🧠  
A **Python Tkinter-based Quiz Application** with **SQLite database**, **timer**, **CSV export**, and **CRUD support** for managing quiz questions.

---

## **📌 Features**
✅ **Interactive GUI** built using **Tkinter**  
✅ **SQLite database** for storing questions & answers  
✅ **Timer** ⏳ for each question (default: 15 seconds)  
✅ **Color-coded answers** 🎨  
   - 🟢 Correct answers → Green  
   - 🔴 Wrong answers → Red  
✅ **Student name & roll number input**  
✅ **Automatic score calculation** 🏆  
✅ **Download results as CSV**  
✅ **CRUD-ready database** — manage questions easily  
✅ **Package as `.exe`** for sharing with others

---

## **📂 Project Structure**
```
quiz_app.py        # Main application file
quiz.sqlite        # SQLite database (auto-created on first run)
quiz_results.csv   # Exported quiz results (optional, generated on demand)
README.md          # Documentation
```

---

## **🛠️ Installation Guide**

### **Step 1 — Install Python**
Download and install **Python 3.12.x** (recommended):  
🔗 [https://www.python.org/downloads/](https://www.python.org/downloads/)

During installation:
- ✅ Check **"Add Python to PATH"**  
- ✅ Enable **pip** installer

Verify installation:
```bash
python --version
```

---

### **Step 2 — Clone or Download the Project**
```bash
git clone https://github.com/your-username/quiz-app.git
cd quiz-app
```
Or simply download the project ZIP and extract it.

---

### **Step 3 — Install Required Packages**
```bash
pip install tk
```
> **Note**: SQLite is built into Python, no installation required.

---

### **Step 4 — Run the App**
```bash
python quiz_app.py
```

---

## **🎮 How to Use the App**

### **1️⃣ Student Login**
- Enter **Student Name** 🧑‍🎓
- Enter **Roll Number**
- Click **“🚀 Start Quiz”**

---

### **2️⃣ Answer Questions**
- The app displays **one question at a time**.
- Choose the correct option.
- A **timer** counts down (default: 15s per question).
- **Color feedback**:
    - 🟢 **Correct** → Button turns **green**
    - 🔴 **Wrong** → Button turns **red**

---

### **3️⃣ Quiz Completion**
- Displays **final score** → `Your Score / Total Questions`
- Options:
    - ⬇️ **Download Results** → Saves `quiz_results.csv`
    - 🔄 **Restart Quiz**

---

### **4️⃣ Manage Questions (CRUD)**
- Click **“🛠 Manage Questions”**.
- Opens **SQLite database** directly.
- You can **add, edit, delete** questions manually using **DB Browser for SQLite**.  
  🔗 [https://sqlitebrowser.org/](https://sqlitebrowser.org/)

---

## **🗄️ Database Structure**
**Database Name:** `quiz.sqlite`

### **Table: questions**
| Column | Type    | Description         |
|--------|---------|---------------------|
| id     | INTEGER | Question ID         |
| text   | TEXT    | Question text       |

### **Table: answers**
| Column      | Type    | Description             |
|------------|---------|-------------------------|
| id         | INTEGER | Answer ID               |
| question_id| INTEGER | Linked Question ID      |
| text       | TEXT    | Answer text             |
| correct    | INTEGER | 1 = Correct, 0 = Wrong  |

---

## **📤 Exporting Results**
- After quiz completion, click **⬇️ Download Results**.
- Creates `quiz_results.csv`:
```csv
Student Name,Roll Number,Score,Total Questions
Logesh,21CS001,4,5
```

---

## **📦 Creating an Executable (.exe)**

You can package the app into a **standalone executable** so others can run it **without Python**.

### **Step 1 — Install PyInstaller**
```bash
pip install pyinstaller
```

### **Step 2 — Build the .exe**
```bash
pyinstaller --onefile --noconsole quiz_app.py
```

### **Step 3 — Find Your Executable**
The `.exe` file will be inside:
```
dist/quiz_app.exe
```
You can now **share it with anyone**. 🎉

---

## **⚠️ Error Handling**
- **Database not found** → Auto-created on first run.
- **No questions available** → App warns you.
- **Missing student info** → Prompts to enter Name & Roll No.
- **Timer expired** → Moves to next question automatically.
- **CSV export issues** → App shows error message if file saving fails.

---

## **📌 Future Enhancements**
- CRUD panel **inside Tkinter** (Add/Edit/Delete without SQLite browser)
- Leaderboard system 🏆
- Web version using **Flask + HTML/CSS/JS**
- Dark/Light mode support 🌙

---

## **👨‍💻 Author**
**Logesh**  
_Aspiring Full Stack Developer_
