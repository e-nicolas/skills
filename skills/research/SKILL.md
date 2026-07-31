---
name: research
description: Coordinate in-depth, parallel research across sources. Use to investigate a topic, compare findings, create separate Markdown reports, and generate a linked index.
---

# Research

Research the topic I requested. For each investigation unit, create a subagent to conduct in-depth research and write a `.md` file with its findings and consulted sources. In each batch, assign a distinct investigation unit to each subagent.
Run subagents up to the available slot limit and process the remainder in batches. Do not limit the total number of sources.

For each investigation, provide a brief description of the key differentiators in its findings.
After completing all investigations, generate a `.md` file containing only an index of the generated `.md` files in the following format:

- [Link title](file.md): file details

Create a dedicated directory for the run.
