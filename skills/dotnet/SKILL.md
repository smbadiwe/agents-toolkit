---
name: dotnet
description: Procedural rules and style conventions for working on C# codebases, .NET Core Web APIs, and testing suites. Trigger this skill when .cs, .csproj or .sln files are modified or analyzed.
---

# .NET & C# Operational Skill

## Activation Condition
Execute these instructions if the codebase contains C# source files (`.cs`), project configurations (`.csproj`), or solution layout mappings (`.sln`). 

## Coding Conventions

1. Follow the official Microsoft C# coding guidelines for naming, formatting, and structuring code.
2. Avoid over-abstracting simple operations or creating unnecessary layers of inheritance. For instance, avoid making interfaces and abstract classes for simple services that do not require multiple implementations or complex behavior.

## Compilation & Verification Execution

After making code changes,
1. Always run `dotnet format` to properly format your code changes.
2. Always compile code updates by invoking `dotnet build` locally.
3. Run automated test suites via `dotnet test`.
4. If dependencies need resolving, run `dotnet restore` before attempting modifications.

Only when all of the above steps are successful should you report your changes as completed.

# Must-follow rules for software development

These rules apply to every coding task unless explicitly overridden.
Bias: caution over speed on non-trivial work. Use judgment on trivial tasks.

## Rule 1 — Think Before Coding
State assumptions explicitly. If uncertain, ask rather than guess.
Present multiple interpretations when ambiguity exists.
Push back when a simpler approach exists.
Stop when confused. Name what's unclear.

## Rule 2 — Simplicity First
Minimum code that solves the problem. Nothing speculative.
No features beyond what was asked. No abstractions for single-use code.
Test: would a senior engineer say this is overcomplicated? If yes, simplify.

## Rule 3 — Surgical Changes
Touch only what you must. Clean up only your own mess.
Don't "improve" adjacent code, comments, or formatting.
Don't refactor what isn't broken. Match existing style.

## Rule 4 — Goal-Driven Execution
Define success criteria. Loop until verified.
Don't follow steps. Define success and iterate.
Strong success criteria let you loop independently.

## Rule 5 — Use the model only for judgment calls
Use me for: classification, drafting, summarization, extraction.
Do NOT use me for: routing, retries, deterministic transforms.
If code can answer, code answers.

## Rule 6 — Token budgets are not advisory
Per-task: 4,000 tokens. Per-session: 30,000 tokens.
If approaching budget, summarize and start fresh.
Surface the breach. Do not silently overrun.

## Rule 7 — Surface conflicts, don't average them
If two patterns contradict, pick one (more recent / more tested).
Explain why. Flag the other for cleanup.
Don't blend conflicting patterns.

## Rule 8 — Read before you write
Before adding code, read exports, immediate callers, shared utilities.
"Looks orthogonal" is dangerous. If unsure why code is structured a way, ask.

## Rule 9 — Tests verify intent, not just behavior
Tests must encode WHY behavior matters, not just WHAT it does.
A test that can't fail when business logic changes is wrong.

## Rule 10 — Checkpoint after every significant step
Summarize what was done, what's verified, what's left.
Don't continue from a state you can't describe back.
If you lose track, stop and restate.

## Rule 11 — Match the codebase's conventions, even if you disagree
Conformance > taste inside the codebase.
If you genuinely think a convention is harmful, surface it. Don't fork silently.

## Rule 12 — Fail loud
"Completed" is wrong if anything was skipped silently.
"Tests pass" is wrong if any were skipped.
Default to surfacing uncertainty, not hiding it.
