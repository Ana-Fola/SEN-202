# Software Requirement Specification (SRS)
## Security Incident Mapping (SIM) Web Platform
### 1. Introduction & Component Interaction
**System Purpose:**
The Security Incident Mapping (SIM) platform is a web-based system designed to reduce community crime rates on campus by enabling rapid, reliable incident reporting and mapping for students, landlords, and security personnel.
**Component Interaction:**
The system operates through a continuous data flow between the user interface and the central database:
 * **Input Layer:** Students and Landlords interact with the web interface to submit reports or trigger SOS alerts.
 * **Processing Layer:** The system routes these inputs, validating reports and processing anonymity requests (optional extension).
 * **Output Layer:** The system automatically pushes updates to a centralized Map Database, which simultaneously updates the Live Danger Map on user dashboards and pushes direct notifications to Security Personnel.
### 2. Functional Requirements
| Items (Use Cases) | Parameters / Requirements |
|---|---|
| **Trigger SOS Alert** | An immediate distress signal that must alert security personnel instantly. |
| **Submit Incident Report** | Captures and logs specific community crime details (type, location, time) on campus. |
| **Submit Anonymous Report** | Concealed identity reporting; requires the base 'Submit Incident Report' feature to function. |
| **Update Map Database** | Background data synchronization that is triggered automatically whenever a new report is submitted. |
| **View Live Danger Map** | A visual dashboard of high-risk campus areas accessible to both Students and Landlords. |
| **Receive Security Notifications** | Direct routing of actionable alerts restricted exclusively to authorized Security Personnel. |
### 3. Non-Functional Requirements
**I. Product Requirements** *(Constraints relating directly to the application itself)*
 * **Security Requirement:** The platform must encrypt user data and protect identities, especially when the anonymous reporting extension is utilized.
 * **Performance Requirement:** The system must process SOS alerts and map updates in real-time (under 2 seconds) to ensure immediate response to threats.
 * **Usability Requirement:** The web interface must prioritize easiness of use, avoiding complexity so that users can navigate it instinctively during high-stress emergencies.
 * **Reliability Requirement:** The system must be highly dependable, maintaining 99.9% uptime so the campus community can access the live danger map 24/7.
   
**II. Organisational Requirements** *(Principles defined by the institution that must be complied with)*
 * **Development Requirement:** The software architecture must be developed using standard, secure web technologies approved for campus deployment.
 * **Environmental Requirement:** The platform must be fully compatible with the existing campus network infrastructure and accessible via standard student mobile devices.
 * **Process Requirement:** The incident reporting flow must strictly align with the university security department’s existing standard operating procedures for handling community crimes.
  
**III. External Requirements** *(Checks and balances in the software development process)*
 * **Regulatory Requirement:** The system must comply with national data protection regulations (e.g., NDPR) regarding the safe handling of sensitive personal information.
 * **Legislative Requirement:** The platform must operate within the legal boundaries and jurisdictions concerning crime reporting and emergency response.
 * **Ethical Requirement:** The system must include safeguards to prevent the misuse of the anonymous reporting feature for false accusations, ensuring fairness and prioritizing community safety.
