# RebootManager Frontend

The **frontend application for RebootManager**, built with **Angular 19** and **TailwindCSS**.

The application provides a dashboard for monitoring and analyzing machine reboot activity. It consumes the Spring Boot backend API to display processed reboot data, monitor reboot status, and provide different views and functionalities depending on the user's role.

## Features

- Interactive monitoring dashboard
- Visualization of machine reboot activity
- Display of rebooted and postponed machines
- Role-based views for Managers and Technicians
- Authentication and authorization
- Integration with the Spring Boot backend REST API
- Responsive user interface
- TailwindCSS-based styling

## Technologies Used

- Angular 19.2.8
- TypeScript
- TailwindCSS
- HTML / CSS
- Node.js
- npm

## Project Architecture

The frontend acts as the presentation layer of the RebootManager system:

```text
                 Spring Boot Backend
                         │
                         │ REST API
                         ▼
              ┌─────────────────────┐
              │  Angular Frontend   │
              │                     │
              │  Authentication     │
              │  API Services       │
              │  Dashboard          │
              │  Data Visualization │
              │  Role-based Views   │
              └─────────────────────┘
                         │
                         ▼
                 End User Interface
```

The frontend consumes the processed data provided by the backend pipeline and presents it through a centralized monitoring interface.

## Getting Started

### Prerequisites

Make sure the following are installed:

- [Node.js](https://nodejs.org/) (v16+ recommended)
- [Angular CLI](https://angular.dev/tools/cli)
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/ElMehdiEssakhi/RebootManagerFrontEnd.git

cd RebootManagerFrontEnd
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure the Backend API

The frontend communicates with the Spring Boot backend through REST APIs.

If the backend API URL changes, update the corresponding services:

```text
src/app/services/api.service.ts
src/app/services/auth.service.ts
```

Make sure the Spring Boot backend is running and accessible before using the application's API-dependent features.

### 4. Run the Development Server

```bash
ng serve
```

Then open your browser at:

```text
http://localhost:4200
```

The application will automatically reload when source files are modified.

## TailwindCSS

TailwindCSS is already configured in the project. No additional configuration is required after installing the project dependencies:

```bash
npm install
```

## Project Purpose

The RebootManager frontend provides the user interface for a **data engineering and monitoring system** that processes machine reboot logs.

The backend pipeline cleans and parses raw reboot logs, extracts relevant information, and analyzes reboot activity. This frontend consumes the resulting data and presents it through dashboards and role-based interfaces, allowing users to monitor machine reboot status and identify machines that require attention.
