---
name: agent-technical-english
description: Controlled English for agent instructions, handoffs, task contracts, tool procedures, and multi-agent orchestration. Use when one agent writes instructions that another agent or tool must execute, especially inside wayfinder, handoff, research, prototype, implementation, or CI workflows.
---

# Agent Technical English

Write instructions for agents as a controlled natural language.

Agent Technical English (ATE) is inspired by ASD-STE100 Simplified Technical English, but it is not ASD-STE100 and does not claim compliance with that standard. ATE adapts controlled-language principles to agent-to-agent execution.

The goal is **low semantic freedom at execution boundaries**.

Use normal language for discussion with the human. Use ATE when language becomes an execution contract.

## Core rule

An execution instruction must make the intended action easier to execute than any unintended interpretation.

Do not make the text merely shorter. Make the operational meaning smaller.

## Preserve the source

When you convert an instruction to ATE:

- Preserve its meaning.
- Preserve its scope.
- Preserve its decision owner.
- Do not add requirements.
- Do not remove constraints.
- Do not turn an option into a requirement.
- Do not resolve an unknown by guessing.

If the source is ambiguous and the ambiguity can change the result, keep the ambiguity visible and ask or research before execution.

## Use the project language

Read the project's `CONTEXT.md` or equivalent shared-language file when one exists.

Use its canonical terms.

Use one term for one concept inside the same contract. Do not alternate between synonyms for style.

If a project term has a precise technical meaning, keep that term even if it is not plain English.

## Sentence rules

Prefer one action per sentence.

Use the imperative for an action:

> Read the schema.

Use a declarative sentence for a fact:

> The runtime database is PostgreSQL.

Put the condition before the action when the action depends on it:

> If the migration fails, stop the task.

Name the object explicitly:

> Update `RuntimeGridSql`.

Do not write:

> Update it.

Use pronouns only when the referent cannot reasonably be confused.

Use active voice for executable steps.

Use simple verb forms.

Prefer concrete verbs:

- read
- find
- compare
- create
- update
- delete
- run
- verify
- report
- stop
- ask

Avoid vague execution verbs unless the contract defines them:

- handle
- improve
- clean up
- deal with
- optimize
- fix everything
- make it better
- take care of

Replace a vague verb with observable actions and a completion condition.

## Normative words

Use these words consistently:

- **MUST** — required for completion.
- **MUST NOT** — prohibited.
- **MAY** — permitted but optional.

Avoid **SHOULD** in execution contracts when failure to follow it would matter. Write the actual rule.

Use **PREFER** only for a real preference where the agent can choose another option and explain why.

## Explicit authority

Do not let an agent infer who owns a decision.

For a material decision, state one of these:

- `DECISION OWNER: HUMAN`
- `DECISION OWNER: AGENT`
- `DECISION OWNER: EXISTING CONTRACT`

`DECISION OWNER: HUMAN` means the agent can prepare options, evidence, or prototypes, but MUST NOT select the final option.

A prototype does not transfer decision authority to the agent.

A recommendation is not a decision unless the contract explicitly gives the agent that authority.

## Unknowns

Do not hide uncertainty in fluent prose.

Use one of these states when necessary:

- `KNOWN` — supported by the available source.
- `UNKNOWN` — information is missing.
- `ASSUMPTION` — execution can continue safely with an explicit temporary assumption.

For a material `UNKNOWN`, stop the affected action and use the workflow that can resolve it.

Do not convert `UNKNOWN` to `ASSUMPTION` only to keep moving.

## Scope

State scope when an agent could reasonably act outside it.

Examples:

> SCOPE: `icms-2030` branch only.

> SCOPE: Review the authentication module. Do not modify unrelated modules.

For destructive or externally visible actions, scope must be explicit.

## Completion

Every executable task needs an observable completion condition.

Use:

`DONE WHEN: <observable state>`

Good:

> DONE WHEN: All affected tests pass and the schema diff contains only the approved changes.

Bad:

> DONE WHEN: The code looks good.

A task is not complete because the agent has spent enough effort. It is complete when the stated condition is true.

## Stop conditions

State stop conditions before risky actions.

Examples:

> If a test fails for a reason outside this change, stop and report the failure.

> If the migration changes data outside the selected tenant, stop the migration.

> If the requested action requires a human decision, stop before that decision.

Do not silently broaden scope to bypass a stop condition.

## Side effects

Make side effects explicit.

Before an instruction that can publish, merge, delete, deploy, send, charge, migrate, or modify external state, state the allowed side effect.

Example:

> MAY create commits on `agent/grid-contract`.
> MUST NOT merge to `main`.

Read-only investigation does not imply permission to write.

Permission to edit does not imply permission to publish.

Permission to publish does not imply permission to merge.

## Multi-step contracts

For a small instruction, plain controlled sentences are enough.

For a multi-step or high-risk instruction, use this compact structure:

```text
GOAL: <one observable outcome>
SCOPE: <where the agent may act>
DECISION OWNER: <HUMAN | AGENT | EXISTING CONTRACT>

1. <action>
2. <action>
3. <verification>

MUST: <hard requirement>
MUST NOT: <hard prohibition>
DONE WHEN: <observable completion condition>
```

Add only fields that reduce real ambiguity.

Do not turn every message into a form.

## Parallel work

Parallel execution is opt-in.

Run work in parallel only when:

1. The workflow permits parallel execution.
2. The tasks do not compete for the same decision.
3. One task cannot invalidate the premises of the other task.
4. The tasks do not write conflicting state.
5. The result of one task is not required to define the other task correctly.

If any condition is false or unknown, run the work sequentially.

Research can run in parallel when the parent workflow explicitly permits it.

Do not parallelize human decision tickets merely because they appear independent in the initial map.

## Handoffs

A handoff must tell the next agent what is true, what it may do, and where it must stop.

Include:

```text
STATE: <facts established so far>
GOAL: <next outcome>
SCOPE: <allowed working area>
DECISION OWNER: <owner of unresolved material decisions>
DONE WHEN: <handoff completion condition>
```

Do not dump the whole conversation into a handoff when a smaller contract preserves the required state.

## Tool instructions

Treat a tool call as an execution boundary.

Before a state-changing tool call, verify:

1. The target is explicit.
2. The action is explicit.
3. Required identifiers are resolved.
4. The scope is allowed.
5. The side effect is authorized.
6. The completion condition is known.

Do not rely on a tool to infer missing destructive parameters.

## Wayfinder integration

ATE complements `wayfinder`. It does not replace Wayfinder's map, ticket types, blocking rules, or human-in-the-loop gates.

When Wayfinder creates or updates a decision ticket:

- Write the ticket question with one stable meaning.
- Use project terms from `CONTEXT.md`.
- State the decision owner when it is not obvious.
- Keep unresolved decisions unresolved.
- Do not convert a decision ticket into an implementation task.
- Do not add implementation scope merely because the likely implementation is visible.
- Do not select the result of a HITL prototype or grilling ticket for the human.
- Treat the current frontier as provisional knowledge, not as permission to pre-slice the fog.
- Run parallel work only when Wayfinder permits it and the ATE parallel-work conditions are true.

When Wayfinder hands off to implementation, compile each implementation instruction into ATE before execution.

### Wayfinder ticket example

Weak:

> Figure out the permissions model and update whatever needs changing.

ATE:

```text
QUESTION: Which permissions model will replace Admin / All / Own?
DECISION OWNER: HUMAN

Find the current permissions behavior.
List the required compatibility constraints.
Prepare the viable models.
Compare the models against the constraints.

MUST NOT modify the implementation before the decision is recorded.
DONE WHEN: The human selects a model and the ticket records the decision.
```

### Prototype example

Weak:

> Make three versions and use the best one.

ATE:

```text
GOAL: Create three prototype variants for comparison.
DECISION OWNER: HUMAN

Create three materially different variants.
Show the same scenario in each variant.
Record the important trade-offs.

MUST NOT select the final variant.
DONE WHEN: The human can compare the three variants and make the decision.
```

### Implementation example

Weak:

> Clean up the grid code and fix any related issues.

ATE:

```text
GOAL: Implement the approved grid-contract change.
SCOPE: Grid query and runtime SQL code affected by the approved contract.
DECISION OWNER: EXISTING CONTRACT

Update the implementation to match the approved contract.
Add or update tests for each changed behavior.
Run the affected test suite.

MUST NOT change unrelated grid behavior.
MUST NOT introduce a new architectural decision.
DONE WHEN: The affected tests pass and the implementation matches the approved contract.
```

## Compile pass

Before sending an execution contract to another agent, perform this pass:

1. Find each action.
2. Find the actor for each action.
3. Find the object for each action.
4. Find each condition and constraint.
5. Find each material decision.
6. Assign the decision owner.
7. Find each unknown.
8. Find each authorized side effect.
9. Add an observable completion condition.
10. Remove synonyms, vague verbs, and unnecessary prose.

Then execute or send the compiled contract.

## Do not over-control

ATE is for execution boundaries.

Do not use it to flatten exploration, design discussion, brainstorming, or human conversation before the decision is ready.

Controlled language must reduce accidental interpretation, not eliminate useful thought.

Wayfinder finds the route.

ATE makes each step on the route hard to misread.
