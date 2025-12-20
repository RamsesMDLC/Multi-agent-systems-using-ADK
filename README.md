🚀 Multi-Agent Systems & Workflow Patterns (Google ADK)

Welcome to Multi-Agent Systems & Workflow Patterns, a hands-on project based on the Kaggle 5-Day Agents Course.
This repository demonstrates how to design, build, and orchestrate multi-agent systems using Google’s Agent Development Kit (ADK) and Gemini models.

Instead of relying on a single “do-everything” agent, this project shows how to create teams of specialized agents that collaborate through well-defined workflows—just like real software teams.

✨ What You’ll Learn

This project walks through the core concepts and patterns needed to build reliable agent systems:

✅ When and why to use multi-agent systems

✅ How to orchestrate agents using an LLM as a coordinator

✅ How to pass state between agents using output_key

✅ How to build deterministic workflows with ADK

You’ll implement and compare four major workflow patterns:

Pattern	When to Use	Key Feature
LLM-Managed (AgentTool)	Dynamic orchestration	LLM decides which agent to call
SequentialAgent	Order matters	Fixed, deterministic pipeline
ParallelAgent	Independent tasks	Concurrent execution
LoopAgent	Iterative refinement	Repeated critique & improvement
🧠 Why Multi-Agent Systems?

Single agents don’t scale well.
As tasks grow more complex, monolithic prompts become:

Hard to debug

Hard to maintain

Unreliable in execution order

Multi-agent systems solve this by splitting responsibilities across small, focused agents:

Research

Writing

Editing

Critiquing

Aggregation

Each agent does one job well, and ADK handles coordination.

🧩 Project Structure & Examples

This repository includes several progressively advanced examples:

🔹 Research & Summarization System

ResearchAgent → searches the web

SummarizerAgent → produces concise summaries

Coordinated by a root agent using AgentTool

🔹 Sequential Blog Pipeline

A deterministic “assembly line”:

Outline Agent

Writer Agent

Editor Agent

Implemented using SequentialAgent.

🔹 Parallel Multi-Topic Research

Tech, Health, and Finance researchers run in parallel

An Aggregator agent synthesizes results

Uses ParallelAgent nested inside SequentialAgent

🔹 Iterative Story Refinement

Writer → Critic → Refiner loop

Continues until approved or max iterations reached

Implemented with LoopAgent and a custom exit function

⚙️ Setup & Requirements
Environment

Designed for Kaggle Notebooks

google-adk is pre-installed in Kaggle

To install locally:

pip install google-adk

API Key (Gemini)

Create an API key in Google AI Studio

Add it to Kaggle Secrets as:

GOOGLE_API_KEY


Ensure the secret is enabled for the notebook

⚠️ Usage Notes

❌ Avoid “Run all cells” to prevent hitting API rate limits (429 errors)

▶️ Run cells one at a time, top to bottom

📚 Learning Resources

Google Agent Development Kit (ADK) Documentation

Gemini API Documentation

Kaggle Notebooks Guide

Kaggle Discord 

🎯 Key Takeaways

By the end of this project, you will:

Think in agent teams, not single prompts

Know when to use Sequential, Parallel, or Loop workflows

Understand how to build predictable, scalable agent systems

Be ready to design your own custom agent architectures
