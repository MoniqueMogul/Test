# FarmQuest — Pitch Kit

Three outputs generated from one set of source artifacts: [PRD.md](../PRD.md),
[ARCHITECTURE.md](../ARCHITECTURE.md), and the Night Trail landing page.

---

## 1 · Two-Minute Verbal Pitch Script

*(~290 words · ~2:00 at a natural speaking pace · beat markers in brackets)*

**[0:00 — the hook]**
Think back to your last school field trip to a farm. Thirty kids shuffling between a barn and a coop, half-listening, retaining almost nothing. Teachers get no curriculum connection, farms get no tools, and by Monday it's like the trip never happened. Field trips are the most expensive hour in education — and the most wasted.

**[0:20 — the idea]**
FarmQuest fixes that with one move: the story starts in class, and it *unlocks* at the farm. It's a choose-your-own-adventure game for grades 6 through 12. Before the trip, students open Chapter 1 on their Chromebooks — a mystery is unfolding at the farm they're about to visit. At the farm, they scan QR codes posted at real stations — the dairy barn, the seed shed, the market stand — and each scan opens the next chapter, with choices that branch the story. Some clues only exist in the physical world: a feed chart on the wall, a tag on a tractor. Back in class, the finale resolves differently for every group, based on the choices they made.

**[0:55 — the trust story]**
Now, AI stories for minors — that should make you nervous. Here's why it doesn't here. Every story pack is AI-drafted, machine-moderated, and then read and approved by the teacher — every branch — before a single student can see it. That's not a policy; it's enforced in the data model. No student accounts, no student data, and it works fully offline, because farms don't have Wi-Fi where the cows are.

**[1:25 — the economics]**
The whole thing runs on pre-generated story packs — under two dollars per class, under fifty dollars a month for the entire pilot. Thirty students cost the same as one. Teachers are trip-ready in under forty-five minutes; farms set up once and never touch it again.

**[1:45 — the close]**
We're recruiting a pilot cohort now: a handful of schools, a few local farms, completely free. Curriculum in costume, adventure in the mud. Bring your class — we'll bring the quest.

---

## 2 · Summary for a PM Audience

**One-liner.** FarmQuest is a location-anchored, branching-narrative learning game for grades
6–12: the story begins in class, unlocks chapter-by-chapter via QR codes at a real local farm,
and resolves back in class based on each group's accumulated choices.

**The wedge.** Educational games are screen-only; field-trip materials are paper-only. Nobody
turns the physical trip itself into structured, curriculum-connected gameplay. FarmQuest's core
mechanic — station-locked chapters that reference what students are physically standing in front
of — is the differentiator, and it generalizes later to museums, nature centers, and historic
sites.

**Product shape (MVP/pilot).**
- **Three-phase arc:** pre-visit setup (Chromebooks) → on-site chapters (student phones, groups
  of 2–4, one phone per group suffices) → finale + reflection (back in class).
- **Content pipeline:** AI-generated branching "story packs" per farm/class (OpenAI, <$2/pack),
  auto-moderated, then **teacher-reviewed and approved before students can play** — a hard
  invariant enforced in the data model, not by policy.
- **Zero student PII:** join by class code + nickname; grade bands instead of ages. This is the
  strongest low-budget COPPA/FERPA posture available.
- **Offline-first:** the pre-visit lesson doubles as the caching step (PWA/service worker), so
  the farm experience needs zero connectivity; choices sync back later. TTS narration is
  pre-synthesized per chapter and cached — accessibility included, marginal cost ~zero.

**Why the economics work.** All expensive operations scale with *classes* (generation) or
*chapters* (TTS), never with students. Pilot run-rate target: **<$50/month total**. The pilot is
free; monetization (schools vs. farms vs. both) is deliberately deferred with
willingness-to-pay signals collected in exit interviews.

**Success metrics that matter.** ≥70% three-phase story completion; ≥80% of teachers
would-run-again; ≤45 min median teacher prep; 0 parent opt-outs over AI/privacy; ≥60% of
reflections correctly referencing a trip concept. Instrumentation (generation latency,
per-chapter drop-off funnel, completion rate) ships in the MVP.

**Biggest risks.** Farm connectivity (mitigated: offline-first + printed fallback codes),
branch-quality variance (mitigated: schema-constrained generation + per-section regeneration),
and teen credibility (mitigated: "indie narrative game" design language, explicitly not a kids'
app).

**Status.** PRD, architecture, design exploration, and a working single-file MVP are done;
pilot cohort (2–5 schools, 1–3 farms) is being recruited for the 2026–27 school year.

---

## 3 · Discord Recruiting Post

> 🚜 **Teachers & farm folks: want to turn a field trip into a playable mystery?**
>
> We're building **FarmQuest** — a choose-your-own-adventure game for grades 6–12 where the
> story starts in class and *unlocks* at a real local farm 🕵️
>
> How it works:
> 📖 **In class** — students open Chapter 1: something's off at Hilltop Farm…
> 📱 **At the farm** — scan QR signs at the barn, the field, the market stand; every scan
> unlocks the next chapter, and the clues are hiding in the real world
> 🏁 **Back in class** — every group gets a different ending based on their choices
>
> The parts grown-ups care about ✅
> • Every story is **teacher-reviewed before students see it** — no exceptions, ever
> • **Zero student accounts, zero student data** — join with a group code
> • Works **fully offline** (because cows don't do Wi-Fi 🐄)
> • Groups of 2–4 share one phone — nobody's left out
> • Teacher prep: under 45 minutes, total
>
> We're recruiting the **2026–27 pilot cohort**: 2–5 schools + 1–3 farms, **completely free**.
> You bring a class (or a farm) — we bring the quest, the QR signs, and the story.
>
> 🎓 Teacher? 🚜 Farm owner? 👋 Know one? Drop a 🌾 below or DM us to grab a pilot spot.
