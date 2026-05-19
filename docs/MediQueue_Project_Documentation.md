# MediQueue Project Documentation

## Project Title

**MediQueue: Clinic Management System with Patient Adherence Support**

## Project Overview

MediQueue is a mobile clinic management application developed to improve patient flow, reduce waiting time, support clinical record keeping, and help patients follow medication schedules after consultation. The system provides separate workflows for patients, receptionists, doctors, and pharmacists.

The application was built with React Native and TypeScript, with Firebase used for authentication and cloud data storage. It supports patient registration, appointment booking, queue tracking, consultation recording, pharmacy dispensing, medication reminders, and medication adherence monitoring.

## Team Members

1. ADARKWAH ELVIS YIADOM
2. OWUSU AUGUSTINA ADWOA BANFOWA
3. SENNOR JOHN
4. SIMPSON EMMANUELLA
5. GYAMFUAAH GEORGETTE MARTHA

## Abstract

Many clinics experience long waiting times, manual patient registration, misplaced records, weak communication between departments, and poor follow-up after medication is prescribed. These challenges affect both clinic staff and patients. MediQueue addresses these problems by digitizing the major stages of a clinic visit.

The application allows patients to create accounts, book appointments, view their position in the queue, receive queue notifications, view consultation history, and track medication schedules. Receptionists can register patients and manage the clinic queue. Doctors can view queued patients, record consultation details, prescribe medication, and review consultation history. Pharmacists can view pending prescriptions and mark medications as dispensed. Firebase Realtime Database enables live updates across screens, while Notifee provides local notifications for medication and appointment reminders.

MediQueue demonstrates how a mobile-based clinic management system can improve patient flow, reduce manual workload, and support patient adherence after treatment.

## Chapter One: Introduction

### Background of the Study

Healthcare facilities often depend on manual systems for patient registration, queue control, appointment booking, and medication follow-up. In busy clinics, this can lead to overcrowding, confusion about who should be served next, delayed consultation, and incomplete patient records. Patients may also forget prescribed medications after leaving the clinic, which can reduce treatment effectiveness.

Mobile technology provides an opportunity to improve this process. A clinic management app can make patient information easier to access, help staff coordinate activities, and allow patients to monitor their own care. MediQueue was developed to bring these benefits into a single application.

### Problem Statement

The current manual approach used by many clinics creates several problems:

- Patients may wait for long periods without knowing their queue position.
- Receptionists manually record patient details and assign queue numbers.
- Doctors may not have an organized digital view of consultation records.
- Pharmacies may receive prescriptions through informal or manual channels.
- Patients may forget medication times after leaving the clinic.
- Clinic managers may lack quick statistics about daily patient flow.

These issues reduce efficiency and can affect the quality of care. MediQueue provides a digital solution that connects patient registration, queue management, consultation, pharmacy, appointments, and medication reminders.

### Aim of the Project

The aim of MediQueue is to develop a mobile clinic management system that improves patient queue handling, appointment management, consultation documentation, pharmacy coordination, and patient medication adherence.

### Objectives

The objectives of the project are to:

- Develop a role-based authentication system for patients, receptionists, doctors, and pharmacists.
- Allow receptionists to register patients and automatically assign queue tokens.
- Enable doctors to view queued patients and record consultation details.
- Allow pharmacists to view and dispense prescribed medication.
- Allow patients to book appointments with available doctors.
- Enable patients to view their queue status in real time.
- Generate medication reminders from consultation prescriptions.
- Track medication adherence using taken, missed, and pending dose counts.
- Provide dashboards for quick monitoring of clinic activity.

### Scope of the Project

MediQueue covers the following areas:

- User registration and login.
- Patient registration at reception.
- Queue token generation and queue status updates.
- Doctor consultation and prescription recording.
- Pharmacy prescription dispensing.
- Appointment booking and appointment viewing.
- Medication reminders and medication history.
- Patient and staff dashboards.
- Firebase-backed data storage and real-time updates.

The current implementation is focused on Android mobile use. It uses local device notifications and Firebase cloud services.

### Significance of the Project

MediQueue is useful to:

- **Patients**, because they can book appointments, view queue status, receive reminders, and track medications.
- **Receptionists**, because they can register patients and manage queues more efficiently.
- **Doctors**, because they can view patient queues, record consultations, and access previous consultation records.
- **Pharmacists**, because they can see prescriptions awaiting dispensing.
- **Clinic administrators**, because daily activity is easier to monitor through dashboard statistics.
- **Academic evaluation**, because it demonstrates practical use of mobile development, cloud databases, authentication, notification services, and healthcare workflow analysis.

## Chapter Two: Literature Review

### Clinic Management Systems

A clinic management system is software designed to help health facilities manage patient information, appointments, consultations, prescriptions, billing, and administrative workflows. Digital systems reduce dependence on paper files and help improve speed, accuracy, and accessibility of information.

### Queue Management in Healthcare

Queue management is important in clinics because patients are usually served in order of arrival or urgency. Without a clear system, patients may become frustrated and staff may find it difficult to coordinate service delivery. A digital queue system improves transparency by showing who is waiting, who is currently being served, and who has completed consultation.

### Appointment Scheduling

Appointment scheduling allows patients to choose a date and time for consultation. It helps clinics plan workload and reduces overcrowding. In MediQueue, patients can select a doctor, date, and time. Doctors can view appointments assigned to them.

### Medication Adherence

Medication adherence refers to how well patients follow prescribed medication instructions. Poor adherence may happen when patients forget dose times, misunderstand prescriptions, or stop taking medication early. MediQueue supports adherence by generating schedules, sending reminders, and allowing patients to mark doses as taken.

### Mobile Health Applications

Mobile health applications improve access to healthcare support by allowing patients and staff to interact through smartphones. MediQueue uses this approach to provide queue updates, appointments, consultation history, medication reminders, and medication tracking through a mobile app.

## Chapter Three: Methodology

### Development Approach

The project follows an iterative development approach. Core features were developed as separate modules and then integrated into one mobile application. The development process included requirement gathering, system design, implementation, testing, and documentation.

### Requirement Gathering

Requirements were identified by studying common clinic workflows:

- Patient arrives or creates an account.
- Reception registers the patient.
- Patient is added to the queue.
- Doctor calls and consults the patient.
- Doctor records symptoms, diagnosis, prescription, dosage, and notes.
- Pharmacy dispenses medication.
- Patient receives reminders and tracks medication usage.

### Functional Requirements

The system must allow:

- Users to register and log in.
- Users to be assigned roles.
- Receptionists to register patients.
- Queue tokens to be generated automatically.
- Receptionists and doctors to view the queue.
- Doctors to consult selected patients.
- Consultations to be saved to the database.
- Prescriptions to be sent to the pharmacy module.
- Pharmacists to dispense medication.
- Patients to book appointments.
- Doctors to view their appointments.
- Patients to view queue position.
- Patients to receive medication reminders.
- Patients to mark medication doses as taken.
- Patients and doctors to view consultation history.

### Non-Functional Requirements

The system should be:

- **Usable:** screens should be simple and easy to understand.
- **Responsive:** Firebase real-time listeners should update information quickly.
- **Secure:** authentication should be required before user-specific data is accessed.
- **Maintainable:** source files should be separated by screen and configuration.
- **Portable:** the mobile app should run on Android devices.
- **Reliable:** important data should be stored in Firebase rather than only on the device.

### System Architecture

MediQueue uses a client-cloud architecture.

The mobile application is the client. It contains the user interface, navigation, local notification logic, and business workflows. Firebase provides cloud services for authentication, data storage, and file storage configuration.

Main architecture layers:

- **Presentation layer:** React Native screens under the `pages` directory.
- **Navigation layer:** React Navigation stack defined in `App.tsx`.
- **Service layer:** Firebase and notification configuration under the `config` directory.
- **Data layer:** Firebase Authentication and Firebase Realtime Database.

### Technology Stack

| Technology | Purpose |
| --- | --- |
| React Native | Mobile application framework |
| TypeScript | Typed JavaScript development |
| React Navigation | Screen navigation |
| Firebase Authentication | User registration and login |
| Firebase Realtime Database | Cloud data storage and live updates |
| Firebase Storage | Cloud storage configuration |
| Notifee | Android local notifications |
| DateTimePicker | Appointment date and time selection |
| Jest | Testing framework |
| Android Gradle | Android build system |

### Development Tools

- Visual Studio Code or any code editor.
- Node.js 22 or later.
- npm or Yarn.
- Android Studio and Android SDK.
- Firebase project configuration.
- React Native CLI.

## Chapter Four: System Analysis and Design

### User Roles

MediQueue supports four main user roles.

| Role | Main Responsibilities |
| --- | --- |
| Patient | Book appointments, view queue, view consultation history, manage medication reminders |
| Receptionist | Register patients, assign queue tokens, manage patient records and queue |
| Doctor | View queue, consult patients, record diagnosis and prescriptions, view appointments |
| Pharmacist | View pending prescriptions and dispense medication |

### Authentication and Role Routing

Users register with their name, email, password, and selected role. Firebase Authentication creates the account. The application then stores the user profile under `users/{uid}` in Firebase Realtime Database.

During login:

1. The user enters email and password.
2. Firebase Authentication validates the credentials.
3. The application reads the user's role from `users/{uid}`.
4. The user is redirected to the correct dashboard:
   - Doctor: `DoctorDashboard`
   - Receptionist: `Home`
   - Pharmacist: `Pharmacy`
   - Patient: `PatientDashboard`

### Navigation Structure

The main navigation stack is defined in `App.tsx`.

| Screen Name | Component | Purpose |
| --- | --- | --- |
| Loading | `LoginScreen` | Initial login screen |
| Register | `RegisterScreen` | Account creation |
| Home | `HomeScreen` | Reception dashboard |
| RegisterPatient | `RegisterPatient` | Patient registration and queue entry |
| Queue | `QueueScreen` | Queue management |
| Consultation | `ConsultationScreen` | Doctor consultation form |
| Pharmacy | `PharmacyScreen` | Prescription dispensing |
| Patient | `PatientDashboard` | Patient dashboard |
| Appointments | `AppointmentsScreen` | Appointment booking |
| DoctorDashboard | `DoctorDashboard` | Doctor dashboard |
| DoctorAppointments | `DoctorAppointmentsScreen` | Doctor appointment list |
| PatientRecords | `PatientRecordsScreen` | Patient record search |
| ConsultationHistory | `ConsultationHistoryScreen` | Staff consultation history |
| PatientConsultationHistory | `PatientConsultationHistoryScreen` | Patient consultation history |
| MedicationReminder | `MedicationReminderScreen` | Medication schedule and reminders |
| MedicationHistory | `MedicationHistoryScreen` | Medication adherence statistics |
| PatientQueue | `PatientQueueScreen` | Patient queue position |

### Main Workflows

#### User Registration Workflow

1. User opens the registration screen.
2. User enters full name, email, password, and role.
3. Firebase creates the authentication account.
4. User details are saved under the `users` node.
5. User is redirected to the login screen.

#### Patient Registration and Queue Workflow

1. Receptionist opens the reception dashboard.
2. Receptionist selects **Register Patient**.
3. Receptionist enters patient name, phone number, email, and gender.
4. The system calculates the next queue token, such as `Q001`, `Q002`, or `Q003`.
5. Patient details are saved under `patients`.
6. Queue details are saved under `queue` with status `waiting`.
7. The patient appears in the queue list.

#### Queue Management Workflow

1. Queue records are loaded from Firebase.
2. Records are sorted by token.
3. Receptionist or doctor presses **Call Next Patient**.
4. The first waiting patient is updated to `in-progress`.
5. The current token appears under **Now Serving**.
6. Doctor can open consultation for an `in-progress` patient.
7. Receptionist can mark the patient as served where applicable.

#### Doctor Consultation Workflow

1. Doctor opens the queue from the doctor dashboard.
2. Doctor selects a patient whose status is `in-progress`.
3. Doctor enters symptoms, diagnosis, drug, dosage, duration, and notes.
4. The system saves consultation details under `consultations`.
5. The system generates medication schedule dates from dosage and duration.
6. Reminder data is saved under `reminders`.
7. Patient queue status is updated to `consulted`.

#### Pharmacy Workflow

1. Pharmacist logs in and opens the pharmacy screen.
2. The system loads consultations with status `pending-pharmacy`.
3. Pharmacist reviews patient prescription details.
4. Pharmacist presses **Dispense Medication**.
5. Consultation status is updated to `completed`.
6. Reminder information is saved for the patient.

#### Appointment Booking Workflow

1. Patient opens **Book Appointment**.
2. The app loads users whose role is `doctor`.
3. Patient selects doctor, date, and time.
4. Appointment data is saved under `appointments`.
5. A local appointment reminder is scheduled.
6. Patient can view their appointment list.
7. Doctor can view appointments assigned to their user ID.

#### Medication Reminder Workflow

1. Patient opens medication reminders.
2. The app loads reminders that match the logged-in patient's email.
3. The app schedules notifications for future medication times.
4. Patient can view each dose time.
5. Patient can mark a dose as taken.
6. Taken status is stored under the reminder's `taken` field.

#### Medication History Workflow

1. Patient opens medication history.
2. The app reads the patient's reminders.
3. For each scheduled dose, the app checks whether it is taken, missed, or pending.
4. The system calculates total taken, missed, and pending doses.
5. The system calculates adherence percentage.

### Database Design

MediQueue uses Firebase Realtime Database. The main database nodes are described below.

#### `users`

Stores registered account profiles.

```json
{
  "users": {
    "uid": {
      "name": "User Name",
      "email": "user@example.com",
      "role": "patient"
    }
  }
}
```

#### `patients`

Stores patient records registered by reception.

```json
{
  "patients": {
    "patientKey": {
      "name": "Patient Name",
      "phone": "0240000000",
      "gender": "Female",
      "patientEmail": "patient@example.com",
      "createdAt": "2026-05-19"
    }
  }
}
```

#### `queue`

Stores patient queue entries.

```json
{
  "queue": {
    "queueKey": {
      "token": "Q001",
      "patientName": "Patient Name",
      "patientEmail": "patient@example.com",
      "status": "waiting",
      "date": "2026-05-19"
    }
  }
}
```

Common queue statuses:

- `waiting`
- `in-progress`
- `consulted`

#### `consultations`

Stores consultation and prescription details.

```json
{
  "consultations": {
    "consultationKey": {
      "patientId": "queueKey",
      "patientName": "Patient Name",
      "token": "Q001",
      "patientEmail": "patient@example.com",
      "symptoms": "Headache and fever",
      "diagnosis": "Malaria",
      "prescription": "Medication Name",
      "dosage": "3 times daily",
      "duration": "5",
      "doctorNote": "Take after meals",
      "date": "2026-05-19",
      "status": "pending-pharmacy"
    }
  }
}
```

Common consultation statuses:

- `pending-pharmacy`
- `completed`

#### `appointments`

Stores appointment bookings.

```json
{
  "appointments": {
    "appointmentKey": {
      "patientEmail": "patient@example.com",
      "patientName": "Patient Name",
      "doctorId": "doctorUid",
      "doctorName": "Doctor Name",
      "date": "2026-05-20",
      "time": "09:30",
      "createdAt": "2026-05-19T10:00:00.000Z"
    }
  }
}
```

#### `reminders`

Stores medication schedules and adherence data.

```json
{
  "reminders": {
    "reminderKey": {
      "patientId": "queueKey",
      "token": "Q001",
      "patientEmail": "patient@example.com",
      "drug": "Medication Name",
      "dosage": "3 times daily",
      "duration": "5",
      "tips": "Take after meals",
      "schedule": [
        "2026-05-19T08:00:00.000Z",
        "2026-05-19T14:00:00.000Z",
        "2026-05-19T20:00:00.000Z"
      ],
      "taken": {
        "2026-05-19T08:00:00_000Z": true
      }
    }
  }
}
```

### Module Descriptions

#### Login Module

File: `pages/LoginScreen.tsx`

The login module authenticates users through Firebase Authentication. After login, it reads the user's role from Firebase Realtime Database and redirects the user to the correct dashboard.

#### Registration Module

File: `pages/RegisterScreen.tsx`

This module allows new users to create accounts and select their role. The selected role determines which functions the user can access after login.

#### Reception Dashboard Module

File: `pages/HomeScreen.tsx`

The reception dashboard displays daily statistics:

- Patients registered today.
- Waiting queue count.
- Served or consulted patients.
- Appointments for the day.

It also provides navigation to patient registration, queue management, appointments, and patient records.

#### Patient Registration Module

File: `pages/RegisterPatient.tsx`

This module allows receptionists to register patients and add them to the queue. It generates a queue token automatically by counting existing queue entries and formatting the next number.

#### Queue Management Module

File: `pages/QueueScreen.tsx`

This module displays all queue entries, sorted by token. It allows the next waiting patient to be called and enables role-specific actions:

- Receptionist can manage queue progress.
- Doctor can open consultation for a patient in progress.

#### Doctor Dashboard Module

File: `pages/DoctorDashboard.tsx`

The doctor dashboard shows the number of waiting patients and consulted patients. It provides access to the queue, doctor appointments, and consultation history.

#### Consultation Module

File: `pages/ConsultationScreen.tsx`

This module allows doctors to record symptoms, diagnosis, prescription, dosage, duration, and notes. It also generates medication schedules based on dosage and duration.

Current dosage schedule logic:

- `1 time` means 08:00.
- `2 times` means 08:00 and 20:00.
- `3 times` means 08:00, 14:00, and 20:00.
- Other values default to 08:00.

#### Pharmacy Module

File: `pages/PharmacyScreen.tsx`

The pharmacy module displays prescriptions with `pending-pharmacy` status. When the pharmacist dispenses medication, the consultation is updated to `completed`.

#### Appointment Module

Files:

- `pages/AppointmentsScreen.tsx`
- `pages/DoctorAppointmentsScreen.tsx`

Patients can book appointments by selecting a doctor, date, and time. Doctors can view appointments assigned to their account.

#### Patient Dashboard Module

File: `pages/PatientDashboard.tsx`

The patient dashboard displays:

- Total medications.
- Pending doses.
- Consultation count.
- Current queue position.

It also links patients to appointments, reminders, medication history, queue status, and consultation history.

#### Patient Queue Module

File: `pages/PatientQueueScreen.tsx`

This module shows the patient's queue position, number of people ahead, and the currently served token. It can also notify the patient when it is their turn.

#### Medication Reminder Module

File: `pages/MedicationReminderScreen.tsx`

This module displays medication schedules and uses Notifee to schedule local reminders. Patients can mark each dose as taken.

#### Medication History Module

File: `pages/MedicationHistoryScreen.tsx`

This module summarizes medication adherence. It calculates:

- Taken doses.
- Missed doses.
- Pending doses.
- Adherence percentage.

#### Consultation History Modules

Files:

- `pages/ConsultationHistoryScreen.tsx`
- `pages/PatientConsultationHistoryScreen.tsx`

The staff consultation history screen shows all consultations and allows searching by patient name or token. The patient consultation history screen filters records by the logged-in patient's email.

## Chapter Five: Implementation

### Application Entry Point

The app starts from `index.js`, which registers the main React Native application. `App.tsx` defines the navigation stack and maps screen names to React Native components.

### Firebase Configuration

Firebase is configured in `config/firebase.tsx`. The application exports:

- `auth` for Firebase Authentication.
- `db` for Firebase Realtime Database.
- `storage` for Firebase Storage.

The Android Firebase configuration file should be placed at:

```text
android/app/google-services.json
```

The repository includes `android/app/google-services.example.json` as an example placeholder.

### Notification Configuration

Notification features are implemented in `config/NotificationService.tsx`.

Supported notification functions:

- Create Android notification channel.
- Request notification permission.
- Show immediate notification.
- Schedule medication reminder.
- Schedule appointment reminder.
- Display queue alert.
- Cancel all notifications.

The app uses Notifee and an Android notification channel named `MediQueue Notifications`.

### Android Permissions

The Android manifest includes permissions for:

- Internet access.
- Network state access.
- External storage access.
- Media image access.

Internet permission is required for Firebase communication.

### Data Synchronization

The app uses Firebase Realtime Database listeners through `onValue`. This allows screens to update when database records change. For example:

- Queue screens update when a patient is called.
- Dashboards update when new patients or appointments are added.
- Medication screens update when dose status changes.

### Error Handling

The application uses React Native `Alert` dialogs to show feedback for:

- Login errors.
- Registration errors.
- Missing required fields.
- Successful patient registration.
- Successful appointment booking.
- Successful consultation saving.

### User Interface Design

The interface uses simple mobile screens with cards, buttons, text inputs, and lists. The main colors are blue for primary actions, green for successful actions, and red for logout or warning actions.

The design prioritizes clarity because the application is intended for clinic staff and patients who need quick access to tasks.

## Chapter Six: Testing

### Testing Strategy

Testing was performed using functional testing, workflow testing, and basic application testing.

### Functional Test Cases

| Test Case | Expected Result |
| --- | --- |
| Register user with valid details | Account is created and saved under `users` |
| Login as doctor | User is redirected to doctor dashboard |
| Login as receptionist | User is redirected to reception dashboard |
| Login as pharmacist | User is redirected to pharmacy screen |
| Login as patient | User is redirected to patient dashboard |
| Register patient at reception | Patient record and queue record are created |
| Call next patient | First waiting queue entry becomes `in-progress` |
| Doctor opens consultation | Consultation form opens for selected patient |
| Save consultation | Consultation and reminder records are created |
| Pharmacist dispenses medication | Consultation status changes to `completed` |
| Patient books appointment | Appointment is saved and reminder is scheduled |
| Patient views queue status | Queue position and now-serving token are displayed |
| Patient marks medication as taken | Dose is updated under reminder `taken` field |
| Patient views medication history | Taken, missed, pending, and adherence values are shown |

### Validation Testing

The application checks required fields in important forms:

- Patient registration requires name, phone, email, and gender.
- Appointment booking requires doctor, date, and time.
- Consultation saving requires drug, dosage, and duration.

### Unit Testing

The project includes Jest configuration and a default React Native test file under `__tests__/App.test.tsx`. Additional tests can be added for schedule generation, role routing, and database helper functions.

### Manual Testing

Manual testing should be done on an Android emulator or Android device:

1. Install dependencies with `npm install`.
2. Start Metro with `npm start`.
3. Run Android app with `npm run android`.
4. Create users for each role.
5. Test the complete clinic workflow from patient registration to pharmacy dispensing.

## Chapter Seven: Deployment

### Development Setup

Install dependencies:

```sh
npm install
```

Start the Metro bundler:

```sh
npm start
```

Run on Android:

```sh
npm run android
```

Run tests:

```sh
npm test
```

### Firebase Setup

To configure Firebase:

1. Create a Firebase project.
2. Enable Firebase Authentication with email and password sign-in.
3. Enable Firebase Realtime Database.
4. Add an Android app in Firebase.
5. Download `google-services.json`.
6. Place it inside `android/app/`.
7. Configure database rules according to the security needs of the clinic.

### Android APK

The repository contains an Android release APK:

```text
release/MediQueue-v1.0.1.apk
```

When installing outside Google Play Store, Android may ask the user to allow installation from the browser or file manager.

## Chapter Eight: Results and Discussion

### Achieved Results

MediQueue successfully implements a complete clinic workflow:

- Users can register and log in by role.
- Receptionists can register patients and manage queues.
- Doctors can view queues and save consultation records.
- Pharmacists can view and complete prescriptions.
- Patients can book appointments.
- Patients can track queue position.
- Patients can receive medication reminders.
- Patients can monitor medication adherence.

### Benefits of the System

- Reduces manual queue management.
- Improves communication between reception, doctor, pharmacy, and patient.
- Provides real-time queue visibility.
- Keeps consultation and medication records digitally.
- Encourages patients to take medication on schedule.
- Gives staff quick dashboard statistics.

### Limitations

Current limitations include:

- The system does not yet include administrator-level user approval.
- Queue token generation is based on count and may need stronger transaction logic for high-concurrency clinics.
- The app currently focuses on Android.
- It does not include billing, laboratory, insurance, or inventory management.
- Medication schedules currently support simple dosage interpretation.
- Firebase database rules must be configured carefully before real clinical deployment.
- The system does not currently include offline-first data synchronization.

### Future Enhancements

Recommended future improvements:

- Add admin approval for staff accounts.
- Add stronger role-based database security rules.
- Add triage priority for emergency patients.
- Add laboratory request and results module.
- Add pharmacy inventory management.
- Add billing and payment module.
- Add SMS reminders for patients without smartphones.
- Add analytics reports for clinic administrators.
- Add push notifications through Firebase Cloud Messaging.
- Add offline support for unstable network environments.
- Add exportable PDF consultation reports.

## Security and Privacy Considerations

Because MediQueue handles healthcare-related information, security and privacy are important.

Recommended production security measures:

- Use strict Firebase Realtime Database rules.
- Prevent patients from reading other patients' records.
- Limit doctor, receptionist, and pharmacist access by role.
- Validate all user input before saving.
- Require strong passwords.
- Avoid storing unnecessary sensitive information.
- Use HTTPS-backed services only.
- Back up the database regularly.
- Train clinic staff on responsible handling of patient information.




## Conclusion

MediQueue provides a practical digital solution for clinic management and patient adherence support. It connects the key stages of a clinic visit: registration, queue handling, consultation, prescription, pharmacy dispensing, and post-consultation medication tracking. By using React Native and Firebase, the application delivers real-time updates and mobile accessibility.

The project demonstrates the value of technology in improving healthcare service delivery, reducing manual workload, and supporting patients beyond the consultation room.


