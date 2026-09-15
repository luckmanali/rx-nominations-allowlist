# rx-nominations-allowlist

The signed list of computers approved to run RxWeb Nominations.

- `allowlist.json` — the approved computers (scrambled IDs and a label for each) and the date the list expires.
- `allowlist.json.sig` — an Ed25519 signature over the exact bytes of `allowlist.json`.

**Do not edit these files by hand.** Any change, even a single space, breaks the signature. The app then
rejects the whole list, which locks out every computer. The list is maintained with `tools/allowlist.mjs`
in the app's own repository.
