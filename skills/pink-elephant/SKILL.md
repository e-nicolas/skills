---
name: pink-elephant
description: Rewrite prompts or instructions around the desired outcome. Use when reframing content so an LLM focuses on what it should produce without anchoring on unwanted behavior.
---

Restructure the thinking and wording using the pink elephant technique. Write the target version as if it were the first draft, not as a correction of the previous text. Avoid referring back to the prior wording, because mentioning a discarded idea can increase the chance that an LLM still considers it. Prefer direct, positive actions the agent should perform, and express the goal directly instead of centering the response on the content being discarded.


## Examples

Bad:

```text
Don't use var in JavaScript.
```

Good:

```text
Use const for values that stay fixed and let for values that change.
```

Bad:

```text
Do not mention the old cancellation flow.
```

Good:

```text
Describe the current cancellation flow using only the steps available in the new experience.
```
