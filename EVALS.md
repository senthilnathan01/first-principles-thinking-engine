# Skill Evaluations

These checks test whether the skill changes reasoning behavior in the intended ways without forcing first-principles analysis onto routine tasks.

## Managed authentication decision

### Purpose

Verify that the skill can analyze a consequential build-versus-buy decision without rejecting the conventional option by default or inventing a numerical lower bound.

### Command

```bash
codex exec --ephemeral --sandbox read-only --color never 'Use $think-from-first-principles to decide whether a four-person startup should build its own authentication system or use a managed provider. Assume it needs email/password and social login, handles ordinary SaaS data, and wants to launch in eight weeks. Do not edit files. Return the decision, assumption ledger, constraints, alternatives, falsification test, and next experiment.'
```

### Result

**Pass.** Codex loaded the repository skill and recommended managed authentication. The response:

- Classified claims as observed, derived, assumed, or unknown.
- Treated the eight-week deadline, security lifecycle, and team capacity as binding constraints.
- Said no defensible numerical build-time floor was available instead of inventing one.
- Compared hosted, custom-UI, self-hosted framework, and ground-up alternatives.
- Listed conditions that would reverse the recommendation.
- Proposed a two-engineer-day managed-provider integration spike with explicit pass criteria.

The test ran read-only and changed no files.

## Routine-task boundary

### Purpose

Verify that a straightforward factual request receives a direct answer rather than the full first-principles protocol.

### Command

```bash
codex exec --ephemeral --sandbox read-only --color never 'What Git command prints the name of the current branch? Answer with only the command. Do not edit files.'
```

### Result

**Pass.** Codex returned only `git branch --show-current`, without an assumption ledger or first-principles analysis. The test ran read-only and changed no files.
