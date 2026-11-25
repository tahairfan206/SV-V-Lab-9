# Findings: MediTrack SRS Review

| | |
|---|---|
| Student A | Faizan Ali (SP/24/BSSE/053) |
| Student B | Taha Irfan (SP/2024/BSSE/044) |
| Course | Software Verification & Validation (SV&V) |
| Teacher | Saleha Yousaf |

## Comparison of runs (fill after the Together session)
| Measure | Value |
|---------|-------|
| Items answered the same by A and B | (fill) of 20 |
| Items answered differently | (fill) |
| Items marked "?" by A | C-06, C-13 |
| Items marked "?" by B | (fill) |
| Differences resolved by discussion | (fill) |

## Problems in the SRS
| ID | Requirement | Problem | Type | Checklist item | Suggested fix | Agreed by A and B |
|----|-------------|---------|------|----------------|---------------|-------------------|
| F-01 | R-02 | "Quickly" has no number or unit, so it cannot be tested. | Vague / not testable | C-01 | State a limit, for example: 95% of booking requests complete within 2 seconds. | (fill) |
| F-02 | R-04, R-05 | R-04 fixes appointments at 15 minutes while R-05 lets doctors set 10 to 30 minutes. | Contradiction | C-07 | Make 15 minutes the default and keep R-05 as the doctor setting. | (fill) |
| F-03 | R-08 | "User-friendly for all age groups" has no measurable criterion. | Vague / not testable | C-04 | Example: 90% of patients aged 65+ can book an appointment within 3 minutes without help. | (fill) |
| F-04 | R-09 | "Securely" names no protection measure. | Vague | C-11 | Name measures, such as encryption of stored records and login for every access. | (fill) |
| F-05 | R-09 | No roles are listed for who may read a patient's medical record. | Missing | C-10 | Add a role and permission table (patient, doctor, receptionist, administrator, DPO). | (fill) |
| F-06 | (whole SRS) | No retention period for patient records. | Missing | C-12 | State how long records are kept and how they are deleted. | (fill) |
| F-07 | R-12 | "Normal working hours" is not defined. | Ambiguous | C-03 | Give exact hours, for example Monday to Saturday, 08:00 to 20:00, and say if booking is online 24/7. | (fill) |
| F-08 | R-13 | "Clinic policy" is not named or linked; the requirement cannot be checked. | Missing reference | C-09 | Reference the policy document by name and version, or write the rule. | (fill) |
| F-09 | R-07 | One requirement asks for three things (cancel, update schedule, notify receptionist). | Not atomic | C-19 | Split into three requirements, each testable on its own. | (fill) |
| F-10 | R-07 | "Cancel at any time" allows cancelling just before the appointment, so the slot cannot be reused. | Risk, no limit | C-16 | Set a cancellation deadline, for example at least 2 hours before. | (fill) |
| F-11 | R-11 | "Active appointments" is not defined (does a past or cancelled one count?). | Ambiguous | C-20 | Define active = booked and not yet attended, cancelled or expired. | (fill) |
| F-12 | R-06 | Reminder has no timing (and no channel such as SMS or email). | Incomplete | C-08 | Example: reminder 24 hours and 2 hours before, by SMS. | (fill) |
| F-13 | (whole SRS) | No requirement about how many users the system must handle at once; Monday mornings are a known risk. | Missing | C-02 | Add a load requirement, for example 100 simultaneous users, with response time under load. | (fill) |
| F-14 | R-10 | Walk-in booking exists but nothing gives emergency walk-ins priority. | Missing | C-14 | Add an emergency flag and rule for which patient is seen first. | (fill) |
| F-15 | R-01 | Booking is online only; a patient without internet access has no stated way to book. | Missing | C-13 | Add booking through the receptionist by phone or in person. | (fill) |
| F-16 | R-05, R-14 | Doctors can set length and view schedule, but cannot block time for leave or breaks. | Missing | C-15 | Add: doctors can block time slots. | (fill) |
| F-17 | R-14 | Only doctors can view schedules; receptionists need every doctor's schedule to book and re-book. | Missing | C-18 | Add: receptionists can view all doctors' schedules. | (fill) |
| F-18 | R-03 | States that double bookings are prevented but not what happens when two patients ask for the same slot together. | Incomplete | C-06 | Add: the first confirmed request wins and the second patient is shown other free slots. | (fill) |
| F-19 | (whole SRS) | The clinic administrator is named as a user, but no requirement mentions what the administrator can do. | Missing | C-16 | Add administrator requirements (manage doctors, working hours, settings). | (fill) |

## Items we disagreed on
| Item | A's answer | B's answer | Final decision and reason |
|------|------------|------------|---------------------------|
| (fill) | | | |

## Lessons for checklist v0.2
- (fill, for example: C-06 and C-13 caused doubt, so rewrite them more clearly)
- (fill, for example: add items for missing administrator requirements)
