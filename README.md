# Local-First Medical AI

Concepts and workflows for privacy-conscious, local-first AI in clinical documentation — for radiology and other medical specialties.

## Overview

This repository explores practical approaches to medical AI systems designed to operate close to the clinical workflow, with a strong focus on local processing, data privacy, and real-world usability.

The main areas of interest include medical speech recognition, clinical documentation, radiology reporting workflows, and AI-assisted processing of medical imaging data.

## Who it is for

The approach is not limited to radiology. It is designed for any physician who produces documentation through dictation or conversation with a patient, including:

- **Radiology** — MRI, CT and X-ray reports
- **Orthopedics** — examination findings and consultation notes
- **Gynecology** — visit and examination documentation
- **General practice** — notes from conversations with patients
- **Other specialties** — any workflow based on dictated or spoken clinical content

Templates and document structure can be adapted to the specialty and to the requirements of each healthcare facility.

## Clinical problem

Many AI systems used in healthcare depend heavily on cloud processing and disconnected workflows.

In clinical practice, this can create additional friction around:

- sensitive medical data
- workflow integration
- latency and reliability
- dependence on external infrastructure
- physician review and responsibility

A local-first approach aims to reduce these barriers by keeping as much processing as possible within the healthcare environment.

## How it works

```
Audio → Speech recognition → Clinical text processing → Draft documentation → Physician review
```

1. **Audio capture** — dictation or a conversation in the examination room is recorded with professional audio equipment.
2. **Speech recognition** — speech is transcribed locally.
3. **Clinical text processing** — a language model corrects the transcript, organizes it into document sections and fits it to the facility's template.
4. **Draft documentation** — a structured draft is prepared for review.
5. **Physician review** — the physician edits, verifies and approves the final document.

Example:

| Step | Content |
| --- | --- |
| Dictation | *"kolano prawe łąkotka przyśrodkowa bez szczelin ACL zachowane wysięk niewielki"* |
| Structured draft | **Menisci:** medial meniscus without tears. **Ligaments:** ACL intact. **Joint fluid:** small effusion. |

## Areas of interest

### Speech recognition and documentation

Local speech recognition and AI-assisted processing of dictated or conversational clinical content, across specialties.

### Radiology workflow

AI-assisted tools for radiology reporting, including:

- report drafting
- structured information extraction
- workflow automation
- integration with medical imaging and DICOM-based systems
- physician-in-the-loop verification

### Medical imaging

Exploration of AI-assisted interpretation workflows for medical imaging, particularly MRI and musculoskeletal radiology. This work is at the research and development stage and is not available for clinical use.

## Local processing

The core principle is that sensitive medical data should, where technically appropriate, be processed locally within the healthcare organization.

Local processing can provide several advantages:

- improved control over medical data
- reduced dependence on external cloud services
- lower latency
- easier integration with existing clinical infrastructure
- greater flexibility in deployment

Hybrid architectures may still be useful where appropriate, but the local environment remains the primary focus.

## Design principles

- Physician remains in control
- AI output requires clinical verification
- Privacy by design
- Local-first architecture
- Integration into existing workflows
- Modular components
- Interoperability with medical systems

## Roadmap

**Current stage**

- Testing audio devices for dictation and for conversations in the examination room
- Starting beta tests in medical practices

**Next stage**

- Optimizing the full pipeline to run 100% locally, with no cloud processing
- Selecting hardware configurations for local deployment in three versions:

| Version | Goal |
| --- | --- |
| **Standard** | Lowest-cost hardware that runs the full pipeline locally |
| **Medium** | Balance between cost and processing speed |
| **Pro** | Fastest processing for high-volume practices and departments |

## Related projects

- [radiology-text-utils](https://github.com/marcinblaumann/radiology-text-utils) — deterministic formatting and normalization of report text, used as a final clean-up step after transcription and structuring.

## Regulatory note

The tools described here are intended to support clinicians, not to replace their decisions. Every generated document requires physician verification.

This repository does not constitute a declaration of conformity or a statement of medical-device certification. Keeping data within the healthcare facility is intended to make it easier to meet data protection (GDPR) requirements. The regulatory status of the solution, including medical-device (MDR) and AI Act requirements, will be assessed as the project develops.

## Project status

Early-stage development with beta testing in medical practices.

This repository documents concepts, workflows, and technical directions. Implementation details and proprietary components are not published here.

## About

Created by [Marcin Blaumann](https://github.com/marcinblaumann), Consultant Radiologist working at the intersection of medical imaging, AI, speech recognition, and clinical workflow automation.

[Website](https://medical-ai.pl) · [LinkedIn](https://www.linkedin.com/in/marcin-b-a16b6a431)
