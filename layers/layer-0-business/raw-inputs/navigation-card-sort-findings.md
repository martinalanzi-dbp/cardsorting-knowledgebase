# Navigation Card Sort Findings — Internal vs. External

**Status:** Source of truth — updated after internal panel, external panel, and validation session
**Last updated:** September 2026

---

## Overview

This document consolidates findings from card-sorting activities run to inform the navigation structure for a training-management platform (with K9 training features). The same 15–18 features were sorted independently by two audiences:

- **Lexipol staff** — organized results around *workflow function* (what job am I doing: configuring, reporting, managing operations)
- **External (agency) users** — organized results around *product domains* (what area am I in: the library, K9 stuff, admin settings)

This internal/external split is a classic IA tension: internal users tend to organize around the tasks they perform, while external/end users tend to organize around the named things they interact with.

A follow-up **team validation session** was run afterward to stress-test the groupings and surface additional feedback.

---

## The 2 audiences

### Internal (5 groups)

**Training Content** · **Configuration** · **Operational Management** · **Records & Reporting** · **Attributes**

- Training Content: Assignments & Learning Plans, Library, Types, Topics, Custom Courses
- Configuration: Course Credits, Settings, Code Manager
- Operational Management: Manage Locations, Inventory, K9 Management, Events Manager
- Records & Reporting: Surveys, Custom Certificates, Reports, Credentials, Recorded Training, Topics, K9 Records
- Attributes (cross-cutting, duplicated from other groups): Types, Topics, Manage Locations

Notes:
- Category labels were actively debated and renamed live: *Learning → Training Content*, *Course → Configuration*, *Training → Records & Reporting*
- K9 items were split across two functional buckets (Operational Management, Records & Reporting) — treated as a feature, not a domain
- Settings and Credentials were split across Configuration and Records & Reporting
- The Attributes concept (Types, Topics, Manage Locations as shared/cross-cutting metadata) was tried and ultimately set aside in favor of Configuration, which read more clearly to the group

### External (5 groups)

**Training Library** · **Analytics/Tracking** · **K9** · **Admin Settings** · **Training Administration/Management**

- Training Library: Library, Types, Topics
- Analytics/Tracking: Surveys, Course Credits, Custom Certificates, Recorded Training, Reports
- K9 (standalone): K9 Records, K9 Management
- Admin Settings (standalone): Settings, Credentials
- Training Administration/Management: Events Manager, Assignments & Learning Plans, Manage Locations, Custom Courses, Code Manager, Inventory

Notes:
- K9 was independently pulled into its own standalone category, merging K9 Records + K9 Management
- Admin Settings was independently pulled into its own standalone category
- Content was split further than internal: "Training Library" (browse/find) is separate from "Training Administration" (assign/manage)
- No Attributes concept was surfaced at all — Types/Topics sat quietly inside Training Library

---

## What the difference means

| Signal | Internal | External |
|---|---|---|
| K9 | Split across two functional buckets | Own standalone category |
| Admin / Settings | Split across Configuration and Records & Reporting | Consolidated into one clean category |
| Content vs. assigning | One combined Training Content bucket | Split into Library (browse) vs. Administration (assign/manage) |
| Cross-cutting metadata | Explicitly surfaced as its own "Attributes" idea | Not surfaced — folded quietly into Training Library |
| Naming style | Functional: Operational Management, Records & Reporting | Literal: Training Library, K9, Analytics/Tracking |

**Big takeaway:** internal staff seem to think in terms of *workflow function* — what job am I doing: configuring, reporting, managing operations. External users seem to think in terms of *product domains* — what area am I in: the library, K9 stuff, admin settings. This matters most for the K9 and Admin Settings debate: external users — who are closer to who'll actually use this navigation day to day — independently chose to give both their own standalone space, without being prompted to.

---

## Item-by-item placement (internal vs. external)

| Item | Internal | External | Status |
|---|---|---|---|
| Library | Training Content | Training Library | Stable concept, different name |
| Assignments & Learning Plans | Training Content | Training Administration/Management | Minor shift |
| Topics | Training Content, Records & Reporting, *and* Attributes | Training Library | New naming conflict found |
| Types | Training Content *and* Attributes | Training Library | New naming conflict found |
| Custom Courses | Training Content | Training Administration/Management | Minor shift |
| Course Credits | Configuration | Analytics/Tracking | Minor shift |
| Settings | Configuration | Admin Settings | Debated again |
| Code Manager | Configuration | Training Administration/Management | Minor shift |
| Manage Locations | Operational Management *and* Attributes | Training Administration/Management | Resolved |
| Inventory | Operational Management | Training Administration/Management | Debated |
| K9 Management | Operational Management | Standalone K9 category | Still contested |
| Events Manager | Operational Management | Training Administration/Management | Minor shift |
| Surveys | Records & Reporting | Analytics/Tracking | Stable concept, different name |
| Custom Certificates | Records & Reporting | Analytics/Tracking | Stable concept, different name |
| Reports | Records & Reporting | Analytics/Tracking | Stable concept, different name |
| Credentials | Records & Reporting | Admin Settings | Debated again |
| Recorded Training | Records & Reporting | Analytics/Tracking | Stable concept, different name |
| K9 Records | Records & Reporting | Standalone K9 category | Still contested |

---

## Resolving the Attributes question (internal-specific)

A closer pair of boards from the internal session — identical placements everywhere, except for whether Types, Topics, and Manage Locations get a standalone "Attributes" group alongside their primary category.

- **With Attributes:** Types, Topics, and Manage Locations each appear twice — once in their primary content category, once again in a standalone Attributes group.
- **Without Attributes:** Same three items settle into a single primary home each; no standalone cross-cutting group.

These two boards represent the internal group's sort shown before and after the Attributes concept was discussed and dropped — not two independent outcomes. Since external users never introduced Attributes at all, it looks like a concept internal staff considered and set aside on their own, rather than one that needs testing with external users too.

**Internal takeaway (verbatim from session summary):** *"Configuration was clearer than Attributes."*

---

## Validation session — additional findings

A follow-up live group session was run to validate the proposed groupings. Key findings:

- **"Training Content"** label approved as-is.
- **Concern raised:** Assignments & Learning Plans feels admin-facing, not learner-facing, within Training Content. (Consistent with external users independently placing it in Training Administration/Management rather than the browsable Library group.)
- **"Types" naming conflict flagged as a real issue:**
  - In Training Content, *Types* = course category (legal, skill development, interpersonal)
  - In Operational Management, *Types* = training modality (conference, field training)
  - This is not a placement disagreement — it's the same label carrying two different meanings.
  - **Suggested fix:** rename one instance to "Category" before the next round.
- **Code Manager:** used primarily for accreditation codes (POST numbers, KALEA); not universally adopted across agencies. (Adoption note, not a navigation/placement issue.)
- **Inventory:** debated between operational and analytics framing; leaned operational due to its tracking function.
- Prior week's proposed structure was largely validated by this session's groupings.

---

## What still needs a decision

These are open items that repeated sorting alone hasn't resolved — they need a deliberate design call.

### 1. K9 placement
Internal staff split K9 across two functional buckets; external users independently gave it its own standalone category. The validation session listed it both standalone *and* inside Operational Management in the same pass. External users leaning standalone without prompting is a meaningful signal in favor of giving K9 its own space.

**Sub-decision:** if K9 goes standalone, does it absorb both K9 Management *and* K9 Records (as external users did), or does K9 Records stay with Records & Reporting (as internal staff did)?

### 2. "Types" means two different things
Same label, two different underlying concepts (course category vs. training modality). Needs a naming fix — suggested: rename one instance to "Category" — before further testing, so participants aren't sorting one word into two unrelated ideas.

### 3. Admin Settings keeps reappearing and dissolving
Internal staff split Settings and Credentials across two other categories; external users independently consolidated them into a standalone Admin Settings group. Flagged as "debated" again in the validation session. Worth testing this specific pairing with both audiences rather than assuming either grouping holds.

### 4. Assignments & Learning Plans reads as admin-facing
Flagged in the validation session as feeling admin-facing rather than learner-facing within Training Content. External users already separated it out into Training Administration/Management. Worth checking whether a browse-vs-assign split should carry into the final IA regardless of audience.

---

## Recommendation going into review

**Stable across every audience and session — proposed core structure:**

> Training Content · Configuration · Operational Management · Records & Reporting

These four held up across internal, external, and validation sessions, even where naming and edge-item placement differed between groups.

**Open decision to bring to the team:** K9 Management — standalone category, or inside Operational Management?

- **Standalone** — what external users chose independently; also explains why it was "most discussed" internally (it may not fit any existing internal bucket cleanly)
- **Inside Operational Management** — matches the internal sort; fits functionally alongside Manage Locations, Events Manager, Inventory

**Attributes:** tried and set aside internally, never surfaced externally — not recommended for the final structure.

---

## Sources

- Internal live group card sort
- External live group card sort
- Team validation session notes
- Internal with/without-Attributes board pair (same session, before/after discussion)
