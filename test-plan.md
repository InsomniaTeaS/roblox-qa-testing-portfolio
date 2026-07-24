# Bug Reports

## BUG-001 — Ladder blocked by upper platform

**Area:** Four Towers  
**Severity:** High

**Steps**
1. Walk to the ladder leading to the upper level.
2. Climb near the top.
3. Try to step onto the platform.

**Expected:** The player reaches the platform without getting stuck.  
**Actual:** The character is blocked by overlapping geometry near the top.

**Regression check:** Test climbing up and down with different avatar sizes.

---

## BUG-002 — Bridge does not fully connect to landing

**Area:** Neon Transit Hub  
**Severity:** High

**Steps**
1. Enter the elevated route.
2. Walk across the bridge at normal speed.
3. Approach the far landing.

**Expected:** The bridge meets the landing with a continuous surface.  
**Actual:** A gap or height mismatch forces a jump or can cause the player to fall.

**Regression check:** Cross in both directions without jumping and test the left, center, and right side.

---

## BUG-003 — Flood and ground lava can conflict

**Area:** Disaster systems  
**Severity:** Critical

**Steps**
1. Trigger flood.
2. Trigger ground-floor lava before the flood state fully clears.
3. Watch the hazard level and damage behavior.

**Expected:** The systems are mutually exclusive.  
**Actual:** Both can compete for the same ground area and create an unclear or broken state.

**Regression check:** Test flood then lava, lava then flood, and near-simultaneous trigger requests.

---

## BUG-004 — Props overlap or float after map generation

**Area:** Multiple maps  
**Severity:** Medium

**Steps**
1. Load a generated map.
2. Inspect props near stairs, walls, and routes.
3. Walk through the area.

**Expected:** Props sit on a valid surface and do not block movement.  
**Actual:** Some props clip into structures, float, or block routes.

**Regression check:** Run placement validation and manually inspect every prop near a player path.

---

## BUG-005 — Crusher passes through roof

**Area:** Crusher disaster  
**Severity:** High

**Steps**
1. Run the crusher on a multi-level structure.
2. Watch it reach the roof.
3. Continue observing after contact.

**Expected:** The crusher stops at the roof and damages only the intended area.  
**Actual:** It can pass through the roof geometry.

**Regression check:** Test short, medium, and tall structures with different roof thicknesses.

---

## BUG-006 — Warning text is cramped on smaller screens

**Area:** User interface  
**Severity:** Medium

**Steps**
1. Use a phone-size emulator.
2. Trigger a disaster with a long name.
3. Observe the warning card and timer.

**Expected:** The name and timer remain readable.  
**Actual:** Long names crowd the card or overlap nearby elements.

**Regression check:** Test the shortest and longest names on desktop, tablet, and phone layouts.

---

## BUG-007 — Generator appears in an impractical location

**Area:** Map placement  
**Severity:** High

**Steps**
1. Load each map with generator placement enabled.
2. Check the floor, wall clearance, and route access.
3. Try to interact with the generator.

**Expected:** The generator is stable, reachable, and placed in a sensible service area.  
**Actual:** It can appear on a wall, in a route, or in another impractical location.

**Regression check:** Confirm every map has a reachable generator with clear interaction space.

---

## BUG-008 — Flood rises again after clearing

**Area:** Flood disaster  
**Severity:** High

**Steps**
1. Run flood to completion.
2. Wait for the water to lower.
3. Continue the round.
4. Watch the water level.

**Expected:** Water stays cleared until a new flood starts.  
**Actual:** Water can begin rising again without a new valid event.

**Regression check:** Complete several rounds and confirm the flood state resets every time.
