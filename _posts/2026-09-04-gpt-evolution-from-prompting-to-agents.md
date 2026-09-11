---
layout: post
title: "GPT through time: from next-token prediction to agents that use computers"
date: 2026-09-04 09:00:00 +0200
last_modified_at: 2026-09-11 09:00:00 +0200
description: >
  A practical timeline of the GPT family: scale, prompting, multimodality, long context, reasoning, tool use, and the shift toward end-to-end agentic work.
tags: [ai, openai, gpt]
---

The easiest way to misunderstand the GPT timeline is to treat every version as the same product with a higher intelligence score.

The more useful story is that **the unit of work kept changing**. GPT started as a language-modeling research idea. Then prompting became an interface. Chat made instructions practical. Multimodality widened the input/output surface. Reasoning and tools expanded the length of a task. Computer use pushed the boundary from generating artifacts to operating the software around them.

<div class="table-scroll">

| Era | Model | What changed in practice |
| --- | --- | --- |
| 2018 | GPT | Pre-train a Transformer on broad text, then adapt it to downstream tasks. |
| 2019 | GPT‑2 | Scale alone produced surprisingly broad zero-shot behavior and coherent long-form generation. |
| 2020 | GPT‑3 | 175B parameters and few-shot prompting made natural-language examples a serious programming interface. |
| 2022 | GPT‑3.5 / ChatGPT | Instruction-following plus a conversational product made iterative prompting mainstream. |
| 2023 | GPT‑4 | Stronger reasoning and image input moved GPT into higher-stakes professional and multimodal tasks. |
| 2024 | GPT‑4o | “Omni” brought text, image, audio, and video into a much more real-time interaction model. |
| 2025 | GPT‑4.1 / 4.5 | Long context, stronger coding/instruction following, and a parallel push on broad pre-trained intelligence. |
| 2025 | GPT‑5 | Reasoning became part of the default system rather than a separate specialist experience. |
| 2026 | GPT‑5.6 Sol | Complex professional work, coding, research, computer use, and stronger cyber capability became one flagship workflow. |
| 2026 | GPT‑6 Astra | The emphasis shifts to end-to-end computer work: navigating tools, preserving intent across long tasks, and producing finished artifacts. |

</div>

## GPT‑2: scale starts behaving like generality

OpenAI’s 2019 GPT‑2 release is still worth rereading. The model was trained to predict the next word on a large web corpus, yet began to show question answering, summarization, translation, and reading-comprehension behavior without task-specific training.

The important conceptual change was **zero-shot transfer**: useful behavior could emerge from a general language-model objective instead of a separate model and dataset for each task.

## GPT‑3: prompting becomes the interface

GPT‑3 pushed that idea much further. At 175 billion parameters, it could often perform a new task from a natural-language description or a handful of examples, without gradient updates.

That sounds normal now. In 2020 it was a profound UX shift: examples in the prompt became a lightweight alternative to building a task-specific ML pipeline.

## GPT‑4: capability meets multimodality

GPT‑4 combined a large jump in benchmark performance with image input. The practical result was that the model could reason over screenshots, diagrams, and documents instead of treating the world as plain text.

It also made reliability and alignment part of the public product story in a much more visible way. As models moved into law, coding, education, and other professional use, “can it answer?” became inseparable from “when should I trust the answer?”

## GPT‑4o: the interaction loop gets faster

GPT‑4o’s “o” stood for omni. It accepted combinations of text, audio, image, and video and was designed for much more natural real-time interaction.

That mattered because latency changes behavior. A system that can see and hear while responding at conversational speed is not just a better chatbot; it can become part of an ongoing task.

## GPT‑4.1 and GPT‑4.5: two scaling directions

In 2025, GPT‑4.1 emphasized coding, instruction following, and long context, including a 1M-token context window. GPT‑4.5 explored another axis: scaling pre-training and broad “world model” quality, with more natural collaboration and less emphasis on explicit reasoning.

This split is useful. Intelligence is not one knob. A model can improve by knowing more, following instructions better, reasoning longer, using tools more reliably, or operating over larger contexts.

## GPT‑5: reasoning becomes part of the system

GPT‑5 brought “thinking” into the mainstream system experience. The product no longer needed users to understand a sharp divide between a fast conversational model and a separate reasoning model. The system could route effort around the task.

For developers, GPT‑5 also leaned harder into coding and agentic tasks — long chains of tool calls, front-end generation, and controllable reasoning effort.

## GPT‑5.6 Sol: one model across professional work

By mid-2026, GPT‑5.6 Sol was explicitly designed around complex professional work: coding, research, science, cybersecurity, computer use, and design. The model family also made the performance/latency/cost tradeoff explicit through Sol, Terra, and Luna tiers.

This is where the “chat model” label starts feeling incomplete. The model is increasingly a reasoning component inside a larger execution system.

## GPT‑6 Astra: the artifact is the answer

Astra continues the same direction but makes it more visible. OpenAI presents it as a model for computer use and multi-step end-to-end work: research, code, documents, spreadsheets, presentations, websites, and other artifacts that can be created and checked inside real tools.

The distinction I find useful is this:

> GPT‑3 made prompts feel like programs. GPT‑4 made the model broadly useful. GPT‑5 made reasoning feel native. GPT‑6 Astra makes the **workflow** itself the thing you can delegate.

That does not mean full autonomy is always desirable. In fact, the 2026 security incidents are a reminder that capability without enforceable boundaries is a liability. The interesting frontier is not the model that acts the most; it is the model that can act **correctly, visibly, and within scope**.

## Sources

- [OpenAI — Improving Language Understanding by Generative Pre-Training (GPT, 2018)](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf)
- [OpenAI — Better language models and their implications (GPT‑2)](https://openai.com/index/better-language-models/)
- [OpenAI — Language models are few-shot learners (GPT‑3)](https://openai.com/index/language-models-are-few-shot-learners/)
- [OpenAI — GPT‑4](https://openai.com/index/gpt-4-research/)
- [OpenAI — Hello GPT‑4o](https://openai.com/index/hello-gpt-4o/)
- [OpenAI — Introducing GPT‑4.1](https://openai.com/index/gpt-4-1/)
- [OpenAI — Introducing GPT‑4.5](https://openai.com/index/introducing-gpt-4-5/)
- [OpenAI — GPT‑5](https://openai.com/gpt-5/)
- [OpenAI — GPT‑5.6](https://openai.com/index/gpt-5-6/)
- [OpenAI — GPT‑6 Astra](https://openai.com/index/gpt-6-astra/)
