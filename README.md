# Hamlog AI Drama Pipeline for Codex

Codex용 한국어 AI 드라마 제작 플러그인입니다. 스토리 아이디어를 각본, 컷 프롬프트, 영상 제작 운영, QC와 조립 단계까지 이어갈 수 있도록 4개의 Codex 스킬을 묶었습니다.

English version: [English](#english)

## 포함된 스킬

- `screenplay-pipeline`: 한국어 트리트먼트, 씬별 대본, 밈 패러디, IP 체크리스트, DOCX 변환 워크플로
- `seedance-cut-prompt`: 각본 씬을 Seedance 2.0용 컷 프롬프트로 변환
- `ai-character-drama`: 캐릭터 일관성을 유지하는 멀티샷 AI 드라마 제작 워크플로
- `drama-ops`: 후보 보드, QC 프레임 시트, 리테이크 비교, ffmpeg 조립 스크립트

## 설치

Codex에서 아래 명령어를 순서대로 실행하세요.

1단계: 이 GitHub 저장소를 Codex 마켓플레이스로 추가합니다.

```bash
codex plugin marketplace add hamlog-ai/codex-ai-drama-pipeline --ref main
```

2단계: 플러그인을 설치합니다.

```bash
codex plugin add hamlog-ai-drama-pipeline@hamlog-ai
```

설치 후 새 Codex 스레드를 시작하면 스킬이 로드됩니다.

## 업데이트

최신 버전을 받으려면 아래 명령어를 순서대로 실행하세요.

1단계: 마켓플레이스 스냅샷을 갱신합니다.

```bash
codex plugin marketplace upgrade hamlog-ai
```

2단계: 플러그인을 다시 설치합니다.

```bash
codex plugin add hamlog-ai-drama-pipeline@hamlog-ai
```

## 구성

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

일부 워크플로는 단계에 따라 Higgsfield, ElevenLabs, Suno, ffmpeg, Node.js, Python 같은 외부 제작 도구를 사용할 수 있습니다. 각 스킬 문서가 해당 단계에서 필요한 도구를 안내합니다.

## 라이선스

CC BY-ND 4.0입니다. 자유롭게 사용하고 원본 그대로 공유할 수 있지만, 출처 `햄로그 (Hamlog)`를 표기해야 하며 수정한 버전을 재배포할 수 없습니다. 자세한 내용은 [LICENSE](LICENSE)를 확인하세요.

## English

Hamlog AI Drama Pipeline for Codex is a Codex plugin for Korean AI drama production. It bundles four Codex skills that move a story idea through screenplay writing, cut prompt generation, production operations, QC, and assembly.

## Included Skills

- `screenplay-pipeline`: Korean treatment, scene script, meme parody, IP checklist, and DOCX export workflow
- `seedance-cut-prompt`: screenplay scene to Seedance 2.0 cut prompt conversion
- `ai-character-drama`: consistent multi-shot character video production workflow
- `drama-ops`: candidate boards, QC frame sheets, retake comparison, and ffmpeg assembly scripts

## Install

Run these commands in Codex.

Step 1: add this GitHub repository as a Codex marketplace.

```bash
codex plugin marketplace add hamlog-ai/codex-ai-drama-pipeline --ref main
```

Step 2: install the plugin.

```bash
codex plugin add hamlog-ai-drama-pipeline@hamlog-ai
```

Start a new Codex thread after installing so Codex can load the new skills.

## Update

Run these commands to refresh the marketplace snapshot and reinstall the plugin.

Step 1: refresh the marketplace snapshot.

```bash
codex plugin marketplace upgrade hamlog-ai
```

Step 2: reinstall the plugin.

```bash
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

CC BY-ND 4.0. You may use and share the original material with attribution to `햄로그 (Hamlog)`, but you may not redistribute modified versions. See [LICENSE](LICENSE) for details.
