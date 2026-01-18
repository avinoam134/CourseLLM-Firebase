## CourseWise Specifications (Current Truth)

This document defines the **user-visible behavior** and **constraints** expected for the CourseWise application at the present checkpoint of this repository.

These specifications are written as **requirements** using normative language (**MUST/SHALL**) and include concrete **scenarios** that describe expected behavior.

---

## Product Scope

CourseWise is an educational platform that provides:
- **Role-based dashboards** for Students and Teachers
- **Onboarding** to complete a user profile (role, department, courses)
- **Teacher course management** and a **file management** experience
- **Student course browsing** and a **Socratic AI course chat**
- **Personalized learning assessment** generation
- **Monitoring** endpoints/pages for operational visibility

---

## Glossary

- **Firebase user**: The authenticated identity from Firebase Authentication.
- **Profile**: The application user record stored in Firestore (collection `users`, document id = `uid`).
- **Onboarding**: The flow that collects required profile fields and marks the profile as complete.
- **Role**: One of `student` or `teacher`, stored in the profile.
- **Neutral entry pages**: Pages that do not assume a role/dashboard context (e.g. `/`, `/login`).

---

## Requirements

### Requirement: Authentication gating
The system SHALL prevent access to protected areas when the user is not authenticated.

#### Scenario: Unauthenticated user visits a protected page
- **WHEN** a user is not authenticated
- **AND** the user navigates to a protected student or teacher route
- **THEN** the system redirects the user to `/login`

#### Scenario: Authenticated user remains in app
- **WHEN** a user is authenticated
- **THEN** the system allows navigation to role-appropriate content (subject to onboarding completion)

---

### Requirement: Profile and onboarding completion
The system SHALL require a completed profile before granting access to role dashboards.

#### Scenario: New app user is authenticated but has no app profile
- **WHEN** a user is authenticated
- **AND** no profile exists for the user in Firestore
- **THEN** the system redirects the user to `/onboarding`

#### Scenario: Authenticated user has an incomplete profile
- **WHEN** a user is authenticated
- **AND** the user profile is missing required fields (including role)
- **THEN** the system redirects the user to `/onboarding`

---

### Requirement: Role-based routing and guards
The system SHALL enforce role-based access to role-specific routes.

#### Scenario: Teacher attempts to access student dashboard
- **WHEN** a user is authenticated
- **AND** the user has role `teacher`
- **AND** the user navigates to a student-only route
- **THEN** the system redirects the user to `/teacher`

#### Scenario: Student attempts to access teacher dashboard
- **WHEN** a user is authenticated
- **AND** the user has role `student`
- **AND** the user navigates to a teacher-only route
- **THEN** the system redirects the user to `/student`

---

### Requirement: Neutral-page redirect after authentication
The system SHALL route authenticated users from neutral entry pages to onboarding or the correct dashboard.

#### Scenario: Authenticated user on a neutral page with onboarding required
- **WHEN** a user is authenticated
- **AND** onboarding is required
- **AND** the user is on `/` or `/login`
- **THEN** the system redirects the user to `/onboarding`

#### Scenario: Authenticated user on a neutral page with a complete profile
- **WHEN** a user is authenticated
- **AND** the user has a complete profile with a role
- **AND** the user is on `/` or `/login`
- **THEN** the system redirects the user to the role dashboard (`/student` or `/teacher`)

---

### Requirement: Onboarding data collection and persistence
The system SHALL collect and persist minimum user profile data during onboarding.

#### Scenario: User completes onboarding successfully
- **WHEN** an authenticated user selects a role (`student` or `teacher`)
- **AND** the user provides a department value
- **AND** the user saves onboarding
- **THEN** the system writes the profile document to Firestore `users/{uid}`
- **AND** the profile includes `role`, `department`, and `courses`
- **AND** the profile is marked complete (e.g., `profileComplete: true`)
- **AND** the system redirects the user to the role dashboard

#### Scenario: User attempts to save onboarding with missing required fields
- **WHEN** an authenticated user attempts to save onboarding
- **AND** role or department is missing
- **THEN** the system SHALL block saving and present an error to the user

---

### Requirement: Student dashboard and course navigation
The system SHALL provide a student dashboard and course navigation experience.

#### Scenario: Student opens their dashboard
- **WHEN** an authenticated user with role `student` navigates to `/student`
- **THEN** the system renders the student dashboard experience

#### Scenario: Student browses courses
- **WHEN** an authenticated user with role `student` navigates to `/student/courses`
- **THEN** the system renders the student course list page

---

### Requirement: Socratic AI course chat
The system SHALL provide a Socratic chat experience for students, grounded in the provided course material.

#### Scenario: Student asks a question about course material
- **WHEN** a student provides course material content
- **AND** the student asks a question
- **THEN** the system generates a Socratic response intended to guide understanding

#### Scenario: Non-compliant response is blocked
- **WHEN** the system determines the response is not compliant with the provided course material
- **THEN** the system returns a refusal-style message indicating it cannot provide a compliant response

---

### Requirement: Personalized learning assessment generation
The system SHALL generate a personalized assessment based on the student learning path and course context.

#### Scenario: Assessment is generated from provided inputs
- **WHEN** the system is provided the student learning path, course content, Q/A history, and learning objectives
- **THEN** the system returns an assessment and suggested areas for improvement

---

### Requirement: Teacher dashboard and course management
The system SHALL provide teacher routes for course management.

#### Scenario: Teacher opens their dashboard
- **WHEN** an authenticated user with role `teacher` navigates to `/teacher`
- **THEN** the system renders the teacher dashboard experience

#### Scenario: Teacher opens a course management page
- **WHEN** an authenticated user with role `teacher` navigates to `/teacher/courses/[courseId]`
- **THEN** the system renders a course management experience for that course

---

### Requirement: Teacher file management and file CRUD API
The system SHALL provide file listing and upload/delete capabilities through an API route.

#### Scenario: Teacher lists available files
- **WHEN** the client requests `GET /api/files`
- **THEN** the system returns a list of files available in the server file store used by the app
- **AND** the server file store SHALL be the app `public/` directory at runtime

#### Scenario: Teacher downloads a file by path
- **WHEN** the client requests `GET /api/files?path=...`
- **THEN** the system returns the file bytes
- **AND** the system returns 404 when the file cannot be found

#### Scenario: Teacher uploads a file
- **WHEN** the client sends `POST /api/files` with multipart form data containing `file`
- **THEN** the system persists the file into the server file store used by the app
- **AND** the system returns an error when no file is provided

#### Scenario: Teacher deletes a file
- **WHEN** the client requests `DELETE /api/files?path=...`
- **THEN** the system deletes the file if it exists
- **AND** returns 404 if the file does not exist

---

### Requirement: Monitoring page and endpoint
The system SHALL provide a monitoring page and an API endpoint for monitoring data.

#### Scenario: Operator opens monitoring page
- **WHEN** a user navigates to `/monitoring`
- **THEN** the system renders a monitoring page

#### Scenario: Monitoring data is requested
- **WHEN** the client requests `GET /api/monitoring`
- **THEN** the system returns monitoring data in JSON form

---

## Operational and Safety Constraints

### Requirement: Emulator support
The system SHALL support running against Firebase emulators when configured by environment variables.

#### Scenario: Emulator mode enabled
- **WHEN** `NEXT_PUBLIC_USE_FIREBASE_EMULATOR` is set to `true`
- **THEN** the client connects to emulator endpoints for Auth and Firestore

---

## Non-Goals (Current Checkpoint)

- The system does not define a formal RBAC model beyond `student` vs `teacher`.
- The system does not define a completed “course material compliance verifier”; compliance enforcement is currently treated as a tool step and may be placeholder.
- The system does not define persistence or indexing requirements for large-scale course content ingestion beyond current implementation.


