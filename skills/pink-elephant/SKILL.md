---
name: pink-elephant
description: "Rewrite prompts, instructions, or text using the pink elephant technique: state the desired outcome directly without naming, negating, or referencing the unwanted behavior, wording, or prior version. Use when the user asks to reframe or restructure content so an LLM is less likely to anchor on what should be avoided."
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
