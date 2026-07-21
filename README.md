### Hi, I'm Orazio 👋

I'm an MSc student in Computational Linguistics at the University of Turin, with a humanities background (BA in Film & Media Studies, 110/110 *cum laude*). I work where language meets AI: NLP, corpus linguistics, and how technical communities actually use words.

The slightly unusual part: I use AI coding tools (Claude Code, Codex, Antigravity) hard, every day, as a real workflow, and I've completed 10 of Anthropic's own courses to back it up, including Building with the Claude API, Claude Code in Action, and Introduction to Subagents. Right now I'm learning the ML underneath from scratch, in public.

The common thread is empirical AI safety: evaluating and interpreting agentic systems, in setups where the results are checkable.

**What I work on**

- LLM evaluation and interpretability. My MSc thesis (topic locked June 2026) asks whether a model's internal state, read through pretrained sparse autoencoders, can warn that a multi-agent dialogue is about to collapse before the failure is visible in the text. The harness measures lead time and calibration against honest text baselines, runs entirely on an M3 Pro, and treats collapse-onset annotation (with inter-annotator agreement) as a research question in its own right, not an afterthought.
- Coding-agent failure evals. [agent-failure-eval-bench](https://github.com/oraziooztas/agent-failure-eval-bench) is a public task set for studying how coding agents actually break: 10 task specifications, 3 executable fixtures with hidden checks, a failure taxonomy, a grading rubric, and redacted trace evidence from a small cross-model pilot. The claims are deliberately narrow. The three fixtures are disclosed examples, not an unseen holdout, and the pilot is evidence about eval design rather than a ranking of models.
- Eval infrastructure. [agent-eval-harness](https://github.com/oraziooztas/agent-eval-harness) is the runner underneath: it turns hidden-check separation into a structural invariant rather than a convention. The agent only ever sees the public tests; grading happens in a clean room with the hidden tests pulled from the fixture, so an agent that rewrites its own tests moves its grade by nothing. Every run records the SHA-256 of the hidden set, and it imports the bench's disclosed fixtures (ADR-001), so the taxonomy and the runner are one pipeline. Stdlib-only runtime, 94% test coverage.
- Judge reliability. The LLM-as-a-judge question I was scoping earlier didn't die, it became [dark-current-mlx](https://github.com/oraziooztas/dark-current-mlx): a local, Apple Silicon test for hidden position bias in small judge models.
- Corpus linguistics. My current paper looks at how the word *agent* changed meaning between two ML eras, comparing arXiv abstracts from 2017-2018 (the reinforcement-learning era) and 2024 (the LLM-agent era). Python for the data, R for the stats.
- Before this: a bibliometric case study of the AI/neural-networks field, and a BA thesis on artificial intelligence in science-fiction cinema and society, including AI alignment.

**Thesis, in one breath**

Can sparse-autoencoder features fire an alarm a few turns before a multi-agent conversation loops, escalates, drifts or stonewalls? Detection, not steering: calibrated warning scores, lead time at a fixed false-positive rate, and an annotation protocol for when the collapse actually began. Design doc and feasibility spike are done (SAE inference works on consumer hardware); real-dialogue experiments run through my exchange semester. The eval harness and an inter-annotator agreement toolkit go public after one more review pass.

**Learning right now (and posting about it)**

- Working through the ARENA curriculum on my own: tensor ops now, toy SAEs next
- Reading ML papers properly, one at a time, notes in the open
- Math foundations (linear algebra, statistics) underneath it all

**Tools I actually use**

Python (uv, ruff, pytest, mypy), MLX and sae_lens on Apple Silicon, R for stats (chi-square, effect sizes), regex, corpus tools (Sketch Engine, AntConc, KWIC), the arXiv API, and a lot of AI-augmented development (Claude Code, Codex, Antigravity).

---

📫 [Email](mailto:orazio.oztas@gmail.com) · [LinkedIn](https://www.linkedin.com/in/orazio-oztas-a48848232/) · [X](https://x.com/OrazioOzta76081)

Heading to UCLouvain (Belgium) for an exchange semester in September 2026. Open to NLP and AI internships for summer 2027.
