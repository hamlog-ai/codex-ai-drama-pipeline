# Hamlog AI Drama Pipeline for Codex

Codex marketplace package for Korean AI drama production. It bundles four skills:

- `screenplay-pipeline`: Korean treatment, scene script, meme parody, IP checklist, and DOCX export workflow
- `seedance-cut-prompt`: screenplay scene to Seedance 2.0 cut prompt conversion
- `ai-character-drama`: consistent multi-shot character video production workflow
- `drama-ops`: candidate boards, QC frame sheets, retake comparison, and ffmpeg assembly scripts

## Install

Add this GitHub repository as a Codex marketplace, then install the plugin:

```bash
codex plugin marketplace add hamlog-ai/codex-ai-drama-pipeline --ref main
codex plugin add hamlog-ai-drama-pipeline@hamlog-ai
```

Start a new Codex thread after installing so Codex can load the new skills.

## Update

Refresh the marketplace snapshot and reinstall:

```bash
codex plugin marketplace upgrade hamlog-ai
codex plugin add hamlog-ai-drama-pipeline@hamlog-ai
```

## Contents

```text
.agents/plugins/marketplace.json
plugins/hamlog-ai-drama-pipeline/
  .codex-plugin/plugin.json
  skills/
    ai-character-drama/
    drama-ops/
    screenplay-pipeline/
    seedance-cut-prompt/
```

Some workflows expect external creative-production tools such as Higgsfield, ElevenLabs, Suno, ffmpeg, Node.js, and Python depending on the step being run. The skills describe the required tool for each stage.

## License

MIT
