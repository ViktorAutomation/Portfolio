# Construction Project Management System  
**Monday.com + Make.com**

An end-to-end **project responsibility management system** built in **Monday.com** and powered by **Make.com**.  
It replaces a massive Excel responsibility matrix with a structured, automated engine where roles are defined once and applied to **600+ project tasks** automatically.

---

## 🔍 Project Overview

This solution replaces a large, manual responsibility spreadsheet with a **role-driven project engine** inside Monday.com.

Key elements:

- A **Main Project Board** where 10–12 key roles are defined once per project  
- A **Project Template Board** with 600+ tasks mapped to roles and responsibility types (P/C/R/W/I)  
- Make.com scenarios that:
  - Create full execution boards from the template  
  - Distribute people into all tasks based on role assignments  
  - Reassign owners across the entire project from a single status change  

Previously, every change in roles or owners required manual updates across **hundreds of rows** in a static spreadsheet.

---

## 🎯 Problem & Goals

Previously:

- Responsibilities for **600+ tasks** were managed in a **static Excel matrix**  
- Every change to a role (e.g., new CX Provider, new Owner PM) meant **touching hundreds of cells**  
- P / C / R / W / I assignments (Primary, Coordinator, Reviewer, Witness/Monitor, Inspector) had to be maintained manually  
- There was no simple way to:
  - Assign people at the **role level**, then reuse them across all tasks  
  - Quickly **reassign responsibilities** when people changed  

**Goals:**

- Let the client **assign people to roles once** (Owner PM, Owner Inspectors, CX Provider, Architect, GC PM, subs, etc.) and distribute them automatically to all related tasks  
- Reassign responsibilities across the entire project by **changing a single role assignment**  
- Preserve a clear, auditable responsibility model (**P/C/R/W/I**) per task  
- Build a **reliable, scalable project engine** where responsibilities are driven by role definitions, not manual, cell-by-cell edits  

---

## 🧩 Solution & Workflow

### 1. Main Project Board (Project Hub)

A central **Main Project Board** in Monday.com, with one item per project:

- **Status column** (e.g., `Create project`, `Reassign owners`) to drive automation  
- **Subitems** for the 10–12 key roles, such as:
  - Owner PM  
  - Owner Inspectors  
  - CX Provider  
  - Architect  
  - GC PM  
  - Various subcontractors and specialists  
- **People/contact columns** where exactly one person per role is assigned for that project  

This board is the **source of truth** for “who is in which role” for each project.

---

### 2. Project Template Board (Responsibility Matrix)

A preconfigured **Project Template Board** representing the full responsibility matrix (~600 tasks):

- Each item mirrors a task from the **legacy Excel matrix**, including original IDs  
- Role columns define which roles are involved and their responsibility type:
  - **P** – Primary  
  - **C** – Coordination  
  - **R** – Review Documentation  
  - **W** – Witness/Monitor  
  - **I** – Inspect  
- Roles are stored in a **normalized structure** (columns/subitems) so automations can process them efficiently  

Every new project execution board is created from this template.

---

### 3. Make.com – Project Creation & Role Distribution

**Trigger:** The project status on the Main Project Board changes to **“Create project”**.

The Make.com scenario:

1. **Creates a new project board** from the Project Template Board (all 600+ tasks included).  
2. **Renames the new board** to match the project name from the Main Project Board.  
3. **Reads role assignments** from the project’s subitems on the main board  
   (e.g., Owner PM = Sam Jones, Owner Inspector = Руслан, CX Provider = a specific consultant).  
4. Iterates through all tasks and subitems on the new project board and, for each role:
   - Finds where that role is marked as **P, C, R, W, or I**  
   - Writes the correct person into the corresponding people/owner column  
     (e.g., `Owner PM – Primary`, `CX Provider – Coordinator`)  
5. Completes with a fully prepared execution board where **all 600+ tasks are populated** with the right people per responsibility type — with **no manual editing**.

---

### 4. Make.com – Owner Reassignment Across the Project

**Trigger:** The project status on the Main Project Board changes to **“Reassign owners”**.

The Make.com scenario:

1. Reads the **updated role assignments** on the Main Project Board (who is now Owner PM, CX Provider, etc.).  
2. Locates the corresponding **execution project board** previously created from the template.  
3. Scans all tasks and subitems where each role appears and:
   - Updates the people/owner columns to the **new person** for that role and responsibility type  
4. Ensures that a **single change** (e.g., new CX Provider) cascades through:
   - All related tasks  
   - All P/C/R/W/I columns  
   - The entire project structure  

This removes the need to manually touch hundreds of records when someone in a key role changes.

---

### 5. Responsibility Model & Transparency

The original P/C/R/W/I legend from the legacy spreadsheet is fully preserved:

- **P** – Primary Responsibility  
- **C** – Coordination  
- **R** – Review Documentation  
- **W** – Witness / Monitor  
- **I** – Inspect  

Design highlights:

- Roles (Owner PM, CX Provider, etc.) are **decoupled from people** – stored as role definitions and linked via automation.  
- Changing **who occupies a role** is safe and fast; the responsibility model remains stable.  
- Each task clearly displays **who does what** using P/C/R/W/I assignments.  
- Progress can be **aggregated by group or role**, giving leadership a high-level view across all responsibilities.

---

## 🛠 Tools & Technologies Used

- **Monday.com** – Main Project Board, Project Template Board, status-driven triggers, people columns  
- **Make.com (Integromat)** – project board creation, role distribution, and bulk owner reassignment  
- **Legacy Excel Responsibility Matrix** – original source for the task list and P/C/R/W/I structure  

---

## 📈 Results & Impact

- **Massive time savings:** Replaced a 600+ row manual spreadsheet with a fully automated, role-driven system.  
- **Error reduction:** Eliminated manual cell-by-cell edits when people change roles.  
- **True “define once, apply everywhere” roles:** One change in the Main Project Board updates responsibilities across the entire execution board.  
- **Transparency:** Every task shows clear P/C/R/W/I assignments, improving accountability and communication.  
- **Scalability:** New projects, roles, or stakeholders can be added without reworking the entire matrix.

---

## 🖼 Screenshots

> (Add your screenshots in this format once ready, for example:)

**Main Project Board – Role Assignments**  
![Main Project Board](LINK-TO-IMAGE)

**Project Template Board – Responsibility Matrix (600+ Tasks)**  
![Project Template Board](LINK-TO-IMAGE)

**Make.com Scenario – Project Creation & Role Distribution**  
![Project Creation Scenario](LINK-TO-IMAGE)

**Make.com Scenario – Owner Reassignment Across the Project**  
![Owner Reassignment Scenario](LINK-TO-IMAGE)
