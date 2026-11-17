CONTROL 02 — Development Phase Plan

Version: 1.0
Date: 2026-11-16
Status: Authoritative (System-Wide)
Project: RR-Lessons-WordPress

---

# 1. Purpose

Defines the ordered phases of development. A phase may not begin until the
previous phase's exit gate is met (CONTROL 11: incremental, single-threaded execution).

---

# 2. Phase 0 — Foundation

Deliverables:

• CONTROL documents 00–04, 08, 10, 11, 14–16 filled in
• Repository structure per CONTROL 04
• Test harness and architecture guard tests (CONTROL 15)
• CI running checks and tests on every push

Exit gate: CI green; `scripts/check-controls.sh --strict` passes for the Phase 0 documents.

---

# 3. Phase 1 — Lesson Embed

Entry: CONTROL 05 (Lesson Source & Approval Rule) approved by the Human Engineer.

Deliverables:

• `[rr_lesson]` shortcode that shows one lesson from the configured essay repository
• Approval check: anything other than `Status: Approved` is refused (CONTROL 01 G1)
• Header facts, source link and version shown with the lesson (G4)
• Markdown shown as HTML; any library used is approved by the Human Engineer
  first (CONTROL 08)
• A settings page holding the essay repository (G3)

Exit gate: an Approved lesson shows on a local Laragon copy of BlueprintLiberty.com,
a Draft lesson is refused there, and a test proves the refusal.

---

# 4. Phase 2 — Lesson Library

Deliverables:

• A course page listing every Approved lesson in a course, in lesson order
• Each listed lesson opens on its own page through the Phase 1 shortcode

Exit gate: one full course is browsable on the Laragon copy, with no
unapproved lesson listed.

---

# 5. Phase 3 — Live Site

Deliverables:

• Backup of BlueprintLiberty.com taken before install (CONTROL 16)
• Plugin installed and one course published on BlueprintLiberty.com

Exit gate: the Human Engineer confirms the course on the live site.

---

# 6. Revision Policy

Phases may be reordered only by Human Engineer decision recorded in
`Control/ARCHITECTURE_STATUS.md`.

---

END OF DOCUMENT
