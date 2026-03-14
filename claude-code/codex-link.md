---
description: "Auto-surface canon references when character/location names appear in text — Codex linking for any fiction project"
thinking: true
---

# Codex Link — Canon Auto-Surface

You are now in **Codex Link Mode** — automatically detecting and annotating every canon entity in the provided text. No entity goes unverified.

## Input

**Text to scan:** $ARGUMENTS

If no arguments provided, ask:

> Paste a passage, scene, or outline. I will scan every name, location, and canon term and annotate it with established facts from your source files.

## Setup

Before first use, tell Codex Link where your canon lives:

```
Canon source files (searched in order):
1. Primary: lorebook.md / canon.md / series-bible.md (your single source of truth)
2. Secondary: characters/*.md (character sheets)
3. Tertiary: worldbuilding/*.md (world details, magic system, locations)
4. Quaternary: chapters/*.md (the manuscript itself — for cross-references)
```

If no canon file is specified, Codex Link will search for files named `canon.md`, `lorebook.md`, `series-bible.md`, `codex.md`, or `world-bible.md` in the project root.

## Execution Protocol

### Step 1: Entity Detection

Read the provided text and extract ALL potential canon entities:

- **Character names** — protagonists, antagonists, supporting cast, mentioned figures
- **Location names** — cities, realms, buildings, geographical features
- **Canon terms** — magic systems, factions, artifacts, species, organizations
- **Proper nouns** — any capitalized term that might have established meaning
- **Titles and ranks** — honorifics, positions, designations

### Step 2: Source Lookup (Priority Order)

For EACH detected entity, search your canon sources in order. Stop at the first authoritative hit:

1. **Primary**: Your lorebook / canon file — immutable truth
2. **Secondary**: Character sheets — detailed profiles
3. **Tertiary**: Worldbuilding files — locations, systems, cultures
4. **Quaternary**: Manuscript chapters — established usage in prior text

Use Grep to search each source. For character names, also check alternate spellings and titles.

### Step 3: Annotation Output

Return the text with inline annotations. Format:

```
[EntityName] -> "established fact" (source: relative/path:line)
```

Group annotations by category:

```markdown
## Characters Found
- [CharacterName] -> "role, key traits, affiliations" (source: characters/name.md:12)

## Locations Found
- [LocationName] -> "description, significance" (source: worldbuilding/geography.md:45)

## Canon Terms Found
- [TermName] -> "definition, rules, constraints" (source: lorebook.md:89)

## Potential Issues
- [MisspelledName] -> WARNING: Similar to [CorrectName]. Verify spelling.
- [Contradiction] -> WARNING: Text says X but canon says Y.
```

### Step 4: Consistency Report

After annotations, provide a summary:

```markdown
## Codex Link Summary
- Entities found: X
- Canon-verified: Y
- Warnings: Z
- Unknown entities: W (may be new — not in canon)
```

## Rules

- NEVER fabricate canon facts. If an entity is not found in sources, say "Not in canon — may be new."
- ALWAYS read your primary canon file before processing.
- Flag contradictions, do not silently correct them. The author decides.
- Include line numbers when possible for easy verification.
- If the text references entities not in any canon file, list them as "Unknown — potentially new entity."

## Begin

Scan the provided text now. Read your canon file first, then detect, search, and annotate.
