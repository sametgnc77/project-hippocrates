# Requirements Specification

## Product Name

MENTIS

## Internal Code Name

Project Hippocrates

## First Learning Pack

TUS Learning Pack

---

# Purpose

This document defines what MENTIS must be able to do.

Architecture, database design, AI design, and code must follow these requirements.

---

# Requirement Categories

MENTIS requirements are divided into the following categories:

1. Core Product Requirements
2. User Interface Requirements
3. Source Library Requirements
4. AI Core Requirements
5. Learning Engine Requirements
6. Flashcard Requirements
7. Question & Exam Requirements
8. Voice Tutor Requirements
9. Analytics Requirements
10. Technical Requirements

---

# 1. Core Product Requirements

## R-001

The system must function as an AI-powered personal learning operating system.

## R-002

The system must support multiple learning packs in the future.

Examples:

- TUS
- YDUS
- DUS
- USMLE
- PLAB
- KPSS

## R-003

The first learning pack must be TUS.

## R-004

The system must separate raw source files from processed learning intelligence.

## R-005

The system must remain useful even when raw source files are unavailable.

## R-006

Every meaningful user action must update the learning model when possible.

## R-007

No user data should be treated as single-use data.

## R-008

Every major module must feed at least two other modules.

---

# 2. User Interface Requirements

## R-009

The system must provide a web panel.

## R-010

The system must provide a Telegram bot.

## R-011

The system must support future Android application integration.

## R-012

The web panel must show daily, weekly, and monthly progress.

## R-013

The web panel must show learning tasks.

## R-014

The web panel must show flashcards.

## R-015

The web panel must show uploaded sources.

## R-016

The web panel must show knowledge graph relationships.

## R-017

The Telegram bot must send daily tasks.

## R-018

The Telegram bot must receive user updates.

## R-019

The Telegram bot must support review sessions.

## R-020

The Telegram bot must support quick wrong-answer entry.

---

# 3. Source Library Requirements

## R-021

The system must allow the user to register PDF files.

## R-022

The system must allow the user to register video files.

## R-023

The system must allow the user to register scanned book pages.

## R-024

The system must allow the user to register question bank scans.

## R-025

The system must allow the user to register practice exams.

## R-026

The system must allow the user to register audio notes.

## R-027

Raw source files may be stored on a local SSD.

## R-028

Processed learning data must be stored separately from raw source files.

## R-029

Each processed item must keep a reference to its source when possible.

Examples:

- book page
- video timestamp
- question page
- exam name
- user note

---

# 4. AI Core Requirements

## R-030

The system must use AI to parse uploaded materials.

## R-031

The system must use AI to classify information using PACER++.

## R-032

The system must use AI to generate flashcards.

## R-033

The system must use AI to criticize and improve generated flashcards.

## R-034

The system must use AI to detect teacher emphasis in video transcripts.

## R-035

The system must use AI to align videos with book pages.

## R-036

The system must use AI to analyze wrong answers.

## R-037

The system must use AI to update knowledge graph relationships.

## R-038

The system must use AI to generate personalized study tasks.

## R-039

The system must support multiple AI models through a model router.

## R-040

AI-generated content must be clearly marked as AI-generated.

## R-041

Critical AI outputs must include confidence scores.

## R-042

Critical AI outputs must preserve source traceability.
