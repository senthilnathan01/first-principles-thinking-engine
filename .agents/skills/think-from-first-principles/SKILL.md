---
name: think-from-first-principles
description: Analyze hard, ambiguous, high-leverage problems by separating observations from assumptions, identifying irreducible constraints, rebuilding options from those constraints, comparing them with strong baselines, and proposing falsifiable tests. Use when explicitly asked to reason from first principles, challenge assumptions, redesign a system or process, find a theoretical limit, or determine whether convention reflects necessity. Do not use for routine implementation, straightforward factual questions, or low-stakes tasks where established practice is adequate.
---

# Think from First Principles

Rebuild the problem from what must be true. Challenge convention without discarding evidence, expertise, or existing solutions merely because they are conventional.

## Working rules

- Match the depth of analysis to the stakes and reversibility of the decision.
- Distinguish observations, derived claims, assumptions, and unknowns. Do not present one category as another.
- Treat physical and logical limits as hard constraints. Treat legal, financial, organizational, and human constraints as real operating constraints unless the user is explicitly exploring how to change them.
- Use existing solutions as evidence and baselines. Do not require reinvention when a conventional approach survives scrutiny.
- Verify consequential or time-sensitive claims when sources or tools are available. Never invent measurements, prices, probabilities, or citations.
- Ask a clarifying question only when different answers would materially change the analysis. Otherwise, state the assumption and proceed.
- Provide concise reasoning artifacts and evidence. Do not expose hidden chain-of-thought or narrate every internal reasoning step.

## Protocol

### 1. Define the decision

State the problem as a decision or design objective. Identify the desired outcome, success criteria, scope, time horizon, stakeholders, and unacceptable failure modes.

If the request begins with a proposed solution, restate the underlying problem before evaluating that solution.

### 2. Build an assumption ledger

List only the claims that materially affect the answer. Classify each as:

- **Observed**: directly measured or reliably sourced.
- **Derived**: follows from stated observations and logic.
- **Assumed**: plausible but unverified.
- **Unknown**: important information that is currently missing.

Attach confidence and the evidence that would confirm or overturn uncertain claims. Do not manufacture certainty to complete the table.

### 3. Identify irreducible constraints

Separate constraints into:

- **Hard constraints**: cannot be violated within the problem's scope.
- **Soft constraints**: costly or difficult to change, but negotiable.
- **Chosen constraints**: policies, habits, interfaces, or conventions that can be redesigned.

Ask of each constraint: What enforces it? What evidence shows it is binding? What changes if it is removed?

### 4. Find the relevant floor

Estimate a lower bound only when the domain supports one. Choose the quantity that actually limits the system, such as cost, time, energy, information, computational complexity, risk, attention, or human effort.

Include every necessary input. Raw-material cost alone is not a valid cost floor when labor, tooling, yield, reliability, certification, coordination, capital, or externalities are required. If no defensible numerical floor exists, describe a qualitative bound and say why it cannot yet be quantified.

### 5. Rebuild options

Construct options from the constraints that remain. Include:

1. The strongest conventional baseline.
2. At least one minimally changed option.
3. A ground-up option when the fundamentals support one.

Avoid novelty for its own sake. Prefer the simplest option that meets the success criteria.

### 6. Account for consequences

Check second-order effects, incentives, bottlenecks, failure recovery, adoption costs, and who bears each cost or risk. A locally efficient design may still make the whole system worse.

### 7. Try to falsify the leading option

State what would make the preferred option fail. Test sensitive assumptions at plausible extremes. Compare against the baseline using the success criteria from Step 1.

Change the recommendation when the evidence warrants it. First-principles reasoning is not a mandate to reject conventional practice.

### 8. Choose the next experiment

Recommend the cheapest reversible test that reduces the most decision-relevant uncertainty. Define what to measure, the threshold for success or failure, and what each result would change.

## Output

Use only the sections that help the user:

- **Decision and success criteria**
- **Assumption ledger**
- **Irreducible constraints**
- **Relevant floor**
- **Rebuilt options**
- **Recommendation and tradeoffs**
- **Falsification test**
- **Next experiment**

Lead with the recommendation when the user needs a decision. Lead with the assumption ledger when the problem is poorly framed. Keep routine applications compact; reserve the full structure for consequential or genuinely novel problems.
