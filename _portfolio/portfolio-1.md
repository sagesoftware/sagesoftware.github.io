---
title: "CodeAI — Full-Stack AI Code Analysis Platform"
excerpt: "A production-ready AI SaaS platform with JWT auth, RAG pipeline, and LLM-powered code review.<br/>"
collection: portfolio
---

**Stack:** React, FastAPI, OpenAI API, ChromaDB, SQLite, Docker

**GitHub:** [github.com/sagesoftware/codeai-platform](https://github.com/sagesoftware/codeai-platform)

## Overview

CodeAI is a full-stack web application where users sign up, paste code, and receive AI-powered feedback — detecting bugs, security vulnerabilities, and performance issues. The more you use it, the smarter it gets.

## How It Works

1. **Auth** — users register and log in via JWT authentication with bcrypt password hashing
2. **Submit code** — paste any code snippet and select the language
3. **RAG retrieval** — the code is embedded using OpenAI text-embedding-3-small and compared against the user's past reviews in a ChromaDB vector store via cosine similarity
4. **LLM analysis** — GPT-3.5-turbo receives the code plus similar past reviews as context and returns structured feedback: bugs, security issues, performance tips, and a suggested rewrite
5. **Storage** — the review is persisted to the database and the embedding is stored for future RAG retrieval

## Features

- JWT authentication with per-user sessions
- Per-user RAG vector store — feedback improves over time
- Structured AI output — bugs, security, performance, best practices, score out of 10
- Review history dashboard with language breakdown and average score
- Multi-language support — Python, JavaScript, Java, C++, TypeScript, Go, Rust
- Dockerized and ready for cloud deployment
