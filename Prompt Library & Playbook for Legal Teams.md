---
# ⚖️ AI Prompt Library & Playbook for Legal Teams

## 📌 Table of Contents
- How to Use
- Core Prompt Template
- Contract Review & Drafting
- Legal Research & Case Analysis
- Summarization & Document Intelligence
- Client Communication
- Policy & Compliance
- Due Diligence
- Structured Output Add-ons
- Weak vs Strong Prompts
- Prompt Refinement Workflow

---

# 🎯 How to Use

Every effective prompt follows this structure:

ROLE → CONTEXT → TASK → CONSTRAINTS → OUTPUT FORMAT

**Best Practices:**
- Always include jurisdiction and client context  
- Be explicit about output format  
- Add constraints to improve precision  
- Treat prompts like reusable templates  

---

# 🧱 Core Prompt Template

## Template
```markdown
Act as a [ROLE].

Context:
[Background, client, jurisdiction]

Task:
[What needs to be done]

Constraints:
[Limits, tone, exclusions]

Output Format:
[Structure]
````

## Example

```markdown
Act as a senior corporate lawyer in India.

Context:
We represent a mid-sized SaaS company entering into a vendor agreement with a US-based cloud provider. The agreement is governed by Indian law.

Task:
Identify key legal and commercial risks in the agreement.

Constraints:
Focus on liability, indemnity, and data protection risks. Avoid generic explanations.

Output Format:
Table:
- Clause
- Risk
- Risk Level
- Suggested Fix
```

---

# 📄 Contract Review & Drafting

## Contract Risk Review

### Example

```markdown
Act as a senior commercial counsel.

Context:
Client is an Indian fintech startup entering a payment processing agreement with a large bank.

Task:
Identify:
- High-risk clauses
- Regulatory exposure
- One-sided obligations

Constraints:
Focus on RBI compliance, liability caps, and termination.

Output Format:
Table:
- Clause
- Risk
- Risk Level
- Suggested Revision
```

---

## NDA Review (IP-Focused)

```markdown
Act as a senior commercial counsel representing a startup.

Context:
We are sharing proprietary AI models with an enterprise client.

Task:
Identify clauses that:
- Expose IP risk
- Allow misuse of confidential information
- Create long-term obligations

Focus Areas:
- Confidential Information definition
- Residual rights
- Term

Output Format:
- Clause
- Risk
- Suggested Redline
```

---

## Clause Drafting (Zero-Shot)

```markdown
Draft a limitation of liability clause for a SaaS agreement where liability is capped at 12 months of fees, excluding fraud and wilful misconduct.
```

---

## Clause Drafting (Few-Shot)

```markdown
Examples:
Clause A: Liability capped at last 6 months fees  
Clause B: Liability capped at annual value with fraud exception  
Clause C: Liability capped with IP carve-out  

Using the same style, draft a clause for a cloud services agreement with a 12-month cap.
```

---

# 🔍 Legal Research & Case Analysis

## Case Law Summarization (IRAC)

```markdown
Act as a litigation associate.

Context:
We represent a landlord in a lease dispute involving force majeure during COVID-19.

Task:
Summarize using IRAC:
- Issue
- Rule
- Application
- Conclusion

Focus:
Force majeure and rent obligations

Constraints:
Ignore procedural history
```

---

## Chain-of-Thought Legal Analysis

```markdown
Analyze enforceability of a non-compete clause in India.

Think step by step:
1. Identify governing law
2. Evaluate reasonableness
3. Apply facts
4. Conclude
```

---

## Legal Research Query

```markdown
Act as a legal research analyst.

Task:
Find Indian case law on arbitration clauses in unstamped agreements.

Constraints:
Focus on Supreme Court and recent rulings

Output:
- Case Name
- Principle
- Relevance
```

---

# 🧾 Summarization & Document Intelligence

## Contract Summary

```markdown
Summarize this SaaS agreement in 5 bullet points covering:
- Payment terms
- Obligations
- Termination
- Liability
- Data protection
```

---

## Judgment Summary

```markdown
Act as a legal analyst.

Task:
Summarize into:
- Key issue
- Holding
- Practical takeaway

Format:
Bullet points
```

---

# 📧 Client Communication

## Explain Legal Concept

```markdown
Act as a lawyer in India.

Context:
Client is a startup founder unfamiliar with legal processes.

Task:
Explain "legal due diligence" in a funding round.

Constraints:
- Simple language
- Reassuring tone
- Avoid jargon

Output:
Email format
```

---

## Status Update Email

```markdown
Draft a client update email.

Context:
Initial contract review is complete.

Include:
- Summary of findings
- Key risks
- Next steps

Tone:
Professional and concise
```

---

# 🏢 Policy & Compliance

## AI Policy Drafting

```markdown
Act as a Chief Compliance Officer.

Context:
Healthcare startup handling sensitive data.

Task:
Draft an AI usage policy.

Include:
- No PII in public AI tools
- Approval workflow
- Monitoring

Format:
- Headings
- Bullet rules
- Acknowledgement section
```

---

## Compliance Gap Analysis

```markdown
Compare GDPR requirements with internal policy.

Output:
- Requirement
- Current Policy
- Gap
- Recommendation
```

---

# 📊 Due Diligence

## Contract Review at Scale

```markdown
Act as a due diligence lawyer.

Context:
Reviewing contracts in an acquisition.

Task:
- Identify risks
- Flag non-standard clauses

Output:
Summary report with risk categories
```

---

## Checklist-Based DD

```markdown
Checklist:
- Change of control
- Termination
- Assignment

Task:
Audit against contract.

Output:
- Item
- Status
- Notes
```

---

# 🧠 Structured Output Add-ons

## Table Format

```markdown
Return:
- Issue
- Clause Reference
- Risk Level
- Recommendation
```

## Jurisdiction Constraint

```markdown
Apply only Indian law.
Flag if outcome differs in other jurisdictions.
```

## Tone Control

```markdown
Use plain English suitable for clients.
```

---

# 🚫 Weak vs Strong Prompts

## ❌ Weak

```markdown
Review this NDA.
```

## ✅ Strong

```markdown
Act as a senior commercial counsel.

Context:
Startup sharing IP with enterprise partner.

Task:
Identify IP and liability risks.

Output:
Structured risk table
```

---

# 🔁 Prompt Refinement Workflow

```markdown
1. Draft prompt
2. Test on multiple scenarios
3. Evaluate:
   - Accuracy
   - Completeness
   - Risk coverage
4. Refine:
   - Add constraints
   - Improve structure
   - Include examples
```
