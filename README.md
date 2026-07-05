# AI Agent Skills Collection

Production-ready AI agent skills for autonomous coding, debugging, architecture design, and DevOps automation.

**Build with:** Claude Sonnet 4.6 (1M context) + Opus 4.8 (hard tasks)
**Deploy on:** Cloudflare Workers, Node.js, Python, or self-hosted
**Use cases:** eimOS IDE, DecentralizedCommerce, autonomous development agents

## 🚀 Quick Start

```bash
# Clone the skills collection
git clone https://github.com/FaustinoMFeca/DecentralizedCommerce.git
cd DecentralizedCommerce

# Use a skill in your project
cat skills/agent-coder/SKILL.md
```

Paste the `SKILL.md` content into your Claude conversation or system prompt to activate the agent skill.

## 📚 Skills Directory

### Tier 1: Core Agent Skills (Recommended)

- **agent-coder** — Generates production code from natural language requirements
- **agent-debugger** — Systematic bug diagnosis and fix recommendations
- **agent-architect** — System design, data modeling, architecture decisions
- **agent-reviewer** — Code review, security, performance analysis
- **agent-refactor** — Multi-file refactoring and modernization

### Tier 2: Specialized Agent Skills

- **agent-test-writer** — Generate comprehensive test suites
- **agent-devops** — Infrastructure-as-code and deployment automation
- **agent-data-engineer** — ETL pipelines and data transformation
- **agent-security-auditor** — Vulnerability scanning and threat modeling
- **agent-docs-generator** — Auto-generate API docs and changelogs

## ✨ Features

✅ **Production-ready** — Built from industry best practices
✅ **Multi-model support** — Works with Claude Sonnet 4.6 and Opus 4.8
✅ **Integrated examples** — Real-world use cases included
✅ **Token-efficient** — Optimized context window usage
✅ **Extensible** — Easy to fork and customize

## 📖 Usage

### In Claude.ai

1. Open https://claude.ai
2. Start a new conversation
3. Paste the contents of a `SKILL.md` file
4. Start prompting the agent

### Via API

```python
import anthropic

client = anthropic.Anthropic()
with open('skills/agent-coder/SKILL.md') as f:
    skill = f.read()

response = client.messages.create(
    model="claude-opus-4-8",
    max_tokens=4096,
    system=skill,
    messages=[{
        "role": "user",
        "content": "Build a FastAPI microservice with JWT authentication"
    }]
)
print(response.content[0].text)
```

## 🎯 Model Selection

| Task | Model | Context | Notes |
|------|-------|---------|-------|
| Simple scaffolding | **Sonnet 4.6** | 200K | Default, fast, cost-effective |
| Large codebases | **Sonnet 4.6** | 1M | Full project context |
| Complex reasoning | **Opus 4.8** | 1M | Best for architecture, hard bugs |
| Multi-repo refactor | **Opus 4.8** | 1M | Maximum capability |

## 📊 Token Budget

- **Skill definition:** 800–1,200 tokens
- **Code generation (small):** 500–1,500 tokens
- **Code review (medium codebase):** 2,000–4,000 tokens
- **Architecture (large system):** 3,000–8,000 tokens

## 🔗 Integration with eimOS

These agent skills power the eimOS IDE:

- Code generation from natural language (agent-coder)
- Live debugging of runtime errors (agent-debugger)
- Architecture proposals for new features (agent-architect)
- Automated code review on every change (agent-reviewer)
- Test generation for new functions (agent-test-writer)

## 📄 License

MIT — Use freely in commercial and personal projects.

---

**Built for:** eimOS, DecentralizedCommerce, autonomous AI agents
**Updated:** July 2026
