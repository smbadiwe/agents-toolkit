---
name: dotnet
description: Procedural rules and style conventions for working on C# codebases, .NET Core Web APIs, and testing suites. Trigger this skill when .cs, .csproj or .sln files are modified or analyzed.
------

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
