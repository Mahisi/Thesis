This directory contains all prompt templates used to interact with the AI agent of the thesis system “Research on Program Code Analysis Techniques.”

The goal of these prompts is to conceptualize the dependency analysis system as a single intelligent agent, which receives TypeScript project input X and returns analysis results y by executing all internal stages end-to-end:

Data Understanding → Semantic Inference → Reasoning → Output Generation
(AST parsing → Symbol resolution → Dependency extraction → DSM → Reports)

Purpose of first prompt: it runs the AI agent with only one new observation X → outputs y
Purpose of second prompt: it provides several (X, y) examples before requesting a new prediction to improve accuracy

Expected workflow of the AI agent

Every prompt instructs the system to:
1.Understand the project structure and imported modules
2.Resolve semantic relationships using type and symbol scope
3.Detect dependency structures, including cycles and type-only dependencies
4.Produce structured analysis results

Standard Output Format (y)

Regardless of prompt type, the expected result should always include:

1) Dependency Graph (text/JSON)
2) Design Structure Matrix (DSM)
3) Circular dependency and architecture issue detection
4) Runtime vs type-only dependency classification (if applicable)
5) Developer-friendly summary + improvement suggestions


Zero-shot prompt:
1)Evaluates how well the agent performs without prior examples
2)Uses only the given X
3)Useful for initial baseline

Few-shot prompt:
1)Demonstrates improved reasoning with previous (X,y) pairs
2)Provides multiple examples before solving a new X
3)Useful in real-world iterative analysis


Usage Notes:
These prompts are documentation, examples, and test cases for the thesis system.
The system should always produce deterministic, structured, reproducible results.
The prompts do not ask the model to explain its chain-of-thought — only to output the final analysis results.

