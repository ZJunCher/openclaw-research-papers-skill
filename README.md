# OpenClaw Research Papers Skill

An OpenClaw AgentSkill for finding, ranking, and summarizing academic papers with OpenAlex.

This skill is optimized for AI + neuroimaging research workflows, including dynamic functional brain networks, rs-fMRI/fMRI, graph neural networks, spatiotemporal attention, Alzheimer's disease, MCI, Parkinson's disease, and neurodegenerative disease classification.

## What it does

- Search academic papers by topic, author, title, or DOI.
- Expand short Chinese/English research prompts into stronger English academic queries.
- Look up DOI metadata through OpenAlex.
- Inspect citation chains around a paper.
- Discover legal open-access URLs and PDFs when available.
- Generate structured Markdown literature reviews.
- Optionally stage long review files for QQBot delivery.

## Files

```text
.
├── SKILL.md
└── scripts/
    └── scholar-search.py
```

## Requirements

- OpenClaw with AgentSkill support
- Python 3
- `requests` Python package
- Internet access to OpenAlex

OpenAlex does not require an API key. You may optionally set `OPENALEX_MAILTO` for polite API usage.

## Example usage

Search papers:

```bash
python scripts/scholar-search.py search "dynamic functional brain network Alzheimer's disease graph neural network" --limit 10 --years 2020-2026
```

Look up a DOI:

```bash
python scripts/scholar-search.py doi "10.1038/s41586-021-03819-2"
```

Generate a literature review:

```bash
python scripts/scholar-search.py review "dynamic functional brain networks in Alzheimer's disease" --papers 30 --years 2020-2026 --output review.md
```

## ClawHub

Published on ClawHub as:

https://clawhub.ai/zjuncher/research-papers

Install with ClawHub:

```bash
clawhub install research-papers
```

## Notes

- This skill uses OpenAlex and legal open-access metadata.
- It does not bypass paywalls.
- Output defaults to Chinese explanations when the user asks in Chinese.

## License

MIT-0
