# FarmQuest — Product Requirements Document (PRD)

**Version:** 1.0 (MVP / Pilot)
**Date:** July 2026
**Status:** Draft for pilot approval

---

## 1. Product Overview

FarmQuest is an interactive, choose-your-own-adventure storytelling game for middle and high school students (grades 6–12) that connects classroom learning to real visits at local farms.

Each FarmQuest experience is a three-phase narrative journey:

1. **Pre-visit (in class):** Students begin a branching story on Chromebooks that sets up characters, a mystery or mission, and the farm they are about to visit.
2. **On-site (at the farm):** Students use their own phones to scan QR codes posted at farm stations (barn, coop, field, market stand, equipment shed). Each scan unlocks the next story chapter, tied to what students are physically standing in front of, with choices that branch the narrative.
3. **Post-visit (in class):** Students complete the story's finale and a reflection chapter that consolidates what they learned.

Stories are **pre-generated using the OpenAI API** as branching "story packs," customized per farm and per class, and **reviewed by teachers before the trip**. Students never interact with the AI directly — this keeps the experience safe for minors, nearly free to operate, and functional on farms with poor connectivity.

Story tone and content must remain appropriate and appealing for K-12 students, and comfortable for parents and educators to endorse.

---

## 2. Problem Statement

**For students:** Farm field trips are one of the few chances students in grades 6–12 get to see agriculture, food systems, and rural careers firsthand — but the visits are often passive walk-throughs. Students shuffle between stations, half-listen, and retain little. Middle and high schoolers in particular disengage from experiences that feel like they were designed for younger kids.

**For teachers:** Teachers struggle to connect a one-day trip to their curriculum. Prep materials are generic or nonexistent, there's no structured activity during the visit, and post-trip reflection is usually a worksheet nobody enjoys. Building custom materials for a specific local farm is more work than most teachers can take on.

**For farms:** Local farms that host school groups have no tools to make visits engaging or educational beyond a guided tour. A better visit experience means better relationships with schools and repeat bookings, but farms lack the time and expertise to create it.

**The gap:** No existing product turns a real farm visit into a structured, narrative, curriculum-connected learning experience. Educational games are screen-only; field trip materials are paper-only. FarmQuest bridges the two: a story that starts in the classroom, physically unfolds across the farm, and concludes back in class.

---

## 3. Goals & Non-Goals

### Goals (Pilot)
- Validate that a story-driven farm visit measurably increases student engagement versus a standard visit.
- Validate that teachers will adopt, review, and run FarmQuest with minimal training (< 30 minutes).
- Validate that farms will host QR stations and see value in participating.
- Prove the pre-generated story pack model: high-quality, safe, curriculum-relevant branching stories at near-zero marginal cost.
- Operate the entire pilot for **under $50/month** in API + hosting costs.

### Non-Goals (Pilot)
- Revenue or monetization (business model decided after the pilot).
- Grades K–5 support (story reading level targets grades 6–12).
- Native mobile apps or app-store distribution.
- Live/real-time AI story generation for students.
- Student accounts with personal data, grading integration, or LMS integration.
- Supporting farms/schools beyond the pilot cohort (2–5 schools, 1–3 farms).

---

## 4. Personas & Key User Journeys

### Persona 1 — Maya, 7th-grade student (age 12)
Curious but easily bored; has her own phone; groans at anything that feels babyish; loves games with choices and secrets.

**Key journey:**
1. In class, Maya's teacher opens FarmQuest on the projector and each student (or pair) opens the class link on a Chromebook. Maya picks a story role and makes the first choices in Chapter 1: a mystery is unfolding at Hilltop Farm — the harvest numbers don't add up, and her character is called in to investigate.
2. On the field trip, Maya scans the QR code at the dairy barn with her phone. Chapter 3 loads instantly (cached), referencing the actual barn she's standing in. A choice requires her to find a real detail nearby ("Check the feed chart on the wall — which ration is listed for the heifers?") before picking a path.
3. She and her group debate a branching decision about whether the farm should switch to rotational grazing — the story shows consequences either way.
4. Back in class two days later, she finishes the finale on a Chromebook. The mystery resolves differently depending on her accumulated choices. A short reflection chapter asks her to connect story decisions to what she saw at the farm.

**Success looks like:** Maya finishes the whole arc voluntarily, talks about her branch choices with classmates, and can explain a real agricultural concept from the story.

---

### Persona 2 — Mr. Alvarez, 10th-grade agriscience teacher
Runs one or two farm trips a year; time-poor; skeptical of edtech that adds work; needs any material he uses in class to be vetted and standards-relevant.

**Key journey:**
1. Mr. Alvarez signs up (email + password), picks the partner farm and trip date, selects grade level (10), subject emphasis (ag careers + sustainability), and class size.
2. FarmQuest generates a customized branching story pack for his class overnight (OpenAI API, batched). He gets an email when it's ready.
3. He reviews the full story tree in the teacher dashboard — every branch, every chapter — flags one paragraph as too advanced, and clicks "Regenerate section." He approves the pack.
4. He prints the one-page trip sheet (station map, QR checklist, timing guide) and runs the pre-visit chapter in class.
5. On the trip, his dashboard (on his phone) shows which groups have checked in at which stations, so he can keep the class moving.
6. After the trip, he runs the finale + reflection lesson and exports a summary of class choices and reflection responses as a CSV.

**Success looks like:** Total prep time under 45 minutes; he says he'd run it again next semester.

---

### Persona 3 — Denise, farm owner–operator (Hilltop Farm)
Hosts 6–10 school groups per season; wants visits to go smoothly and schools to come back; no time to learn complicated software.

**Key journey:**
1. Denise does a one-time 30-minute onboarding call. She lists her farm's stations (barn, creamery, pasture, market stand) and shares a few facts and stories about each — these become raw material the AI weaves into every story pack for her farm.
2. FarmQuest sends her a PDF of weatherproof QR station signs to print and post. The QR codes are permanent — one per station, reused across all visits.
3. On trip days, she does nothing extra: the QR signs are already up, and the story guides student groups from station to station in a sensible route.
4. At season's end she receives a simple report: number of students hosted, engagement highlights, and quotes from student reflections mentioning her farm.

**Success looks like:** Setup once, zero per-visit effort, and schools rebooking for next season.

---

### Persona 4 — Priya, parent of an 8th grader
Signs the field-trip permission slip; wants to know what her kid is doing on their phone at school; sensitive to AI content aimed at minors.

**Key journey:**
1. The permission slip links to a one-page FarmQuest parent explainer: what the game is, that stories are AI-assisted but **teacher-reviewed before students see them**, and that no student personal data is collected.
2. After the trip, her son shows her his story path on his phone — she can read the whole branch he took.
3. She's reassured: content is wholesome, educational, and nothing was collected about her child.

**Success looks like:** No parent opt-outs due to AI or privacy concerns during the pilot.

---

## 5. Business Success Metrics (Pilot)

The pilot is free; success is measured in validation, not revenue.

| Metric | Target |
|---|---|
| Pilot partnerships live | 2–5 schools, 1–3 farms within the school year |
| Trips completed with FarmQuest | ≥ 6 class trips across the pilot |
| Story arc completion rate | ≥ 70% of students complete all three phases (pre, on-site, post) |
| Teacher NPS / would-run-again | ≥ 80% of pilot teachers say they'd run it again |
| Teacher prep time | ≤ 45 minutes median from signup to approved pack |
| Farm retention | ≥ 2 of 3 farms agree to continue next season |
| Parent opt-outs (AI/privacy concerns) | 0 |
| Learning signal | ≥ 60% of reflection responses correctly reference a concept from the trip (rubric-scored sample) |
| Willingness-to-pay signal | ≥ 50% of pilot teachers/farms answer "yes" or "maybe" to a paid version in exit interviews |

---

## 6. Technical Success Metrics

| Metric | Target |
|---|---|
| Monthly run cost (API + hosting + domain amortized) | **< $50/month** |
| Story pack generation cost | < $2 per class pack (OpenAI API, batched) |
| On-site chapter load after QR scan | < 2 s when cached offline; < 5 s on 3G |
| Offline resilience | 100% of on-site chapters readable with zero connectivity after pre-visit caching |
| QR scan → correct chapter success rate | ≥ 98% (correct station, correct group state) |
| Uptime during scheduled trips | 99.5% (trips are scheduled — maintenance windows avoid them) |
| Content safety | 0 unreviewed AI text shown to students (hard invariant, not a percentage) |
| Teacher regeneration turnaround | Section regeneration < 60 s; full pack < 15 min |
| Device coverage | Works on iOS Safari and Android Chrome from the last 4 years, plus ChromeOS |

---

## 7. Scope of MVP

### In scope

**Story engine**
- Branching story data model: chapters, choices, station-locks (a chapter unlocks only at its QR station), state carried across phases and devices via a group code.
- Three-phase structure: pre-visit (2–3 chapters), on-site (4–6 station chapters), post-visit (finale + reflection chapter).
- Reading-level targeting per grade band (6–8 vs 9–12) at generation time.

**Story pack generation (teacher-triggered only)**
- OpenAI API generates full branching packs from: farm profile (stations + facts), grade band, subject emphasis (ag science / food systems / careers / literacy), and class parameters.
- OpenAI Batch API for overnight generation (50% cost reduction); a cheaper model tier is acceptable since all output is human-reviewed.
- Teacher review UI: read every branch, flag/regenerate a section, approve pack. **Packs are unplayable by students until approved.**

**Student experience (responsive web app)**
- Join via class link + group code — no student accounts, no student PII.
- Chromebook-friendly classroom view; phone-friendly farm view.
- QR scan (native camera → URL) opens the correct chapter for that station and group.
- Pre-visit step caches the full on-site pack on students' phones (PWA/service worker) so the farm works offline; choices sync back when connectivity returns.
- Choice tracking so the finale reflects the group's accumulated decisions.

**Teacher tools**
- Signup, trip setup wizard, pack review/approval, printable trip sheet + QR station signs (PDF), simple live check-in view on trip day, CSV export of choices and reflection responses.

**Farm tools**
- Admin-assisted farm profile (stations, facts, photos optional) — during the pilot, the FarmQuest team enters this from the onboarding call; no farm-facing login required.
- Permanent per-station QR codes, generated once per farm.

**Ops**
- Parent-facing one-page explainer (static page).
- Basic analytics: completion rates, station check-ins, generation costs.

### Out of scope (MVP)
- Student accounts, logins, or any student PII; grading/LMS integration.
- Live AI generation for students; student-typed free-text sent to the AI.
- AI-generated imagery (stock/illustrated assets only in MVP — image APIs would blow the budget).
- Native apps; push notifications; GPS/geofencing (QR codes are the location mechanism).
- Farm self-service portal; multi-language support; K–5 reading levels.
- Payments, subscriptions, marketplace features.

---

## 8. Technical Considerations

### Architecture (chosen for the < $50/month constraint)
- **Frontend:** Single responsive web app (e.g., React/Next.js or SvelteKit) built as a **PWA** with a service worker for offline on-site play. One codebase serves Chromebooks and phones.
- **Backend:** Small server or serverless functions handling auth (teachers only), pack generation jobs, choice sync, and CSV export.
- **Database:** One managed Postgres or SQLite-on-a-VM; pilot data volume is tiny (thousands of rows).
- **Hosting:** Free/hobby tiers (e.g., Vercel/Netlify/Fly.io/Render) fit the pilot's traffic easily. Target: $0–20/month hosting, $5–15/month API, domain ~$1/month amortized.

### OpenAI API usage
- Generation is **teacher-triggered and batched** — students never call the API. This caps cost, eliminates real-time moderation risk, and removes API latency from the student experience.
- Use the Batch API for full-pack generation; synchronous calls only for single-section regeneration in the teacher review flow.
- Prompt scaffolding enforces: reading level, story tone (adventurous, wholesome, never frightening or violent; appropriate for K-12, parents, educators), curriculum emphasis, farm facts to weave in, and a strict JSON branching schema validated before save.
- Run OpenAI's moderation endpoint (free) on all generated text as a pre-filter **before** teacher review — defense in depth, not a substitute for review.
- Hard monthly spend cap configured on the OpenAI account; alert at 50%.

### Offline & connectivity (the hardest technical problem)
- The pre-visit classroom session doubles as the **caching step**: completing Chapter 2 on their phone forces the full on-site pack + assets into the service worker cache. The teacher trip sheet includes a "cache check" step the day before the trip.
- QR codes encode station URLs; the service worker resolves them **fully offline** to the correct cached chapter using local group state.
- Choices queue in IndexedDB and sync opportunistically; the story never blocks on network.
- Fallback: the printable trip sheet includes short numeric station codes students can type if a QR sign is damaged or a camera fails.

### Safety, privacy & compliance
- **No student PII**: students join with a class link + group code; no names, emails, or accounts. This keeps the pilot largely outside COPPA/FERPA data-handling obligations — the strongest low-budget compliance posture.
- **Human-in-the-loop invariant:** no AI text reaches a student without teacher approval. Enforced in the data model (packs have a `draft → approved` state; student routes only serve `approved`).
- Teacher accounts: email + password with standard hashing; no OAuth complexity needed for pilot scale.
- Content stored per class pack; deleting a class deletes its choices/reflections.
- Reflection free-text is student-written but never sent to the AI; it goes only to the teacher's CSV export. Teachers instruct students not to include personal information.

### Risks & mitigations
| Risk | Mitigation |
|---|---|
| Farm Wi-Fi/cell dead zones | Offline-first PWA; caching enforced pre-trip; typed station codes as fallback |
| Story quality varies across branches | Strict JSON schema + generation rubric; teacher review of every branch; per-section regeneration |
| Students on personal phones get distracted | Chapters are short (2–3 min); station-locked pacing; teacher check-in view keeps groups moving |
| Some students have no phone | Group-based play (2–4 students/group) means one phone per group suffices |
| QR signs weathered/vandalized | Weatherproof sign PDFs; permanent codes cheap to reprint; numeric fallback codes |
| OpenAI cost creep | Batch API, capped account, generation only on teacher action, cheaper model tier |

---

## 9. UI Style Preferences

**Direction: modern game-like** — contemporary adventure-game energy that respects a 12–18-year-old audience while staying warm enough for parents and educators.

- **Tone:** Duolingo-level polish and playfulness, but **not childish** — no cartoon animals as mascots, no bubbly kid fonts. Think "indie narrative game," not "kids' app."
- **Typography:** Bold, confident display type for chapter titles; highly readable body text (16px+ on mobile) since reading *is* the gameplay.
- **Color:** A modern palette with earthy anchors (deep greens, wheat gold, barn red as accent) so it feels farm-connected without rustic clichés; strong contrast for outdoor sunlight readability — the on-site view must be usable in full daylight (large tap targets, high contrast, no thin gray text).
- **Art:** Illustrated scene headers per chapter (commissioned or quality stock illustration in a consistent style — no AI image generation in MVP). Sparse and reusable to control cost.
- **Game feel:** Progress trail across the three phases, chapter-unlock moments when a QR scan lands, choice buttons that feel consequential (brief "your path diverges" beat), and a story-map recap at the finale showing the branch the group took.
- **Motion:** Subtle and purposeful (unlock, page-turn); nothing heavy — animations must not hurt performance on older phones or offline.
- **Teacher dashboard:** Drops the game styling for a clean, information-dense utility look; teachers are reviewing and running logistics, not playing.
- **Accessibility:** WCAG AA contrast, dyslexia-friendly line spacing, readable at arm's length outdoors, works one-handed on a phone.

---

## 10. Corner Cases

**Connectivity & devices**
1. Student's phone dies mid-visit → group play means another group member's phone continues; group state lives server-side once synced, and any group phone can rejoin with the group code.
2. Student skips the pre-visit caching step (absent that day) → join flow detects an uncached device on trip morning and offers a "quick sync" while still on school Wi-Fi/bus hotspot; otherwise they buddy with a cached group.
3. QR sign missing or unreadable → typed numeric station code fallback printed on the teacher trip sheet.
4. Student scans stations out of order → story engine either adapts (station chapters designed order-independent where possible) or politely redirects: "This part of the story unlocks at the creamery — head there next."
5. Student scans the same QR twice, or two groups scan simultaneously → idempotent: re-scan re-opens the group's current chapter state; group code disambiguates simultaneous scans.
6. Choices made offline by two phones in the same group conflict → last-write-wins per chapter with a visible "your group chose…" reconciliation line; groups are encouraged to designate one narrator phone.

**Content & safety**
7. Generated pack contains a factual error about the actual farm ("the cows" at a crop-only farm) → farm profile constrains generation; teacher review is the backstop; per-section regeneration fixes it in under a minute.
8. Moderation flag on generated text → section auto-quarantined and regenerated before the pack ever reaches teacher review.
9. Teacher forgets to approve the pack before the trip → student links show a friendly hold screen; teacher gets reminder emails at T-3 days and T-1 day; one-tap approve works from the teacher's phone.
10. A story branch touches sensitive ground (animal slaughter, pesticide harm) → generation rubric handles food-system realities honestly but age-appropriately and non-graphically; teachers can regenerate any section they judge wrong for their class.

**People & logistics**
11. Trip canceled or rescheduled (weather) → packs have no hard expiry; teacher updates the trip date and everything carries over.
12. Class splits into more groups than planned on the day → teacher can mint extra group codes from the phone dashboard on-site.
13. A student with low reading skills or an IEP struggles with text → group play provides peer reading support; browser text-to-speech and font-size controls; grade-band selection sets baseline level.
14. Mixed-grade group (e.g., 6th and 9th graders on a joint trip) → teacher picks the lower band; stories are written to be engaging one band up.
15. Farm changes layout mid-season (station removed) → admin edits farm profile; affected chapters flagged in existing approved packs for teacher regeneration; QR sign retired.
16. Student attempts to share the class link publicly → links are unlisted but not secret by design (no PII behind them); group codes expire after the trip window; abuse surface is limited to reading an approved story.
17. Reflection response contains a safeguarding concern (student discloses something worrying) → responses go only to the teacher, who follows existing school safeguarding procedure; the product surfaces reflections to teachers promptly rather than burying them.
18. Two classes visit the same farm on the same day → group codes are class-scoped; identical QR codes resolve per-group, so simultaneous classes don't collide.

---

## 11. Open Questions (post-pilot)

- Monetization: schools, farms, or both? Exit interviews in the pilot gather willingness-to-pay signals.
- Should high-performing story packs become a reusable library (reducing generation cost to near zero)?
- Farm self-service onboarding vs. staying concierge.
- Expansion beyond farms: museums, nature centers, historical sites use the same station-story mechanic.
