# Autonomous Enterprise Software Engineers

Autonomous SWE Agents interact directly with codebases, shells, compilers, and test suites to debug and implement features.

## Conceptual Architecture

```mermaid
flowchart TD
    Issue[GitHub Issue] --> Workspace[SWE Agent Scaffolding]
    Workspace --> Git[Git Tree Reader]
    Workspace --> Shell[Bash Shell Gateway]
    Workspace --> Compiler[Code Compiler / Linter]
    Workspace --> Test[Test Suite Executor]
    Test -->|Fail| Loop[Refactor Code]
    Loop --> Compiler
```

## Detailed Explanation

- **Repository Manipulation:** Reads multi-file directories, makes edits, and creates pull requests.
- **Local Testing Loop:** Runs linting, compilation, and testing, incorporating errors directly back into the prompt context.
- **HORIZON Scaling:** Excels at resolving complex long-horizon software bugs.

[Back to README](../README.md)
