# ecw-jwks

Public JSON Web Key Sets for the LightHouse eClinicalWorks FHIR applications
(SMART Backend Services, RS384). PUBLIC key material only - the private keys
never leave the LightHouse database.

| App | JWKS |
|---|---|
| LightHouse ECW Reader (read app) | `read/jwks.json` |
| LightHouse ECW Writer (write app) | `write/jwks.json` |

Each file may carry several `kid`s (one per environment). Keys are appended
with `scripts/ecw_bridge_keygen.py <role> --jwks-out ... --jwks-merge <this file>`
in the LightHouse repo; never hand-edit.
