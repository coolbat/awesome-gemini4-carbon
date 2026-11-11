# Contributing

All public Gemini 4 Carbon case types are welcome, including unsuccessful attempts and practical limitations. Do not submit private material or mirror original media.

## Evidence checklist

1. Link a public, traceable original source. Confirm explicit **Gemini 4 Carbon** attribution; do not infer the model from a repository title, generic brand name, rumor or neighboring version.
2. Open the exact input source and the corresponding visible result. A prompt may be in the same thread, an author reply, or an accessible linked run record. Supply both URLs.
3. Qualified requires the complete author-disclosed original user input, not a new imitation, summary, unfilled template, generic skill, “prompt below” claim or comment-gated giveaway. Identify supplied files, reference images/audio, skills, project documents, rendering tools and mixed-model dependencies.
4. If any requirement is unresolved, set qualified to false, verification to needs_prompt, and explain the precise gap. If a discovery-index entry has not been opened, use not_opened and keep it in a separate discovery backlog, never the Qualified table/count. Do not contact authors to unlock prompts.
5. Check duplicates by source URL, media/work identity and earlier reposts. A distinct new result using the same prompt can be separate; a repost cannot. A comparison contributes at most one result for the target model.
6. Use a descriptive, non-promotional title. Preserve original-author credit and borrowed-prompt credit. Do not endorse cost, time, “zero bugs”, benchmark scores, physics or historical accuracy without separate evidence.
7. Never copy media into this repository. Link originals. Public accessibility does not grant copyright permissions. Do not paste full third-party prompts into a CC0 dataset without appropriate permission/license; link to them instead.

## PR workflow

- Fork the repository and create a focused branch.
- Append one record to data/cases.json, using stable IDs; do not renumber existing records.
- Add/update the matching type and evidence-tier table in README.md, including counts.
- In the PR description, list which URLs you actually opened, the model/version evidence, where the original input appears, visible-result evidence, dependencies, duplicate check and any limitations. No API keys, private files or login-only screenshots.
- Validate JSON: `python3 -m json.tool data/cases.json > /dev/null`. Check link syntax and that JSON/table IDs and Qualified counts match.
- Maintainers review source provenance; acceptance is not independent visual or functional certification.

## Record format

Required keys: id, title, author, author_url, created_at_shanghai, type, source_url, prompt_url, result_url, model, qualified, dependencies, notes, verification.

- `author`, `author_url`, `created_at_shanghai` and `prompt_url` may be null when not established; explain the gap. Never invent an identity, URL or date.
- Precise dates use ISO 8601 with +08:00 (Asia/Shanghai). Convert UTC/Z first. Store date-only labels separately as `source_date_label` with timezone uncertainty; do not guess a precise timestamp. For run times add `created_at_basis`.
- type: video, animation, game, interactive-slider, web-ui, 3d, music-notation, other. Choose the work’s primary type, not merely its recording format.
- verification: source_verified, needs_prompt, not_opened. Qualified must be true only with source_verified and non-null original-input/result URLs.
- dependencies is an array. Empty means none documented, not proof of no dependency.
- Optional fields can clarify evidence basis, verification date, source date label and duplicate relations.

By contributing your own descriptions and database additions, you agree to dedicate those original contributions under CC0-1.0. This does not change rights in the linked authors’ prompts, media, software or trademarks.
