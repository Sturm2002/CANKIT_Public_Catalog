# CANKIT Public Catalog

Public, **presentation-only** names and descriptions for CANKIT modules, actions and events. This repository does not contain firmware, secrets, pairing information, device identities, CAN addresses or authorization rules.

`catalog/v1.json` is the published data contract. A mobile app may fetch it read-only at startup and refresh it manually. Device discovery is authoritative: the catalog cannot create modules, actions or events; only capabilities actually reported by the connected gateway can be displayed. Catalog content must never grant permission to execute an action, bypass device-side safety checks or turn an offline module online. For unknown/mismatched firmware use the app's built-in safe fallback.

The schema uses exact `moduleType`, `hardwareVersion`, `firmwareVersion` and `kind` + `key` matching. Versions here describe the known firmware profiles and are not update/OTA instructions. Update names only after comparing with the firmware's reported manifest; do not publish sensitive diagnostics or personally identifying device identifiers. Changes to this public repository are reviewed before publishing.

Raw URL after publishing: `https://raw.githubusercontent.com/Sturm2002/CANKIT_Public_Catalog/main/catalog/v1.json`.
