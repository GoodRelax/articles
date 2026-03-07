# ANMS — AI-Native Minimal Spec

A specification template designed for AI-driven software development.

## What is ANMS?

ANMS (AI-Native Minimal Spec) is a lightweight specification template that combines **EARS**, **Gherkin**, and **Mermaid** into a single Markdown document. It uses **STFB (Stable Top, Flexible Bottom)** — a chapter structure inspired by the Stable Dependencies Principle — to make specs that are both human-reviewable and AI-parseable.

## Files

| File | Description |
|------|-------------|
| [anms-essay (JA/EN)](https://github.com/your-username/claude-code-full-auto-dev/tree/main/anms-template) | Full paper: rationale, comparison with existing formats, and design decisions |
| [anms-spec-template (JA/EN)](https://github.com/your-username/claude-code-full-auto-dev/tree/main/anms-template) | The template itself — ready to use in your project |
| [devto-article.md](devto-article.md) | Dev.to summary article |

## Quick Start

1. Get the template from the [claude-code-full-auto-dev](https://github.com/your-username/claude-code-full-auto-dev/tree/main/anms-template) repository
2. Remove the "Design Rationale" and "References" sections at the bottom (they're about the template itself)
3. Fill in Chapters 1-6 for your project
4. Hand it to your AI coding agent

## Chapter Structure (STFB)

```
Ch1  Foundation        ← Most stable / abstract
Ch2  Requirements       (EARS + formulas)
Ch3  Architecture       (Mermaid, color-coded)
Ch4  Specification      (Gherkin)
Ch5  Test Strategy
Ch6  Design Principles ← Quality assurance meta-layer
```

## License

MIT
