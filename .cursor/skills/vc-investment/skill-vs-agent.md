# Skill vs Agent: What to Define First

Use this to separate **what the skill is** from **what the agent does**, and to decide what to nail down first.

---

## Definitions (in this project)

| Term | What it is | Where it lives |
|------|------------|----------------|
| **Skill** | The **what**: criteria, taxonomy, and instructions for assessing something (e.g. track record). The *content layer* — what “good” looks like, what to check, what to output. | SKILL.md, track-record.md, western-lp-expectations.md |
| **Agent** | The **how**: the Capital Readiness Copilot — the *tool or flow* that a user interacts with. Collects input, runs the skill logic, returns structured output. Can be: you in Cursor (chat + skill), or a separate CLI/app. | agent.md (strategy); the actual flow/UI/code when you build it |

**Skill** = the rulebook and the assessment logic.  
**Agent** = the thing that uses the rulebook (prompts, steps, interface).

---

## Should you figure out the skill before the agent?

**Yes.** Define the skill first.

1. **The agent depends on the skill.** The Copilot’s job is to “run” the skill: take input, apply criteria, produce an assessment. If the skill is vague or incomplete, the agent won’t know what to ask, what to check, or what to return.
2. **Output shapes the agent.** Once you know the skill’s *output* (e.g. “ownership/role + attribution + relevance + gaps + strengths”), you can design the agent’s flow and output sections. The skill defines *what* the agent produces.
3. **Input follows from the skill.** The skill implies what evidence is needed (e.g. deal list by ownership, geography, check sizes). That tells you whether the agent asks questions, accepts a deck, or both.
4. **Scope control.** Getting the skill clear keeps the agent from drifting (e.g. into fundraising advice or extra pillars) because “done” is defined by the skill.

So: **skill = contract for the agent.** Define the contract first; then build the thing that fulfills it.

---

## How to “figure out the skill”

Answer these **for the skill** (not the agent). When these are clear, the agent is “the thing that runs this.”

### 1. What is in scope for the skill?

- **In scope (v1):** e.g. “Track record assessment for emerging managers raising from Western LPs and deploying in non-Western markets.”
- **Out of scope (v1):** e.g. “Other pillars (governance, team, terms), fundraising how-to, educational content.”

### 2. What are the inputs the skill needs?

- What evidence does the assessment require? (e.g. deal list with ownership type, role, geography, stage, check size, outcomes.)
- Where does that evidence come from in practice? (e.g. user narrative, deck, memo, or structured form.)
- Note: “Input” here is *what the skill assumes it can see*, not yet the UI (that’s the agent).

### 3. What are the outputs of the skill?

- What does a “complete” assessment consist of? (e.g. ownership/role clarity, attribution, relevance, proof, format, verifiability, consistency; list of gaps; list of strengths; optional LP-type weighting.)
- In what form? (e.g. structured sections, checklist, one narrative.)
- What must *not* be in the output? (e.g. fundraising steps, generic encouragement.)

### 4. What are the boundaries?

- When does the skill *not* apply? (e.g. Fund II+ managers, managers not targeting Western LPs, founders seeking startup support.)
- What language and tone? (e.g. diagnostic, clear, no “helping/empowering” drift.)

---

## Once the skill is clear, the agent is:

- **Input step(s):** Get the evidence the skill needs (questions, upload, or form).
- **Run the skill:** Apply the criteria (ownership/role, attribution, relevance, proof, format, verifiability, consistency; LP-type weighting if relevant).
- **Output step(s):** Return the assessment in the shape the skill defines (sections, gaps, strengths).

So: **figure out the skill (scope, inputs, outputs, boundaries); then design the agent (flow, prompts, interface) to match.**
