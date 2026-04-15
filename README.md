# playwright-manual-to-test-generator-info

Deterministic QA tool: manual steps → consistent Playwright TypeScript tests (overview repo)

---

# Playwright Manual-to-Test Generator (Overview)

**Manual test steps → deterministic Playwright TypeScript tests**

This repository is an **overview and documentation landing page** for a QA tool built by **Ryan Goede (TekQA Consulting)** to solve a real-world manual-to-automation migration problem.

👉 **Main Repository (Code + Extension)**  
https://github.com/rmgoede/playwright-manual-to-test-generator  

Use this to install and run the generator.

This repo exists to explain **what the tool does, why it exists, and how it’s used**.

---

## The Problem This Tool Solves

Many teams still maintain large regression suites as:

- Excel spreadsheets  
- ALM / QC test cases  
- Jira tickets  
- Plain-text procedural steps  

Manually converting these into Playwright tests is:

- Slow  
- Error-prone  
- Inconsistent  
- Hard to scale  

Prompting an LLM helps — but direct code generation can vary run to run.

---

## What This Tool Does

The **Playwright Manual-to-Test Generator** converts **plain-text manual test steps** into:

- A **single, runnable Playwright TypeScript test**
- Using **deterministic generation rules**
- With **Playwright-recommended structure and locators**
- No heuristic selector inference, scraping, or DOM inspection
- Uses a structured JSON contract (V1.5) to enforce consistent output

Output is designed to be:

- Predictable  
- Readable  
- Easy to refine once the real DOM is inspected  

---
## How It Works (Architecture)

The generator supports two modes:

**V1 (Direct Generation)**  
Manual Steps  
→ LLM  
→ Playwright TypeScript test  

**V1.5 (Structured Mode)**  
Manual Steps  
→ LLM  
→ Structured JSON (schema-enforced)  
→ Deterministic Renderer  
→ Playwright TypeScript test  

### Why this matters

Instead of letting the LLM generate final code directly,  
V1.5 introduces a structured contract (JSON) between interpretation and execution.

This results in:

- More consistent output  
- Reduced variability between runs  
- Clear validation boundaries  
- Deterministic final code generation
---

## Key Characteristics

- Controlled, consistent output (schema + renderer reduce variability)
- Rule-based selector generation (role/text-based)
- Produces a clean first draft, not a “magic” passing test
- Designed for **real migration work**, not demos

Some selector refinement is expected by design.

---

## How It’s Used

This tool is used:

- By QA engineers modernizing legacy test suites
- During manual → Playwright migration efforts
- As a repeatable workflow for generating first-draft automation
- As a practical example of build-when-gaps-exist engineering

It reflects a **build tooling when needed**, not just use tooling mindset.

---

## Screenshots / Demo

> Demo GIF below reflects real output from the tool against common automation flows (login, add-to-cart, verification).

![Playwright Manual-to-Test Generator demo](assets/DemoFinal.gif)

---

## Source Code & Quick Start

The generator is fully open-source:

👉 https://github.com/rmgoede/playwright-manual-to-test-generator

Installation and usage instructions are in the main repository README.

---

## Related Work

- TekQA Consulting: https://tekqaconsulting.com  
- Playwright Portfolio: https://github.com/rmgoede/tekqa-playwright-portfolio  
- Postman API Portfolio: https://github.com/rmgoede/qa-apis-postman-sample

---

## About

Built by **Ryan Goede**  
Senior QA Engineer | Automation & CI/CD  
28+ years across healthcare, banking, government, and e-commerce

This repo documents **real tooling built for real automation problems**.
