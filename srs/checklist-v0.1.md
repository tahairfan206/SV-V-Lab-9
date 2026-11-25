# MediTrack SRS Validation Checklist v0.1

| | |
|---|---|
| Authors | Faizan Ali (SP/24/BSSE/053) and Taha Irfan (SP/2024/BSSE/044) |
| Course | Software Verification & Validation (SV&V) |
| Teacher | Saleha Yousaf |

Rule: every item is Atomic, Observable, Unambiguous and Traceable (AOUT). "Yes" is always the good answer. Allowed answers: Yes, No, N/A.

## Sources used in the "Where question came from" column
| Code | Meaning |
|------|---------|
| Rule: Testable / Complete / Unambiguous / Consistent / Atomic | Rules of a good requirements document |
| Risk 1 | Double bookings |
| Risk 2 | Patients forget appointments, which costs money |
| Risk 3 | Medical information is private |
| Risk 4 | Elderly patients and emergency walk-ins are left out |
| Risk 5 | Monday mornings are very busy |
| User: Patient / Doctor / Receptionist / Administrator / DPO | What that person would look for in the document |

## Checklist
| ID | Item | Answer | Evidence | Where question came from |
|----|------|--------|----------|--------------------------|
| C-01 | Does every requirement about response time state a maximum time in seconds? | | | Rule: Testable; Risk 5 |
| C-02 | Does the document state how many users must be able to use the system at the same time? | | | Rule: Complete; Risk 5 |
| C-03 | Does the document give the exact opening and closing times for system availability? | | | Rule: Unambiguous; User: Patient |
| C-04 | Does every ease-of-use requirement include a measurable pass criterion? | | | Rule: Testable; Risk 4; User: Patient |
| C-05 | Does the document contain a requirement that prevents two bookings of the same doctor at the same time? | | | Risk 1 |
| C-06 | Does the document say what happens to the second patient when two patients request the same time slot together? | | | Risk 1; Rule: Complete |
| C-07 | Do all requirements that mention appointment length give the same length? | | | Rule: Consistent |
| C-08 | Does the document say how long before an appointment a reminder is sent? | | | Risk 2; User: Patient |
| C-09 | Does every requirement that refers to a clinic policy say where that policy is written? | | | Rule: Complete; Rule: Traceable |
| C-10 | Does the document list which roles may read a patient's medical record? | | | Risk 3; User: DPO |
| C-11 | Does every security requirement name a specific protection measure? | | | Rule: Testable; Risk 3 |
| C-12 | Does the document state how long patient records are kept? | | | Risk 3; User: DPO |
| C-13 | Does the document say how a patient with no internet access can book an appointment? | | | Risk 4; User: Patient |
| C-14 | Does the document say how an emergency walk-in patient gets priority? | | | Risk 4; User: Receptionist |
| C-15 | Does the document say how a doctor can block time for leave or breaks? | | | User: Doctor |
| C-16 | Does the document set a limit on how late a patient may cancel? | | | Risk 2; User: Administrator |
| C-17 | Does the document say that receptionists can book appointments for walk-in patients? | | | User: Receptionist |
| C-18 | Does the document say that receptionists can see the schedule of every doctor? | | | User: Receptionist |
| C-19 | Does each requirement ask for only one thing? | | | Rule: Atomic |
| C-20 | Does the document define the word "active" for appointments? | | | Rule: Unambiguous |
