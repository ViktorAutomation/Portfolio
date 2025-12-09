# Construction Project Management System
**Monday.com + Make.com**

## Project Overview

This project delivers an end-to-end **project responsibility management system** built on Monday.com, with Make.com handling all automation between a **high-level project board** and detailed **project/task boards**.

Instead of maintaining a huge, manual responsibility matrix in Excel, the client now uses:

- A **single project hub** in Monday.com to define 10–12 key project roles once per project.
- An **automated project board** with **600+ activities**, where responsibilities are auto-filled based on those roles.
- A **one-change update model** — reassigning a role in the main board instantly updates all related tasks across the entire project.

## Problem & Goals

The client needed a robust way to manage a complex project responsibility model across hundreds of tasks and many stakeholders, without repetitive manual updates.

Key challenges:

- A **static spreadsheet** where every P / C / R / W / I assignment (Primary, Coordinator, Reviewer, Witness/Monitor, Inspector) had to be updated **cell-by-cell**.
- **600+ tasks** that needed to be kept in sync every time a role owner changed.
- Multiple stakeholders (Owner PM, Owner Inspectors, CX Provider, Architect, GC PM, subcontractors, etc.) who needed clear, consistent responsibility mapping.
- No easy way to **reassign responsibilities** when a person in a key role changed.

Goals:

- Let the client **assign people once per role** (e.g., Owner PM, CX Provider) and automatically distribute them to all related tasks.
- Enable **fast reassignment** when a role changes, without touching hundreds of rows.
- Maintain a clear, auditable view of **who is P, C, R, W, or I** on each task.
- Build a reliable, scalable **project engine** where responsibilities are driven by role definitions, not manual edits.

## Solution & Workflow

### 1. Structured Monday.com Boards

Two main boards form the backbone of the system:

#### Main Project Board (Project Hub)

Central list of all projects, each represented as a single item:

- **Status column** (e.g., “Create project”, “Reassign owners”) to drive automation.
- **Subitems for 10–12 roles**, such as:
  - Owner PM  
  - Owner Inspectors  
  - CX Provider  
  - Architect  
  - GC PM  
  - Various subcontractors and specialists
- **People/contact columns** where exactly one person per role is assigned for that project.

This board acts as the **source of truth** for “who is in which role” per project.

#### Project Template Board (Responsibility Matrix)

A preconfigured Monday.com board that represents the full responsibility matrix (~600 tasks):

- Each item mirrors the original spreadsheet task and **legacy task ID**.
- Role columns define which roles are involved and **what responsibility type** they hold: P, C, R, W, I.
- Roles are stored in a **normalized structure** (via subitems/columns) so that automations can process them efficiently.

This template is used as the **blueprint** for every new project board.

---

### 2. Make.com Scenarios (Automation Backbone)

Two core Make.com scenarios orchestrate the flow between the main board and project boards.

#### a) Project Creation & Role Distribution

**Trigger:** Project status on the main board changes to **“Create project”**.

The scenario:

1. **Creates a new project board** from the Project Template Board with all tasks and role mappings included.
2. **Renames the new board** to match the project name from the main board.
3. **Reads role assignments** from the project’s subitems on the main board  
   (e.g., Owner PM = Sam Jones, Owner Inspector = Руслан, CX Provider = specific consultant).
4. Iterates through all tasks and subitems on the new project board and, for each role:
   - Finds where that role is marked as **P, C, R, W, or I**.
   - Writes the correct person into the corresponding people/owner column  
     (e.g., “Owner PM – Primary”, “CX Provider – Coordinator”).
5. Completes with a project board where **all 600+ tasks are fully populated** with the right people per responsibility type — **without manual edits**.

#### b) Owner Reassignment Across the Project

**Trigger:** Project status on the main board changes to **“Reassign owners”**.

The scenario:

1. Reads the **updated role assignments** on the main board (e.g., new CX Provider, new Owner PM).
2. Finds the corresponding **execution project board** that was created from the template.
3. Scans all tasks and subitems where each role appears and:
   - Updates the people/owner columns to the **new person** for that role and responsibility type.
4. Ensures that a **single change in the main board** (e.g., replacing the CX Provider) cascades through:
   - All tasks  
   - All responsibility types (P, C, R, W, I)  
   - The entire project structure

No manual edits on individual tasks are required.

---

### 3. Responsibility Model & Transparency

The system preserves the original responsibility legend from the legacy spreadsheet:

- **P** – Primary Responsibility  
- **C** – Coordination  
- **R** – Review Documentation  
- **W** – Witness / Monitor  
- **I** – Inspect  

Key design principles:

- Roles (Owner PM, CX Provider, etc.) are **stored separately from people**, and linked through automation.
- Changing **who occupies a role** is simple and safe – the system updates all related tasks automatically.
- Each task clearly shows **who does what** using the P/C/R/W/I model.
- Overall status can be aggregated at **group or subitem level**, giving a high-level view of progress across roles and workstreams.

This design keeps the **responsibility model stable** while allowing people to change with minimal effort.

## Tools & Technologies Used

- **Monday.com** – main project hub, role definitions, project template board, status-driven triggers.
- **Make.com (Integromat)** – automation layer for project board creation, role distribution, and mass reassignment.
- **Legacy Excel Responsibility Matrix** – original task list and P/C/R/W/I structure used as the source for the template logic.

## Results & Outcomes

- **Replaced a 600+ row manual spreadsheet** with a scalable, automated project engine.
- **Eliminated repetitive data entry** when assigning or reassigning responsibilities.
- Enabled role-based changes where **one update in the main board** instantly propagates through the entire project.
- Maintained a clear, auditable responsibility model (P/C/R/W/I) for every task.
- Gave project leadership a **central, reliable view** of who owns what, while reducing risk of human error.

