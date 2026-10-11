# -Pixel-3-Android-10-Evidence-Case-Study
A practical mobile forensics project documenting the structured examination of an authorised Android 10 logical copy from a Google Pixel 3. The case study demonstrates artefact identification, manual validation, timestamp interpretation, and cross-source correlation across Android system services, Google applications, and selected third-party applications.

**Project Overview**
This repository accompanies Case File CIPB106 Android10 and presents an evidence-reconstruction workflow for a supplied Pixel 3 Android 10 training package. It focuses on what the authorised material can establish about the device environment, accounts, settings, installed applications, communications, media, location-related artefacts, and selected activity. The work uses neutral forensic terminology and distinguishes verified facts from inference, uncertainty, and information that remains unknown.

**Objectives**
•	Document a reproducible examination workflow for the supplied logical copy.
•	Identify relevant AOSP, Google Mobile Services, and third-party application artefacts.
•	Preserve raw values and explain timestamp and coordinate conversions.
•	Correlate findings across independent sources where the evidence permits.
•	Record empty, unavailable, encrypted, or unverified sources as limitations.

**Evidence Scope and Limitations**
The source material is a course-issued logical copy acquired after TWRP root access; it is not a bit-for-bit image. Accordingly, the project supports conclusions only about artefacts present and reliably interpreted in the supplied package. The acquisition process does not establish that the original device user rooted or compromised the phone. Application presence, account records, contact labels, coordinates, and timestamps do not independently identify the person operating the device or prove physical presence.

**Artefacts Examined**
•	AOSP services: SMS/MMS, contacts, call history, user profile, and calendar records.
•	Google applications: Messages, Dialer, Maps, and Photos databases and supporting files.
•	Third-party applications: Kik, TextNow, WhatsApp, and Snapchat artefacts where present.
•	Contextual records: package metadata, shared preferences, media paths, location-related data, and account identifiers.

**Tools and Environment**
•	Kali Linux in VMware Workstation
•	Android Debug Bridge (ADB)
•	DB Browser for SQLite
•	Linux command-line utilities, including ls, tree, find, and cat
•	Approved XML and protocol-buffer parsers where required

**Methodology**
1.	Verify the working copy against the applicable course manifest and record the integrity result.
2.	Document acquisition provenance, working location, access time, and tool versions.
3.	Survey the file system and identify relevant packages, databases, XML files, and media directories.
4.	Examine source records manually and retain the path, table or key, row context, and raw value.
5.	Convert timestamps and coordinates with the source unit, method, and time zone clearly stated.
6.	Correlate material findings across independent artefact families.
7.	Report findings with qualifications, alternative explanations, and acquisition limitations.
   
**Selected Findings**
•	A call-log record was interpreted as an incoming missed call on 12 February 2020 with a recorded duration of zero seconds.
•	The associated location label, Questa, MN, is treated as database or lookup context rather than proof of a caller’s physical location.
•	The events, attendees, and reminders tables in calendar.db contained no relevant records in the supplied copy; this is a documented absence, not proof that no historical calendar activity occurred.
•	Additional application, communication, media, account, and location-related sources were examined for their contribution to a corroborated activity reconstruction.

**Repository Guidance**
This repository should contain only sanitised documentation, queries, scripts, directory examples, and non-sensitive screenshots approved for academic submission. Do not commit the original evidence package, extracted private data, credentials, personal account identifiers, phone numbers, precise coordinates, or unredacted screenshots. Use placeholders or masked values when illustrating the workflow.

**Responsible Use and Ethics**
This project is provided for authorised education and defensive digital-forensics practice. It must not be used to access, modify, disclose, or analyse a device or dataset without permission. The examination avoids password recovery, credential disclosure, public evidence uploads, and unsupported attribution of activity to an individual.

**Author and Course Context**
Prepared as part of CIP-B106: Mobile and IoT Forensics. The accompanying report contains the detailed examination notes, source paths, artefact discussions, findings, and stated limitations.

**Disclaimer**
The repository is an academic case study based on authorised training material. Findings are limited to the supplied logical copy and should not be interpreted as legal conclusions, proof of identity, proof of physical presence, or a determination that any person committed an offence.
