---
layout: post
title: AI native software
date: 2026-11-24
description: Software that treats the model as a foundational component rather than a feature bolted on top
categories: [project]
tags: [coding-agents, harness, systems]
---

Nowadays, services may need to take a turn. My recent project [Coursify]({{ '/projects/2_project/' | relative_url }}) is built on this idea.

### What is AI native software?

By AI native I am referring to software that keeps AI integrated as a foundational component. What is not AI native? A chatbot service for Q&A is not; a plug and play function or generative plugin is not. AI native software uses AI as a major component put in front.

### Why AI native, and how?

One constant theme in AI development is whether the value of engineering effort is ever going to last. Often the effort we put into a project does not produce a more productive and usable system. Especially as model ability grows stronger and stronger, keeping the product at the front of model improvements becomes a central concern. What is worse is that the effort we put into building software may not give us privilege in maintaining our position in competition. [REA skills](https://rea.tools/zh-CN/) caught people's eyes. It is not a new thing. It has been long since companies used AI to rebuild their services (bun to rust). We can imagine that with model ability improving, reverse engineering will be cheaper, quicker, better.

### Utilize harnesses

We can integrate bare metal LLMs into the system. But better, we can utilize a harness. If we want to rebuild our own AI inner core within our software, we need to implement connectors to tools, MCPs, and skills; to ensure safety we need sandboxes (a bash tool should be integrated — it is mighty); and to fit a recurring workflow we might want an agent loop. But these are just some of the boilerplate code directly provided by a harness. By integrating a harness in our application we already have the prebuilt tool set to do many amazing things. One example will be openclaw — pi harness as backend.

### Modularization (where humans can still take part)

We want AI to be a core component; however, letting AI write our website from scratch every time a user logs in would be impossible. There will be some prebuilt components that serve as existing modules for the harness to manipulate. This interface should also be carefully designed. It may not be too constrained or too ubiquitous. A suitable toolset is proven to be significant. ([DistDebug-Bench]({{ '/projects/distdebug-bench/' | relative_url }}))

### Self evolution

To further accelerate our improvements, we can also let the system be able to do self improvement. One of the easiest ways would be to let the LLM inspect the log and improve on skills, just like backpropagation in model training.
