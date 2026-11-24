---
layout: page
title: Coursify
img: assets/img/projects/coursify.png
description: Plan a course with an AI assistant, edit lessons block by block, and share them as slides
importance: 2
category: product
---

Designed for solo educator and developer who want to share their experience without hustling for illustration, slides, etc.

Coursify is efficient. It uses Rust, [Leptos](https://www.leptos.dev/), and SQLite. It embeds the [Nanocode](https://nanocode.xyz/) agent runtime so authors can resume a conversation about the whole course or return to one about a particular module. Slidev builds the presentation decks from the lesson content.

The idea is that first, AI should exel us is its ability to generate eye catching illustrations. We already prompts them to create all kinds of amazing visual effects; Second, it is good at laying out thoughts process that is easy to understand - We rely on that daily. These two combined gives me the incentivity to create this project.

Coursify is also a web app project that implement the [AI Native Software]({{ '/blog/2026/ai-native-software/' | relative_url }}) idea.

## Design

{% include figure.liquid path="assets/img/projects/coursify-design.svg" alt="Design graph: course modules and sessions sit on the Nanocode runtime alongside Agent.md, Notes.md, skills, and web components, connected to a client agent through an MCP server and tools." caption="How a course, its modules, and their agent sessions fit together: the Nanocode runtime supplies the agent loop, skills and notes carry the course context, and an MCP server exposes the authoring tools to a client agent." zoomable=true %}

[Coursify MCPs & Skills](https://github.com/SalmonAI99/coursify).

## Demo recordings

### Part 1

<video controls playsinline preload="metadata" width="100%" aria-label="Coursify demo, part 1">
  <source src="{{ '/assets/video/coursify/demo-1.webm' | relative_url }}" type="video/webm">
  <a href="{{ '/assets/video/coursify/demo-1.webm' | relative_url }}">Download part 1 (WebM)</a>
</video>

### Part 2

<video controls playsinline preload="metadata" width="100%" aria-label="Coursify demo, part 2">
  <source src="{{ '/assets/video/coursify/demo-2.webm' | relative_url }}" type="video/webm">
  <a href="{{ '/assets/video/coursify/demo-2.webm' | relative_url }}">Download part 2 (WebM)</a>
</video>
