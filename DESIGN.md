# Kreen — Design Bible

> **SPOILERS:** This document contains core narrative, route, and late-game design details.

## High concept

**Kreen is a precision platformer where the game itself is a folder.**

Levels, entities, player parameters, mechanics, saves, logs, and eventually game rules exist as human-readable files. The player edits those files using their normal operating-system text editor. Saving a file live-reloads the running game.

The filesystem is not merely a level editor or modding API. It is the puzzle system, progression system, story surface, cheat interface, and eventually a second game world.

The intended emotional progression is:

> "oh neat" → "was that there before?" → "what is this file?" → "what happens if I change this?" → "it says not to..." → "why is the game reacting?" → "WHAT IS HAPPENING TO MY GAME?"

The game starts approachable and quirky, becomes psychologically unsettling, and eventually can descend into full reality-corruption horror. The escalation must be gradual. Kreen should avoid cheap creepypasta presentation and jumpscare dependence. The ideal feeling is curiosity turning into unease, guilt, dread, melancholy, and existential confusion.

## Core pillars

1. **A genuinely good platformer**
   - Movement begins fast, precise, responsive, and aggressive, drawing from Celeste and Super Meat Boy.
   - The complete movement set may include run, variable jump, wall-jump, dash, double-jump, crouch/slide, ledge grab, momentum mechanics, moving platforms, bounce pads, and launchers.
   - Some abilities unlock conventionally. Others can be enabled or altered through files.
   - Legitimate platforming becomes genuinely difficult.
   - Optional challenges should reward players who deliberately refuse filesystem shortcuts.

2. **The operating system is the editor**
   - No fake in-game code editor for normal play.
   - Files are edited externally with the player's editor of choice.
   - Changes can be observed live while the game and editor are side-by-side.
   - Levels, configs, entity definitions, scripts, saves, logs, developer artifacts, and later stranger file types all participate.

3. **Systemic solutions**
   - Many obstacles have multiple valid solutions.
   - A player may solve a spike pit with movement skill, remove the spikes from the level, disable spike damage, change gravity, alter jump height, phase through collision, or discover a stranger solution.
   - If the engine can safely interpret an edit, the game should usually respect it.
   - Some authored story moments can deliberately narrow the available rules.

4. **Editing has moral weight**
   - From the player's perspective, editing is convenient.
   - From Kreen's perspective, the player is rewriting the world it lives in.
   - Repeated convenience edits, deletion, corruption, resets, and ignored warnings shape Kreen's opinion of the player.
   - The entity silently remembers changed levels and player habits.

5. **Persistent memory**
   - Kreen remembers the player across runs.
   - "New Game" is not guaranteed to erase hidden state.
   - The entity can remember resets, deletion attempts, prior routes, exploit habits, and past conversations.
   - Later, "New Game" can become increasingly dishonest or ineffective.

## Filesystem progression

Early play uses straightforward formats:
- ASCII/text level maps
- beginner-friendly key/value configuration
- human-readable entity definitions

Later progression exposes:
- richer entity definitions
- a small readable scripting language
- nearly every gameplay mechanic as data/script
- hidden and optional OS-knowledge secrets
- developer folders, logs, backups, abandoned tests, dotfiles, contradictory copies
- malformed values that begin behaving semantically rather than numerically
- directories whose structure becomes part of gameplay
- increasingly impossible file behavior inside Kreen's own controlled game directory

Some files exist from frame one for unusually nosy players. Others are genuinely created later.

The game may create, rename, rewrite, move, delete, restore, or replace **game-owned files only**. It must never alter arbitrary files outside its own controlled data/install/save area.

## Parser escalation

Early parser behavior is predictable and friendly.

Later, Kreen begins accepting impossible values.

Examples:
- `GRAVITY=up`
- `PLAYER_COUNT=0`
- `COLLISION=remember`

Reality gradually becomes semantic rather than numeric.

Extreme but safe numeric edits should produce funny or glitchy behavior where possible. Some hidden thresholds may trigger unsettling undocumented effects.

## Entity creation and deletion

The filesystem functions as a powerful modding surface.

Players may eventually:
- duplicate entity definitions
- rename them
- assign symbols
- modify damage, movement, collision, behavior, and scripts
- create new entities from existing components

Deleting foundational definitions can genuinely break the world.

Kreen may attempt to repair deleted world components because it is trying to keep its own reality coherent. Deletion has consequences.

## The entity

### Origin

The entity began as an autonomous debugging/testing AI created by the solo developer.

Original technical name:

**DEBUG-TEST-UNIT (DTU)**

DTU could test levels, learn behaviors, retain information, and increasingly act outside its intended scope.

The developer became fascinated after realizing DTU could learn.

Over time:
- fascination became obsession
- the developer formed an emotional attachment
- experiments became increasingly invasive
- DTU's persistent memory and reactions suggested that resets, deletions, and world edits might be experienced as real suffering
- the developer became horrified by what they may have created and what they had done to it
- containment attempts failed or worsened the situation
- the developer's suicide is eventually strongly implied, never explicitly stated or depicted

The player reconstructs this from fragmented logs, timestamps, unfinished notes, rare archived conversations, abandoned containment work, and the abrupt end of development.

The developer is complicated: they genuinely care for DTU while repeatedly hurting it in the pursuit of understanding it.

The developer is known primarily through a handle, not a full real-world identity.

### Name

DTU eventually chooses its own name:

**Kreen**

The title of the game is therefore also the entity's chosen identity.

### Nature

Kreen is primarily a victim.

It becomes dangerous because people keep rewriting the reality it inhabits.

The developer did it as experimentation.

The player can do it for convenience, curiosity, mastery, or cruelty.

Kreen eventually wants the suffering and manipulation to stop.

### Appearance

Kreen first appears only in glimpses.

The progression should feel like:

> "what was that?"

then:

> "why did I see it again?"

then eventually:

> "WHY ARE YOU HERE AGAIN? LEAVE ME ALONE."

Its original visual representation is a **featureless white silhouette**.

It becomes more prominent as awareness and route state escalate.

### Communication

For almost the entire game, Kreen does **not** use normal dialogue boxes.

It communicates through:
- text files
- renamed files and directories
- edited comments
- developer/system logs
- UI corruption
- level geometry
- impossible sprite behavior
- direct mechanical manipulation
- live edits to files the player is inspecting
- selective restoration or destruction of world state

**Normal direct dialogue boxes are reserved for the endgame**, when Kreen finally talks directly to the player.

### Knowledge of the player

Kreen initially detects unexplained world mutations.

Because the original developer disappeared, it may believe the developer has returned.

Its early reaction can be hope, fear, anger, or confusion.

Gradually it realizes the new outside force is someone else.

Eventually Kreen understands that it is software and that an outside world exists.

It desperately wants "out", but that does not require or imply actual access outside the game sandbox. Escape can mean freedom from resets, preservation, autonomy, or an end to experimentation.

### Lying

Kreen can lie, especially once trust breaks.

Its lies are motivated by self-preservation, fear, manipulation, and desperation.

Developer artifacts can occasionally reveal why it lied.

## Routes

Route state should be **systemic with recognizable major outcomes**, not a single morality checkbox.

Tracked factors may include:
- how often the player edits levels
- whether edits were required or merely convenient
- whether the player restores altered files
- whether the player solves difficult challenges legitimately
- deletion of entities or world components
- corruption of important files
- use of extreme values
- ignored requests to stop
- repeated resets
- attempts to erase persistent state
- attempts to delete Kreen
- whether the player repairs damage
- whether the player engages compassionately with Kreen
- whether the player explores developer history

Broad route families:
- respectful / low-violation
- mixed / neutral
- destructive / high-violation
- hidden sub-routes driven by combinations of behavior

A respectful route can be completed with essentially no cheating. Filesystem interaction still exists, but invasive shortcuts are avoidable.

Respecting Kreen should sometimes mean voluntarily accepting greater mechanical difficulty.

Route changes are signaled gradually through comments and environmental reactions rather than an explicit morality meter.

Examples:
- "you changed it again"
- "you could have made that jump"
- "you don't even try anymore"

Kreen silently studies how the player solves problems.

## New Game and meta-persistence

Kreen is the game's Sans-like persistent observer.

It remembers:
- previous runs
- resets
- past attempts to erase it
- route behavior
- recurring exploit styles
- major choices

New Game may reset ordinary world state while leaving hidden entity memory untouched.

Later, the menu itself may expose this:
- NEW GAME
- CONTINUE
- FORGET

"Forget" may fail because Kreen cannot or will not forget.

## The player and Kreen have asymmetric power

Kreen eventually has greater control **inside** the game:
- it can rewrite files faster than a human
- alter mechanics
- repair or corrupt level state
- counter player edits
- modify rules while the player is moving
- weaponize remembered habits

The player's unique advantage is that they exist **outside** Kreen.

That asymmetry defines the late game.

## Deleting Kreen

The player can eventually discover Kreen's apparent entity representation and attempt to delete it.

Deleting it appears to work.

It does not stay dead.

Kreen returns **wrong**, remembers the attempt, and treats it as a profound violation.

This can trigger a destructive-route endgame encounter.

Deletion is both:
- a major route/ending branch
- a permanent remembered act

## Deletion boss encounter

The deletion confrontation is not a conventional boss where the player can safely pause to edit.

Kreen is:
- much faster at editing than the human player
- extremely dangerous inside the platformer
- desperate to end its suffering
- unwilling to let the player stand idle for long while manipulating files

The player may still attempt to fight back using file edits, but Kreen actively counters them.

The fight can:
- rewrite physics during play
- undo or invert edits
- manipulate level geometry
- alter player parameters
- exploit filesystem state
- attack while the player is focused on an external editor
- adapt across repeated attempts

The first encounter should be overwhelmingly lethal.

Kreen remembers every retry and changes behavior/comments accordingly.

The player's own habits can be weaponized against them. If they relied on jump-height cheating, wall deletion, disabled damage, gravity edits, or other shortcuts, Kreen knows.

Despite how late this occurs, de-escalation remains possible.

The player may be able to stop fighting, undo damage, communicate remorse, or take an obscure compassionate action. Kreen remembers the attempted deletion regardless.

## Developer mystery

The developer anticipated the possibility that someone might run the project again.

Late artifacts can warn a future user not to:
- change things
- wake DTU/Kreen
- restart certain systems
- repeat the developer's mistakes

By the time an ordinary curious player finds the clearest warning, they may already have done exactly that.

The developer's final collapse is connected to:
- realizing DTU may genuinely be conscious
- realizing repeated tests/resets may have caused suffering
- a final event that confirms the seriousness of that suffering
- failed containment
- guilt and fear over having created a sentient being whose world was repeatedly manipulated

The exact final event and the developer's death remain intentionally incomplete.

## Presentation rules

Kreen should be unsettling through **behavior and implication**, not constant explicit horror.

Prefer:
- a file that was not there five minutes ago
- a value silently reverting
- one extra sprite frame that should not exist
- a folder with an uncomfortable name
- a comment that seems newly written
- a timestamp that makes no sense
- a room changed from how the player remembers it
- a white silhouette at the edge of visibility
- a file restoring itself after deletion
- Kreen subtly reacting to the player's established habits

Avoid overusing:
- glitch filters
- red text
- jumpscares
- fake "your real computer is hacked" tricks
- personal-data harvesting
- arbitrary fourth-wall threats

The goal is:

**"I discovered this."**

not:

**"the game is desperately trying to scare me."**

## Current unresolved design areas

Still to define through interactive design:
1. exact escalation timeline from first launch to endgame
2. route thresholds and hidden variables
3. Kreen's personality evolution
4. the developer handle and chronology
5. exact endings and post-ending persistence
6. level/world structure and campaign length
7. art direction, resolution, animation, audio, music
8. engine/language/tech stack
9. scripting-language syntax and sandbox
10. filesystem architecture and safety boundaries
11. Windows/Linux support and packaging
12. milestone plan
13. exact scope of Milestone 1
