# CampusPulse requirements

Name or team: Fatima Al Mazrouei

Date: 8 September 2026

Status: working draft

Use the source IDs `S1` to `S6` from the lab handout. Keep every requirement
short enough to test and trace.

## 1. Release scope

### In scope

- University sign-in for students, approved group officers, and campus moderators.
- Verified group profiles with announcements, events, and following.
- RSVP with private-by-default attendee visibility.
- University-wide and members-only event audiences.
- Event corrections and notifications to students who RSVP.
- Reporting, moderation, evidence records, and appeals.

### Out of scope

- Native mobile applications.
- Direct messages and access for external users.
- Payments, video hosting, and AI recommendations.

## 2. User requirements

- UR-1 [Must] Students can view announcements and events from verified groups they follow. [Source: S1, S4]
- UR-2 [Must] Students can RSVP with their identity hidden from the public unless they choose to show it. [Source: S1, S5]
- UR-3 [Must] Approved group officers can create, edit, and publish announcements and events. [Source: S2]
- UR-4 [Must] Group officers can limit an event to the whole university or group members. [Source: S2]
- UR-5 [Must] Students who RSVP receive notice when an event's place or time changes. [Source: S2]
- UR-6 [Must] Campus moderators can review reports, hide harmful events, and preserve evidence and decision records for appeals. [Source: S3]
- UR-7 [Must] Only groups checked by Student Affairs can display an official badge. [Source: S4, S6]
- UR-8 [Must] CampusPulse can serve a pilot of 5,000 students and 200 groups before Orientation Week. [Source: S4]
- UR-9 [Should] Students can use CampusPulse through mobile browsers and screen readers. [Source: S1]
- UR-10 [Must] Attendance data for a cancelled event is deleted within 30 days. [Source: S5]
- UR-11 [Could] Campus moderators can identify repeated announcements from a compromised group account. [Source: S6]

## 3. Functional requirements

- FR-1 [Must] The system shall display announcements and events from verified groups followed by the signed-in student. [Source: UR-1]
- FR-2 [Must] The system shall hide a student's RSVP identity from the public by default and allow the student to make it public. [Source: UR-2]
- FR-3 [Must] The system shall allow approved group officers to create and edit drafts, but shall deny publishing attempts by unapproved users. [Source: UR-3]
- FR-4 [Must] The system shall allow an approved officer to set an event audience as the whole university or group members only. [Source: UR-4]
- FR-5 [Must] The system shall notify students who RSVP when an approved officer changes an event's place or time. [Source: UR-5]
- FR-6 [Must] The system shall allow a signed-in user to report an event and record the reported content and reason. [Source: UR-6]
- FR-7 [Must] The system shall remove a hidden event from all student views immediately and retain the reported content, report reason, moderator identity, decision time, and appeal record for access by authorized moderators. [Source: UR-6]
- FR-8 [Must] The system shall display an official badge only after Student Affairs records that the group is verified. [Source: UR-7]
- FR-9 [Must] The system shall delete RSVP attendance records no later than 30 days after an event is cancelled. [Source: UR-10]
- FR-10 [Could] The system shall warn a moderator when the same group publishes an identical announcement more than once within 10 minutes. [Source: UR-11]

## 4. Non-functional requirements

- NFR-1 [Must] The system shall support the CampusPulse pilot population. [Measure: successfully store and retrieve records for 5,000 student accounts and 200 group profiles during the pre-release load test] [Source: UR-8]
- NFR-2 [Should] The system shall make the main student journeys accessible. [Measure: zero critical WCAG 2.1 AA failures when browsing events, following groups, and submitting an RSVP using supported mobile browsers and screen readers] [Source: UR-9]
- NFR-3 [Should] The system shall deliver event-change notifications promptly. [Measure: at least 95% of notifications are delivered within 60 seconds after a place or time correction under normal pilot load] [Source: UR-5]
- NFR-4 [Must] The system shall respond promptly during Orientation Week. [Measure: at least 95% of page requests complete within 2 seconds while 500 users are active concurrently] [Source: UR-8]
- NFR-5 [Must] The system shall enforce the attendance-data retention limit. [Measure: 100% of RSVP attendance records are deleted within 30 days after their event is cancelled] [Source: UR-10]

## 5. User stories and acceptance criteria

### US-1 [Source: S1, UR-1, UR-2]

As a student attendee,

I want to find events from groups I follow and RSVP privately,

so that I can participate without exposing my identity.

Acceptance criteria:

- Given that a student follows a verified group, when the student opens the event feed, then that group's available events are displayed.
- Given that a student submits an RSVP, then the student's name is absent from the public attendee list unless the student explicitly chooses public visibility.

### US-2 [Source: S2, UR-3, UR-4, UR-5]

As a group officer,

I want approved officers to prepare and publish events for a chosen audience,

so that the correct students receive accurate event information.

Acceptance criteria:

- Given two approved officers, one can save a draft and the other can edit and publish it to the selected university-wide or members-only audience.
- Given an unapproved user, when that user attempts to publish an event, then publishing is denied and the event remains unavailable to students.
- Given students who RSVP, when an approved officer changes the event's place or time, then at least 95% receive a notification within 60 seconds under normal pilot load.

### US-3 [Source: S3, UR-6]

As a campus moderator,

I want to hide a reported event while preserving its evidence,

so that I can limit harm and support a fair appeal.

Acceptance criteria:

- Given a submitted report, the moderator can view the reported content and the reporter's stated reason.
- When a moderator hides an event, it disappears immediately from all student views while the reported content, report reason, moderator identity, decision time, and appeal record remain available to authorized moderators.

### US-4 [Source: S5, UR-10]

As the Data Protection Officer,

I want cancelled-event attendance data deleted within 30 days,

so that CampusPulse follows its privacy and retention obligations.

Acceptance criteria:

- When an event is cancelled, its RSVP attendance records receive a deletion deadline no later than 30 days after cancellation.
- After the deadline passes, an authorized attendance-data search returns no RSVP attendance records for that event.

## 6. MoSCoW summary

- Must: UR-1 to UR-8, UR-10, FR-1 to FR-9, NFR-1, NFR-4, NFR-5, and US-1 to US-4.
- Should: UR-9, NFR-2, and NFR-3.
- Could: UR-11 and FR-10.
- Won't this release: Native mobile applications; direct messages; external-user access; payments; video hosting; and AI recommendations.

## 7. Traceability

| Stakeholder need | User requirement | System requirement | User story |
|---|---|---|---|
| S1: Find events from followed verified groups | UR-1 | FR-1 | US-1 |
| S1 and S5: Keep RSVP identity private by default | UR-2 | FR-2 | US-1 |
| S2: Allow only approved officers to publish | UR-3 | FR-3 | US-2 |
| S3: Remove hidden events from student views while retaining appeal evidence | UR-6 | FR-7 | US-3 |
| S5: Delete attendance data after cancellation | UR-10 | NFR-5 | US-4 |

## 8. Assumptions and open questions

### Assumptions

- A1: WCAG 2.1 AA is the assumed accessibility standard because the source notes do not specify a standard.
- A2: Delivering at least 95% of change notifications within 60 seconds under normal pilot load is an assumed target.
- A3: The performance test assumes 500 concurrently active users because the Orientation Week peak is unknown.
- A4: The repeated-announcement warning uses an assumed 10-minute comparison period.

### Open questions

- Q1: What peak number of concurrent users should CampusPulse support during Orientation Week?
- Q2: Which mobile browsers and screen-reader versions must the first release officially support?
