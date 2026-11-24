---
layout: page
title: Cirdan
img: assets/img/projects/cirdan.png
description: Tracing distributed-system failures from symptoms to the code that caused them
importance: 1
category: research
---

A log message can point to the component that detected a failure rather than the code that caused it. Cirdan is a coding agent that tests competing explanations before it settles on a diagnosis. The agent surveys the repository, gathers evidence for each hypothesis, then investigates the most promising ones in depth. The whole process is based on the concept of **Tree of thought**. Each hypothesis has its own branch, so the agent can return to an earlier lead without losing the evidence it already collected.

{% include figure.liquid path="assets/img/projects/cirdan-investigation.png" alt="A hypothesis tree beside the agent’s context for the active branch." caption="Cirdan keeps the full investigation history for the current hypothesis and short summaries of the alternatives." zoomable=true %}

**Evaluation.** On 34 real bugs from 11 distributed systems, Cirdan improved diagnosis accuracy with four of the five models tested. With GPT-5.2-Codex, it identified 6.3–22.7 percentage points more of the code blocks responsible for the failures, depending on the baseline.

{% include figure.liquid path="assets/img/projects/cirdan-results.png" alt="Five plots comparing code-block coverage and precision for Cirdan and baseline agents." caption="Each arrow shows how coverage and precision changed when the same model used Cirdan instead of its baseline agent." zoomable=true %}

The 34 bugs are a subset of [DistDebug-Bench]({{ '/projects/distdebug-bench/' | relative_url }}), a benchmark for evaluating whether agents can identify the code responsible for distributed-system failures.
