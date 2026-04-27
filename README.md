# CS-255-Portfolio
Portfolio artifacts from CS-255 System Analysis and Design DriverPass project.

# DriverPass System — CS-255 Portfolio Artifacts

This repository contains portfolio artifacts from CS-255 System Analysis and Design at Southern New Hampshire University. The artifacts document the analysis and design work completed for the DriverPass project, a fictional client used throughout the course.

## Contents

| File | Description |
|------|-------------|
| `DriverPass_BRD.docx` | Business Requirements Document from Project One. Captures the purpose, scope, objectives, functional requirements, nonfunctional requirements, assumptions, constraints, and project schedule for the DriverPass system. |
| `DriverPass_SDD.docx` | System Design Document from Project Two. Contains the UML diagrams (use case, activity, sequence, and class) and the technical requirements that translate the business requirements into a buildable system design. |

Together, these documents demonstrate the ability to collect requirements from a client and design a system that meets those needs.

## Reflection

**Briefly summarize the DriverPass project. Who was the client? What type of system did they want you to design?**

The client was DriverPass, a driving instruction and test preparation company represented in the interview transcript by the owner, Liam, and the IT officer, Ian. DriverPass identified a business problem: too many students fail the driving test on their first attempt, and existing preparation options do not combine online study material with practical on-the-road training. The solution they requested was a cloud-based web application accessible from any internet-connected device. The system needed to support customer account registration, online practice exams modeled on DMV content, reservations for two-hour driving lessons matched to a specific driver and car, three tiered service packages, role-based access for the Secretary, IT Officer, and Owner, activity logging with printable reports, automated password resets, and integration with the DMV for updates on rules, policies, and sample questions.

**What did you do particularly well?**

Every requirement in the business requirements document traces back to a specific statement in the interview transcript. Rather than inventing features or substituting assumptions for evidence, functional requirements were extracted from Liam's business vision and nonfunctional requirements were extracted from Ian's security and infrastructure concerns. The system design document preserved that traceability by mapping each technical requirement to its source in the business requirements. The UML diagrams stayed within the documented scope, which kept the design focused on what DriverPass actually asked for rather than expanding into unnecessary complexity.

**If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?**

The sequence diagram in the system design document captured only the successful path for the Create Reservation use case. It did not include alternative flows for scenarios such as an unavailable driver, an unavailable car, or a failed payment. I would revise the diagram to add alt fragments showing these error paths, which would give developers a more complete picture of the interactions they need to implement. I would also tighten the class diagram by distinguishing aggregation from composition on relationships such as Reservation to Customer, since that distinction affects how the eventual database handles cascading record deletion.

**How did you interpret the user's needs and implement them into your system design? Why is it so important to consider the user's needs when designing?**

The interview transcript served as the authoritative source, and the stakeholders were separated by role before any requirement was written. Liam's statements defined business goals and customer-facing features, which became functional requirements. Ian's statements defined security, logging, and infrastructure constraints, which became nonfunctional and technical requirements. Each distinct user type named in the transcript, including Customer, Secretary, IT Officer, and Owner, received a dedicated actor in the use case diagram and a defined set of permissions in the role-based access design. Considering the user's needs matters because a system built on assumptions rather than stated needs tends to miss the problem it was meant to solve, which produces low adoption, costly rework, and wasted development effort.

**How do you approach designing software? What techniques or strategies would you use in the future to analyze and design a system?**

My approach starts with requirements gathering from documented sources such as interview transcripts and stakeholder notes, followed by modeling the system before any code is written. Process models clarify how data moves through the system, object models identify the components and their relationships, and UML diagrams communicate both structure and behavior to other stakeholders. Each design decision is validated by tracing it back to a requirement. In future projects I would add two techniques that were not used here. First, I would build low-fidelity prototypes of key user interfaces before finalizing the design, so that stakeholders can respond to something concrete rather than to diagrams alone. Second, I would apply iterative review checkpoints with the client after each major modeling phase, which would surface misinterpretations earlier than a single end-of-project review.

## Course

CS-255 System Analysis and Design
Southern New Hampshire University
