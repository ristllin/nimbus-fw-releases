# Nimbus firmware releases

Public delivery channel for **signed** [Nimbus](https://github.com/ristllin/Nimbus) firmware OTA updates.

Each release attaches `firmware-esp32s3.bin`, `firmware-test.bin`, and a `manifest.json`
(version + per-variant sha256 + ECDSA-P256 signature). Devices poll
`releases/latest/download/manifest.json`, verify the signature against a public key baked
into the running firmware, and install over the air. The source repo stays private; only
the signed binaries (which carry no secrets) are public here.
