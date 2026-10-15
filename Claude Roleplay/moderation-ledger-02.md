# Coreworld IV: Moderation Chat Ledger 02

This is the handoff for the next moderation (prompt-design) chat. It replaces ledger 01 as the current state. Keep `moderation-ledger-01.md` for history and detail: it holds the trim history, the full threat walkthrough notes (T1–T14, C1–C8, F1–F2), and older decisions.

**Read `coreworld-moderator-prompt.md` first.** It holds the working method and the design principles. This ledger holds the current state, the decisions made, and what's still open.

---

## 1. Files

All paths are relative to the `Claude Roleplay` folder.

| File | What it is |
|---|---|
| `coreworld (playthrough2)/coreworld-prompt-v4.md` | **The live narrator prompt** (~56.6 KB, CRLF). All rule changes go here. |
| `coreworld (playthrough2)/coreworld-prompt-v3.md` | The old backup. Don't edit it. |
| `coreworld-moderator-prompt.md` | Instructions for moderation chats: how the user works, the self-critique method, design principles, and known narrator failure modes. |
| `moderation-ledger-01.md` | History: the trim, the threat walkthrough (threats 1–7), the combat notes, and the format intermission. |
| `coreworld (playthrough3)/session-log-01.md`, `session-log-02.md` | Playthrough 3 feedback logs (Enn, Shooter, The Starless Sky). |
| `playthrough1-feedback.md` | Playthrough 1 feedback. |

**Warning:** v4 has been changed on disk by something other than this chat twice: an earlier modes version, and an earlier disclaimer. The user also edits v4 by hand (for example the Shooter line and the "Smaller story plotlines." taglines). **Always re-read the target lines before editing**, keep the user's own edits, and flag anything you find that you didn't write.

Memory: the project's Claude Code memory folder has the narrator feedback memories and a pointer to the moderator prompt.

---

## 2. How the user works now (on top of moderator prompt §2)

- They test in real runs and paste the **narrator's own self-review** of each drop. Review it critically: say which self-criticisms are right, which overcorrect, and what it missed. The user usually agrees with some and disagrees with others.
- They're **token-constrained** (they may play on the Claude Free plan). Prefer cheap methods. A simulated AI-vs-AI playtest was offered and declined because of token cost.
- They ask for weak-spot evaluation in the way they "trained" it: propose, list each weak spot with the wording that guards it, then give a pick.
- Questions they asked in OOC are fair game for the narrator to answer, including future plans.

---

## 3. Changes since ledger 01 (all applied to v4)

**Combat, weapons and drop design** (details are in ledger 01; the current wording is in v4):
- `=== COMBAT ===` section (after CORE LOOP). The observation bullet now says "Plan it when you build the drop, so it lands before the first fight." Round 2 is rare.
- Every miner gets a pistol and a knife. Ammo is limited (a reissue each rotation that carries over, plus buying, scavenging and trading). Only a lost gun is fined.
- Noise responders and situational sound: wind, storms and battles swallow sound; still air carries it. Never conjure weather to make a fight convenient.
- Drop design lines: the turn partway through each drop; several workable approaches; clever plays keep their gains; perceived danger; tuning guards (never takes back what was earned, never softens for a smaller crew, signs come before hits).
- PEOPLE: fragments and talk under pressure; vets act without solving.
- Control-taking effects follow only from the player's choices.

**Game start (BEFORE THE FIRST DROP):**
- **Order:** format step → TIME note and Free plan note → `-------` → play modes → "Regardless…" disclaimer → difficulty modifier → miner questions → intake.
- **Modes (the user's wording):**
  - **Trailblaze:** "Play for 1–3 hours (Assuming it's all in one go). Shit goes very bad on the first drop. Smaller story plotlines." First drop ~7.
  - **Burnplan:** "3+ hours (…), with no intention to continue. One and done session. Smaller story plotlines." First drop 5–6, steep, lands an ending.
  - **Ashplan:** "3+ hours (…), with the intention to continue." The default. First drop 3–4.
  - The narrator reads these as roughly 1–2 drops, one long session, or an open campaign.
  - **After the first drop,** drops vary around the mode's level. Dips for pacing are OK; dips that spare a hurt crew are not. (The user chose option B, an average, over a floor.)
- **TIME note:** "TIME refers to finishing a mission (drop) all in one go. It's through Claude, so you can basically stop and continue whenever, but the immersion loss & forgetting key details are at your own risk."
- **Free plan note:** "Recommend Trailblaze if you're using Claude Free plan. 1 Run might be just enough in Free Plan's Context Window & Usage, though writing quality may be questionable."
- **Difficulty modifier:** optional, from -5 to +5. It stacks with everything; a rating never goes below 1. "Less lethal, not less eventful."
- **Intake:** the harder answer is +1–2 actual danger.

**Danger scale:**
- **Past 10:** the difficulty breaks, and the player character will die on that drop. The narrator shows `[Out of Character: The difficulty has surpassed the max]` at the start of the drop. The player then continues as crewmates until all die or a stalemate. Only stacking or an earned story can cause it, never background tuning.
- "Unfair but survivable" now has that one exception.

**Formats:**
- The Starless Sky: +2 actual (it also feels a little more dangerous and heavier).
- The End of Nothing: +0 actual (the smaller crew is the difficulty).
- Both summaries show `+Danger` (the average of the three meters).
- New DIFFICULTY line: drops are built for a crew of 4 with normal preparation.

**Trailblaze run 1 review (KW-12, the Reservoir):**
- Hard Rule 6 now says counts must say exactly what they cover (rounds loaded vs spare, crystals intact vs cracked).
- Visible clocks run at the pace shown on the page, and any speed-up shows its cause first.
- ACC exception: "Rarely, a break from this is the start of something: it's a thread, not a habit, and it gets followed up." The user liked the Peacekeeper who touched the ring.
- **Dropped:** "the final stretch pays the rating", "nothing conjured" (the lever and winch belonged in a pod and cost something), "no mid-narration corrections", and "reviews look back only" (OOC questions are fair game).

**Drop 2 review (TN-6, the Threshing Field):**
- "Losses" now explicitly means deaths, crew gone, gear, or quota.
- The user judged the burn-ring refuge earned, not a flaw. The pack not adapting was OK because it had already landed damage. The rifle click was a fair gotcha because it was set up in the armory scene. The crew suggesting routes was fine.

**Roles:**
- **Signaller removed** (too passive). The handler-on-time rule moved to the handlers line.
- **Rigger reworked into traps:**
  - 5 beam tripwires per drop. Each one trips, then deactivates. Its **module** burns but stays seated until swapped by hand. Setup and swapping take time.
  - **Modules:** Warning (radio beep, then live for 3 more seconds), Alarm (loud, pistol level), Shock (damages flesh; a temporary EMP against machines, never a kill), Explosive (damage, loud, heat clock).
  - **No per-type cap.**
  - **Prices:** tripwire 1 Cap; modules 3 Caps for any 2, mixed types allowed, and buying one still costs 3.
  - **Kept:** field repair, and coaxing life out of a failing beacon or window clock.
  - **Cut:** base setup and demolitions. The noise order's loudest item is now "an Explosive module."
  - **Status list** at the end of each reply while any tripwire is set: `Tripwires (Last seen):` then `1. <place> | <module> | <status>`. Status is Ok, Triggered (seen or heard), or Triggered (?) (burnt, but it can't be told whether it worked). Modules left are shown only when an action needs them.
  - The user renamed "chips" to "modules" (too close to "Caps").
- **Pickable roles:** driller, medic, hauler. Rigger or shooter. Nothing else.
- **Rarity:** Shooter uncommon; Rigger rare (an NPC Rigger's tripwires are awkward to track).
- **The user edited the Shooter line:** "the rifle itself is prone to damage (repairs are expensively billed)." The awkward-guns clause is gone.

**Input conventions:**
- New: "If and only if the entire message consists of a ( ) thought that seems to be a typo for a < > action, ask OOC for clarification."

**Drop pay (SUNSPOT, after the quotas line):**
- The pay structure differs each playthrough (per crystal, a flat sum on quota plus a little per extra, or something else). It's picked at the start and stays consistent until the world shifts it.
- The board posts each drop's pay, urgent slips included. Pay is a fair read of danger, judged against the playthrough's usual pay.
- It undershoots only rarely, when something Sunspot didn't foresee changes the situation. When that happens the drop is regraded: the handler may announce a raise mid-drop, before the worst lands, never a cut, with no reason given.
- A raise is always backed by real danger, and it only pays if quota is still met. Pay never overshoots.
- **Rejected grade schemes:** S/A/C letters (gamer language), cryptic schemes, and multipliers. The user chose plain pay figures in whatever form the run uses.

**Danger scale extended to 0–12 (this chat, applied to v4 L83–95, L286):**
- Why: the Reservoir (planned ~8–9) and the Threshing Field (one step lower) felt a massive jump apart. Relabeling alone wouldn't fix it (3–12 is still 10 steps), so the new step went at the top.
- Bands: 0–2 reference only, never a real drop · 3–4, 5–6, 7–8 unchanged · new 9–10 "losses are near-certain; good play decides who and what" · 11–12 = the old 9–10 (getting out is the win; earned or death mission) · Past 12 = the old past 10.
- New line after the bands: unfairness climbs steeply with the rating; from 9 up the world gets "much, much more unfair" (worse odds, worse timing, subtler and shorter warnings, costlier ways out); unfair never means unreadable. "Costlier," not "fewer," to keep L80's several approaches. This partly closes "make unfair concrete."
- Modifier floor is now 3. Mode anchors are unchanged (Trailblaze 7, Burnplan 6, Ashplan 4). The Starless Sky stays +2.
- The optional "shows in the situation, not in every beat" guard was not added.
- Not yet answered: which of the two drops felt harder. If the lower-rated Threshing Field felt harder, part of the problem is the narrator not following the rating in play, not only the scale.

**Modes and modifier replaced by a preset screen (v4 BEFORE THE FIRST DROP). This supersedes the "Modes", "Free plan note" and "Difficulty modifier" bullets above.** I drafted a version with a Length question; **the user then rewrote it by hand**, and this is the current state:
- Screen: a Time Disclaimer, then three presets described in plain player terms: Trailblaze, Burnplan (default), Ashplan. "(If you want slightly more specific settings, ask)" opens a second screen.
- Specific settings: Starting Difficulty Easy/Medium/Hard (**5**/6/8; the user raised Easy from 4 to 5 by hand); Story Downtime "I have no time" / Normal / Slow. The Length question is gone. Escalation is a slow ramp by default, from cause and effect, never from how long the player plans to play.
- Presets: Trailblaze = Hard + I have no time; Burnplan = Medium + Normal; Ashplan = Easy + Slow. Preset answers are hidden unless asked.
- Normal downtime leans toward Slow in story but keeps ship time shorter (the user's call).
- The Free plan note and the difficulty modifier are removed. L103 ship downtime now follows the Story Downtime answer. The pacing line no longer says "In Ashplan Mode."
- Because difficulty is now picked as Easy/Medium/Hard, 11–12 can't be chosen directly, so L91 ("only when earned or a death mission") needed no change.

**`=== BEASTS ===` section added to v4 (L153–174, between THE WORLD and SUNSPOT; it replaces the two-line version).** Guides, not a checklist:
- **Designing a species:** what it bends (a sense, a tool, a habit, or a fear), not its shape; strength and weakness from one nature; a normal-acting beast is fine if its beginning or end isn't (the user's Reservoir point); wholly plain beasts suit combat-test drops and are kept uncommon (the Threshing Field as a one-off was fine); what it notices and what it does then; limits from its nature; a narrow habitat and a plentiful diet.
- **Individuals:** a danger range set by age, growth, hunger, and time left alone, readable before it matters. Beasts change by growing; they can change mid-drop from their own needs, but never to cancel a counter.
- **On a drop:** chosen like a level's threats; a background beast eventually touches the drop; its needs can drive the turn; something a crew could have always reaches it.
- **Factions:** cultists who know a species can make it part of their craft (material, tool, bait, a technique), and then it's a creation, not a beast. "Wants to experiment" was rejected as too simple. The ACC removes beasts for its own reasons, never as a rescue.
- **Also:** names per speaker; species recur within a playthrough; usually winnable; appearance revealed only as far as the character can see.
- Cost: about 550 tokens more per message (v4 is now ~60 KB).
- The user didn't experience the Reservoir as a puzzle, which suggests its rule read as the world, not a gimmick.

**Drop variety and length (v4 L81, L84, L106, L160):**
- L81: vary drops across a playthrough: threats to read, straight fights (cultists or plain beasts), or both; a drop's character can shift midway. The user's C1 (3 cultists in a building) counts as normal, and normal is fine as part of the variety. Walk-ins were given as one example only.
- L106 (pacing knob): drop length varies per drop as level design: usually 6+ hours when threats are meant to be learned, shorter for pressure or straight-fight drops.
- L84: the site doesn't stand still; actors pursue their needs, and the narrator keeps the drop moving and never skips ahead on its own. Calm is fine when earned. **The user rejected "something meaningful each hour" (arbitrary) and narrator summarising ("its job is to keep things moving, not skip")**; PASS THE TIME stays the player's tool.
- BEASTS: plain beasts are "part of a varied mix of drops," no longer "uncommon."
- Not changed: L103's ship downtime still says "summarize when nothing is happening" (the user's wording).

**11–12 and past the max (v4 L94–95):** stacking alone never takes a drop above 10. 11–12 happens only when earned or on a death mission; higher starting difficulty and stacking make both come more readily, but they stay rare. The max breaks only when the story has clearly earned it; the old "stack past the max" route was removed at the user's request. Side effect: the harder intake answer adds nothing to a first drop already at 10 (Trailblaze with The Starless Sky).

**Monster training (this chat):** the user shares creature designs as examples to train the moderator; **don't log the designs.** The principles are in memory (`feedback-coreworld-monster-training.md`). The scenario format, the difficulty options (walk-ins, bigger quota, mid-drop raise) and their guards are in the moderator prompt.

---

## 4. Open items

1. **Heat clock examples: DONE (2026-10-13).** "chanting on a radio" was cut from the hidden heat clock line (v4 L206). Nothing else changed.
2. **Signaller rework: CLOSED (2026-10-13).** The user decided the Signaller won't be reworked. Don't propose it again.
3. **The End of Nothing, solo, past the max: CLOSED (2026-10-13).** Left to each narrator's interpretation. No prompt line.
4. **Do the user's own species (Mimic, Cyno) appear in play,** or are they training examples only? This decides whether the v4 beasts line should say "invented fresh each playthrough." Also open: whether the Cyno gets a narrow habitat (the user's call).
5. **Threat walkthrough threats 8–10** were never done (paused after threat 7). Remaining types not covered: a ship-based threat, a hidden threat at max unknown-ness, a death mission.
6. **Still open from ledger 01:**
   - A5 (cutting the "learned rule" half of "The best moments…").
   - Item 31 (the Remembrance Packages example).
   - "Make unfair concrete."
   - The handler bar ("dot" from playthrough 1).
   - The playthrough 3 rollback decision.
7. **Building fights toward the extraction:** case by case, deliberately not in the prompt.
8. **Playthrough 4 difficulty review (drops GT-9, CR-11; End of Nothing, Burnplan).** The player is still in this run, so don't spoil it. The narrator rated both drops 8; they played at about 7 and about 6, and CR-11 played below the 5–6 band text (no wounds, well over quota). Core problem: the narrator rates the drop it designed, not the one that got played, and every danger had a cheap answer or cost the player's crew nothing.
   - **Applied (2026-10-13):** L80, the safest path's cost lands "on this drop or soon after, that we can see" (it was "later", a loophole). L196, a pay raise's danger "reaches us, not just the site". L198, another crew's losses "never stand in for what my crew's drop costs".
   - **Applied (2026-10-13), item 1, at the end of L88:** rate by what a drop costs a crew of 4 playing well; a cost is something taken from us, the way CONSEQUENCES means it, not what we chose to spend; at build time, take the cheapest answer to every threat at once and check the drop still costs what its band says, without just removing those answers; vary where the cost comes from. **Rejected from the narrator's review:** "the crew actually sent" (it would undo L47 and The End of Nothing's +0), "Caps don't count" (it conflicts with L70's debt), restating the other-crews rule (L198 already covers it), and "a forced spend still counts" (L70's "fewer options" covers it, and spelling it out reopens the inflation).
   - **Applied (2026-10-13), item 3, new COMBAT line L218 in the user's wording:** every enemy fights at the full strength of its nature; a thinking one "never intentionally puts itself in an easy death"; a lower drop "may have weaker or fewer enemies, but never dumber ones"; plan how each fights at build time, including how it uses the site and other actors where its nature gives it a reason. Additions from the narrator's review (applied): "using only what it knows, the way KNOWLEDGE BOUNDARIES limits NPCs"; "a made thing fights the way it was made to" (creations and ACC units); mistakes come only from nature or knowledge, "never convenient ones". **Rejected:** "never throws itself away for nothing" and "to live unless dying wins" (loopholes, since the narrator can always say a death bought something), and merging with L217 (it already sits directly below it).
   - **Applied (2026-10-13), item 6, L47:** "...whoever is sent: never pick or size a drop's threats to fit a smaller crew... Quota is set per head; the threats aren't." The narrator admitted building CR-11 for two. **Not added:** "rounded to whole crystals" (L195's simple-number rule covers it), and a fixed-quota squeeze as a WORLD SHIFTS line (a written example becomes a default; the narrator can still do it in play as a world event). Past quotas stand, with no retcon.
   - **Applied (2026-10-13), item 7, L159:** "its counter always costs something real (see the cheapest-answer check in DROP DESIGN)". Item 1's check gives "something" a bar to meet. Cost categories and rising repeat costs were dropped (one duplicates CONSEQUENCES, the other risks T14).
   - **All items from this review are done.**
   - **Follow-up (2026-10-13), regrades as noise, L196:** "most drops have no regrade"; a regrade is planned when the drop is built, "never added on the fly because a drop turned out harder than you meant"; the drop is built and cost-checked at the rating the raise implies, while the posted pay reads the lower one. This replaced my "from then on" wording, which implied escalating after the announcement (the narrator's catch). Accepted side effect: hidden tuning upward can leave a hard drop underpaid with no signal. The two raises already given stay canon.
10. **v6 restructure (2026-10-14).** `coreworld-prompt-v6.md` is now the live prompt, and v5 is the backup. The restructure was structural only, with no rule text reworded. It was checked line by line: the only lines lost were the 6 old sub-header lines, which were restyled.
   - **A layout map** after the opening line. It lists the sections in file order, notes that sections are referenced by name, and points to BEFORE THE FIRST DROP as the start.
   - **DESIGN NOTES sub-headers** are now marked `--- X ---`.
   - **=== THE HUB ===** is split out of SUNSPOT and placed right after it. It holds the mothership, terminal, town, visits, rotation clock, the town-and-drops loop, and groups. SUNSPOT went from about 20% of the prompt to about 12%.
   - **PACING AND SECRECY** moved from the end to after THE WORLD SHIFTS, so the setup sequence comes last.
   - **A build-time checklist** was added at the end of DROP DESIGN, made of section references only: built for 4; the turn, the cost of the safest path, and the cheapest-answer check; how each enemy fights and the observation before the first fight; any regrade planned now. **"Check them again before the turn lands" is my addition and still needs the user's approval.**
   - **Sub-bullet splitting:** the four longest bullets (the terminal, the town, the rotation clock, drop pay) are split into sub-bullets at sentence boundaries, with every word unchanged. A check confirmed each block rejoins to its exact v5 line.
   - **Applied after review:**
     - The user kept the checklist's "Check them again before the turn lands."
     - New OOC bullet: "When they apply, end a reply with, in order: the Prep Action state (SPECIAL ACTIONS), then the Tripwires list (ROLES MUST MATTER)."
     - The ECONOMY line's "possibly an illicit market" is now "an illicit market".
     - Small fixes from another Claude's review:
       - The handlers' "(EXAMPLES)" is now "(Examples, not requirements:)". It was the user's label, misread as a stray placeholder.
       - The map now says "Parts of DESIGN NOTES are marked with ---".
       - PEOPLE's "object loud and before" is now "object loudly and beforehand" (grammar only; their "before acting" was rejected because it changed the meaning).
     - SCOUT is confirmed NPC-only; no change, since the setup's pickable roles already exclude it.
   - About 69.5 KB and 404 lines. The prompt was about 17k tokens before this.
9. **Ship time and the hub (2026-10-14).** Ship sections take too long (the first ship visit is about 3 hours) and go stale on replays.
   - **Rejected:** a separate Shipless mode, and summary-first downtime (PASS THE TIME already covers it).
   - **Applied, end of L120:** when the player seems to be idling, an out-of-character reminder that PASS THE TIME exists, never while something's closing in, and at most once per 20 of the player's messages.
   - **Applied as v5 (2026-10-14): the Hub.** `coreworld-prompt-v5.md` is now the live prompt, and v4 is the backup. The old L191 is replaced by four bullets:
     - **A small mothership:** the necessities plus one wildcard room that varies each playthrough. A lost second mothership is implied, as a thread, never the whole story.
     - **The town:** on an ACC-scoured ruined world. It isn't Sunspot's: it depends on Sunspot's trade, takes Caps, resents miners, and knows Sunspot exists. It has its own dangers, never drop-level ones. It's planned at the start, one line per place: 3–4 shops, 1–2 black markets, 2 production buildings, and 2–4 wildcards. A shop is defined by "who runs it and what makes it its own". Places open and close between visits, and the town is shown in a few lines, never as a tour.
     - **Visits:** 2 drops, then 1 night in town. Radio warnings come as the return nears; anyone left behind is labeled a Dropout. If that's the player, what follows comes from cause and effect, never quiet forgiveness. The user rejected "Defect" and "marked".
     - **The loop:** the town and the drops feed each other, and world shifts show in the town. Downtime scenes on the ship or in town give humor and character room.
     - **Follow-ons:** L74, ledger item 14, The End of Nothing's "emptying ship and town", and L367.
   - **v5 follow-ups applied:**
     - **PASS THE TIME reminders merged.** I had added a reminder to L120 without noticing the existing one-time tip (around L237). I removed the L120 addition. The tip now covers the ship and the town, and after it "the tip itself never repeats", followed by a short OOC reminder at most once per 20 messages, never while something's closing in.
     - **Economy section:** the header is now "ECONOMY, THE SHIP, AND THE TOWN", and the line reads "the ship and the town offer".
     - **L105:** now "Downtime between drops (aboard and in town)".
     - **Story Downtime wording:** "ship time" is now "downtime", and "long ship stretches" is now "long downtime stretches" (the user approved changing their own wording).
   - **Applied:**
     - **Groups-of-interest bullet:** the veterans, one black-market group, and one or more wildcards that don't need to appear right away. Each wants something and offers something, they don't fold into the player's side or each other, and they vary each playthrough.
     - **Ledger item 11:** now adds groups.
     - **Shop line rewritten** (the old "defined by who runs it… not by what it sells" was backwards). Shops feel like building a kit, never an RPG. Items are mostly variants and upgrades of existing gear, each with its strength and drawback from the same nature. Combinations are never pointed out. Stock shifts with the war, and better stock opens "however makes sense in the world". Production buildings sell what they make, and every wildcard gives something to do, gain, or risk. The principles are now in the moderator prompt under "Hub and shops".
     - **Request terminal (the user's idea), a bullet after the mothership:** the player can request anything; the answer is 2–3 realistic options, often less than asked, each with a price, lead time and a drawback from its own nature. A 3-Cap fee is credited if the player buys (added to L187). Prices are set against usual drop pay (an upgrade is about one drop's worth, something new two or three); refills are at least double a shower, rising with demand and the world. It's gated by track record or standing. Everything made stays Sunspot property, and it never makes a perfect counter. Added in the user's wording: other miners, veterans most of all, "may have a chance of carrying" their own invented gear, and the player's gear only shows up on others "through a cause I can see" (saw it, traded, Sunspot sold the design). **After testing** (a Cy-Hive drone nest, "a big mech", a joke "domain expansion" request):
       - Sunspot's make is "rough and hands-on next to the ACC's: nothing that flies or thinks for itself" (drones were rejected before because they blur the ACC tech contrast).
       - Items already sold aboard are redirected to their shop at its price.
       - The gating line is replaced by the user's admin wording: every request goes through admin, which can change an option before purchase, demand authorization (standing, track record, or a signature; bigger requests need more), or cut an option as it's read or before, leaving [INFORMATION EXPUNGED]. Cuts are rare and always have a reason.
       - **Terminal sourcing** (my invented lore, approved): "Sunspot doesn't make it aboard: orders are sourced, much of it from the town's workshops, the rest from somewhere nobody's told." This gives the lead times a cause and ties the terminal to the town.
       - **Story Downtime line:** now "sets how much of each rotation gets played and how much world fills it" (it said "how much time", which contradicted the fixed clock).
       - **Ledger item 8:** adds pending orders (item, price paid, when due).
       - Not done: removing the duplicate radio-warning mention in Visits (optional; skipped).
       - L187 also has, in the user's wording, "Anyone can end up carrying role kit, but using it well takes the role: in other hands it's slower, cruder, and fails more, unless dedicatedly learnt." This closes the route through the town's shops.
       - L187 now says "Role kit is sold only to that role" (anyone could buy tripwires before, so anyone could become a Rigger for 15 Caps).
       Test case: the user's "Pyre Blade" became a friction-sink blade with a blast at arm's reach instead of a ray.
     - **Mothership list now:** bunks, mess hall, toilets, a med bay, a shooting range, commissary, the counter and board, admin, the pod and shuttle bays (the last two added so the clock's places exist).
     - **Rotation clock (replaced "about a day"):** counted from pod recovery. Pay and the med bay within 1 h, the board posts the next drop at about R+2h, about 8 h lights down, briefing at about R+20h, launch at about R+22h. On a visit, the shuttle leaves after the board posts and returns by morning, with radio warnings at 60/30/10 min. Urgent slips post at any time with their own deadlines. The user wants it mechanical and grounded ("it's literally a schedule"), not left to the narrator.
     - **Rotation length (the user's idea), a new bullet after Visits:** a rotation is about a day aboard, or a night in town and back by morning. The med bay heals wounds about twice as fast and bills for it ("nobody asks how", my invented line, kept). On a drop, a wound is as bad as it looks. The med bay was added to the mothership's necessities. Healing per rotation is unchanged (twice as fast over half the time).
     - **Dropouts (the user's idea):** "Sunspot's security and automated defenses treat Dropouts as threats wherever Sunspot holds ground, so they rarely band together."
   - **Earlier note (now superseded):** Replace the mothership with a hub that varies each playthrough (the user's ideas: different stores and people, black markets, vagrants on old routes). My pick is a town-sized ship (it keeps stealth, L179/L182) run as a company town, which keeps the capitalist feel. The user asked to settle how it works in the overarching story before its contents. Lore lines affected: L179, L182, L191, L228, L367.
   - **Unanswered:** did GT-9 feel right for a first drop? If both drops felt soft, Medium = 6 may be too low.

---

## 5. Playtest record

| Run | Setup | Drops | Notes |
|---|---|---|---|
| Trailblaze run 1 | Trailblaze + The Starless Sky (Reservoir designed at 9) | KW-12 "The Reservoir", TN-6 "The Threshing Field" | Combat worked: the player shot, and the hip shot taught them something. The noise economy worked. Turns had visible causes. Open threads in-world: the ring on the hatch, the Peacekeeper who touched it, Hollow Anselm, the deep hum, the old pod, Odile's chip, Teo's reassignment. |

**Usage note given to the user:** usage grows with chat length, since every message resends the whole chat and the prompt alone is ~14k tokens. Start new chats from a ledger every drop or two.

**Later (setup screen):** the game-start modes became a single setup screen: a TIME note, then 3 presets (Trailblaze 7/Fast/Compact, Burnplan default 6/Session/Middle, Ashplan 4/Open/Full), then 3 questions (Difficulty 3–12, **Arc** (renamed from Length because Length was ambiguous; it sets when the story comes to a head: Fast, Session or Open), and Story (Compact, Middle or Full)), then one closing disclaimer. Redundancies were cut: the per-tagline "(Assuming it's all in one go)", the "Smaller story plotlines." text (Story covers it), the "Base Game" and "Former Base Game" labels, and the repeated three-line disclaimer.

**Setup screen v2 (2026-10-11; v4 L103, L275–309, L325). This supersedes the "Later (setup screen)" note above:**
- **Arc question removed.** The story is fleshed out with loose ends whatever the session length. New line: escalation is a slow ramp by default, comes from cause and effect, never from how long the player plans to play. The user accepted that a short Trailblaze run may not reach a climax (runs take 2–3 hours anyway).
- **Questions:** 1. Starting Difficulty, A Easy / B Medium / C Hard (hidden mapping 4 / 6 / 8). 2. Story Downtime, A "I have no time / I don't like freedom" / B Normal / C Slow (these replace Compact / Middle / Full, same hidden meanings).
- **"Any number 3–12" dropped**, to keep the screen simple.
- **Presets:** Trailblaze = Hard + I have no time (7 → 8). Burnplan (default) = Medium + Normal. Ashplan = Easy + Slow. The preset lines show only the user's bullet taglines. The narrator gives a preset's answers only if asked. "(old default)" was cut. Burnplan's bullet now reads "Medium starting difficulty".
- **Old closing paragraph cut** ("keep playing past an ending…", the guardrails warning).
- **Follow-ons:** the L103 pacing knob is now "[set by the Story Downtime answer; summarize when nothing is happening]". L325 lost "In an open campaign,".
- **Max stack check:** Hard 8 + Starless +2 + intake +2 = 12, so setup alone never breaks the max.
- **Note:** v4 is CRLF, as the moderator prompt says. Git Bash grep reports no CRs on it, so check endings with Python instead.
- **Revision (same day):** the setup screen now shows only the time disclaimer, the presets under "Pick a preset", and "(Ask for more custom settings)" at the bottom. The SELECT THINGS block is shown only if the player asks, and its option titles are bold. Trailblaze's second bullet is now "Get me into the hard stuff quickly" (it was "Shit goes very bad on the first drop.").
- **Revision 2:** the user's exact layout was applied: bold "Time Disclaimer:" and bold preset names, with "Pick a preset" directly above Trailblaze. The bottom line is now "(If you want slightly more specific settings, ask)", and the trigger reads "If I ask for more specific settings". Skipped answers now fall back to the chosen preset's answers, or to Burnplan's if no preset was picked.
