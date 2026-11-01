# Sweet Security Competitive Intelligence Workflow

A competitive intelligence system I built with Claude, working as if I were a product marketing manager at Sweet Security, tracking Upwind.

## Demo

[▶ Watch the demo](PASTE-VIDEO-LINK-HERE)

## What it does

- **Research workflow:** a Claude Project that researches Sweet Security and Upwind weekly, monthly and quarterly from public sources only, and feeds a Master CI Brief.
- **CI interface:** a page built on the Master CI Brief with three tabs:
  - **Battle card:** objection handling, positioning, strengths, friction, claims to avoid and discovery questions.
  - **Ask the CI:** a chat that answers only from the competitive intel, asking follow-up questions based on the person's role.
  - **Decision board:** recommendations with evidence, owner, confidence and a success measure.
- **Auto-update:** when the Master CI Brief changes, the battle card and decision board rebuild themselves.

## How it works

- **Source of truth:** one Master CI Brief (Google Sheet).
- **Evidence rules:** every claim is labelled FACT, INTERPRETATION or HYPOTHESIS. No invented proof, no attacks on competitors.
- **Tools:** Claude Pro, Claude Projects, skills, artifacts and the Google Sheets connector. $0 extra spend, 2–3 hours a week.

## What's in this repo

| Folder | What it is |
|---|---|
| `skills/ci-battle-card-interface` | Skill for answering from the CI and building the interface |
| `skills/ci-research-workflow` | Skill for the research workflow |

## Limitations

Public data only, so product, pricing and strategy recommendations are labelled HYPOTHESIS.

## About me

[Your name] · [LinkedIn link] · [Portfolio link]
