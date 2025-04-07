# 📟 Contribution Report - Hardik Vaghasiya

## 👤 Member: Hardik Vaghasiya
**Email:** vaghasiya.hardik2001@gmail.com  
**Role:** Full-stack Developer (Frontend + Backend)

---

## ✅ Major Responsibilities & Contributions

### 🔐 1. Google Authentication & Role-Based Access
- Integrated **Google Login** functionality using `@react-oauth/google`.
- Implemented **role-based redirection** to different dashboards (Admin, Team Lead, Team Member) based on authenticated email.
- Stored user details and role in **localStorage** for persistent login session.
- Ensured security and clean logout functionality.

### 🧑‍💼 2. Team Lead Dashboard
- Developed a full-featured **Team Lead Dashboard** with multiple cards for actions:
  - **Create Task**: Inline task creation with dynamic input and calendar.
  - **Assign Task**: Dropdown-based team member selection with reassignment option.
  - **View All Tasks**: Included advanced filters for priority, status, and assignee.
- Ensured modular component structure and responsive layout.

### 📧 3. Email Notifications
- Integrated **Nodemailer** to send email notifications on task assignment and reassignment.
- Triggered email logic on task creation and status change using backend logic.
- Verified real-time notification delivery for successful task collaboration.

### 📊 4. Task Distribution Visualization
- Built **Pie Chart** using `Recharts` to visualize task status (To Do, In Progress, Completed).
- Implemented **PDF Export** feature with `html2canvas` and `jsPDF` for reporting needs.
- Created visually appealing purple-themed chart layout with legends and labels.

### 💬 5. Commenting Feature (Team Member)
- Developed **comment submission form** within the Team Member Dashboard.
- Connected backend endpoint for adding and saving comments.
- Displayed timestamped comments per task using structured component rendering.

### 🧪 6. Design Patterns Implementation
- Applied **Strategy Pattern**:
  - Calculated task priority dynamically based on user input, deadline, or mocked AI logic.
- Applied **Decorator Pattern**:
  - Added metadata (like urgency tags) to each task before sending to frontend for display.
- Initialized structure for **Command Pattern** (to modularize future status updates and undo logic).
- Ensured real-world pattern demonstration for bonus marks and scalability.


---

## 🛠️ Technologies & Tools Used

### Frontend:
- **React.js**
- **Axios**, **Recharts**
- **Tailwind CSS**, CSS Modules
- **html2canvas**, **jsPDF** (PDF export)

### Backend:
- **Node.js**, **Express.js**
- **MongoDB**, **Mongoose**
- **Nodemailer**, **dotenv**

### Testing & Auth:
- **Jest**, **Supertest**
- **@react-oauth/google** (Google Login)

---

## 🧱 Other Contributions
- Structured folders and files for **clear frontend/backend separation**.
- Assisted with **Kanban board layout and filtering logic**.
- Debugged several **API and routing issues**.
- Maintained clean Git commit history with **descriptive messages**.
- Collaborated regularly with team for **code reviews and troubleshooting**.

---

## 🔹 Summary (Bullet Form)
- Built **Google OAuth login** and **role-based routing**.
- Developed full **Team Lead Dashboard** with create/assign/view tasks.
- Added **task email notifications** using Nodemailer.
- Designed **Pie chart + PDF export** for task visualization.
- Implemented **commenting** and **task filtering**.
- Integrated **Strategy and Decorator Design Patterns**.
- Contributed to UI/UX and backend logic for task workflow.
- Focused on **real-world maintainability and usability**.



