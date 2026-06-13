
The model processes **all of it** at once.  
If the total token count exceeds the limit:

### → The oldest messages are removed  
### → The model loses access to them  
### → The conversation may drift or forget instructions  

This process is called **context truncation**.

---

## Why Models “Forget”
Models don’t forget because they are confused.  
They forget because:

- The context window filled up  
- Older messages were pushed out  
- The model literally cannot see them anymore  

If it’s not inside the window, it does not exist to the model.

---

## Typical Context Window Sizes
Different models support different limits (e.g., 4k, 16k, 32k, 100k+ tokens).  
But the rule is always the same:

**If it doesn’t fit, it gets dropped.**

---

## Example of Context Truncation
Imagine a model with a 10‑token window.

Conversation:

1. “Hello” (2 tokens)  
2. “Explain gravity” (3 tokens)  
3. “Give an example” (3 tokens)  
4. “Make it shorter” (3 tokens)

Total = 11 tokens → exceeds the limit.

The model drops the oldest message:

**“Hello”**

Now the model sees only:

- Explain gravity  
- Give an example  
- Make it shorter  

This is why long conversations drift.

---

## How to Work WITH the Context Window

### 🔹 Keep system prompts short  
Long system prompts consume valuable space.

### 🔹 Summarize earlier turns  
Replace long history with compact summaries.

### 🔹 Reinforce key rules  
Repeat critical constraints in short form every few turns.

### 🔹 Use structured memory  
Store important facts outside the window and re-inject them when needed.

### 🔹 Avoid unnecessary verbosity  
Every token counts.

---

## Why This Matters for Agentic AI
Your agents will:

- Run long workflows  
- Pass messages between each other  
- Maintain state  
- Follow long instructions  
- Generate long outputs  

To make them reliable, you must:

- Control context size  
- Summarize intelligently  
- Reinforce key rules  
- Use memory modules  
- Prevent prompt drift  

Understanding context windows is essential for building stable multi-agent systems.

---

## Key Takeaway
A context window is not “memory.”  
It is simply the **visible text buffer** the model can process at once.  
If something falls out of the window, the model cannot use it —  
which is why managing context is one of the most important skills in LLM engineering.
