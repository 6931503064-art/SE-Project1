# SE-Project1

Project name: Medication Reminder
Team Members
6931503035 Takkan Khanlui
6931503049 Nichanan Lalua
6931503064 Yar Oo -
6931503066 Rossatorn Sangkaew
6931503079 Suchitra Khomdee
PROBLEM
The problem: Elderly people on regular or multiple medications often forget doses or take them late, since common reminder apps are hard to
use — forcing caregivers to repeatedly call and check.
Who exactly has it: Elderly patients on regular medication, and the children or relatives who monitor them but aren't present all day.
Why it matters / what it costs them today: Missed or late doses can affect disease control and burden caregivers with manual tracking.
GATE 1 — REACHABLE USERS
1. Peerapap Kummongkon — by phone — September 3, 2026, 12:00–12:20 PM
2. Mrs. Wun Daengsan — by phone — September 4, 2026, 4:20–4:30 PM
3. Ms. Chanantida Nosuk — by phone — September 4, 2026, 4:40–4:50 PM
4. Ms. Sakura — contacted via Instagram — September 4, 2026, 2:30–2:40 PM
GATE 2 — MVP SHAPE 3–5 planned functional requirements:
FR-1: Medication schedule with type-based reminders, showing name/photo at dose time.
FR-2: One-tap "Medication Taken" confirmation button, no typing needed.
FR-3: Two automatic push reminders if unconfirmed; if still unconfirmed, escalate to FR-4.
FR-4: Real-time caregiver alert and status view, triggered by (a) no confirmation after both reminders, or (b) no confirmation for 2 consecutive days.
Which FR carries a real rule or decision (not plain CRUD)?
FR-3: Automatic Repeat Reminders and FR-4: Caregiver Alert + Status View
What data has to persist between sessions?
1. Patient Profile: Name, profile photo, and linked caregiver account
2. Medication List: Medication name, photo link (actual file stored on Cloudinary), and scheduled time
3. Confirmation Log: scheduled time, actual confirmation time, status (drives escalation and dashboard)
4. Escalation State: Waiting → Reminder 1 sent → Reminder 2 sent → Caregiver notified
5. Caregiver Link: Patient–caregiver relationship and data access permissions
GATE 3 — ACCESS: The system uses Firebase (FCM, Authentication, Firestore) and Cloudinary — all with free tiers requiring no credit card.
Firestore provides 1 GiB of storage with 50,000 reads/20,000 writes per day, while Cloudinary provides 25 credits per month.
How access will be verified: The team will create trial accounts for each service and run practical tests — sending a push notification, registering
and logging in, reading and writing to Firestore, and uploading a photo via Cloudinary — checking results against the quotas before relying on
these services for the MVP.
PROCESS & TEAM
Team Process SDLC: Agile — because the team can develop the system in short cycles and continuously incorporate feedback from real
elderly patients and caregivers to improve the UX and notification system.
