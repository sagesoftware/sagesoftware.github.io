---
title: "Guardrail & Red-Team Harness"
excerpt: "An adversarial AI safety testing framework that stress-tests LLM guardrails against jailbreaks, prompt injection, and harmful content.<br/>"
collection: portfolio
---

**Stack:** Python, FastAPI, OpenAI API, SQLite, Streamlit

**GitHub:** [github.com/sagesoftware/guardrail-redteam-harness](https://github.com/sagesoftware/guardrail-redteam-harness)

## Overview

A red-team testing framework that stress-tests LLM systems against adversarial attacks — jailbreaks, prompt injections, harmful content, and data exfiltration attempts. Achieved ~92% detection accuracy with less than 8% false positive rate across 13 adversarial test cases.

## How It Works

1. **Layer 1 — Regex scrubbers** — 8 pattern rules targeting known attack signatures
2. **Layer 2 — OpenAI Moderation API** — ML-based scoring across hate, violence, self-harm, and sexual content
3. **Logging** — every attempt stored in SQLite with severity, block reason, and moderation scores
4. **Dashboard** — real-time Streamlit UI showing block rate, category breakdowns, and incident log

## Why It Matters

Enterprise AI deployments need to be hardened against adversarial misuse. This project directly addresses that problem — giving security teams visibility into what gets blocked and what slips through.
