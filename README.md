# VFlow

![Status](https://img.shields.io/badge/Status-In%20Setup-blue)
![.NET](https://img.shields.io/badge/.NET-9-purple)
![Angular](https://img.shields.io/badge/Angular-18-red)
![C#](https://img.shields.io/badge/C%23-12-blueviolet)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-blue)

## 📋 Project Description

**VFlow** is a modern, integrated agile project management platform designed for students, researchers, and small teams. The goal is to provide the visual flexibility of a **Kanban board** and the structured power of **Scrum** in a lightweight, intuitive, and collaborative web application.

The project is built as a full-stack application, featuring a secure and scalable backend API using **.NET 9** with **Clean Architecture**, and a dynamic, real-time frontend built with **Angular 18**. A key feature is its deep integration with the Google Workspace ecosystem, allowing users to authenticate, attach files from Google Drive, and create meetings in Google Calendar seamlessly.

## 🚀 Project Status

**Last Updated:** 2025-10-05

The project is currently in the **initial setup and foundation phase**. The core architecture for the backend and frontend has been defined, and the initial project structures have been created.

### ✨ Main Features (Planned)

* **Google-Only Authentication:** Secure and simple sign-up/login process exclusively through Google accounts (OAuth 2.0).
* **Kanban Board Management:** Create custom boards, columns, and cards with a fluid drag-and-drop interface.
* **Real-Time Collaboration:** Changes made by one user (e.g., moving a card) will be reflected instantly for all other team members on the same board, powered by **SignalR**.
* **Scrum Methodology Support:** Manage projects with Sprints, backlogs, and story points.
* **Calendar View:** Visualize tasks and deadlines in an integrated calendar.
* **Google Drive Integration:** Attach files directly from Google Drive to tasks/cards.
* **Google Calendar Integration:** Create meetings associated with tasks and add them directly to your Google Calendar.

---

## 🏛️ Project Architecture

VFlow is architected as a decoupled full-stack application, ensuring a clear separation of concerns between the backend API and the frontend client.

### Backend (.NET 9 - Clean Architecture)

The backend follows the **Clean Architecture** principles, separating the project into four distinct layers to ensure maintainability, testability, and independence from external frameworks.

* **`Domain`** Contains the core business entities (e.g., `Card`, `Board`) and domain logic. It has no dependencies on other layers.
* **`Application`:** Orchestrates the business logic and use cases. It depends only on `Core`.
* **`Infrastructure`:** Handles implementation details like database access (EF Core), external API integrations (Google APIs), and other services. It depends on `Application`.
* **`API`** Exposes the application's functionality through a RESTful API. It is the entry point of the application and depends on `Application`.

**Dependency Flow:** `API` -> `Application` -> `Core` <- `Infrastructure`

### Frontend (Angular 18)

The frontend is a **Single-Page Application (SPA)** built with Angular, organized into feature modules to support scalability and lazy loading.

* **`CoreModule`:** Provides singleton services like `AuthService` and HTTP interceptors.
* **`SharedModule`:** Contains reusable components, directives, and pipes.
* **Feature Modules:** Each major feature (e.g., `Board`, `Auth`, `Calendar`) will have its own lazy-loaded module to optimize application loading times.

---

## 🔧️ Technologies

* **Backend:** C# 12, .NET 9, ASP.NET Core Web API
* **Frontend:** Angular 18, TypeScript 5.x
* **Real-Time:** ASP.NET Core SignalR
* **Database:** PostgreSQL, Entity Framework Core 9
* **Authentication:** OAuth 2.0 (Google Identity)
* **UI Components:** Angular Material
* **Architecture:** Clean Architecture (Backend), Modular (Frontend)
* **IDE:** JetBrains Rider

---

## 🛣️ Development Roadmap

The project will be developed in iterative sprints, focusing on delivering value incrementally.

<details>
<summary><b>Sprint 0: Foundation & Setup (Completed)</b></summary>

* [x] Define project architecture for backend and frontend.
* [x] Create solution and project structures.
* [x] Set up initial Git repository.

</details>

<details>
<summary><b>Sprint 1: Core Authentication & Main Structure</b></summary>

* [ ] Implement Google OAuth 2.0 for user sign-up and login.
* [ ] Generate JWT tokens for managing user sessions.
* [ ] Create protected routes and a basic authenticated dashboard view.
* [ ] Set up the main application layout (header, sidebar).

</details>

<details>
<summary><b>Sprint 2: The Kanban Heart</b></summary>

* [ ] Implement CRUD functionality for boards, columns, and cards.
* [ ] Develop the drag-and-drop interface for moving cards.

</details>

<details>
<summary><b>Sprint 3: Real-Time Collaboration</b></summary>

* [ ] Integrate SignalR for real-time updates on the Kanban board.
* [ ] Implement workspace and team member management.

</details>

<details>
<summary><b>Sprint 4: Scrum & New Views</b></summary>

* [ ] Add support for Sprints, backlogs, and story points.
* [ ] Implement the calendar view for tasks.

</details>

<details>
<summary><b>Sprint 5: Productivity Integrations</b></summary>

* [ ] Implement Google Drive integration for file attachments.
* [ ] Implement Google Calendar integration for meeting creation.

</details>

---

## ⚙️ Setup & How to Run

> ⚠️ **Note:** Instructions will be updated as the project progresses.

---

## 📄 License

This project is licensed under the MIT License - see the `LICENSE` file for details.