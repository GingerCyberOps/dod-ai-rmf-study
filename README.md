[README.md](https://github.com/user-attachments/files/30391677/README.md)
# DoD AI & RMF Study Quiz

A free, self-contained study project for DoD and Army cybersecurity compliance professionals (ISSOs, ISSMs, assessors, and anyone working RMF packages). It covers the NIST AI Risk Management Framework, current DoD and Army AI policy, and the core RMF/ISSO body of knowledge: NIST SP 800-37, SP 800-53, eMASS practice, POA&Ms, STIGs, and CUI.

**Contents**

| File | What it is |
|---|---|
| `index.html` | Interactive 106-question quiz. One file, no dependencies, works offline and on mobile. |
| `study-guide.md` | The companion study guide, organized to match the quiz topics, with primary source links. |
| `data/questions.json` | The full question bank in JSON if you want to build your own tools on it. |

## Features

- Study Mode (instant feedback with explanation and primary source per question) and Exam Mode (graded review at the end)
- Filter by topic, choose 10/25/50/all questions, shuffled questions and answer positions every run
- Per-topic score breakdown so you know exactly what to restudy
- Every question cites a public primary source (NIST, DoD issuances, Army guidance)

## Run it

Open `index.html` in any browser. That is the whole install.

### Host it on GitHub Pages

1. Create a new GitHub repository and upload these files.
2. Repository Settings, then Pages, then under "Build and deployment" choose "Deploy from a branch," select `main` and `/ (root)`, and save.
3. Your quiz will be live at `https://<your-username>.github.io/<repo-name>/` within a few minutes.

## Topic coverage (106 questions)

NIST AI RMF (14) · Generative AI risks, NIST AI 600-1 (8) · DoD AI policy (14) · Army AI policy (8) · RMF process, SP 800-37 and DoDI 8510.01 (16) · Security controls, SP 800-53 (12) · eMASS and POA&M practice (10) · STIGs and scanning (8) · CUI (6) · DoD cyber policy and cloud impact levels (4) · NAF IT, DoDI 1015.16 (6)

## Updating the questions

Questions live in a `QUESTIONS` array near the top of the `<script>` block in `index.html` (and in `data/questions.json`). Each entry:

```json
{
  "id": "A1",
  "topic": "NIST AI RMF",
  "type": "mc",
  "q": "Question text",
  "options": ["A", "B", "C", "D"],
  "answer": 1,
  "explain": "Why the answer is right",
  "source": "Source name",
  "url": "https://primary-source-link"
}
```

`answer` is the zero-based index into `options`. The app shuffles option order at runtime.

## Disclaimer

This is an unofficial personal study project built entirely from publicly available policy and guidance. It is not an official product of, or endorsed by, the U.S. Government, the Department of War/Defense, or the U.S. Army. It contains no CUI. Policy changes; verify anything you rely on against the cited primary source. Content current as of July 2026.

## License

MIT for the code. Question text and study guide released under CC BY 4.0; attribution appreciated.
