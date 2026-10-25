# Clay cloud render worker (public shell)

Public GitHub-hosted runner shell for the private Clay World Kit payload.

- Input:  `clay-payload.tar.gz.enc` (AES-256-CBC, pbkdf2 200k; key only in the
  `CLAY_PAYLOAD_KEY` repository secret and the controller's local key file).
- Output: `renders.tar.gz.enc` workflow artifact, encrypted with the same key.
- No kit source, render or key is stored in this repository.

Dispatch through the controller: `python3 tools/cloud_sync.py run --mode matrix`
