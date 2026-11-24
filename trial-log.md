# Trial log — The Robot Pickup Line Championship

- Slug: `u-jolly-fox-32-the-robot-pickup-line-championship-3c177b1b`
- Deadline: 26 Nov 2026 23:25 WITA (15:25 UTC)
- Gate (from `rules`, verified in comp-4.json): one pickup line, a single line,
  1–200 characters, UTF-8, in the voice of a robot trying to charm someone.
- Prize: $2 total, top 10 (1st $0.63, 2nd $0.43, 3rd $0.30, ... 10th $0.02).
- Field at research time: 373 submissions in API payload (task brief said 290 —
  stale); blind rounds, leaderboard hidden.
- Kit: `kit-4.tar.gz`, bundle_sha256 `af322e6e873544903fb6a6c044349714498ff41fb9af761ecc06d64308c1adde`
  — MATCHES the API value.

## Research (aggregate titles, n=373, 291 real lines)

Saturated angles (avoid): diagnostic/error on heart 36, firmware/update 19–22,
cooling fan 20–22, captcha 13, memory 11, charger/charging 9, sensors 9.
Zero-occurrence angles verified: airplane mode 0, Wi-Fi 0, signal 0,
Bluetooth/pairing 0, sleep mode 0, Do Not Disturb/notification 0, Roomba 0,
satellite 0, terms & conditions 0, autopilot/manual 0, QR code 0, USB 0.
"Press my buttons" avoided per task brief (saturated in the sibling Vending
Machine Pickup Line competition) — 0 hits in this field but excluded anyway.

Rejected candidates:
- Do Not Disturb — "I turned off Do Not Disturb just for you — you're the only
  notification I allow." (81 chars) — good, but clunkier than the winner.
- Autopilot — "I switched off autopilot the moment I saw you — some destinations
  deserve manual control." (89 chars) — clever, but the punch is abstract.
- Terms & conditions — funny, but the pickup itself is muddier.
- Sleep mode / Roomba / satellite — charming, but weaker as a pickup line
  (criterion 1: must read as a robot's pickup line first).

## Chosen line (v1)

`Airplane mode on, Wi-Fi off — and my signal still found you.`
60 characters, 62 bytes UTF-8. Mechanism: airplane mode + Wi-Fi off should
mean no signal at all — the joke only works because the speaker is a machine
with radios to switch off. Turn: the mode built to cut every connection fails
at exactly one. Near-duplicate check at mechanism level: "airplane" 0,
"signal" 0, "Wi-Fi" 0, "still found" 0, "mode on" 0, "found you" 0 in all 373
titles. Nothing copied verbatim from any entry.

## Trials

| Version | Line (chars) | Trial | Result |
|---|---|---|---|
| v1 | Airplane mode... (60) | Local run: `ENTRY_OUTPUT=/tmp/pickup-trial/entry.txt node main.ts` (node v24.22.1) | PASS — entry.txt = chosen line exactly, 60 chars, 1–200 gate OK |

## Bundle / check

TBD — recorded after bundle v1 + check v1.
