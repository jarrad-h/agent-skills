# Agent Skills

Personal collection of [Agent Skills](https://agentskills.io) for use with Claude and other compatible AI agents.

## Skills

### data-upskilling
A personalised learning coach for building capabilities in AI/ML, Azure cloud data management, and data engineering. Covers structured learning plans, concept teaching, practice exercises, certification guidance, and progress tracking.

**Domains covered:**
- Artificial Intelligence & Machine Learning
- Azure Cloud Data Management (Data Factory, Synapse, Databricks, Azure ML, etc.)
- Supporting data disciplines (data engineering, analysis, DataOps)

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
