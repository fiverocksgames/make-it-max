# BGM Source Provenance

## Approved tracks

| Runtime role | File | Source | Bytes | SHA-256 |
|---|---|---|---:|---|
| Lobby | `bgm_lobby_clockwork.mp3` | **The Clockwork Parlor**, Project Lead supplied, generated with Gemini Lyria | 4,190,264 | `c522f1f0456cc2cdfa9b9a1b4bd584bb5001dbf0e8df148814ad0b0714215bfc` |
| In-game | `bgm_game_gentle.mp3` | **Gentle Rhythm of Play**, Project Lead supplied, generated with Gemini Lyria | 4,170,829 | `8e2ac0e89d11e900e7ed5e8a6e596ae1ac08d7d97b30224ce091e976830b567b` |

These tracks were explicitly selected by the Project Lead on 2026-10-06 for Make It Max.

## Binary ingress evidence

The original Project-Lead-supplied MP3 files were staged privately in Google Drive under the shared `FiveRocks-Binary-Ingress/make-it-max/2026-10-06/<full-sha256>/` convention. Reader access was granted only to the shared binary-ingress service identity.

The project used the verified shared workflow `fiverocks-dev/tools/.github/workflows/binary-ingress-verify.yml@37c3c9aa2078f80dd77472a1d8468a6653f9e650`. The reusable workflow verified Drive metadata, exact byte size, and SHA-256 before producing a one-day handoff artifact. A separate project-local write job re-verified the same byte size and SHA-256 before writing each file into `public/audio/`.

Verified ingress runs:

- Lobby / Clockwork: Make It Max Actions run `37420365744` — success.
- In-game / Gentle: Make It Max Actions run `37420450201` — success.

The final repository tree reports the same byte sizes at the approved destination paths.

This file records project provenance only. It does not assert broader redistribution or standalone relicensing rights beyond the Project Lead's authorized project use.
