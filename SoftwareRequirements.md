# Software Requirements Specification (SRS) - AZ Education

This document outlines the software requirements for the AZ Education project, focusing on the functional and non-functional aspects as validated by the Acceptance Test Report.

## 1. Introduction

### 1.1 Purpose
This SRS details the requirements for AZ Education, a mobile e-learning application supported by a microservice backend and an admin panel. It serves as a foundational document for understanding the system's intended behavior and capabilities.

### 1.2 Scope
AZ Education is a Flutter mobile application backed by a Go microservice architecture that streams educational videos, delivers flashcard-based homework, and exposes a React-Admin web panel for course management. Manual subscription via Telegram is supported. Online payments are deferred to a future release (Version 2).

## 2. Functional Requirements

The following vital processes and functionalities are required and implemented:

* **User Authentication:** Users must be able to register, log in, and log out securely.
* **Secure Adaptive Video Streaming:** The system must deliver educational video content securely and adaptively.
* **Flashcard Homework Flow:** Users must be able to access and complete flashcard-based homework assignments using a spaced repetition algorithm (SM-2).
* **Manual Subscription via Admin Panel:** Administrators must be able to manually manage user subscriptions through a dedicated panel.
* **Responsive Admin CRUD (Create, Read, Update, Delete):** The admin panel must allow administrators to manage courses, users, and other data effectively.
* **Course Browse & Subscription:** Users can browse available courses and initiate subscription requests.
* **Course Summary and Performance Tracking:** The system should track and display user progress and performance within courses.
* **Connectivity & Offline Handling:** The application should manage connectivity states and potentially offer limited offline capabilities (as applicable).

## 3. Non-Functional Requirements

### 3.1 Performance Requirements
* **Response Times:** All responses to API calls should be 2xx code.
* **Load Handling:** The server should be able to handle at least 1000 requests/sec with acceptable response times (as per acceptance tests).

### 3.2 Security Requirements
* **HTTPS/TLS:** All communication with the server must be secured using HTTPS, with the server handling TLS handshake and providing SSL certificates.
* **Password Hashing:** User passwords must be securely hashed before storage in the database.
* **Authentication:** Invalid/empty JWTs (JSON Web Tokens) should result in a 401 (Unauthorized) response code from the server.

### 3.3 Usability Requirements
* **User Experience/User Interface (UX/UI):** The application should provide a good and intuitive user experience. (Note: Initial interactive guide not implemented in V1, deferred to V2).

### 3.4 Reliability Requirements
* **High Availability:** Procedures for maintaining high availability.
* **Recovery:** Procedures for data restoration in case of failures.

### 3.5 Scalability
* **VPS Upgrades:** Hosting plan can be scaled to accommodate increased user load.
* **Modular Design:** System components designed for easy scalability.



## 4. Future Plans (Version 2 Enhancements)

* **Automated Online Payments:** Integrate a payment gateway.
* **Web/Desktop Support:** Develop web and desktop applications.
* **Advanced Analytics:** Implement detailed activity logs and analytics.
* **Additional Courses:** Expand the course catalog.
* **PDF Export:** (From Acceptance Test Report issues)
* **Onboarding Tips/Interactive Guide:** (From Acceptance Test Report issues)