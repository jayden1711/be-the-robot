# be-the-robot: PLAN (skeleton, not yet reviewed by the owner)

_Status: skeleton only. No code yet. The first session writes the full plan for approval and builds nothing before that._

Goal: a browser game. The player's webcam pose drives a physics-simulated G1 (standard arena G1) through balance
challenges. Runs entirely client-side.

Fixed constraints (from the owner):
- Shares the camera → pose → G1 retarget with shadowbox through a planned repo `g1-pose` (Apache-2.0,
  TypeScript + Python with shared golden tests). Until it exists, propose the boundary in this plan.
- Apache/BSD/MIT dependencies only (candidates: MediaPipe Tasks JS, MuJoCo WASM). No SMPL.
- Webcam frames never leave the browser.

Open questions for the plan: control mapping (direct pose targets vs. assisted balance controller),
challenge design, latency budget, browser/device targets, hosting (needs the owner's go).
