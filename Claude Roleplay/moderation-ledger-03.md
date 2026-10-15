# Coreworld IV: Moderation Chat Ledger 03

The handoff for the next moderation chat (2026-10-15). It replaces ledger 02 as the current state. Ledgers 01 and 02 are history: read them only when you need the reasoning behind an old decision.

**Read first, in order:**
1. `coreworld-moderator-prompt.md`: the method, design principles, and how the user works.
2. This ledger.
3. `coreworld moderator/Monster Design Work (Reference Only)/monster-design-work.md`, before any creature or threat design.

---

## 1. Files

All paths are relative to the `Claude Roleplay` folder.

| File | What it is |
|---|---|
| `coreworld (playthrough2)/coreworld-prompt-v6.md` | **The live narrator prompt.** About 71 KB, about 18k tokens, CRLF. All rule changes go here. |
| `coreworld (playthrough2)/coreworld-prompt-v5.md` | Backup from before the v6 restructure. |
| `coreworld (playthrough2)/coreworld-prompt-v4.md` | Backup from before the hub rewrite. Don't edit v3, v4 or v5. |
| `coreworld moderator/Monster Design Work (Reference Only)/monster-design-work.md` | Worked examples (the Mimic, the Cyno, the Mendicants, the RS-9 drop) and the principles behind them. Never copy its creatures into the narrator prompt. |
| `moderation-ledger-01.md`, `-02.md` | History: the threat walkthrough (T1–T14), combat notes, setup screen history, and full reasoning for decisions up to the Hollins review. |
| `coreworld (playthrough4)/` | Playthrough 4 (Enn): narrator notes, which are SPOILERS. Don't read them unless asked. |
| `v4-diff-2026-10-13.md` | A one-off diff the user requested. Not maintained. |

**Editing v6:**
- **Encoding:** v6 is UTF-8 with CRLF line endings. Edit with Python in binary mode; anchor each change on a unique string and assert it appears exactly once.
- **Re-read first:** the user also edits by hand, so check the target lines before every edit.
- **Console output:** the console shows "…" and "–" as �. That's the console, not the file.

**Git:** nothing since the hub work is committed. The last commit is `f570927` on branch `coreworld-difficulty-review`, which isn't merged to main. Commit only when the user asks.

---

## 2. How the user works (on top of moderator prompt §2)

- **Reviews from other Claudes.** They paste narrator self-reviews and reviews by other Claudes. Judge each point: accept, reject with a reason, or adjust. They decide.
- **Their wording.** They often reply with a rewritten line. Apply it word for word, fixing only grammar.
- **Generalize examples.** They ask to generalize any example that could become a default ("otherwise the narrator will just use those").
- **Point to sections by name** instead of restating rules ("see DROP DESIGN"). They like this.
- **Concrete numbers for real schedules.** Things that really are schedules or systems in-world (the rotation clock, visit rhythm) get fixed numbers, not "the narrator decides". Mechanical is fine.
- **Self-assessment.** They ask for "any objections" or a "final assessment". Give honest remarks, including flaws in your own proposals.
- **No spoilers.** They're mid-run, so don't speculate about the current run's mysteries.
- **Token cost.** They're token-conscious: prefer cheap methods, and report the cost of additions.

---

## 3. What v6 does now (the current design, in brief)

**Difficulty and rating** (DIFFICULTY, DROP DESIGN)
- **Built for 4:** drops are built for a crew of 4 whoever is sent. Threats are never sized to the crew; quota is set per head.
- **Rate by cost:** rate a drop by what it costs a crew of 4 playing well, using the CONSEQUENCES meaning of cost. At build time, take the cheapest answer to every threat at once, and the drop must still cost what its band says.
- **Hazards:** they don't carry the band, unless the hazard is the main setpiece or acts like an enemy (spreads, closes in, worsens on its own).
- **Perceived danger:** it comes only from what's on the page. Hidden threats don't count until sensed.
- **The 0–12 scale:** 9+ is steeply more unfair, but never unreadable. Past 12 means character death, and only when the story has earned it.

**Drop design**
- **Every drop pushes on us.** Something reaches the crew whatever they do: a seeker, a reactive threat whose needs grow, a setpiece that spreads or closes in, or a rival. A reactive threat is never the only pressure.
- **The safest path is never free.** That includes ignoring the threat, hiding, waiting it out, and "moving somewhere it isn't". Its cost lands on this drop or soon after, visibly.
- **The twist:** every drop has a mid-drop twist (called "the turn" before 2026-10-15).
- **The build checklist** (end of DROP DESIGN): built for 4, the turn, the cost of the safest path, the cheapest-answer check, how each enemy fights, the observation before the first fight, each beast's style, and any regrade planned now. Re-check before the turn lands.
- **Any drop may be the last one played** (PACING AND SECRECY): each is complete at full weight, with a climax at its own scale. Nothing about the character makes a drop easier. The old "early drops are simpler" line was removed.

**Combat**
- Every enemy fights at the full strength of its nature, using only what it knows. A thinking one never intentionally takes an easy death. A lower drop has weaker or fewer enemies, never dumber ones. Mistakes come only from nature or knowledge, never convenience.
- Noise responders come to where the noise was and *may* search outward.

**Beasts**
- **Styles** (BEASTS "On a drop"): hunters, reactors, holders, followers, growers. A species can have several, and an individual can lean differently by age, hunger or growth. Styles change the way beasts change.
- **Mixing:** if a drop has several beasts, they get different styles, and a beast is never added just to have a mix.
- **Reactors and holders never carry a drop alone.**

**Pay** (SUNSPOT)
- Regrades are rare and planned at build time, never added on the fly.
- A raised drop is built and cost-checked at the higher rating; the posted pay reads the lower one.
- Other crews' losses never stand in for the player's crew's costs.

**The hub** (=== THE HUB ===)
- **The mothership is small:** the necessities (including the med bay, the counter and board, and the pod and shuttle bays) plus one wildcard room per playthrough. A lost second mothership is implied, as a thread.
- **The request terminal:**
  - 2–3 realistic options, often less than asked, each with a price, lead time and a drawback from its own nature.
  - Sunspot's make is rough: nothing that flies or thinks for itself.
  - A 3-Cap fee, credited if you buy. Prices are set against drop pay.
  - Admin can change, gate, or expunge options.
  - Orders are sourced from the town's workshops and elsewhere, and stay Sunspot property.
- **The town:**
  - On an ACC-scoured world. It isn't Sunspot's, and it has its own dangers.
  - Planned at the start: 3–4 shops, 1–2 black markets, 2 production buildings, 2–4 wildcards.
  - Shops feel like building a kit, never an RPG: mostly variants of existing gear, with strength and drawback sharing one nature.
  - Shown in a few lines, never as a tour.
- **Visits:** 2 drops, then about 8 hours in town. Radio warnings come at 60, 30 and 10 minutes. Anyone not back is labeled a Dropout; Sunspot's defenses treat Dropouts as threats.
- **The rotation clock,** counted from pod recovery (R): pay slip and med bay at R+1h; the board posts at R+2h; 8 hours of lights down; briefing at R+20h; launch at R+22h. The med bay heals twice as fast, and bills for it.
- **Groups of interest:** the veterans, one black-market group, and wildcard groups.
- **Role kit** is sold only to that role. Anyone else using it is slower and cruder, unless they've dedicatedly learnt it.

**Structure:** a layout map at the top, DESIGN NOTES parts marked `---`, THE HUB split out of SUNSPOT, long bullets split into sub-bullets, and the setup sequence last.

---

## 4. Runs and evidence

| Run | Setup | Drops | Verdict |
|---|---|---|---|
| Trailblaze run 1 | Trailblaze + The Starless Sky | KW-12 Reservoir, TN-6 Threshing Field | Combat and the noise economy worked. Designed at 9, played at about 7. |
| Playthrough 4 (Enn, Rigger) | The End of Nothing + Burnplan | GT-9, CR-11 | Rated 8, played at about 7 and about 6. Cultists charged guns, and the costs fell on another crew. These drove the cost check, full-strength, built-for-4 and regrade fixes. |
| **Current run (Hade, Rigger)** | The Starless Sky + Burnplan, on v6 | CATENARY-7 "Hollins Yard" | **The narrator rated it 9/9/8/8 (perceived/designed/actual/psychological); the user rated it 4/7/6/4.** Every threat was reactive, so leaving made the crew safe. The turn was a lock on the pod, bought off through Lowe. Hazards carried the cost. This drove the "every drop pushes on us", hazard, perceived and beast-style fixes. |

**Current run, details:**
- Played in claude.ai cloud sessions, which this app can't read. The user has Campaign Ledger #2; it isn't saved locally.
- **Next:** Orison-2, a Cantor drop. Recovery about 2350, then the **first town visit** (board about 0150, shuttle about 0250, back about 1050), then drop 3 launches about 2150.
- **Advised:** start a new narrator chat with the current v6 plus Campaign Ledger #2 before Orison-2. The old chat ran v6 from before the Hollins review.
- **Hub evidence so far (aboard only):**
  - Working: the clock is followed, the wildcard room is "the Window", the terminal is known, groups are forming, and town threads are seeded.
  - Concerns: each downtime ran about 10 scenes, and the real-time length was never reported. Continuity slips continue (a pronoun slip, "a year"), though the ledger audit catches them.

**Watch list for the next review:**
1. Does something come for the crew? Leaving shouldn't be free.
2. Are the narrator's ratings close to the user's?
3. Is there earned calm, or a constant chase? (overcorrection)
4. Real-time downtime length. The target is about 1 hour on Normal.
5. The town: arrival in a few lines; kit-like shops; wildcards with a use; the curfew felt; at least one town thread pointing to a drop.
6. Terminal answers: realistic, often less than asked, correct prices.

---

## 5. Open items

1. **Fix 3: DONE (2026-10-15),** with the user's "may", at the end of the DROP DESIGN checklist (L111): "and if we beat the twist early, what may keep the pressure on: …". Originally proposed: add to the build checklist "what keeps the pressure on if we beat the twist early: something new, often following from how we beat it, never the old twist taken back." Hollins went flat after the trade.
2. **"Turn" vs "twist": DONE (2026-10-15).** All 8 uses in v6 are renamed (L86 ×3, L92, L111 ×2, L180, L266). L86 now opens "every drop has a twist". The moderator prompt is updated to match. Backup: `v6-before-twist.md` in that session's scratchpad (not kept).
3. **The Mimic and the Cyno: CLOSED (2026-10-15).** Reference only, never in play. No prompt line is needed, since no species is named in v6. The Cyno's habitat question is moot.
4. **A trim pass:** the user said "maybe". MYSTERIES (about 1k tokens) and ROLES (about 0.9k) are the likeliest cuts. Each cut needs the user's review.
5. **Old leftovers from ledger 01:**
   - **Closed (2026-10-15):** A5 (L109 kept as is: its examples are systems, which are meant to be learnable), "make unfair concrete" (covered by the 9+ unfairness line), and the playthrough 3 rollback (that run is over).
   - **Still open:** item 31, the Remembrance Packages example at L199 (my pick: keep it, since Sunspot's memorial scheme recurring is consistent lore); the handler bar (needs the user to say what made "dot" good).
6. **The threat walkthrough (threats 8–10):** my pick was to close it, except perhaps a death-mission stress test. The user never confirmed.
8. **LN-4 case study (2026-10-15).** The user had a fresh agent with the files design a Burnplan + Starless first drop, then had it run a concrete crew through it and explain its failures. Don't log its creature design.
   - **Finding:** v6 already had every rule the drop broke (every drop pushes, the cheapest-answer check, "understanding should rarely make it safe", reactors and holders never alone), and the agent had read them. It built in story order (from "the teller's seat"), costed each path only at its dramatic moment, and wrote a check section that confirmed its chosen rating instead of computing it. Both of its self-reviews also missed the ACC as the only noise responder, a dusk event after the window had closed, and a harder version that removed a burden (Dorrin).
   - **Applied to the moderator prompt:** §3b now runs one concrete crew in time order, and the new §3e, "A check is arithmetic".
   - **Applied to v6 (2026-10-15), after the user's review** (revised after the other agent's counter-review):
     1. L96: "take the cheapest answer to every threat at once and check" becomes "take the cheapest answer to every threat together, each at the moment it's cheapest for us, and check". "Cheapest", not "earliest" (the agent's point: waiting can be the cheap answer); "together" replaces "at once" so the two don't contradict.
     2. L111: "check silently before play:" becomes "check silently before play, walking the drop in time order from touchdown the way a crew of 4 playing well would play it, not in story order:" ("playing well" is L96's phrase, the agent's point).
     3. L170, BEASTS: after "limits that come from its nature." add "They're never absolute (see DROP DESIGN): a limit makes a place or a time safer, never safe." The current line conflicts with L85; the agent read "can't come up through concrete" as a limit. Its "the way DROP DESIGN means it" was rejected: DROP DESIGN never defines "tendencies".
9. **Site variety (2026-10-15), applied to v6 as a new DROP DESIGN line after "Vary drops across a playthrough" (L89).** Grain silos turned up in playthrough 4, playthrough 5 and the VR-8 hypothetical. Rural industrial ruins dominate generally: the Threshing Field, Hollins rail yard, the Reservoir. Small details repeat too ("nine days", cultists holed up and shelled). The line says to think past the first site, vary sites along categories, not repeat a kind of place within a playthrough "unless going to a previous site" (the user's addition), and avoid grain silos and crop fields.
   - **Ban list:** grow it only when the logs show a new repeat. The likely next defaults are rail yards, reservoirs and quarries.
   - **Watch:** repeated small specifics like "nine days". No rule; a rule about numbers would over-apply.
   - **Not changed:** the Starless Sky farmland image (L322, the user's line). Playthrough 5 got silos without The Starless Sky, so that line isn't the cause.
10. **VR-8 case study (2026-10-15).** A second fresh agent built a Burnplan + Starless first drop (the silos), worked from v6 with today's L97, L112 and L171 changes in force, and claimed "the check holds" at 8. Run with a concrete crew, it played at about 5. The agent had also read this ledger's LN-4 entry before building. Don't log its creature design.
   - **My review was partly wrong.** I named "the crossing to the pod" as the real cost, but the crew launches from the pod it waits in, so there's no crossing. I missed that its two actors cancel each other at the pod.
   - **Its self-analysis (accepted):** the rating was fixed first and never reopened, so the check could only pass or force a patch. It patched inside the check (the pod undermining). Today's "never safe" (L171) licensed danger with no mechanism. It walked the actors' schedule, not the crew's, and picked one convenient line. It merged the safest-path test with the cheapest-answer check. The actors met only as spectacle, never in the check. One seeker arrival satisfied "seeks us out". It counted a risk as a cost. Arithmetic on the easy parts made the verdict look counted. Craters plus the fan held 12 crystals against a quota of 8.
   - **Core finding:** explaining a failure doesn't prevent it. Change the shape of the check (measure, then compare) and close the exact wordings it slipped through.
   - **Logged to the moderator prompt:** §3a "Licences"; §3e's sub-points (measure then compare, a check isn't a design step, count losses not risks, walk from the crew's side, put the actors together); the new §3f; and three §5 failure modes (ratings about 2 high, guards met by their letter, recurring defaults).
   - **Applied (2026-10-15), from the overbuilding discussion:** L97's "check the drop still costs what its band says" is now "what its rating says, taking the lower rating when unsure". Bands are two points wide, so a drop counting as a 7 used to pass as an 8; this gives about a 1-point margin with no 9+ side effects. **Rejected:** overbuilding by +2 and assuming it plays easier (loopholes stay free at any rating, 9+ changes the drop in kind, and it would need easing in play). Revisit a small in-band margin only if drops still play about 2 easier after the attack method.
   - **Pending, approved one by one by the user** (these replace the five proposals above; old 1-3 became A and B after the agent's "attack as the player" workflow answer):
     - **A. L97: APPLIED (2026-10-15) in the user's own wording.** Changes from my draft: "the cheapest 'path' a smart and adaptive crew of 4", "where each threat is at its weakest" (was "can't touch us"), "interact or avoid each other", and the fix may take answers away "unless that answer trivializes significant parts of the drop".
     - **B. L112: APPLIED.** The checklist is back to "check silently before play:" and lists "the attack (DROP DESIGN)". The two "see the cheapest-answer check in DROP DESIGN" pointers (BEASTS L168, terminal L224) now say "see the attack in DROP DESIGN".
     - **C. L171: APPLIED.** "...never safe, and what still reaches us there comes from its nature."
     - **D. L93: PARKED (2026-10-15).** The user dropped it for now. Revisit only if play shows a seeker reaching the crew once and then going quiet. The attack in L97 should already count that as a cheap path. Proposed: "an actor that seeks us out" becomes "an actor that seeks us out and keeps coming until something we paid for stops it".
11. **Quota per head (2026-10-15).** Slips had started posting "3 per head (12 for a crew of 4)", from L55's "Quota is set per head". L55 now reads, from the user's "set based on head": "Quota is based on headcount, and the slip posts it as one total; the threats aren't based on headcount." **Applied, L204, in the user's wording:** "One easy spot can fill quota, but the drop must stay as dangerous as its rating, or more." Earlier drafts ("pays for it", "costs") were rejected as ambiguous for a tired narrator. Possible later trim: reword "cost" and "cheapest" across DROP DESIGN into plain words.
12. **K-7 "Kessler Hollow" case study (2026-10-15).** A fresh agent built a Burnplan + Starless first drop under v6 with the new attack line (L97), and its own embedded attack said 8. Asked to self-attack, it first patched the flaws and graded the patched drop as passing; the user rejected that (no chance to fix once a player starts). Graded as built in `drop_self_assessmentattack.md`: **FAIL, 6–7**, because killing the leader early stopped the haul that drove the twist, the early-win fallback needed her alive, and the planned raise paid more for an easier drop. Also: an actor in two places, no pre-fight observation for the cultists, and a dawn sign with no touchdown time. Don't log its creatures.
   - **Findings:** the attack line works when run as a separate pass, but the attack written together with the drop still walked the designer's path. The gap is about 1–2 points, the same as before but caught by the agent itself this time.
   - **Logged to the moderator prompt:** §3e "Remove each actor early", "Track positions over time", "Grade as built"; a §5 failure mode (the build-time attack walks the designer's path).
   - **Memory:** another session saved `feedback-coreworld-attack-as-built.md`; I added that fixing and re-attacking before play is still the narrator's procedure.
   - **Applied to v6 (2026-10-15), one by one:** E, L97: the attack adds "and what happens if we take out any one actor early". F, L86: "It grows from cause and effect, usually a threat's own needs, typically already under way when we land, and it never depends on a crewmate disobeying or slipping up." (The examples were dropped, and so was a parenthetical about twists 'surviving' interception, as misreadable and then too explicit. "Even if the crew does exactly as told" was replaced because "told" by whom was unclear; it came from T3.) G, L112 checklist: "where each actor is over time, and the clock time of every timed sign". Also added to the moderator prompt: list background tuning and a rare round 2 as in-play options in self-assessments, but never count them toward the grade.
7. **The duplicate radio-warning mention** in Visits and the clock: left for now (the user, 2026-10-15).

---

## 6. Rejected; don't propose again

- A Signaller rework.
- A separate Shipless mode.
- Summary-first downtime (PASS THE TIME covers it).
- Rating by "the crew actually sent", which would undo built-for-4.
- "Caps don't count" as cost.
- "A forced spend still counts."
- A seeker "on a schedule we can read". It would make it a puzzle again.
- "Never throws itself away for nothing" and "live unless dying wins". The narrator can always say a death bought something.
- "Leeway is luck at the margins" (the user skipped it).
- A fixed-quota squeeze written as a WORLD SHIFTS line (it can still happen in play).
- "Defect" and "marked" for those left behind (the user chose "Dropout").
- Named examples in hazard and beast lines. Always generalize.
