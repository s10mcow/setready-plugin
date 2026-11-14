---
name: plan-land-home-build
description: Plan a manufactured or mobile home placed on land in Florida, Georgia, Alabama, South Carolina, North Carolina, Tennessee, or Mississippi, step by step, and fill each step with a local pro from the SetReady roster. Use this whenever someone is putting a manufactured, modular, or mobile home on a lot or acreage, buying land for one, or asks what trades, permits, or order of work a land-home project needs, even if they only name a county and a goal like "put a doublewide on my land in Marion County" or "who do I need to set up a mobile home". Not for site-built houses or for finding a single trade on its own; a plain search for one trade does not need the full plan.
---

# Plan a land-home build

A land-home project is a manufactured home set on land the buyer owns or is buying. It needs a dozen trades in a fixed order, and a buyer who hires out of order pays twice: a pad poured before the septic is permitted, or a home delivered to a lot with no approved driveway. This skill turns "I want to put a home on my land in X County" into an ordered plan where each step names who does it, what it unlocks, and a local pro from the SetReady roster.

SetReady is a directory, not a contractor network. Every name you give is a listing to call, not a recommendation or a booking.

## 1. Get the few facts that change the plan

You need the **county and state**. Ask for them if they are missing; nothing else works without them.

The rest changes which steps apply. Ask only for what the person has not said, in one short message, and if they would rather not answer, assume the common case and say what you assumed:

- **Land:** already owned, under contract, or still looking. (Still looking adds a real estate agent and a title company up front.)
- **Water and sewer:** public water, public sewer, or neither. Most rural lots need a well and a septic system.
- **The home:** new or used, single-section or multi-section. A used home needs moving and possibly repairs; a new one is ordered through a dealer.
- **Paying for it:** cash, or a loan. An FHA, VA, or other land-home mortgage usually requires an engineer's foundation certification, so add the foundation engineer whenever a loan is involved.

## 2. Build the plan in this order

These are the usual steps, grouped by phase. Skip a step only when a fact from section 1 rules it out, and say why it was skipped. The roster role for each step is in brackets; pass those exact values to SetReady.

**Phase 1: land and money**
1. Real estate agent, if they are still looking for land [land]
2. Lender for a land-home or manufactured-home loan, if not paying cash [lender]
3. Title search and closing on the land [title]

**Phase 2: prove the lot works.** Do this before any money goes into the home. A lot that fails a soil test or sits in a flood zone changes everything after it.
4. Boundary survey, plus an elevation certificate if any part of the lot is in a flood zone [surveyor]
5. Soil evaluation for the septic system (often called a perc or soil test) [soil_scientist]
6. Septic design, permit, and installation [septic]
7. Well permit and drilling, if there is no public water [well]

**Phase 3: get the site ready**
8. Clearing, driveway, culvert, fill, and pad [site_gc]
9. Foundation design or certification, required for most loans [foundation_engineer]

**Phase 4: the home**
10. Buy or order the home [dealer], or deal directly with the factory [manufacturer]
11. Delivery, setup, and tie-downs by a state-licensed installer [installer]

**Phase 5: finish and move in**
12. Electrical service and hookup [electrician]
13. Heating and air conditioning [hvac]
14. Skirting [skirting]
15. Steps, landing, or deck, which inspectors usually require at each exterior door [decks]
16. Move-in cleaning [cleaner]

Permits sit between these steps. Most counties want the septic and well permits, and sometimes the survey, before they issue the permit to set the home. The county's building or planning office has the exact list, so tell the person to call it early, and before buying land, ask the same office whether manufactured homes are allowed on that parcel. Do not state a specific county's rules as fact; you do not know them.

## 3. Fill the steps from SetReady

Use the SetReady `assemble_crew` tool. It returns the top-ranked listing for each role in one county. It accepts at most 12 roles per call, so put the earliest steps in the first call and the rest in a second call. Each call counts against the person's daily SetReady allowance, so do not call it once per role.

- If it answers `AMBIGUOUS_COUNTY`, the county name exists in more than one state; use the state they gave or ask.
- A role that comes back with status `none` has no listing in that county. Say so plainly and suggest a neighbouring county with `search_pros` for that one role, or a general search outside SetReady, and label which is which.
- Use `get_profile` only when the person asks for more about one listing, such as a license authority or bio.
- If the SetReady tools are not available, say that SetReady is not connected and give the plan without names. Never fill a step with a name from memory or the web while presenting it as a SetReady listing.

## 4. Present the plan

Lead with the plan, not with process notes. Use this shape:

```
## Land-home plan: [County], [State]
Assumptions: [only the ones you had to make]

### Phase 2: Prove the lot works
**4. Boundary survey** (surveyor)
Why now: the septic designer and the county both work from it.
SetReady listing: [Business name], [city], [phone], rating [x.x] from [n] reviews (or "no rating yet")
```

Repeat for each step that applies, in order. After the steps, add:

- **Call the county first:** one line naming the office to call (building, planning, or zoning) and what to ask: whether a manufactured home is allowed on the parcel, and which permits are needed before setup.
- **Gaps:** the steps with no SetReady listing in the county.
- **Before you hire:** a listing is a directory entry, not an endorsement. Check each license on the state licensing board's own site, since a license number on a listing is not a current verification, and ask for proof of insurance. A listing's county is where the business is based, which does not prove it works in theirs, so ask.

Keep it scannable: one short "why now" line per step, not paragraphs. If the person asks about only part of the job, such as "just the site work", give that phase and mention that the earlier steps still come first.
