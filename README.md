<h1 align="center"><img src="media/logo.svg" width="640" alt="Awesome Socratic Tutor"></h1>

<p align="center">
<a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
<a href="LICENSE"><img src="https://img.shields.io/badge/licence-CC0_1.0-lightgrey.svg" alt="Licence: CC0 1.0"></a>
<a href="#contributing"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs welcome"></a>
<a href="https://github.com/nodo-labs-uk/awesome-socratic-tutor/commits/main"><img src="https://img.shields.io/github/last-commit/nodo-labs-uk/awesome-socratic-tutor" alt="Last commit"></a>
</p>

A list of resources on Socratic tutoring: the method, the research on why tutoring works, and the prompts, models and apps that make a language model teach by asking questions.

A Socratic tutor answers with a question. It finds out what you already know, asks you to explain your reasoning, and lets you find the gap yourself.

## Contents

- [The method](#the-method)
- [Learning science](#learning-science)
- [Research on LLM tutors](#research-on-llm-tutors)
- [Datasets and models](#datasets-and-models)
- [Prompts and skills](#prompts-and-skills)
- [Terminal apps](#terminal-apps)
- [Web apps and products](#web-apps-and-products)
- [Spaced repetition](#spaced-repetition)
- [Contributing](#contributing)

## The method

- [Meno](https://www.gutenberg.org/ebooks/1643) by Plato. Socrates leads an enslaved boy through a geometry problem with questions alone. It is the best-known example of the method. Free on Project Gutenberg.
- [Socrates](https://plato.stanford.edu/entries/socrates/), Stanford Encyclopedia of Philosophy. Who Socrates was and how the Socratic dialogues work.
- [The Thinker's Guide to Socratic Questioning](https://www.criticalthinking.org/store/products/art-of-socratic-questioning/231) by Richard Paul and Linda Elder. A short book with a taxonomy of Socratic questions and annotated transcripts.
- [Socratic teaching](https://www.criticalthinking.org/pages/socratic-teaching/606), Foundation for Critical Thinking. A free page on how to run Socratic questioning in a classroom.

## Learning science

- [The 2 Sigma Problem](https://doi.org/10.3102/0013189X013006004) by Benjamin Bloom (1984). Students with a one-to-one tutor scored two standard deviations above students taught in a class. Most AI tutor papers cite it as their goal.
- [The relative effectiveness of human tutoring, intelligent tutoring systems, and other tutoring systems](https://doi.org/10.1080/00461520.2011.611369) by Kurt VanLehn (2011). A review that finds step-based tutoring systems come close to human tutors.

## Research on LLM tutors

- [LearnLM: Improving Gemini for Learning](https://arxiv.org/abs/2412.16429) (Google, 2024). Trains Gemini to follow teaching instructions in the system prompt. Expert raters preferred it to GPT-4o, Claude 3.5 Sonnet and the base Gemini 1.5 Pro.
- [Tutor CoPilot: A Human-AI Approach for Scaling Real-Time Expertise](https://arxiv.org/abs/2410.03017) (2024). A randomised trial where an LLM suggested guidance to human maths tutors during live sessions.
- [Enhancing Critical Thinking in Education by means of a Socratic Chatbot](https://arxiv.org/abs/2409.05511) (2024). Fine-tunes Llama 2 7B and 13B to ask Socratic questions on local hardware. In tests with a simulated student, it did better than standard chatbots at building critical thinking.
- [Boosting Large Language Models with Socratic Method for Conversational Mathematics Teaching](https://arxiv.org/abs/2407.17349) (2024). SocraticLLM and the SocraticMATH dataset of Socratic maths dialogues.
- [Discerning minds or generic tutors?](https://arxiv.org/abs/2508.06583) (2025). The GuideEval benchmark. It finds that LLMs often fail to change their guidance when a learner is confused.
- [SocraticAI: Transforming LLMs into Guided CS Tutors Through Scaffolded Interaction](https://arxiv.org/abs/2512.03501) (2025). A tutor for undergraduate computer science that asks for well-formed questions and limits daily use.

## Datasets and models

- [MathDial](https://github.com/eth-nlped/mathdial). About 3,000 tutoring dialogues where human teachers taught an LLM that played a student making mistakes. EMNLP Findings 2023 ([paper](https://arxiv.org/abs/2305.14536)).
- [SocraticLM](https://github.com/Ljyustc/SocraticLM). Code and data for a model trained to teach maths by Socratic dialogue (NeurIPS 2024).
- [socratic-llm](https://github.com/GiovanniGatti/socratic-llm). A training pipeline that fine-tunes Phi-3-mini-instruct to follow the Socratic method ([paper](https://ceur-ws.org/Vol-3879/AIxEDU2024_paper_26.pdf), AIxEDU 2024).

## Prompts and skills

- [socratic-tutor skill](https://github.com/janestreet/agent_skills/tree/master/socratic-tutor), Jane Street. An agent skill for Claude: a diagnostic, a skill map with levels 0 to 5, spaced review and a final assessment. MIT licence.
- [socratic-tutor prompts](https://git.fri.uni-lj.si/martin.vuk/socratic-tutor), University of Ljubljana. Prompts that turn a chatbot into a tutor, with a Socratic style and a Feynman style.

## Terminal apps

- [Socratui](https://github.com/nodo-labs-uk/socratui). A Rust TUI that runs the Jane Street socratic-tutor method against Claude, OpenAI, Hugging Face or a local llama.cpp model. It keeps a skill map and your learning history, and schedules concepts for spaced Socratic review. It also makes flashcards that you can review in the app or export to Anki. The keys are vim-style.
- [dint](https://github.com/safe049/dint). A Python tutor that will not give you the answer. It has long-term memory and SM-2 review.
- [LearnLock](https://github.com/MitudruDutta/learnlock). A Python CLI that argues with you: it looks for contradictions in your answers and feeds your score into SM-2 scheduling. MIT licence.
- [recode](https://github.com/ever-oli/recode). Spaced repetition for coding problems. You write the solution from memory, get AI hints, and compare with the reference in a diff.
- [alix](https://github.com/Alex6323/alix). A Rust flashcard tool with FSRS scheduling and a tutor you can ask about a card. It calls a model through a CLI such as Claude Code.

## Web apps and products

- [OpenTutor](https://github.com/zijinz456/OpenTutor). A self-hosted learning workspace. Upload material and it makes notes, quizzes, flashcards and an adaptive tutor.
- [Khanmigo](https://www.khanmigo.ai/), Khan Academy. A tutor tied to the Khan Academy curriculum that guides students without giving answers.
- [Claude for Education](https://www.anthropic.com/news/introducing-claude-for-education), Anthropic. Anthropic launched learning mode in April 2025. It guides the student with questions and holds back the answer. The learning style is now in Claude.ai and Claude Code.
- [ChatGPT study mode](https://techcrunch.com/2025/07/29/openai-launches-study-mode-in-chatgpt), OpenAI. Launched in July 2025. It works through custom system instructions on the existing models.
- [Gemini Guided Learning](https://blog.google/outreach-initiatives/education/guided-learning/), Google. Launched in August 2025. It uses the LearnLM work that Google built into Gemini 2.5.

## Spaced repetition

A Socratic session finds what you don't know. Spaced repetition stops you forgetting what you learnt.

- [Augmenting Long-term Memory](https://augmentingcognition.com/ltm.html) by Michael Nielsen. How he uses Anki to read papers and learn new fields.
- [How to write good prompts](https://andymatuschak.org/prompts/) by Andy Matuschak. How to write flashcards that test whether you understand an idea.
- [FSRS for Anki](https://github.com/open-spaced-repetition/fsrs4anki). The Free Spaced Repetition Scheduler, now built into Anki.

## Contributing

Open a pull request. Add one line per resource, in the right section, with a link and one or two sentences that say what it is. Check that the link works.

## Licence

[CC0 1.0](LICENSE). To the extent possible under law, the contributors have waived all copyright to this list.
