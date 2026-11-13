<h1 align="center">
	<a href="https://plato.stanford.edu/entries/socrates/"><img src="media/logo.svg" width="640" alt="Awesome Socratic Tutor"></a>
	<br>
	<a href="https://github.com/sindresorhus/awesome"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
</h1>

<p align="center">
	<a href="contributing.md"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome"></a>
	<a href="https://github.com/nodo-labs-uk/awesome-socratic-tutor/commits/main"><img src="https://img.shields.io/github/last-commit/nodo-labs-uk/awesome-socratic-tutor" alt="Last commit"></a>
</p>

> Resources on Socratic tutoring: the method, the research on why tutoring works, and the prompts, models and apps that make a language model teach by asking questions.

A Socratic tutor answers with a question. It finds out what you already know, asks you to explain your reasoning, and lets you find the gap yourself.

## Contents

- [The method](#the-method)
- [Learning science](#learning-science)
- [Research on LLM tutors](#research-on-llm-tutors)
- [Datasets and models](#datasets-and-models)
- [Prompts and skills](#prompts-and-skills)
- [Terminal apps](#terminal-apps)
- [Web apps and products](#web-apps-and-products)

## The method

- [Meno](https://www.gutenberg.org/ebooks/1643) - Plato's dialogue in which Socrates leads an enslaved boy through a geometry problem with questions alone. It is the best-known example of the method. Project Gutenberg has it for free.
- [Socrates](https://plato.stanford.edu/entries/socrates/) - Stanford Encyclopedia of Philosophy entry on who Socrates was and how the Socratic dialogues work.
- [The Thinker's Guide to Socratic Questioning](https://www.criticalthinking.org/store/products/art-of-socratic-questioning/231) - Short book by Richard Paul and Linda Elder, with a taxonomy of Socratic questions and annotated transcripts.
- [Socratic teaching](https://www.criticalthinking.org/pages/socratic-teaching/606) - Free page from the Foundation for Critical Thinking on how to run Socratic questioning in a classroom.

## Learning science

- [The 2 Sigma Problem](https://doi.org/10.3102/0013189X013006004) - Benjamin Bloom, 1984. Students with a one-to-one tutor scored two standard deviations above students taught in a class. Most AI tutor papers cite it as their goal.
- [The relative effectiveness of human tutoring, intelligent tutoring systems, and other tutoring systems](https://doi.org/10.1080/00461520.2011.611369) - Kurt VanLehn, 2011. A review that finds step-based tutoring systems come close to human tutors.

## Research on LLM tutors

- [LearnLM: Improving Gemini for Learning](https://arxiv.org/abs/2412.16429) - Google, 2024. Trains Gemini to follow teaching instructions in the system prompt. Expert raters preferred it to GPT-4o, Claude 3.5 Sonnet and the base Gemini 1.5 Pro.
- [Tutor CoPilot: A Human-AI Approach for Scaling Real-Time Expertise](https://arxiv.org/abs/2410.03017) - 2024. A randomised trial where an LLM suggested guidance to human maths tutors during live sessions.
- [Enhancing Critical Thinking in Education by means of a Socratic Chatbot](https://arxiv.org/abs/2409.05511) - 2024. Fine-tunes Llama 2 7B and 13B to ask Socratic questions on local hardware. In tests with a simulated student, it did better than standard chatbots at building critical thinking.
- [Boosting Large Language Models with Socratic Method for Conversational Mathematics Teaching](https://arxiv.org/abs/2407.17349) - 2024. SocraticLLM and the SocraticMATH dataset of Socratic maths dialogues.
- [Discerning minds or generic tutors?](https://arxiv.org/abs/2508.06583) - 2025. The GuideEval benchmark. It finds that LLMs often fail to change their guidance when a learner is confused.
- [SocraticAI: Transforming LLMs into Guided CS Tutors Through Scaffolded Interaction](https://arxiv.org/abs/2512.03501) - 2025. A tutor for undergraduate computer science that asks for well-formed questions and limits daily use.

## Datasets and models

- [MathDial](https://github.com/eth-nlped/mathdial) - About 3,000 tutoring dialogues where human teachers taught an LLM that played a student making mistakes. EMNLP Findings 2023 ([paper](https://arxiv.org/abs/2305.14536)).
- [SocraticLM](https://github.com/Ljyustc/SocraticLM) - Code and data for a model trained to teach maths by Socratic dialogue. NeurIPS 2024.
- [socratic-llm](https://github.com/GiovanniGatti/socratic-llm) - Training pipeline that fine-tunes Phi-3-mini-instruct to follow the Socratic method. AIxEDU 2024 ([paper](https://ceur-ws.org/Vol-3879/AIxEDU2024_paper_26.pdf)).
- [Socratic Debugging Benchmark](https://github.com/taisazero/socratic-debugging-benchmark) - Dataset of buggy Python programs with Socratic dialogues that guide a novice to find and fix the bug, plus the tool used to write them. BEA 2023 ([paper](https://aclanthology.org/2023.bea-1.57/)).

## Prompts and skills

- [socratic-tutor skill](https://github.com/janestreet/agent_skills/tree/master/socratic-tutor) - Jane Street's agent skill for Claude: a diagnostic, a skill map with levels 0 to 5, spaced review and a final assessment. `MIT`.
- [socratic-tutor prompts](https://git.fri.uni-lj.si/martin.vuk/socratic-tutor) - Prompts from the University of Ljubljana that turn a chatbot into a tutor, with a Socratic style and a Feynman style.
- [Socrates Skill](https://github.com/bevibing/socrates-skill) - Agent skill that never answers and only asks. It works on code, documents, API docs and config files. `MIT`.
- [learn-codebase](https://github.com/ktaletsk/learn-codebase) - Agent skill that teaches you a codebase by questioning. It makes you predict before it reveals an answer, and keeps a journal of what you know and what you are still bluffing. `MIT`.
- [think-before-code](https://github.com/Far-200/think-before-code) - Socratic agent skills for data structures, algorithms and software-engineering judgement, with modes for dry runs, complexity, debugging, test design and mock interviews. `MIT`.
- [Learn Anything](https://github.com/ChenChenyaqi/learn-anything) - Generates skills and commands that turn 30+ AI coding tools into a Socratic tutor. It adds a knowledge map, TDD-style exercises, quizzes and a web dashboard. `TypeScript` `MIT`.

## Terminal apps

- [Socratui](https://github.com/nodo-labs-uk/socratui) - TUI that runs the Jane Street socratic-tutor method against Claude, OpenAI, Hugging Face or a local llama.cpp model. It keeps a skill map and your learning history, and schedules concepts for spaced Socratic review. It also makes flashcards that you can review in the app or export to Anki. The keys are vim-style. `Rust` `MIT`.
- [dint](https://github.com/safe049/dint) - Tutor that will not give you the answer. It has long-term memory and SM-2 review. `Python` `MIT`.
- [LearnLock](https://github.com/MitudruDutta/learnlock) - CLI that argues with you: it looks for contradictions in your answers and feeds your score into SM-2 scheduling. `Python` `MIT`.
- [recode](https://github.com/ever-oli/recode) - Spaced repetition for coding problems. You write the solution from memory, get AI hints, and compare with the reference in a diff. `Python` `MIT`.
- [alix](https://github.com/Alex6323/alix) - Flashcard tool with FSRS scheduling and a tutor you can ask about a card. It calls a model through a CLI such as Claude Code. `Rust` `MIT/Apache-2.0`.
- [Socrate](https://github.com/Haaaiawd/Socrate) - CLI that teaches programming by Socratic dialogue, from a course outline or your own PDFs and notes. It saves progress and reviews your code by asking questions. Its docs are in Chinese. `Python` `Apache-2.0`.

## Web apps and products

- [OpenTutor](https://github.com/zijinz456/OpenTutor) - Self-hosted learning workspace. Upload material and it makes notes, quizzes, flashcards and an adaptive tutor. `Python` `MIT`.
- [DeepTutor](https://github.com/HKUDS/DeepTutor) - Personal tutor from HKU, with a desktop app and a CLI. Its EduHub shares teaching skills, including Socratic tutors. `Python` `Apache-2.0`.
- [Bloom](https://github.com/Li-Evan/Bloom) - Tutor named after Bloom's 2 sigma result. It writes a syllabus, gives one lesson at a time and reads your notes to shape the next one. It runs as a Claude Code skill or a web app. `JavaScript` `MIT`.
- [Khanmigo](https://www.khanmigo.ai/) - Khan Academy's tutor, tied to its curriculum. It guides students without giving answers.
- [Claude for Education](https://www.anthropic.com/news/introducing-claude-for-education) - Anthropic launched learning mode in April 2025. It guides the student with questions and holds back the answer. The learning style is now in Claude.ai and Claude Code.
- [ChatGPT study mode](https://techcrunch.com/2025/07/29/openai-launches-study-mode-in-chatgpt) - OpenAI launched it in July 2025. It works through custom system instructions on the existing models.
- [Gemini Guided Learning](https://blog.google/outreach-initiatives/education/guided-learning/) - Google launched it in August 2025. It uses the LearnLM work that Google built into Gemini 2.5.

## Contributing

Suggestions are welcome. Read the [contribution guidelines](contributing.md) first.
