---
layout: page
title: Coursify
img: assets/img/projects/coursify.png
description: Plan a course with an AI assistant, edit lessons block by block, and share them as slides
importance: 2
category: product
---

Coursify is a course-authoring prototype that starts with an outline rather than a generated textbook. Authors can work with an AI assistant to decide what to teach and in what order, then draft and revise one lesson at a time. The outline doubles as an editable mind map: moving a topic on the map changes its place in the lesson list.

A physics lesson, for example, can combine a Markdown explanation, a LaTeX equation, and a diagram. The author can revise the equation without regenerating the lesson, then turn the module into a shareable slide deck. For a lesson on pendulum motion, the presentation assistant can add a built-in simulation with a chosen pendulum length and starting angle.

Coursify v2 uses Rust, Leptos, and SQLite. It embeds the Nanocode agent runtime so authors can resume a conversation about the whole course or return to one about a particular module. Slidev builds the presentation decks from the lesson content.

[View the original Coursify project on GitHub](https://github.com/SalmonAI99/coursify).

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
