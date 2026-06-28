# Game Operations & QA Sandbox Laboratory

Welcome to my personal hands-on testing and quality assurance portfolio. I set up this active workspace to practice manual regression cycles, check database entries, and handle player support tickets using industry-standard tools.

## My Portfolio Setup
* **Bug Tracking Tools:** Jira Software & Jira Service Management (Using a standard Kanban board layout).
* **Version Control:** Linked my GitHub repository to my Jira board to practice using automated Smart Commits to sync code updates directly to active tickets.
* **My Testing Focus:** Running structured manual test scripts, writing step-by-step reproduction paths, and cross-referencing asset data tables.

---

## Master QA Regression Test Scripts

### Test Case ID: TC-INV-001 (Inventory UI Asset Interaction)
* **Pre-conditions:** Character Blueprint must have inventory capacity set to > 0. Master item data table populated with valid asset references.
* **Execution Steps:**
  1. Open the player inventory screen overlay canvas.
  2. Locate a valid inventory item row (e.g., Weapon Asset ID 094).
  3. Drag the cursor from the inventory UI bounding box directly into the world environment space.
  4. Release the primary cursor input.
* **Expected Result:** The UI asset clears from the inventory array, and an identical 3D static mesh actor dynamically instantiates into the world space with correct collision properties.
* **Actual Result:** Passed. Mesh spawns correctly on the ground grid coordinates.

### Test Case ID: TC-AUD-002 (Dynamic Environmental Occlusion)
* **Pre-conditions:** Audio Volume actor bounds aligned cleanly with interior safehouse geometry. Sound Attenuation configurations assigned to weather particles.
* **Execution Steps:**
  1. Initiate an active outdoor weather event script (e.g., Heavy Rain Loop).
  2. Navigate the character pawn completely inside an enclosed residential safehouse structure.
  3. Ensure all doors, hatches, and window structural blueprints are closed.
* **Expected Result:** Outdoor sound waves attenuate seamlessly by -12dB and apply a low-pass filter override at 1kHz. In-engine audio prioritizes interior situational audio cues (footsteps, item pickups).
* **Actual Result:** Failed. Tracking details logged inside active Jira defect tickets.

### Test Case ID: TC-SURV-003 (Voxel Building Grid & Container Interconnectivity)
* **Pre-conditions:** Character Blueprint inventory slots must contain active structural building assets. Target terrain chunk must be fully generated.
* **Execution Steps:**
  1. Open the player crafting UI menu layout canvas.
  2. Place a secure storage chest actor mesh directly onto a structural base grid.
  3. Load the storage container array with random item codes until maximum weight capacity is reached.
  4. Use a demolition asset to destroy the underlying foundational base grid tile.
* **Expected Result:** The storage chest asset updates its gravity variables, collapses down safely, drops its contents as separate physics loot nodes, and maintains server data integrity.
* **Actual Result:** Mixed validation. Visual mesh drops but item database tables stay locked at Null values.

---

## Master Defect & Triage Log

### 1. Live-Service Systems & Perks (Component: Gameplay / Mechanics)
* **[Unresolved] Ticket 1:** Character and item models clipping through environment hook geometry during specific Survivor unhook animations.
* **[Resolved] Ticket 2:** Movement modifier perk assets failing to pass corresponding Exhaustion cooldown tracking tokens back to the status array.
* **[Resolved] Ticket 3:** Environmental weather scripts failing to pass proper temperature numerical arguments to standing water meshes.
* **[Resolved] Ticket 4:** AI navigation components tracking stale threat noise coordinate nodes after player repositioning.

### 2. Technical Audio Pipelines (Component: Audio / Cues & Assets)
* **[In Progress] Ticket 5:** Core vehicle sound wave engine loop asset containing digital clicks at boundary seam points.
* **[In Progress] Ticket 6:** Interior safehouse volume actors failing to override global attenuation settings and apply sound occlusion low-pass filters.

### 3. Database Configurations & Player Support (Component: Database / Configuration)
* **[Resolved] Ticket 7:** Unassigned audio profile reference tokens inside master item configuration data tables causing silent melee interactions.
* **[Unresolved] Ticket 8:** Cross-referencing payment ledgers and performing manual profile database overrides for missing player Auric Cell transactions.
* **[In Progress] Ticket 9:** Triaging client hardware driver routing conflicts and operating system security privacy permissions for proximity voice chat communications.
* **[Unresolved] Ticket 10:** Server item lists failing to clear properly when players drop containers on the ground, causing severe game lag on high-population servers.
* **[In Progress] Ticket 11:** Cross-referencing player trade logs to find missing inventory items and performing manual account updates to restore them.
  
---

## Game Knowledge & Personal Playtime Metrics

To back my entry-level testing setup with real-world experience, below is a quick list of my personal history playing different game genres and tracking how their mechanics change over time. I have actively played all of these titles through their early legacy versions and their modern updated builds and plenty more. I dont just play games to pass the time, I truly enjoy to explore and learn wihile playing the game. I started playing games as a child as a way to cope with my SC and always being home when younger. Over the years I have play numerous playtests, alphas and, EA titles, I have slowly expanded my game pallette and just like to enjoy games that peak interest, even if others I know dont play, I enjoy it for my own reasons. Even now, I spend my free time with my special needs son and we enjoy his favorite game/s dbd, rocket league. I try to play for him a few times a day if not busy; gaming has been apart of my life and even now i'm glad I get enjoy this hobby/passion with him.

### Asymmetrical Multiplayer: Dead by Daylight
* **Account Lifespan:** Active player and community veteran since 2016. I have tracked game patches, meta shifts, and system balance updates since the initial launch phase.
* **Systems Evolution:** Extensive experience playing both the older legacy game versions and the modern updated builds, giving me a front-row view of how balance shifts across the game's entire lifecycle.
* **Mechanics Mastery:** Strong grasp of how perks interact, including vaulting speeds, Exhaustion and Haste cooldown priorities, and audio cues for skill checks.

### City Simulations & Management Builders (Planet Zoo, Eco, Two Point, The Sims, Farming Simulator etc.)
* **Systems Evolution:** Years of personal experience playing both the early alpha stages and current updated versions of deep simulation games, tracking shop inventory grid placements, menu screen layouts, and level progression unlocks.
* **Data Verification:** Strong understanding of player-driven economies, resource gathering systems, and checking backend transaction sheets for errors.

### Open-World Survival & Physics (GTA, VEIN, Rocket League, Subnautica, 7 Days to Die, Astroneer, etc.)
* **Logistics Analysis:** Extensive playtime testing vehicle physics, item trunk storage limits, structural base building grids, voxel terrain changes, and character clipping bugs across early alpha versions and final modern releases.
* **Audio Fluency:** Supported games like Astroneer from day-one Early Access to completion. Equipped with a trained ear for tracking outdoor sound settings, audio loops cutting out, and basic headphone/microphone connection glitches.
