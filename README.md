# CivicDesk – Smart Community Service Management System

CivicDesk is a comprehensive smart community service management platform designed to streamline how citizens report local civic issues, administrators manage and assign tasks, and service staff resolve infrastructure and neighborhood complaints[cite: 1, 2]. 

This project is built from rigorous system analysis, featuring complete **Data Flow Diagrams (Levels 0, 1, and 2)** and **UML Specifications (Use Case, Class, Sequence, and State Machine diagrams)**[cite: 2].

---

## 🏗️ System Architecture & Design

The platform architecture is modeled after structured systems analysis and design principles:
* **Data Flow Diagrams (DFD):** 
  * *Level 0 (Context):* Maps external entities (Citizen, Administrator, Service Staff) interacting with the core CivicDesk system[cite: 2, 3].
  * *Level 1 & 2:* Breaks down subsystems into granular processes such as account management, complaint validation, image/GPS processing, task tracking, and notification logging[cite: 3, 4].
* **UML Diagrams:**
  * *Use Case Diagram:* Defines functional boundaries for Citizens, Administrators, and Service Staff[cite: 5].
  * *Class Diagram:* Details domain classes including `User`, `Citizen`, `Administrator`, `ServiceStaff`, `Complaint` (with geographic attributes like `latitude`, `longitude`, and `locationText`), `Category`, `Attachment`, `StatusUpdate`, `Feedback`, and `Notification`[cite: 5].
  * *Sequence Diagram:* Illustrates the primary messaging sequence from complaint submission to assignment, resolution, and rating[cite: 6].
  * *State Machine Diagram:* Implements the complete complaint lifecycle[cite: 7].

---

## 🔄 Complaint Lifecycle & States

CivicDesk manages issues through a robust 6-state machine workflow[cite: 7]:
1. **Submitted:** Initial state when a citizen files a complaint[cite: 7].
2. **Assigned:** Task assigned by an administrator to a specialized service staff member[cite: 7].
3. **In progress:** Service staff has started working on the issue[cite: 7].
4. **Resolved:** Work has been completed by staff[cite: 7].
5. **Rejected:** Marked by admin if the complaint is invalid or a duplicate[cite: 7].
6. **Closed:** Final state after citizen rating or automatic timeout[cite: 7]. 
*(Note: Citizens can also trigger a **reopen** path from `Resolved` back to `In progress` if unsatisfied[cite: 7]).*

---

## 👥 Staff & Department Mapping

To match community service domains, the system assigns specialized staff across all 6 service categories[cite: 1]:
* **Roads & Potholes:** R. Mukherjee[cite: 1]
* **Waste & Sanitation:** P. Sen[cite: 1]
* **Water & Drainage:** A. Khan[cite: 1]
* **Streetlights:** S. Roy
* **Parks & Public Space:** M. Das
* **Other / General:** V. Sharma

---

## ✨ Core Features

* **Multi-Role Dashboard:** Seamlessly switch between *Citizen*, *Administrator*, and *Service Staff* roles to test end-to-end workflows[cite: 1].
* **GPS & Multimedia Geotagging:** Pin precise latitude and longitude coordinates or attach photographic evidence when submitting complaints[cite: 1, 5].
* **Department-Matched Assignment:** Administrators receive department-match highlights (`★ Dept Match`) to assign tasks to the correct specialized staff member[cite: 1].
* **Feedback & Rating System:** Citizens can rate resolved fixes from 1 to 5 stars with custom feedback notes[cite: 1].
* **Real-time Notifications:** In-app notification alerts track status transitions across user roles[cite: 1].

---

## 🚀 Getting Started

Since CivicDesk is implemented as a self-contained, high-performance single-file web prototype, no complex backend setup or database installation is required to view or test it.

1. Download or clone the repository.
2. Open the `CivicDesk – Smart Community Service Management.html` file in any modern web browser.
3. Use the role switcher buttons in the header to navigate between **Citizen**, **Admin**, and **Staff** views[cite: 1]. Data is automatically persisted locally using browser `localStorage`.
