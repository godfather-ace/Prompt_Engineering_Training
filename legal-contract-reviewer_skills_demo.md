# ⚖️ legal-contract-reviewer

> A Claude Skill for reviewing contracts, flagging risks, and surfacing key terms — in plain English.

![Claude Skill](https://img.shields.io/badge/Claude-Skill-blue?logo=anthropic)
![License](https://img.shields.io/badge/license-MIT-green)
![Use Case](https://img.shields.io/badge/use--case-Legal-purple)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

---

## 📋 Overview

`legal-contract-reviewer` is a Claude Skill — a structured Markdown instruction file (`SKILL.md`) that teaches Claude how to systematically review legal contracts and agreements.

It is **not** a legal advice tool. It is a structured reading assistant that helps users understand what they're signing before they talk to a lawyer.

### What it does

- 📄 Identifies document type and reviewing party
- 🔑 Extracts and plainly explains key terms
- 🚩 Flags risky, vague, or one-sided clauses
- ⚠️ Highlights non-standard or unusual language
- ❓ Generates targeted questions to bring to an attorney
- 🛡️ Always appends a legal disclaimer

---

## 🗂️ Repository Structure

```
legal-contract-reviewer/
├── SKILL.md          # The Claude Skill instruction file
├── README.md         # This file
├── examples/
│   ├── nda-review.md         # Example output: NDA review
│   ├── employment-review.md  # Example output: Employment contract
│   └── saas-review.md        # Example output: SaaS agreement
└── LICENSE
```

---

## 🚀 Getting Started

### 1. Add the Skill to your Claude environment

Place `SKILL.md` in your skills directory, typically:

```
/mnt/skills/user/legal-contract-reviewer/SKILL.md
```

### 2. Register it in your system prompt or skill loader

```xml
<available_skills>
  <skill>
    <name>legal-contract-reviewer</name>
    <description>
      Use this skill when the user asks to review, summarize, or flag issues 
      in a contract, agreement, NDA, or legal clause.
    </description>
    <location>/mnt/skills/user/legal-contract-reviewer/SKILL.md</location>
  </skill>
</available_skills>
```

### 3. Trigger it naturally in conversation

```
"Can you review this NDA and flag anything unusual?"
"I need to check this employment contract before I sign."
"What are the risks in this SaaS agreement?"
```

---

## 📄 The Skill File

The core of this repo is `SKILL.md`. It instructs Claude to:

| Step | Action |
|------|--------|
| **Identify** | Document type, user's role, and review scope |
| **Summarize** | Key terms in plain English |
| **Flag** | Risky, vague, or one-sided clauses |
| **Highlight** | Non-standard language vs. industry norms |
| **Recommend** | 3–5 questions to bring to an attorney |
| **Disclaim** | Always append the legal disclaimer |

### Output Format (every review follows this structure)

```
📄 DOCUMENT TYPE: Non-Disclosure Agreement
👤 REVIEWING AS: Employee / Recipient party

── KEY TERMS ──────────────────────────────
• Term: 2 years from signing
• Scope: All proprietary information shared during partnership
• Governing Law: California

── RISK FLAGS 🚩 ───────────────────────────
1. [Clause] — Plain English explanation of the risk
2. [Clause] — Plain English explanation of the risk

── UNUSUAL CLAUSES ─────────────────────────
• [Clause] is broader than standard — typically X, here it covers Y.

── QUESTIONS FOR YOUR ATTORNEY ─────────────
1. Does the non-compete clause hold in your state?
2. Is the indemnification clause mutual or one-sided?

⚠️  DISCLAIMER: This is not legal advice. Always consult a
qualified attorney before signing any legal document.
```

---

## 🛡️ Safety & Limitations

This skill is designed with guardrails that Claude strictly follows:

| ✅ Claude Will | ❌ Claude Won't |
|----------------|----------------|
| Flag potentially risky clauses | Rule on enforceability |
| Summarize terms in plain English | Give jurisdiction-specific legal opinions |
| Suggest questions for your lawyer | Recommend signing or not signing |
| Note missing standard clauses | Replace a qualified attorney |
| Always include a disclaimer | Skip the disclaimer under any circumstance |

---

## 💡 Example Triggers

The skill activates on prompts like:

- *"Review this contract and flag any risks"*
- *"Can you check this NDA?"*
- *"Summarize the key terms of this employment agreement"*
- *"Is there anything unusual in this vendor contract?"*
- *"What questions should I ask my lawyer about this lease?"*

---

## 📦 Supported Document Types

- Non-Disclosure Agreements (NDAs)
- Employment Contracts
- Freelance / Consulting Agreements
- SaaS & Software License Agreements
- Vendor & Supplier Contracts
- Lease Agreements
- Partnership Agreements
- Terms of Service

---
