---
layout: page
title: DistDebug-Bench
img: assets/img/projects/distdebug-bench.png
description: Can a coding agent pinpoint the code behind a distributed-system failure?
importance: 2
category: research
---

Nowadays, agent can perform really complex tasks. However **long horizon** tasks still remains a major challenge.
DistDebug-Bench focuses on a most complicated and large search space: distributed system debugging. Given an incident report, the available logs or stack traces, and the source code as it stood before the fix, an agent must identify the blocks of code that caused the failure. The evaluator compares its answers with root causes annotated by human reviewers.

{% include figure.liquid path="assets/img/projects/distdebug-task.png" alt="An incident report and logs feed into a coding agent; its diagnosis is validated and scored." caption="A benchmark run starts with the code as it stood before the fix and ends with a score for the code locations the agent identified." zoomable=true %}

The benchmark covers **120 real bugs across 11 distributed systems** written in five languages. In 46% of the cases, no single code block tells the whole story. Agents often found a relevant file but missed the lines responsible for the failure, especially when the cause spanned components.

{% include figure.liquid path="assets/img/projects/distdebug-zookeeper.png" alt="Four panels trace ZooKeeper issue 2845 from replica divergence after restart to stale database state." caption="In ZooKeeper issue 2845, the symptoms pointed toward leader election, but the cause was database state that survived a restart." zoomable=true %}

[Read the paper (PDF)]({{ '/assets/pdf/distdebug-bench.pdf' | relative_url }}), accepted as a poster at the NeurIPS 2026 Evaluations and Datasets Track. The [benchmark and evaluator](https://github.com/OrderLab/distdebug-bench) are available on GitHub; the [leaderboard and agent traces](https://distdebug.com) show how agents investigated the incidents.
