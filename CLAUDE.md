# be-the-robot: Claude rules

**Read `~/projects/NUC_RULES.md` first.** It covers Quatern priority, sim-run/gpu-run, the results policy and publishing.

Browser game: the player's webcam drives a physics-simulated G1 through balance challenges. Plan: PLAN.md
(draft until approved). State: HANDOFF.md.

- **Public repo, Apache-2.0.** Dependencies Apache/BSD/MIT only (e.g. MediaPipe Tasks JS Apache-2.0, MuJoCo
  WASM Apache-2.0). No SMPL or other non-commercial body models. Record every model and asset in THIRD_PARTY.md.
- **Privacy:** webcam frames never leave the browser: no uploads, no analytics, no remote logging. Recordings
  made for testing stay in git-ignored `results/`.
- **Shared pipeline:** the camera → pose → G1 retarget will be shared with shadowbox through a planned repo
  `g1-pose` (not created yet; see `~/projects/INDEX.md`). Don't build the shared parts here without asking.
- **Dev on the NUC, test from the Mac browser.** getUserMedia needs a secure context, so use an SSH tunnel to
  localhost (`ssh -L 5173:localhost:5173 nuc-admin`) or `tailscale serve`. Never bind the dev server to a
  public interface.
- No deploys (Pages, Vercel, etc.) without the owner's go-ahead.
