# NYC Subway Mezzanine/Street-Level Signage: Direction Name Formula

## Lenny Phelan - stay tuned for my app

mailto:lennyphelan@gmail.com

**Scope**: This document covers static directional signs at mezzanine and street level - the signs that direct riders toward the correct platform entrance. These are simpler and more formulaic than platform-level signs, which include service pattern details.

---

## Quick Reference: The Core Rules

1. **In Manhattan or Bronx**: "Uptown" or "Downtown"
   - List all downstream boroughs: no commas, ampersand before last
   - Example: "Uptown Queens & The Bronx"

2. **In Brooklyn or Queens**: "Manhattan" or terminal names
   - Toward Manhattan: "Manhattan"
   - Away from Manhattan: Terminal names (e.g., "Lefferts Blvd & The Rockaways")
   - Branching lines drill down as branches diverge
   - **Fixed names**: J/Z always shows "Jamaica Center"; M in Brooklyn shows "Middle Village"

3. **Crosstown lines in Manhattan**: Special handling
   - L: "8 Av" / "Brooklyn"
   - 7: Comma-separated downstream stops, street numbers stripped

4. **7 train in Queens**: "Manhattan & Times Sq" / "Main Street-Flushing"

5. **G train**: Terminal names only ("Court Sq" / "Church Av")

6. **Shuttles**: Terminal names only

---

## List Formatting Rules

When multiple boroughs appear:

| Pattern | Format |
|---------|--------|
| Two items | "A & B" |
| Three+ items | "A B C & D" (no commas, ampersand before last only) |

Example: "Uptown Manhattan Queens & The Bronx"

**Exception**: 7 train in Manhattan uses commas between stops

---

## Shorthand Terminal Names

| Signage Name | GTFS Station Name |
|--------------|-------------------|
| Brighton Beach | Brighton Beach |
| Coney Island | Coney Island-Stillwell Av |
| Canarsie | Canarsie-Rockaway Pkwy |
| Main St | Flushing-Main St |
| Rockaway Park | Rockaway Park-Beach 116 St |
| Far Rockaway | Far Rockaway-Mott Av |
| The Rockaways | *(collective: Rockaway Park + Far Rockaway)* |
| Lefferts Blvd | Ozone Park-Lefferts Blvd |
| Jamaica Center | Jamaica Center-Parsons/Archer |
| Middle Village | Middle Village-Metropolitan Av |
| Bay Ridge | Bay Ridge-95 St |
| Pelham Bay Park | Pelham Bay Park |
| Woodlawn | Woodlawn |
| South Ferry | South Ferry |

---

## Borough Name Rules

Boroughs appear in two contexts:

1. **As suffix in Manhattan/Bronx**: Listed after Uptown/Downtown
2. **"Manhattan" as destination**: Used in Brooklyn/Queens toward Manhattan

| Borough | Format |
|---------|--------|
| The Bronx | "The Bronx" (always includes "The") |
| Brooklyn | "Brooklyn" |
| Queens | "Queens" |
| Manhattan | "Manhattan" |

- No "To" prefix on any direction names
- **Fixed terminal names** (don't list all branches):
  - J/Z: "Jamaica Center"
  - M (in Brooklyn): "Middle Village"

---

## Omitting Direction Words at Borough Boundaries

At certain stops, the direction word ("Downtown" or "Uptown") is omitted, leaving only the borough list.

**Omit "Downtown"** at the final downtown stop in Manhattan before entering Brooklyn.

**Omit "Uptown"** at:
- The final uptown stop in The Bronx
- The final uptown stop in Manhattan before entering Queens

Examples:
- At Woodlawn (final Bronx stop on the 4): "The Bronx" (not "Uptown The Bronx")
- At South Ferry (final Manhattan stop on the 1 before Brooklyn): "Brooklyn" (not "Downtown Brooklyn")
- At Lexington Av/63 St (final Manhattan stop on the Q before Queens): "Queens" (not "Uptown Queens")

---

## Special Cases

### Crosstown Lines in Manhattan

| Line | Signage pattern |
|------|-----------------|
| L | "8 Av" / "Brooklyn" |
| 7 | Comma-separated downstream stops (street numbers stripped) |

### 7 Train

**In Manhattan**: Comma-separated list of downstream stops, street numbers stripped (e.g., "Grand Central" not "42 St-Grand Central"). Toward Queens, ends with "Main St, Queens".

Examples from Times Sq-42 St:
- Toward Queens: "5 Av, Grand Central, Main St, Queens"
- Toward Hudson Yards: "Hudson Yards"

Examples from 5 Av:
- Toward Queens: "Grand Central, Main St, Queens"
- Toward Hudson Yards: "Times Sq, Hudson Yards"

**In Queens**: Hybrid format unique to 7 - "Manhattan & Times Sq" toward Manhattan, "Main Street-Flushing" away.

⚠️ **Uncertainty**: Queens signage predates 34 St-Hudson Yards (2015). May now read "Manhattan & Hudson Yards". Needs verification.

### G Train

Terminal names only: "Court Sq" / "Church Av"

### Shuttles

| Shuttle | Direction 1 | Direction 2 |
|---------|-------------|-------------|
| 42 St (S) | "Times Sq" | "Grand Central" |
| Franklin Av (S) | "Franklin Av" | "Prospect Park" |
| Rockaway Park (S) | "Broad Channel" | "Rockaway Park" |

### Branching Lines (A train example)

Signage shows terminal names, drilling down as branches diverge:

| Station location | Reachable terminals | Sign shows |
|------------------|---------------------|------------|
| Fulton St line (before any branch) | Lefferts, Rockaway Park, Far Rockaway | "Lefferts Blvd & The Rockaways" |
| After Rockaway Blvd (Lefferts branch) | Lefferts Blvd only | "Lefferts Blvd" |
| Broad Channel (Rockaway trunk) | Rockaway Park, Far Rockaway | "The Rockaways" |
| After Broad Channel (single branch) | One terminal only | "Rockaway Park" or "Far Rockaway" |

Key concepts:
- **Collective names**: "The Rockaways" covers both Rockaway Park and Far Rockaway (only such name in the system)
- **Branch-aware resolution**: Terminals shown are those *reachable from current stop*
