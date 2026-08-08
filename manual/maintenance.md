---
layout: page
title: Backoffice
---

# Maintenance
{:.no_toc}

Regular maintenance is necessary to keep the system operational, up to date, and useful for the community. For the Minodu LCN, maintenance is shared between local users, technical partners, and content partners. The following structure defines the main responsibilities and recommended maintenance rhythm.

## 1. Roles and responsibilities

### Community focal point - daily/regular operational check

The community focal point is the first person responsible for checking that the system is available and functioning from the user's perspective.

**Main responsibilities:**

* Check that the system is switched on and accessible.
* Verify that the main interface and content can be opened normally.
* Check whether users encounter obvious problems.
* Collect and report recurring issues or user feedback in the WhatsApp group.
* The technical focal point will be imformed if a technical intervention is needed.

**Recommended frequency:**
A quick operational check should be carried out regularly, ideally as part of the normal use of the system.



### Technical focal point - first-line technical support : Fablab/CAVRIS

The technical focal point is responsible for basic technical troubleshooting and for coordinating technical problems with the appropriate technical partner.



**Main responsibilities:**

* Check the power supply and physical connections.
* Restart the Raspberry Pi when necessary.
* Check whether the system starts correctly after a restart.
* Check basic network/connectivity issues where applicable.
* Document technical problems and attempted solutions.
* Escalate problems that cannot be solved locally to the maintenance whatsapp group.

**Recommended frequency:**
Intervention when a problem is reported, plus a periodic basic technical check.



### Kara University - content and knowledge support

Kara University supports the quality and relevance of the information available through the system, particularly agricultural and climate-related content.



**Main responsibilities:**

* Support content updates.
* Create new audios/content through the '' Cellule de communication scientifique ''.
* Provide expert answers to agriculture and climate-related questions in the forum
* Provide expert feedback when content needs to be corrected or updated.
* Help identify new content needs based on community feedback.



**Recommended frequency:**
New content should be add periodically or whenever new audios are available from the '' Cellule de communication scientifique ''.



### Fablab / CAVRIS - technical maintenance

Fablab/CAVRIS provides higher-level technical support and maintains the system.



**Main responsibilities:**

* Diagnose technical problems that cannot be solved locally.
* Maintain and update the Raspberry Pi and associated software.
* Check system performance and storage.
* Perform necessary software or system updates.( Digital inspiration for assistance)
* Support hardware troubleshooting and replacement when required.(Ecoteclab for assistance)
* Maintain technical documentation.
* Support recovery in case of system failure.
* Provide the technical focal point that will coordinate with the focal point when an intervention is required.



**Recommended frequency:**
Periodic preventive maintenance, in addition to intervention when technical problems are reported.



## 2. Maintenance rhythm

A simple maintenance calendar helps prevent problems before they affect users.

| Activity                                    | Recommended frequency              | Responsible                                  |
| ------------------------------------------- | ---------------------------------- | -------------------------------------------- |
| Check that the system is running            | Regular / daily when in active use | Community focal point                        |
| Check power and basic hardware              | when problems occur                | Community focal point                        |
| Check system performance                    | Monthly                            | Technical focal point / Fablab-CAVRIS        |
| Backup/export weather data                  | Monthly                            | Technical focal point / Fablab-CAVRIS        |
| Review and new contents                     | Periodically / at least quarterly  | Kara University                              |
| Check and update system/software            | As needed / scheduled maintenance  | Fablab-CAVRIS                                |
| Forum moderation                            | Weekly                             | Community focal point / designated moderator |
| Review user feedback and recurring problems | Regular                            | Community focal point + Kara University      |
| Full maintenance review                     | Every 6 months                     | All focal points                             |

The exact rhythm can be adapted according to the frequency of use, available connectivity, and local capacity.



## 3. Backup and data management

Backups should be performed regularly to avoid losing locally stored data in case of hardware failure or accidental deletion.



### Recommended backup rhythm

**Monthly:**

* Export or back up weather data.
* Check that the backup was completed successfully.
* Keep the most recent backup in a safe location.
* Where possible, maintain more than one copy of important data.

The backup procedure should be documented in the technical documentation so that another person can perform it if the usual technical focal point is unavailable.



## 4. Forum moderation

### Recommended rhythm: weekly

The moderator should:

* Check new posts and questions.
* Identify unanswered questions.
* Remove or flag inappropriate or irrelevant content where necessary.
* Forward technical questions to the technical focal point.( Whatsapp group)
* Forward agricultural or climate questions requiring expert input to Kara University.( Whatsapp group)
* Identify recurring questions or feedback that could lead to content improvements.

Forum moderation should not only be seen as content control: it is also an important **feedback loop** for improving the system and understanding users' needs.



## 5. Problem reporting and escalation

When a problem occurs, it should be reported through a simple escalation process:

**User / Community / Community focal point --> Whatsapp group ( --> Kara University --> Technical focal point --> Fablab/CAVRIS )**

For content-related issues:

**User / Community / Community focal point --> Whatsapp group ( --> Kara University )**

For issues involving both content and technology, the Technical Focal Point and Kara University should coordinate with Fablab/CAVRIS and technical partners as appropriate.

Each significant problem should ideally be recorded with:

* Date and time
* Description of the problem
* Person reporting it
* Actions already taken
* Result of the intervention
* Whether further action is required



## 6. Maintenance log - Fablab/CAVRIS

A simple maintenance log can be used to keep track of interventions.

| Date       | Problem / activity             | Person responsible    | Action taken           | Result           | Follow-up               |
| ---------- | ------------------------------ | --------------------- | ---------------------- | ---------------- | ----------------------- |
| YYYY-MM-DD | Example: system not accessible | Technical Focal Point | Restarted Raspberry Pi | System restored  | Monitor                 |
| YYYY-MM-DD | Monthly backup                 | Technical Focal Point | Weather data exported  | Backup completed | Next backup: YYYY-MM-DD |

Keeping this log makes it easier to identify recurring problems and ensures that maintenance knowledge is not dependent on one person.

## 7. Minimum maintenance checklist

Before considering maintenance complete, verify:

* [ ] System starts correctly.
* [ ] Power supply is stable.
* [ ] Raspberry Pi is operational.
* [ ] Main interface/content is accessible.
* [ ] Recent data is available.
* [ ] Scheduled backup has been completed.
* [ ] Forum has been checked.
* [ ] Reported technical problems have been recorded.
* [ ] Content issues have been forwarded to the appropriate focal point.
* [ ] Any unresolved problem has a designated person responsible for follow-up.

