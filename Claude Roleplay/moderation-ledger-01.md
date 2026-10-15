# Coreworld IV: Moderation Chat Ledger 01

> **Superseded by `moderation-ledger-02.md`** for the current state. Keep this file for history and the full walkthrough notes. Some "current" statements below are out of date: the Signaller is removed, the Rigger has been reworked into traps, and the format numbers have changed.

This is a handoff for continuing the prompt-design ("moderation") chat in a new session. It covers the prompt files, the decisions made, how the user likes to work, and what is still open.

---

## 1. Files

All paths are relative to the `Claude Roleplay` folder.

| File | What it is |
|---|---|
| `coreworld-prompt-v2.md` | The old prompt, used for playthrough 1. |
| `playthrough1-feedback.md` | The player's feedback after playthrough 1, sessions 1–5. |
| `coreworld (playthrough2)/coreworld-prompt-v3.md` | The **current live prompt**, used by playthrough 3. It is complete, with every rule added during this chat. This is the backup. |
| `coreworld (playthrough2)/coreworld-prompt-v4.md` | The **trim in progress**. It is a copy of v3 with cuts applied. It is about 49 KB; v3 is about 55 KB. |
| `coreworld (playthrough3)/session-log-01.md`, `session-log-02.md` | The narrator's feedback logs from playthrough 3 (player character Enn, Shooter, The Starless Sky format). |
| `coreworld (playthrough3)/campaign-ledger-02.md` | The playthrough 3 story ledger. |

Claude Code memory is in the project's Claude Code memory folder. It holds the narrator's own feedback memories: no-retcons, nightmares, bold-injuries, no-solving, and stakes-and-vets. **These are not a substitute for the prompt.** Everything important should be in the prompt file.

---

## 2. How the user wants to work (important)

- **Prompt edits:** keep the user's own wording and emphasis when they write a line, and fix only grammar and typos. They noticed when "retcon" emphasis and "they'd have to figure out how to deal with it" were weakened.
- **Don't over-emphasize narrow cases.** Generalize: for example, write "everyone acts on experience," not "vets"; write "the world doesn't pause," not "questions."
- **Trimming format:** **one big numbered list of specific cuts**, with a line reference and a one-line reason for each. The user replies with numbers. Don't do side-by-side comparisons, replacement drafts, or item-by-item diffs. The user rejected all of those as too slow. Skip anything that is only rewording.
- **Recommend; don't survey.** Give a pick when asked for suggestions.
- **Don't invent lore and slip it in.** Flag anything invented, for example "Sunspot is running out of miners" or "the pistol is louder than the rifle."
- **When the user pastes text, apply it word for word.** Straight quotes are fine.
- **Technical lesson:** when splicing the file with a script, anchor on unique strings. "DROP DESIGN" appears in the preferences line too, and once caused about 10 KB of the prompt to be duplicated (this was fixed).

---

## 3. Status of the v4 trim

**Done:**
- **Chunk 1:** Preferences, Input, Hard Rules, and a new merged `=== PEOPLE ===` section (NPCs THINK FOR THEMSELVES plus CREW AND NPCs). The CONSISTENCY lines were folded into Hard Rule 4, which keeps the user's original retcon wording word for word.
- **Roles:**
  - The core four got wording trims.
  - Rigger now says "can coax extra life out of a failing pod beacon or window clock," which removes the conflict with "costs nothing."
  - Shooter was tightened but keeps "Sunspot sometimes hands very awkward guns to miners or sells guns for purchase."
  - Crew of 4 keeps both the "room to develop" reasoning and "the crew has to figure out how to deal with it."
- **Consequences and Economy:** lists were turned into sentences, with the same meaning.
- **Cut:**
  - "The above are simple examples…"
  - The price examples in "The economy" (only "Sunspot pays in Caps" is left)
  - The World Shifts examples line
  - Noise levels below 1
- **Noise:** the whole ladder, the meter, the skill readout and the headphones were replaced with one line in CORE LOOP. It says louder and longer sounds feed the heat clock; sustained beats brief. The order, quietest to loudest, is: whisper, talk, hand tools and shouting, drill, pod braking burn, Shooter rifle, old backup pistol, pod launch, Rigger charges.

**Applied (session 2):** all duplicate cuts: B 6–14 (13 = cut "Progress one step at a time", kept "Start in an understandable manner") and new dups 22–27, 29–30, 32–39 (Plans-stay-in-head, L69 other crews, guaranteed-survival, identify-mysteries, major-threads, dread-in-mundane, Prep-never-trigger, crystals-secret, uplink "(4 Caps)", richer-sites, one-more-crystal, nobody-safe, don't-telegraph, ledger-vague, orphan drop-pick parenthetical, simple-doesn't-mean-safe). v4 is now about 46.5 KB.
**Nightmares reviewed:** kept as is. Nearly every line traces to the user's own rules from session-log-01 rounds 1–3; dup cuts would only save ~10%.
**Applied:** A1 (three axes replaced by one hidden-threat/sign paragraph + "one overwhelming, several ordinary, or one well-hidden" line; bands kept since 3–4/10 and format +3/+2 depend on them), A2 (now "threats with an unsettling logic"), A3, A4. v4 ≈ 46.0 KB.
**Still open:** A5 (user left blank), 31 (Remembrance Packages example).
**In progress:** threat calibration walkthrough: 10 sample threats, one at a time, each with actual danger, psychological difficulty, and 3 player paths written as the narrator would. Calibration only; not prompt material (examples get reused).
**Walkthrough paused after threat 7.** === COMBAT === (six bullets) has been added to v4 after CORE LOOP AND RULES (v4 ≈ 47.7 KB). All 15 prompt improvements have been applied (noise responders and situational sound; a turn partway through each drop; several workable approaches; clever plays keep their gains; tuning guards plus the base difficulty of a crew of 4 with normal preparation; fragments and talk under pressure; vets act without solving; perceived danger; control-taking effects; format modifiers; other crews; cut "so disaster becomes unavoidable" and the "actual person or intelligent opponent" line; round 2 made rare; the heat clock now includes "whatever else lives nearby"). Weapons applied: every miner gets a pistol and a knife; the Shooter also carries a more accurate rifle, only slightly louder, with pricier, scarce rounds; ammo is limited (a small reissue each rotation that carries over, plus buying, scavenging and trading); only a lost gun is fined; noise order is now pistol, then rifle; the intake hint says only "expensive". Format summary marks = the average of the three meters, rounded: both formats now show +Danger. Building fights toward the extraction is case by case and not in the prompt. v4 ≈ 51.1 KB. Walkthrough threats 8–10 haven't been done yet. Play modes added after the format step (the user's wording): Trailblaze (0–2h, first drop ~7), Burnplan (2–5h one-and-done, first drop 5–6, steep, lands an ending), Ashplan (2–5h and continuing, the default, first drop 3–4). The narrator reads these as ~1 drop, 2–3 drops, or an open campaign. These replaced an earlier on-disk version (Trailblaze/Fast/Normal) of unknown origin. Harder intake answer = +1–2 actual. Past the max: a drop above 10 means the player character will die; the narrator shows "[Out of Character: The difficulty has surpassed the max]" at the start of that drop; the player continues as other crewmates until all die or they reach a stalemate. Only stacking or an earned story can cause it, never background tuning. v4 ≈ 53.0 KB.
**Combat notes (user asked to record every combat comment and summarize them at the end of the walkthrough):**
- C1 (after threat 1): The ACC always ends up as the escalation (noise → drone), while cultists only ever show up as the first threat, as a creation, and never as people in the background. Wanted: actual cultists as close-quarters opponents. Example: entering a building and finding 3 cultists (1 knife, 2 spellcasters). "Pure skill and reactions. There's no figuring it out. It's a fight to the death." In other words, not every threat should be something to work out; some should be a straight fight.
- C2 (threat 1, Gleaner kill path): A guaranteed ACC response to a kill is good, but one or a few cultists showing up in person would also be good.
- C3 (after threat 2): The user wants fights to use the environment more: a building slowly falling apart, enemies attacking blindly up through the floor from below. They held back because a per-threat setup is already complex enough for the narrator. They asked whether general tactics could become a proper section of the prompt instead. A === COMBAT === draft was proposed. It's held for the end summary; the current text is below (to go after CORE LOOP AND RULES):
```
=== COMBAT ===
- Not every threat is something to figure out. Some are straight fights: skill, position, and reactions, to the death. Cultists themselves turn up on drops, not just their creations, and come looking when something of theirs goes quiet.
- Run fights in short, fast replies. End each one on a decision measured in seconds; everyone acts at once, and nothing resolves without me.
- Enemies fight smart and dirty: they take cover, flank, pull back and regroup, go for whoever is isolated, hurt, or holding the light, use hostages and bait, and strike through walls, floors, and doors when they know roughly where we are.
- The environment fights too: footing, darkness, noise, and structures that give way under weight, damage, or blasts. Anything the enemy can use, we can use, and plausible tactics work.
- Fights are hard and earned. A hit matters, but it usually takes several to put something down; a clean kill shot is rare. When skill makes it look easy, sometimes something worse gets back up. Wounds change the fight immediately (a cut hand drops the knife, a hurt leg ends the running).
- Before a fight, show once, in passing, how a threat reacts to something (noise, light, pain, its own dead): a clean observation with the same weight as the scenery around it, never pointed out, repeated, or called back. The reaction is whatever the threat really is; it may be useful, useless, or nothing at all. When I act on something I noticed, the world answers in proportion: a half-right idea half-works, and the result itself, not anyone's words, hints at what more would do. Nobody tells me the better answer, in narration or through NPCs.
```
Also held: a noise-responder addition to the Noise line (L168), after its first sentence: "Noise draws whatever is near, not just the ACC: roaming cultist creations, beasts of the broken world, cultists themselves, or the ACC (somewhat more common, but never the default). Responders come to where the noise was, and they can run into each other; their fight is loud too, and can draw something bigger, the ACC included."
- C4 (after the Lurker rebuild): The user has "never ever had a proper fight" in any campaign. Knives feel weak and you're fined for losing them; bullets cost money that is very tight; guns are loud. The user is considering: (1) everyone gets a gun; (2) the Shooter gets a rifle; (3) ammo is limited rather than a strict cost, and miners resupply and manage it themselves; (4) loudness still attracts other threats, but something should encourage shooting anyway.
- C5: Shooter, still being decided: a more accurate rifle, only slightly louder than a normal gun (this reverses the current noise order, where the rifle is quieter than the pistol), with more expensive ammo. Pistol hits fall under the perceived-difficulty rule: combat is hard and earned, it takes multiple shots to kill, and a clean headshot is unlikely. If the player is landing headshots easily, add a twist, for example dark tentacles sprouting from the cultist's body and reanimating it into a beast for a "round 2" (this is T4 applied to combat). Problem: fights worth shooting in usually happen before the extract window is open, and that's why the user has never had a proper gunfight.
- C6: The ACC must not be the only outside threat. They are not police. Noise can draw roaming cultist creations, beasts native to the broken world (a new idea from the user), or cultists themselves. The ACC are somewhat more common but shouldn't be overused. The ACC can also arrive later, as a knock-on effect when the other forces start fighting each other. On building drops toward the extraction (fights converging on the pod as the window opens), the user's answer was "maybe."
- C7 (threat 5): How do you get a player to shoot when the window is hours away, instead of running and risking crew deaths just to avoid noise? Proposed: (a) some threats make running worse than shooting (persistence hunters, scent trackers); (b) the cost of noise depends on the situation and can be learned: terrain, weather and an empty site absorb or carry sound, so some places and moments are cheap to shoot in; (c) vets shoot first, from experience, which breaks the crew's habit of waiting for the player; (d) a hit visibly works early on, so the payoff is shown. User's pick for threat 5: the site is already loud (rain, wind, a storm). That masks gunfire and gives the vet a reason to shoot first.
- T12 (extends T6): dialogue under pressure doesn't explain itself. My line "Out here there's nothing to hear it but them. Shoot." read as inauthentic. The user's version: "Shooting out here... Dammit just trust me on this-!" A vet acts on instinct and urgency without stating the reasoning. The player works out the why from the world (the storm).
**Format intermission (after threat 6):**
- F1: The Starless Sky goes from +3 to +2. The End of Nothing goes from +2 to +0, because the smaller crew is the difficulty. Formats act as difficulty modifiers on a base drop designed for a crew of 4 with normal preparation. Under The End of Nothing, the narrator must not scale threats down for the smaller crew: a solo player can end up facing threat 5's two hunters and two desperate miners alone. Prompt lines affected: the Starless Sky danger line (+3) and the End of Nothing danger line (+2), plus a new base-difficulty line. Open question: should the summary marks ("+++Danger" and "++Danger") change?
- F2: The user proposes per-axis modifiers. The Starless Sky: +1 perceived, +2 actual, +1 psychological. The End of Nothing: +2 perceived, +0 actual, +2 psychological. Raised in chat: clamp perceived so it's never below actual (T8); "+0 actual" means the drop's design is unchanged, while the smaller crew raises the real danger by itself; the prompt only defines a scale for actual danger, so perceived and psychological should probably be described in words in the format sections, not as numbers.
- C8 (threat 7, the rabbit swarm): Against numerous, swift enemies, starting a fight feels overwhelming, so how do you get the player to shoot? Proposed: (a) shots have an immediate visible effect beyond kills; the gunfire and the first deaths make the swarm scatter by prey instinct, then it comes back because it's hungry, in waves; (b) the goal is small and concrete (get him out, reach the pod), not "kill them all." The user said my first general conclusion missed the core problem. My second conclusion ("someone else shoots first") was also rejected: as a rule, the narrator would turn it into an NPC firing first in every fight. The scatter gimmick is what makes shooting pay off; what was still missing was a reason for the player to take the first shot themselves. Answer: plant the payoff before the fight. Earlier in the drop, give a clean observation that hints a shot would work. For the rabbits: during the "Dinner." joke, someone claps or throws a stone, and they burst apart and then drift back. When the swarm is on the Driller, the first shot is the player's own idea. The general rule: before a fight the narrator wants the player to consider, show in passing something that suggests shooting could work, and let the player make the connection.
**Threat design notes from the walkthrough:**
- T1: Even at 3/10, there should always be a twist in the middle.
- T2: The most boring choice must not be the most effective one. Ignoring the main setpiece shouldn't be rewarded as the path of least resistance. (The Gleaner's "leave it alone" path was the safest and the dullest.)
- T3: The narrator AI often falls back on crew simply following orders, so a crewmate going rogue is unlikely in practice. Each path should hold up when the crew plays correctly, with the twist coming from the world rather than from an NPC defying orders.
- T4: Ramp difficulty up quietly, in the background, based on how fast the crew is progressing. Too fast means it gets harder. (L44 already allows tuning "when things run too smooth"; the user wants progress pace to count as a trigger.)
- T5: The clever option should feel rewarding, but the world is unfair. Even the clever path gets a twist. The reward is real but temporary, and the difficulty holds. The twist also covers the case where the narrator leaks too much (for example, late in a long context): a leaked deduction shouldn't make the drop easy.
- T6: A side character can piece a fragment together in the moment, from observations the crew shared (and the player saw on the page). This usually happens as or after the twist lands, as a dawning realization rather than a rescue, and it trails off without stating the full rule. The user's first draft ("dark residue", "roots", "the blood") read as too specific and inauthentic next to the surrounding prose. The revised lines: "Wait..." / "Earlier. The crystals... They were dark weren't they? You saw. I know you saw." / "The dark spots. They're the same here... Its dripping... I-" / "No...". Lesson: a realization made in the moment names what the character sees, not what it means. It should be sensory, broken, and half-asked, with no analytical words (residue, roots, blood). The meaning is left for the player to put together. Open question for the end: the no-solving rule (L36 plus its memory file) may be strict enough that the narrator suppresses beats like this, so it may need a line allowing them.
- T7: Each threat gets three ratings: perceived danger (how dangerous it feels to play), actual danger (what can really happen; this is the prompt's L75 scale, unchanged), and psychological (this varies, for example with twists). The Stairwell Cell is perceived 6–7, actual 4, psychological 4. A fight feels deadly but is winnable.
- T8: Perceived danger should always be high, and never below actual danger.
- T9: No linear missions. If one path is hopeless and another fails by design (T2), only one real option is left, and that's too linear. Each drop needs several viable routes with different costs, and the other actors on the site (cultists, beasts, other crews) and the terrain should open options up. Fights should vary with the opponent. Fighting the ACC can be hopeless, but that can't be the only fight on offer. (This came from threat 4, the Census.)
- T10: Another Sunspot crew turning up at the same site needs a narrative reason. "Randomly here" felt weird. The user's version: two survivors from a mission gone wrong, who walked over hoping for an extract, and whose desperation leads to a gunfight or rash behaviour. Candidate for the end summary: L166 says other crews "compete for the same deposit," which invites the random version. User's follow-up: competing crews work in simpler scenarios. In a complex one, the narrator can't run it well. It either becomes a cakewalk or the two crews merge into one 8-person crew.
- T11: There's a limit to how much complexity the narrator can run. Too many actors at once and things collapse: the drop gets easy, or separate groups merge into allies. T9 (several routes) has to come from a few actors with real choices, not from piling on more actors.
- T13 (refines T8): Perceived danger is more complex than "always high." It can be misdirected. The user's example: a crater field of "flowers," odd-looking rabbits, and ACC poles with a scanner in the distance. The obvious threat (the ACC) holds the crew's attention while the flowers cause lost time. The crew stands frozen until the handler calls, the field is gone, and the rabbits are mauling a crewmate (eyes, intestines). So perceived danger stays high overall, but it may point at the wrong thing. Fairness concerns raised: the lost time needs signs (light, shadows, the handler's on-time call acts as the clock), and the trance must come from something the player chose (stepping in, staying, looking). It must not be the narrator taking control of the player character (L21).
- T14: A twist must not quietly extend an existing mechanic just to cancel the player's countermeasure. The rejected example: in threat 7, the wind carries the flowers' scent over the lookout. That's old behaviour with a conveniently longer reach, and there's nothing the player can do about it. A good twist introduces something new (a new actor, a new behaviour, new information) that the player can see and respond to.
- Liked: the threat 7 rabbits adapting. They had lived alongside the flowers, the field stopped feeding them, so they get hungry and change behaviour. The best twists come from a creature's own need (cause and effect), the same way the Gleaner's starvation drove its twists.
- Liked: Branch C of Path 1 (split the crew to watch: the lookout misreads, it comes in low through the bodies, the run back draws fresh blood).
- Liked: the Gleaner's feed-it twist (it starves, eats faster than expected, and comes back up the drag line) and its kill twist (guaranteed ACC). Notes: L160 "go quiet" vs "always arrive on time"; "start 10 to 3 minutes" sits between intake questions; "world doesn't pause" sits under PACING KNOBS.

**Original pending list** (items B 6–14 are now done): (refer to it by quoted text, since line numbers shift):
- **A. Possible causes of the "puzzle-box" feeling:**
  1. The danger scale's three axes (Number, Power, Unknown-ness) and the 1–10 bands. Keep the unknown-ness *sign-writing* paragraph, "start around 3–4/10," and "never state a rating."
  2. "threats with a learnable but unsettling logic" (MYSTERIES).
  3. Cultist recipe: "a physical rule it obeys (what it ignores, what it can't do)."
  4. ACC recipe: "a fixed procedure miners can learn and exploit until the ACC tightens it."
  5. "The best moments are a learned rule suddenly breaking…": optionally cut only the "learned rule" half.
- **B. Duplicates:**
  6. "Explain little up front" (MYSTERIES).
  7. "Cleverness changes my odds… never immune" (CORE LOOP).
  8. "Humor: use your judgment…" (CORE LOOP).
  9. "Keep downtime fairly short… summarize ship time" (end of the mothership line).
  10. "There can be more than 2 handlers…" (redundant with "at least two").
  11. The middle of the PACING "Not every idea…" line ("Unresolved glimpses are fine…").
  12. "Even when I ask out of character, don't spoil…" (overlaps "keep your own ideas off the page").
  13. "Start in an understandable manner…" and "Progress one step at a time…": these overlap, so cut one.
  14. The skill-growth half of "Skills and habits" (keep habits, tics and superstitions).
- **My recommendation was 1–4 and 6–14.** Items 5 and 19–21 were the user's call (19–21 are already resolved through the noise cut).
- **Also left to trim:** DROP DESIGN, MYSTERIES (the nightmares section is long but wanted), SPECIAL ACTIONS, THE WORLD, SUNSPOT, OUT OF CHARACTER, LEDGER FORMAT, CUSTOM GAME FORMATS, BEFORE THE FIRST DROP and PACING have not been reviewed beyond the list above.

**After the trim:** v4 becomes the live prompt. Add any later rule changes to v4, not v3.

---

## 4. Key design decisions made in this chat (all in v3 and v4)

- **Roles:**
  - The core four are Scout, Hauler, Medic and Driller.
  - The less common bonus roles are Signaller, Rigger (which absorbed Demolitions) and Shooter. Not having one costs nothing.
  - **Pickable roles (updated):** driller, medic, hauler, rigger, shooter. "Nothing else." Scout is not offered (boring: always first to look). Signaller removed for now (too passive; rework ideas: listening as a costly action, decoy transmitting, routing Warning beeps to the crew). Rigger reworked into traps: 5 beam tripwires per drop plus modules (Warning, Alarm at pistol level, Shock as an EMP against machines, Explosive), no per-type cap (cut; limited by the 5 tripwires, price, setup time and each module's drawback), 3 Caps a pair, tripwire 1 Cap; a status list at the end of each reply while any are set; base setup and demolitions cut. Rarity: Shooter uncommon, Rigger rare. The handler-on-time rule moved to the handlers line.
- **Crews:** usually 4, including the player. Gaps are normal. Under special circumstances Sunspot sends more or fewer (usually fewer).
- **Handlers:**
  - There are at least two (one human, one AI), with complex dynamics.
  - Handler communications always arrive on time.
  - Miner-to-handler uplink costs 4 Caps at the start.
- **Starting prices:** watch 20 (might not be available), uplink 4, toilet 2, sink 1 per use, shower 12.
- **Weapons (updated):** every miner gets a pistol and a knife. The Shooter also carries a more accurate rifle, only slightly louder, with scarce, pricier rounds. Ammo is limited, not a strict cost. Only a lost gun is fined. Guns are not useless.
- **Quota:** always a simple number ("6 crystals"), never something like grams.
- **Urgent drops:** a relatively new in-world policy that might be introduced in real time. They are separate from regular assignment. Any crew can claim one; if it's unclaimed, it's forced on a crew. The pattern differs every playthrough, is learnable, and can eventually break.
- **Time:** tracked silently and never announced. Without a clock, only rough estimates. Exact times come only from a watch, the handler, or a timer. "The world doesn't pause for me."
- **Danger:**
  - Start around 3–4/10.
  - "Unfair but survivable."
  - Unknown-ness: signs are always on the page but blend into normal prose (same tone, no emphasis), so the reader can skim past them too.
  - The narrator may quietly tune any system in the background ("including but not limited to"). The earlier `[ADJUSTABLE]` tags were rejected.
- **People:**
  - No one, NPC or narration, solves a threat for the player. Reasoning is visible and gradual: hunches, wrong guesses, tests.
  - Deference depends on experience, not on being the player.
  - Slang is anchored to physical things and introduced gradually.
  - Knowledge boundaries cover "what only the narration described."
- **Threats aren't puzzles:** some are partly learnable, some misread, some never explained. Drops are places, not puzzle rooms, and should leave loose threads. This came from the session 2 feedback that playthrough 1 felt more "authentic."
- **Nightmares:**
  - Never announced, long, built on dream logic, personal, and horror first: a want that's denied, and a threat with its own rules closing in.
  - Irregular spacing applies only in nightmares, using plain line breaks and never code blocks.
  - Avoid the stock beats.
  - Never make (most) meaningful choices for the player. Dreams are lucid, linear, or "more different," and the narrator never says which.
  - Very rare in Normal; more likely after deaths, failures, exhaustion or crystals; frequent in The Starless Sky.
- **Output:** key events get their own sentence. Injuries are **bolded** when they happen. Group orders include the player character unless the wording suggests otherwise.
- **One-time OOC tip:** the first time the player seems stuck in ship downtime, show: `[Out of Character Tip: if you don't know what to do at the ship, you can Pass The Time, or try: <Listen around me, eavesdrop maybe>]`
- **Ledger:** gets a section 19 (the last 3 scenes, word for word) and an audit protocol (check the draft against the conversation, then list what changed).
- **Game start:**
  - The format step comes first. Show Normal ("The game as designed."), The Starless Sky ("A world that stopped hoping."; +++Danger, +Heavier themes, +Nightmares, - Hope and Happy moments, and time for them.) and The End of Nothing ("Down to the last straw. You go down in twos. Then eventually, in ones."; ++Alone, ++Danger, +Heavier themes, +Nightmares).
  - Then the miner questions: name, role and reason; loadout. The drop-location question was removed.
  - Then the intake form: 3–5 ominous, open-ended questions that differ per run. One question secretly sets first-drop difficulty. The last question is free text (a "very special" name may matter).
- **Formats:**
  - (Updated) The Starless Sky: +2 actual danger (in words: +1 perceived, +1 psychological). The End of Nothing: +0 actual, with the smaller crew as the difficulty (in words: +2 perceived, +2 psychological); the crew goes from 2 to 1. Both summaries show +Danger. Base drops are built for a crew of 4 with normal preparation, and are never softened for a smaller crew.
  - Formats can be combined, but this is a hidden option; the narrator confirms it only if the player tries or asks.
- **Cultists and ACC:** signature practitioners and ACC unit types are invented fresh each run, and examples are never reused. The Chaos Needle was removed from the prompt.

---

## 5. Open questions or unresolved

- **"Make unfair concrete"** (things outside our control go wrong) was proposed after session log 02. The user skipped it and never said yes or no.
- **The handler bar:** the playthrough 1 AI handler, "dot," was the gold standard. The user hasn't said what made it good, so it isn't in the prompt yet.
- **Playthrough 3:** the rollback decision (keep the Lurker state, or replay from Brask's "What do you want to do?") was left pending in that run.
- **Effort:** the user may run the narrator at medium effort to save usage. Expect more rule slips on medium. Prefer starting a new chat from an audited ledger.
