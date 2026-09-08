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

## 3. Functional requirements

Write at least six observable system behaviours. Start each one with "The
system shall" and trace it to one or more user requirements.

Format: `FR-1 [Must] The system shall ... [Source: UR-1]`

- FR-1 [Must] The system shall
- FR-2 [Must] The system shall
- FR-3 [Must] The system shall
- FR-4 [Must] The system shall
- FR-5 [Must] The system shall
- FR-6 [Must] The system shall

## 4. Non-functional requirements

Write at least four measurable quality requirements. State what is measured,
the target, and the condition under which the target applies. If you introduce
a number that is not in the handout, record it as an assumption or open
question in Section 8.

Format: `NFR-1 [Must] The system shall ... [Measure: target and condition] [Source: UR-1]`

- NFR-1 [Must] The system shall
- NFR-2 [Must] The system shall
- NFR-3 [Should] The system shall
- NFR-4 [Must] The system shall

## 5. User stories and acceptance criteria

Write at least three stories from different stakeholder viewpoints. Each story
needs at least two acceptance criteria. Across the set, include a failure,
permission boundary, privacy rule, or other non-happy path.

### US-1 [Source: S?, UR-?]

As a <role>,

I want <capability>,

so that <benefit>.

Acceptance criteria:

-
-

### US-2 [Source: S?, UR-?]

As a <role>,

I want <capability>,

so that <benefit>.

Acceptance criteria:

-
-

### US-3 [Source: S?, UR-?]

As a <role>,

I want <capability>,

so that <benefit>.

Acceptance criteria:

-
-

## 6. MoSCoW summary

List requirement or story IDs in every category. The Won't category must state
what is excluded from this release.

- Must:
- Should:
- Could:
- Won't this release:

## 7. Traceability

Add at least four complete paths. Every row should connect evidence to a user
requirement, a system requirement, and a user story.

| Stakeholder need | User requirement | System requirement | User story |
|---|---|---|---|
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

## 8. Assumptions and open questions

Separate decisions your team has assumed from questions that still need an
answer.

### Assumptions

- A1:

### Open questions

- Q1:
