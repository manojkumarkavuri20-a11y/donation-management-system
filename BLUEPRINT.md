# Blueprint: Donation Management System

## Why this project exists

During my internship at Care4Calais I saw first-hand how a grassroots donation collection point actually runs day to day: donations arriving faster than they can be logged, storage that grows organically rather than by design, and volunteers relying on memory and word of mouth rather than a documented process. This project is my attempt to design what a structured version of that operation would look like, using the kind of process-improvement thinking a business or operations analyst would bring to it. It is a self-initiated design exercise built after the internship, not a system I built or deployed while there, and it was never formally rolled out or measured against a live site.

## The five-area framework

The redesign is organised around five operational areas rather than one big rewrite, because that is how the underlying problems actually showed up: intake, storage, volunteer coordination, donor communication, and reporting. Donation intake gets a standardised form and a fixed categorisation scheme, so every item is logged the same way regardless of who is on shift. Storage moves from ad-hoc piling to zone-based storage with an audit trail, so anyone can find or verify an item without asking around. Volunteer coordination gets defined roles, a training guide, and a shift schedule, replacing the informal handoffs that make a collection point fragile when one or two experienced people are away. Donor communication gets fixed templates for acknowledgement and updates, so donors hear back consistently rather than depending on whoever happens to be free. Reporting moves into an Excel-based dashboard, so the state of the operation is visible at a glance rather than living in one person's head.

## Where the modelled time savings come from

The processing-time estimates in the README (intake dropping from roughly 35 to 12 minutes, dispatch preparation from 45 to 10, item retrieval from 15 to 4) are not measurements from a live rollout, since the system was never formally deployed. They are modelled estimates built directly from the redesign logic itself: removing duplicated handling steps (an item currently gets picked up, put down, and picked up again at several points in the old process) and moving preparation work ahead of collection rather than doing it reactively when a collection is already underway. I built the estimates by walking through the old process and the redesigned process step by step and comparing handling counts and wait states, which is also exactly how I would defend the numbers if asked in an interview.

## The document set

`Donation_Management_System_Refined.docx` is the master document: the full analysis of the current state, the five-area redesign, and an implementation plan. `DonationTracker_v2.xlsx` is the operational tool that actually implements the reporting area of the framework: an intake log, dashboards, and reporting templates a volunteer coordinator could use immediately. The five checklists and guides (communication templates, daily operations, donor drop-off, implementation, volunteer onboarding, zone audit) are the artefacts that make the other four areas usable on the ground rather than just described in a document; a volunteer coordinator could hand any one of them to a new volunteer without further explanation. The five diagrams (framework, before/after comparison, storage layout, system architecture, workflow process, plus a one-page project summary) are there because a process redesign like this is much easier to approve and adopt when a stakeholder can see it rather than only read about it.

## What I'd add next

The natural next step is a small pilot: running the redesigned intake and storage process for a single week at a real or simulated collection point and comparing actual handling times against the modelled estimates, to see how close the model gets to reality and where it needs adjusting.
