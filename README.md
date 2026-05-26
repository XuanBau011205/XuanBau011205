# Hi, I'm Bau Doan

I'm a student building toward **Backend, IoT, Database Design, and Mini System Architecture**.

I focus on turning messy technical ideas into clear structures:

* database schemas
* ERD and table relationships
* backend data flow
* state logic
* fault-aware system notes
* Markdown technical documentation

My goal is not to write the most code, but to make small systems clearer before implementation starts.

---

## Current Focus

I'm currently learning and building around small IoT/backend systems where hardware data flows into a backend, database, and dashboard.

Main areas:

* IoT data flow
* Backend system design
* PostgreSQL database design
* State machine / workflow logic
* Sensor fault detection
* Markdown-based technical documentation
* AI-assisted development workflow

---

## Featured Direction

### Mini Backend Architecture

I help small projects clarify backend logic before implementation.

Typical deliverables:

* database schema draft
* ERD / relationship notes
* backend data flow
* state logic
* fault/risk notes
* clean Markdown documentation

---

## Example Logic Pattern

### Two-Level Threshold Logic

A simple fault-aware logic pattern for sensor/control systems:

| A: High Threshold | B: Low Threshold | State  | Meaning                                                                 |
| ----------------: | ---------------: | ------ | ----------------------------------------------------------------------- |
|                 0 |                0 | LOW    | Below low threshold                                                     |
|                 0 |                1 | MEDIUM | Between low and high threshold                                          |
|                 1 |                1 | HIGH   | Above high threshold                                                    |
|                 1 |                0 | FAULT  | Impossible state: high threshold active while low threshold is inactive |

The key idea:

> A good system should not only handle valid states. It should also detect impossible states.

---

## Project Types I Care About

* IoT dashboards
* Sensor monitoring systems
* Small backend applications
* Database-first MVPs
* Student projects
* Technical design documents
* Fault-aware control logic

---

## Tech Stack

### Backend / Database

* Java
* Spring Boot
* PostgreSQL
* SQL
* REST API basics

### IoT / Embedded

* ESP32 basics
* C/C++ basics
* Sensor data flow
* MQTT / HTTP concepts

### Documentation / Design

* Markdown
* Mermaid diagrams
* ERD
* State logic
* Technical design notes

### Frontend Basics

* HTML
* CSS
* JavaScript

---

## What I Can Help With

I can help small projects with:

* database schema review
* ERD design
* backend data flow documentation
* state machine / workflow design
* README and technical documentation
* IoT sensor logic documentation
* fault-state analysis for simple systems

Best fit:

* small apps
* MVPs
* IoT dashboards
* student projects
* early-stage backend/database design drafts

---

## Working Principle

> Architecture reduces ambiguity. Engineering turns clarity into a working system.

I use code, diagrams, and documentation to validate system ideas — but my main focus is clarity, structure, and trade-off thinking.

---

## Current Direction

```text
IoT + Backend + Database + System Design + AI-assisted workflow
```

I am building toward a hybrid skillset where small systems are:

* clear
* testable
* documented
* fault-aware
* easy to extend


<!--
**XuanBau011205/XuanBau011205** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
