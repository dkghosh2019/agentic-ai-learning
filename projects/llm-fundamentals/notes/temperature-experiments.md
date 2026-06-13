# 🔥 Temperature — Controlling Creativity and Determinism in LLMs

## What Temperature Is
Temperature is the **creativity dial** of a language model.  
It controls how *random* or *deterministic* the model is when choosing the next token.

Low temperature → focused, predictable  
High temperature → creative, varied  

Temperature reshapes the probability distribution before sampling, influencing how likely the model is to pick rare vs common tokens.

---

## How Temperature Works (Conceptual)
Before generating each token, the model assigns probabilities to all possible next tokens.  
Temperature modifies these probabilities:

- **T < 1.0** → sharpens the distribution (more deterministic)  
- **T > 1.0** → flattens the distribution (more random)  

This changes how “bold” or “safe” the model behaves.

---

## Temperature Scale and Effects

| Temperature | Behavior | Best For |
|------------|----------|----------|
| **0.0** | Greedy, deterministic | Math, coding, extraction |
| **0.2–0.4** | Very focused | Technical explanations |
| **0.5–0.7** | Balanced, natural | General chat, teaching |
| **0.8–1.0** | Creative but coherent | Storytelling, narration |
| **1.2+** | Highly creative, chaotic | Brainstorming, poetry |

---

## Examples — Same Prompt, Different Temperatures

Prompt:  
**“Describe a sunrise.”**

### 🔹 Temperature 0.2
> “The sunrise is the moment when the sun appears above the horizon, producing warm light.”

### 🔹 Temperature 0.7
> “The sunrise paints the sky with soft oranges and pinks as the world slowly brightens.”

### 🔹 Temperature 1.2
> “The sun bursts awake, spilling wild ribbons of fire across the sky like a cosmic artist.”

Higher temperature → more imagery, metaphor, and risk-taking.

---

## Why Temperature Matters
Temperature affects:
- **Creativity**  
- **Determinism**  
- **Consistency**  
- **Brainstorming quality**  
- **Narration style**  
- **Agent behavior**  

For your projects:

- **Narrator agent** → T ≈ 0.8  
- **Analysis agent** → T ≈ 0.2  
- **Idea generator** → T ≈ 1.2  

---

## Experiments — Try These Yourself

### 🔹 Experiment 1 — Factual Prompt
Prompt:  
“Explain gravity in one sentence.”

Run it at T = 0.2, 0.7, 1.2  
Observe how the tone shifts from factual → descriptive → poetic.

---

### 🔹 Experiment 2 — Creative Prompt
Prompt:  
“Write a metaphor for patience.”

Try T = 0.5, 1.0, 1.5  
Notice how metaphors become more unusual as temperature rises.

---

### 🔹 Experiment 3 — Coding Prompt
Prompt:  
“Write a Python function that reverses a string.”

Try T = 0.0 vs T = 1.0  
See how higher temperature introduces unnecessary creativity.

---

## Key Takeaways
- Temperature controls **randomness** in token selection  
- Low temperature = accuracy and consistency  
- High temperature = creativity and exploration  
- Temperature does **not** change intelligence — only style  
- Different agents should use different temperatures  
