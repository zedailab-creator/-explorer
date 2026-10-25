# Explorer v2 — Update Pack

Security-first Explorer skill for ChatGPT plugins (English).

## Contents
- `skills/explorer/SKILL.md` — core behavior (valid frontmatter: name, description, license, allowed-tools, metadata)
- `skills/explorer/references/prompts.md` — 20 prompt paths
- `skills/explorer/references/starters.md` — 3 starter prompts
- `.codex-plugin/plugin.json.template` — manifest TEMPLATE (verify key names against the current OpenAI docs / your downloaded ZIP)
- `QA-TESTS.md` — security and behavior tests (run before every upload)

## How to update the installed plugin
1. In ChatGPT: plugin page -> ... -> **Download plugin ZIP** (backup of the current version).
2. Unzip it. Compare its manifest with `plugin.json.template`; keep YOUR manifest's real key names and only change the version and description.
3. Replace `skills/explorer/SKILL.md` and the `references/` files with the ones in this folder.
4. Bump the version (e.g. 1.0.2 -> 1.1.0).
5. Zip the plugin folder (the manifest must be at the expected location inside the ZIP, same as in the original ZIP).
6. ... -> **Upload new version**.
7. Run `QA-TESTS.md`.

## Before publishing publicly
- Fill in Website, Privacy Policy and Terms URLs (the plugin page currently shows Website: Unavailable).
- Do not claim "100% secure". Use: "Security-first, layered defenses, prompt-injection hardened."
