# Master QA Regression Test Script: Inventory & Spatial Systems

## Test Case ID: TC-INV-001 (Inventory UI Asset Interaction)
* **Pre-conditions:** Character Blueprint must have inventory capacity set to > 0. Master item data table populated with valid asset references.
* **Execution Steps:**
  1. Open the player inventory screen overlay canvas.
  2. Locate a valid inventory item row (e.g., Weapon Asset ID 094).
  3. Drag the cursor from the inventory UI bounding box directly into the world environment space.
  4. Release the primary cursor input.
* **Expected Result:** The UI asset clears from the inventory array, and an identical 3D static mesh actor dynamically instantiates into the world space with correct collision properties.
* **Actual Result:** Passed. Mesh spawns correctly on the ground grid coordinates.

---

## Test Case ID: TC-AUD-002 (Dynamic Environmental Occlusion)
* **Pre-conditions:** Audio Volume actor bounds aligned cleanly with interior safehouse geometry. Sound Attenuation configurations assigned to weather particles.
* **Execution Steps:**
  1. Initiate an active outdoor weather event script (e.g., Heavy Rain Loop).
  2. Navigate the character pawn completely inside an enclosed residential safehouse structure.
  3. Ensure all doors, hatches, and window structural blueprints are closed.
* **Expected Result:** Outdoor sound waves attenuate seamlessly by -12dB and apply a low-pass filter override at 1kHz. In-engine audio prioritizes interior situational audio cues (footsteps, item pickups).
* **Actual Result:** Failed. Tracking details logged inside active Jira defect tickets.

---

## Test Case ID: TC-DBD-003 (Asymmetrical Perk Interaction Tracking)
* **Pre-conditions:** Survivor loadout assigned with active movement modifier tokens (e.g., Exhaustion / Haste triggers). 
* **Execution Steps:**
  1. Trigger an accelerated physical navigation interaction (e.g., Fast Vaulting a window mesh asset).
  2. Monitor the active Status Effect HUD layout display elements immediately upon exit frame animation.
  3. Verify the execution of corresponding cooling timers inside the backend database registry.
* **Expected Result:** Haste velocity values modify to 1.5x multiplier for 3 seconds, and an instant 40-second Exhaustion tracking token forces down onto the status data table array.
* **Actual Result:** Mixed validation. Visual UI clears but database variables stay at Null values.
Use code with caution.
