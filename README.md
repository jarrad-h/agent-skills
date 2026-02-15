# Agent Skills

Personal collection of [Agent Skills](https://agentskills.io) for use with Claude and other compatible AI agents.

## Skills

### data-upskilling
A personalised learning coach for building capabilities in AI/ML, Azure cloud data management, and data engineering. Covers structured learning plans, concept teaching, practice exercises, certification guidance, and progress tracking.

**Domains covered:**
- Artificial Intelligence & Machine Learning
- Azure Cloud Data Management (Data Factory, Synapse, Databricks, Azure ML, etc.)
- Supporting data disciplines (data engineering, analysis, DataOps)

### sme-due-diligence
Australian SME due diligence and market research agent. Takes a business name, ABN, and/or owner/director name as input and produces a structured intelligence report consolidating public records, financial information, legal history, news, and risk indicators.

**Report sections:**
- Executive Summary & Business Identity (ABN, ACN, entity type, status, GST)
- Current State Assessment (synthesised analytical overview)
- Business Timeline (reverse-chronological key events)
- Director/Owner Profiles (associated entities with status, enforcement history)
- Financial Overview (best-effort from public sources)
- Legal & Court Records (Federal/state courts, ASIC enforcement, insolvency notices)
- Risk Indicators (red flags, positive signals, information gaps)

**Data sources:** ABR, ASIC, Federal & state courts, Commonwealth Gazette, business news (AFR, SmartCompany), LinkedIn, PPSR

## Usage

### Claude.ai
Upload the skill folder via the Claude.ai interface. See [Using skills in Claude](https://support.claude.com/en/articles/12512180-using-skills-in-claude).

### Claude Code
Register this repo as a plugin marketplace or reference skills directly.

### Other compatible agents
Any agent supporting the [Agent Skills standard](https://agentskills.io) can use these skills.

## Structure

Each skill follows the Agent Skills specification:

```
skill-name/
├── SKILL.md           # Required: instructions + metadata
├── references/        # Optional: supporting documentation
├── scripts/           # Optional: executable code
└── assets/            # Optional: templates and resources
```

## License

Apache 2.0
