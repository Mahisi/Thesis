README — Real Prompt Examples for AI Agent

This folder contains two real prompt examples that demonstrate how the thesis system (TypeScript Dependency Analysis Agent) can work as an end-to-end AI solution. Each prompt sends input data X (TypeScript project source code) to the agent and receives output y (dependency analysis results).

Prompt 1 — Zero-Shot Example
File: prompt1_zero_shot.txt
This prompt provides the agent with only one new project X and does not include any previous examples. The agent must perform the whole workflow independently, including:

AST parsing, semantic understanding, dependency extraction, DSM generation, and final report creation.

The output (y) should include:
1)Dependency graph (JSON)
2)Design Structure Matrix (DSM)
3)Circular dependency detection (if it exists)
4)Summary with architectural insights and recommendations

The zero-shot prompt evaluates the system’s ability to analyze code without prior context.

Prompt 2 — Few-Shot Example
File: prompt2_few_shot.txt
This prompt first introduces several known (X, y) examples to show the agent what kind of output is expected. After the examples, the prompt provides a new project X and asks the agent to generate output y.

The output format is the same as in the zero-shot prompt:
1)Dependency graph
2)DSM
3)Circular dependency findings
4)Structural report and recommendations

The few-shot prompt demonstrates that the agent can improve reasoning and consistency by using the previous examples.

Difference Between the Prompts

Zero-shot: The agent receives only the new project X and must produce output y without seeing any previous examples.
Few-shot: The agent receives several (X, y) example pairs before being asked to generate y for a new X.

Purpose of These Prompts

These prompts show how the thesis system can be conceptualized as a single AI agent that transforms input source code into dependency analysis results. They serve as documentation and demonstration for Labwork 1.4.
