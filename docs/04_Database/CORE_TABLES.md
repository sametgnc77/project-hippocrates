# Core Tables

## Purpose

This document defines the first core database tables of MENTIS.

These tables are draft tables.

They may change before implementation.

---

# 1. users

Stores user identity and basic settings.

Fields:

- id
- name
- email
- created_at
- updated_at

---

# 2. learning_packs

Stores supported exam / learning systems.

Examples:

- TUS
- YDUS
- DUS
- USMLE
- PLAB
- KPSS

Fields:

- id
- name
- description
- status
- created_at
- updated_at

---

# 3. branches

Stores main branches inside a learning pack.

For TUS examples:

- Internal Medicine
- Pediatrics
- Surgery
- Obstetrics and Gynecology
- Pharmacology
- Pathology
- Microbiology
- Anatomy
- Physiology
- Biochemistry

Fields:

- id
- learning_pack_id
- name
- description
- created_at
- updated_at

---

# 4. topics

Stores topics under branches.

Example:

Branch: Internal Medicine

Topics:

- Endocrinology
- Cardiology
- Nephrology
- Gastroenterology

Fields:

- id
- branch_id
- parent_topic_id
- name
- description
- created_at
- updated_at

---

# 5. concepts

Stores atomic medical concepts.

Examples:

- Hypercalcemia
- Primary Hyperparathyroidism
- PTHrP
- Graves Disease
- Diabetic Ketoacidosis

Fields:

- id
- topic_id
- name
- summary
- importance_score
- confidence_score
- created_at
- updated_at

---

# 6. knowledge_edges

Stores relationships between concepts.

Examples:

- Hypercalcemia -> Primary Hyperparathyroidism
- DKA -> Potassium
- Graves Disease -> TRAb

Fields:

- id
- source_concept_id
- target_concept_id
- relationship_type
- strength
- source_reference_id
- created_at
- updated_at

---

# 7. source_items

Stores registered raw learning sources.

Important:

This table does not store the raw file itself.

It stores metadata and file location.

Examples:

- PDF book
- video lecture
- scanned question bank
- exam PDF
- audio note

Fields:

- id
- user_id
- type
- title
- file_path
- external_storage_type
- status
- created_at
- updated_at

---

# 8. source_references

Stores exact references inside source materials.

Examples:

- Book page 142
- Video timestamp 00:38:12
- Question bank page 55
- Exam question 48

Fields:

- id
- source_item_id
- reference_type
- page_number
- timestamp_start
- timestamp_end
- text_excerpt
- created_at
- updated_at

---

# Design Rule

Every important generated item should connect back to a source reference when possible.
