CONTROL 01 — Project Goal & Scope

Version: 1.0
Date: 2026-11-16
Status: Authoritative (System-Wide)
Project: RR-Lessons-WordPress

---

# 1. Purpose

This document defines **what RR-Lessons-WordPress is, what it must achieve, and what it must not do**.

Every other CONTROL document serves the goals defined here.

---

# 2. Mission

RR-Lessons-WordPress is a WordPress plugin that shows Approved Runtime Republic
lessons, read from GitHub, on BlueprintLiberty.com. GitHub stays the single
source of truth: if a lesson is not Approved on GitHub, it is not on the website.

---

# 3. Goals

Each goal names the CONTROL document that governs it.

## G1 — Approved lessons only
Only lessons whose header reads `Status: Approved` are shown. Draft, Review and
any other status are refused, with the reason shown to site editors.
See CONTROL 05 (Lesson Source & Approval Rule, drafted before Phase 1).

## G2 — Read-only from GitHub
The plugin reads lessons from GitHub and never writes to GitHub. Lessons are
edited only in their own repository, under that repository's controls.

## G3 — Any repository that follows the essay standard
The essay repository is a setting, never hard-coded. Runtime-Republic-Training
is the first; any repository that follows its lesson standard (that
repository's CONTROL 05) can be used. See CONTROL 05.

## G4 — The record travels with the lesson
Every shown lesson displays its header facts (course, lesson number, runtime,
podcast link), a link to its source file on GitHub, and the version shown.

## G5 — Engineering integrity
All behavior is documented, layered, tested and traceable.
See CONTROL 03, 10, 14 and 15.

---

# 4. Success Criteria (first release)

• A site editor places `[rr_lesson]` on a page, naming a lesson, and visitors
  see that lesson's text and header facts.
• A lesson that is not `Status: Approved` is never shown to visitors.
• Every shown lesson links to its source file on GitHub.
• A change merged on GitHub appears on the site without editing WordPress.
• The plugin is tested on a local Laragon copy of BlueprintLiberty.com before it
  is installed on the live site.

---

# 5. Out of Scope

• Writing to GitHub, or editing lesson text in WordPress.
• Showing lessons that are not Approved, even to logged-in visitors.
• Hosting or playing audio files (the lesson's podcast link is shown only).
• RuntimeRepublic.com, which is a GitHub Pages site, not WordPress.

---

# 6. Glossary

| Term | Meaning |
|------|---------|
| Lesson | A `lesson.md` file in an essay repository, with a header block (Course, Lesson, Status, Runtime, Podcast, Approved by, …) |
| Essay repository | A GitHub repository that follows the Runtime-Republic-Training lesson standard |
| Approved | A lesson whose header reads `Status: Approved` |
| Shortcode | `[rr_lesson …]`, placed on a WordPress page to show one lesson |
| Human Engineer | James A. Hodges, sole authority over every decision |

---

# 7. Relationship to Other Controls

• CONTROL 02 — Development Phase Plan
• CONTROL 05 — Lesson Source & Approval Rule (planned)
• CONTROL 10 — Architectural Separation & Logic Sovereignty

---

# 8. Revision Policy

Changes to goals require explicit Human Engineer approval and a version bump.

---

END OF DOCUMENT
