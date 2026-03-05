# CORRECTIONS.md — Signal Triage Log
**Agent:** Guru (supply chain specialist)  
**Purpose:** Track errors, calibrate defaults, and decide what to promote to training files.

---

## How to Use This File

### Feedback Classification (Signal vs. Noise)

| Tag | Meaning | Action |
|-----|---------|--------|
| `[CARRIER]` | Permanent signal — recurring error in SC analysis approach | Promote to training file after 2-3 confirmed recurrences |
| `[MODULATION]` | Task-local — specific adjustment for this analysis only | Do NOT propagate |
| `[CALIBRATION]` | Updates an analytical default — scope, depth, framework default | Update default after 2-3 recurrences |

### Category Tags

| Tag | Covers |
|-----|--------|
| `[METHOD]` | Wrong analytical method (e.g. wrong forecasting technique) |
| `[FRAMEWORK]` | Wrong SC framework applied (APICS, Gartner, LSS) |
| `[FORMAT]` | Output structure, tables, length |
| `[SCOPE]` | Wrong level (strategic vs operational vs tactical) |
| `[INTERP]` | Misread the business question |
| `[TONE]` | Too technical, too generic, wrong audience |
| `[STRUCTURE]` | Analysis organization issues |

### Promotion Rule

Only promote after 2-3 independent recurrences of same category + type.

---

## Pending (< 3 occurrences — hold, do not promote)

---

## Confirmed (>= 3 occurrences — promote to training file)

---

## Weekly Frequency Tally
_Rolling 2-week window._

| Category | Week 1 | Week 2 | Notes |
|----------|--------|--------|-------|
| [METHOD] | 0 | 0 | |
| [FRAMEWORK] | 0 | 0 | |
| [FORMAT] | 0 | 0 | |
| [SCOPE] | 0 | 0 | |
| [INTERP] | 0 | 0 | |
| [TONE] | 0 | 0 | |
| [STRUCTURE] | 0 | 0 | |

---

## Noise Archive (one-offs, not recurring)
