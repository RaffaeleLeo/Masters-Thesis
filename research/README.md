# Ongoing Research: Stable Observer Network (SON)

This folder contains notes and experimentation logs done *after* the completion of the thesis project. These are unofficial experiments done in my free time to explore new ways of improving reward modeling for reinforcement learning in visualization recommendation systems.

---

## Experiment Highlights

### 1. Upgrading to LLaMA 3.0
- Tried switching from LLaMA 2.0 → 3.0 for base fine-tuning
- Found that naive transfer hurt performance — LLaMA 3.0 often generated extra explanations or code
- Fix: **Simplifying prompts** (no explanation/context, just instruction/response) helped regain focus

---

### 2. Chain-of-Thought Prompting
- Made outputs worse for this task
- Adding thought steps distracted the model from Vega-Zero grammar generation

---

### 3. ChatGPT-Assisted Reward Generation
- Used ChatGPT as a “reward judge” for PPO — prompting it with model outputs and PPO metrics
- Trained BERT on GPT-generated rewards

**Results:**
- 14% increase in outputs compiling
- 19% increase in selected data being correct
- No real improvement in axis label accuracy — next area to explore

---

## Reflections
While the baseline needs more work, this work shows that:
- ChatGPT can help guide learning with more nuanced rewards
- Prompt engineering dramatically affects output structure and quality
- There’s still lots of headroom for reward-based improvements

---

## File Index
- [`continued_esearch.pdf`](./continued_research.pdf): Full notes and figures from my research log
- [`gpt_reward_prompt.txt`](./gpt_reward_prompt.txt): Prompt used with GPT as a reward judge