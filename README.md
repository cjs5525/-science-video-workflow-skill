# Science Video Workflow

[简体中文](README.zh-CN.md) · English

A reusable Codex skill for turning a science question into a researched script, edited video, cover, bilingual YouTube upload package, and chapter-based short clips. It also supports resuming an episode from its recorded progress.

Adapted from a real Chinese-language science production workflow. Instructions and production templates are in Chinese; this repository provides English and Chinese introductions.

**Xiaoyun character animation is excluded.** The second voice can still ask questions through audio. Scientific diagrams and explanatory motion graphics remain part of production.

## What it covers

| Stage | Deliverables |
|---|---|
| 0 · Setup | Episode rules, settings, progress and version references |
| 1 · Research | Core question, explanation chain, claims and source boundaries |
| 2 · Script | Natural dialogue, separate spoken/production notes, storyboard and recording draft approval |
| 3 · Preparation | Authorized voiceover, explanatory graphics, downloaded and reviewed stock footage, license records and preview selections |
| Recording | User records; the agent registers source files and recording-script version |
| 4 · Rough cut | Complete lines without failed takes or accidental repetitions; usable listening loudness |
| 5 · Final timeline | Measured audio, dialogue, chapter cards and frame-based visual coverage |
| 6 · Finishing | Clean video master, optional separate subtitles, technical/visual/listening checks |
| 7 · Covers | Selected aspect ratios and languages, final PNG files |
| 8 · Upload package | Traditional Chinese title, full description, chapters, Tags/Hashtags and settings guidance; English title and full description |
| 9 · Clips | Actual clips matched to individual copy, a shared series premise and a verified route to the long video |
| 10 · Archive | An independent final delivery set and an explicitly approved cleanup inventory |

## Key production rules

- Prepare sufficient relevant, downloaded, viewable and license-recorded live-action B-roll **before recording**, with alternate selections. Photos do not count as live-action footage.
- Keep source, rough-cut and final-video times distinct. Derive subtitles and published chapters from the current final timeline.
- Preserve the source workflow's configurable visual style: live-action B-roll `R ≥ 35%`, and `R + D ≤ 65%`, where `D` is explanatory motion graphics. If `R = 35%` exactly, `D = 30%`; if `R > 35%`, `D` may be below 30%. Classify by the main information carrier, without double counting, and use exact frame counts. These are project defaults, not platform requirements.
- Deliver a master without burned-in speech captions by default. Optional subtitles use `.zh_CN.srt`, `.zh_TW.srt` and `.en_US.srt` suffixes, with the version before the language suffix.
- Separate successful decoding and loudness measurements from actual visual inspection and listening. Unchecked work stays pending.
- Treat upload copy as a required artifact. Subtitles alone do not complete the upload package.
- Preserve source recordings and prior versions during production. Require approval of an exact inventory before cleanup; uploading a video does not authorize deletion.

## Install locally

Copy only the [`science-video-workflow/`](science-video-workflow/) folder into one of these locations, preserving its name:

- Project scope: `<your-project>/.agents/skills/science-video-workflow/`
- User scope: `~/.agents/skills/science-video-workflow/`

The resulting folder must contain `SKILL.md` directly. Follow your workspace's rules before creating directories, and avoid overwriting a skill with the same name. Codex discovers local skills automatically; restart it if the skill does not appear. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for local discovery and installation guidance, checked on October 31, 2026.

Ask the built-in skill installer to install the `science-video-workflow` subfolder from [cjs5525/-science-video-workflow-skill](https://github.com/cjs5525/-science-video-workflow-skill).

## Use

Start an episode:

```text
Use $science-video-workflow to make a science video about “Why do satellites fall back to Earth?” Start with research and keep me informed of the current stage. Use a voice-only second speaker; do not create character animation.
```

Resume an episode:

```text
Use $science-video-workflow to continue this episode. Read its AGENTS.md and 制作进度.md, verify the current files and approvals, and resume from the earliest unfinished dependency.
```

Provide a core question, an existing script or a recording path. The agent maintains the production records; a transcript or cut-point spreadsheet is not required from the user.

## Requirements and boundaries

This is an instruction-and-template skill, not a bundled video editing application. Actual production requires suitable tools for research, transcription, media inspection, rendering, and any requested TTS or image generation. Existing tools and authorized services should be reused; missing capabilities must be reported rather than claimed complete.

The package contains no credentials, paid-service accounts, media, branded assets, private voice configuration or machine-specific paths. Voice-only dialogue does not grant permission to send original recordings to an external transcription service. The skill does not install global dependencies, alter secrets or CI/CD settings, automatically publish content, or silently delete files.

Character lip sync, breathing, gestures, appearance windows, transparent character videos and character compositing are outside the skill. Existing character assets are not deleted. Adding character animation later requires a separate scope decision.

## Repository layout

```text
README.md
README.zh-CN.md
AGENTS.md
VALIDATION.md
LICENSE
science-video-workflow/
  AGENTS.md
  SKILL.md
  LICENSE
  agents/openai.yaml
  references/
    research-and-script.md
    media-production.md
    publishing.md
    archive-and-changes.md
  assets/
    episode-agents.md
    progress.md
    delivery.md
```

References load by stage. Templates are starting points, not completed episode deliverables. See [VALIDATION.md](VALIDATION.md) for the actual validation scope and GitHub upload status.

## License

[MIT License](LICENSE), selected by the repository owner. A copy is included in the installable skill folder.
