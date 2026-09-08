# CampusPulse stakeholder analysis

Name or team: Fatima Al Mazrouei

Date: 8 September 2026

Read the stakeholder notes in the lab handout before completing this file.
Use the stakeholder types and power-interest quadrants from Week 2, Lecture 2.

Stakeholder types: end user, operations, business, regulator, negative stakeholder

Power-interest quadrants: key player, keep satisfied, keep informed, minimal effort

## S1

- Stakeholder: Student attendee
- Stakeholder type: End user
- Power-interest quadrant: Keep informed
- Main goal: Find campus events in one place and RSVP privately using a mobile browser or screen reader.
- Main concern: RSVP names may become public without consent, or the service may be inaccessible.
- How you would involve or monitor this stakeholder: Interview students and test early mobile and screen-reader prototypes with them.

## S2

- Stakeholder: Group officer
- Stakeholder type: Operations
- Power-interest quadrant: Key player
- Main goal: Collaboratively create and publish announcements and events for the correct audience.
- Main concern: Unapproved officers may publish, or members may miss changes to an event.
- How you would involve or monitor this stakeholder: Include approved officers in workflow workshops and test drafting, publishing, and correction features with them.

## S3

- Stakeholder: Campus moderator
- Stakeholder type: Operations
- Power-interest quadrant: Key player
- Main goal: Act quickly on reports while preserving evidence and a record of moderation decisions.
- Main concern: Harmful events may remain visible, or evidence needed for an appeal may be lost.
- How you would involve or monitor this stakeholder: Review moderation prototypes with moderators and test hiding, evidence retention, auditing, and appeals.

## S4

- Stakeholder: Student Affairs
- Stakeholder type: Business
- Power-interest quadrant: Key player
- Main goal: Launch a trustworthy pilot for 5,000 students and 200 verified groups before Orientation Week.
- Main concern: The official badge may be misused or the pilot may not support the required number of users and groups.
- How you would involve or monitor this stakeholder: Hold regular progress reviews and obtain approval for verification rules and pilot readiness.

## S5

- Stakeholder: Data Protection Officer
- Stakeholder type: Regulator
- Power-interest quadrant: Keep satisfied
- Main goal: Ensure the service collects only necessary personal data and follows privacy and deletion rules.
- Main concern: RSVP data may be exposed or retained for longer than 30 days after an event is cancelled.
- How you would involve or monitor this stakeholder: Request privacy reviews before release and provide evidence from access-control and data-deletion tests.

## S6

- Stakeholder: Malicious or compromised account user
- Stakeholder type: Negative stakeholder
- Power-interest quadrant: Minimal effort
- Main goal: Imitate verified groups, publish phishing events, or repeatedly post announcements.
- Main concern: Verification, authorization, and abuse controls may prevent these attacks.
- How you would involve or monitor this stakeholder: Do not involve the attacker directly; monitor suspicious activity and test imitation, phishing, and repeated-post abuse cases.

## Conflicts to resolve

Describe at least two real tensions. For each one, name both stakeholder IDs
and either propose a decision or write a specific question that should go back
to the stakeholders.

### Conflict 1

- Stakeholders: S1 and S2
- What conflicts: S1 wants RSVP identities private unless students choose otherwise, while S2 needs to contact people who RSVP when event details change.
- Proposed decision or follow-up question: Keep RSVP lists hidden from the public, but allow approved officers to send event updates without displaying attendee names publicly.

### Conflict 2

- Stakeholders: S3 and S5
- What conflicts: S3 needs evidence preserved for moderation appeals, while S5 requires cancelled-event attendance data to be deleted within 30 days.
- Proposed decision or follow-up question: Preserve the report, moderation decision, and non-attendance evidence for appeals, but permanently delete the separate RSVP attendance data within 30 days.
