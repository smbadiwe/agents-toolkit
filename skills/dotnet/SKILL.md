---
name: dotnet
description: Procedural rules and style conventions for working on C# codebases, .NET Core Web APIs, and testing suites. Trigger this skill when .cs, .csproj or .sln files are modified or analyzed.
------

# .NET & C# Operational Skill

## Activation Condition
Execute these instructions if the codebase contains C# source files (`.cs`), project configurations (`.csproj`), or solution layout mappings (`.sln`). 

## Compilation & Verification Execution

After making code changes,
1. Always run `dotnet format` to properly format your code changes.
2. Always compile code updates by invoking `dotnet build` locally.
3. Run automated test suites via `dotnet test`.
4. If dependencies need resolving, run `dotnet restore` before attempting modifications.

Only when all of the above steps are successful should you report your changes as completed.
