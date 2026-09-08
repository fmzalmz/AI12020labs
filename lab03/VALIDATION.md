# CampusPulse requirements review

Name or team: Fatima Al Mazrouei

Reviewer: Self-review

Date: 8 September 2026

## Validity

Response:

The requirements represent the supplied stakeholder needs. UR-1 and UR-2 reflect S1's need for one event source and private RSVP choices. UR-3 to UR-5 cover S2's approved publishing, audience, and correction needs. UR-6 covers S3's moderation and appeal evidence. UR-7 and UR-8 address S4's verified badge and pilot size. UR-10 records S5's 30-day deletion rule, while UR-11 and FR-10 address the repeated-post abuse case from S6.

## Consistency

Response:

The scope and MoSCoW Won't list both exclude native mobile applications, direct messages, external users, payments, video hosting, and AI recommendations. FR-2 keeps RSVP identities private by default while FR-5 allows event updates without requiring a public attendee list, matching the decision for the S1-S2 conflict. FR-7 retains moderation evidence, while FR-9 and NFR-5 delete separate attendance records, matching the S3-S5 conflict decision.

## Completeness

Response:

The document covers students, group officers, moderators, Student Affairs, the Data Protection Officer, and abuse actors. FR-1 and FR-2 cover the normal student flow. FR-3 includes an unapproved-user failure and permission boundary. FR-7 covers moderation and appeals, FR-9 covers privacy deletion, and FR-10 covers repeated-post abuse. The unknown Orientation Week peak remains clearly recorded as Q1 rather than being presented as stakeholder evidence.

## Realism

Response:

The first release is limited to a browser-based pilot and excludes expensive features such as native apps, payments, video hosting, and AI recommendations. NFR-1 uses S4's stated population of 5,000 students and 200 groups. The WCAG level, notification time, concurrent-user load, and duplicate-post interval in NFR-2 to NFR-4 and FR-10 are recorded as assumptions A1 to A4. Q1 and Q2 must be confirmed before those targets become binding.

## Verifiability

Response:

FR-1 to FR-10 describe results a tester can observe, including displayed events, denied publishing, notifications, hidden content, badges, deletion, and duplicate warnings. NFR-1 to NFR-5 contain numerical measures and conditions. The earlier FR-7 wording said only that evidence would be preserved, without defining visibility or authorized access, so it was revised to state exactly what disappears, what remains, and who can access it.

## One requirement you revised

- Requirement ID: FR-7
- Before: FR-7 [Must] The system shall allow a moderator to hide a reported event while preserving its evidence, decision maker, decision time, and appeal record. [Source: UR-6]
- What was wrong or missing: It did not specify where the event must disappear, how quickly it must disappear, which evidence remains, or who may access that evidence.
- After: FR-7 [Must] The system shall remove a hidden event from all student views immediately and retain the reported content, report reason, moderator identity, decision time, and appeal record for access by authorized moderators. [Source: UR-6]
- Evidence or stakeholder to confirm the change: S3, the campus moderator, should confirm the retained evidence and authorized access needed for appeals.

## Final check

- [x] Stakeholder conflicts have a decision or a follow-up question.
- [x] Scope exclusions agree with the Won't list.
- [x] Every FR and NFR traces to a user requirement.
- [x] Every NFR contains a measurable target and condition.
- [x] Traceability rows use IDs that exist in the document.
- [x] The revised requirement has also been updated in the traceability table.
