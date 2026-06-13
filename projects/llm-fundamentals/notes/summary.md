# 📘 Milestone Summary — LLM Fundamentals

This milestone covered the foundational concepts required to understand how large language models operate, how they generate text, and how to control their behavior.  
These notes form the base for all future agentic AI work.

---

## 🧩 1. Tokens — The Building Blocks of LLMs
- Tokens are the smallest units a model reads and writes.  
- Everything (text, punctuation, spaces) is converted into tokens.  
- Token count determines:
  - Cost  
  - Speed  
  - Context window usage  
  - Truncation behavior  
- Understanding tokens helps you design efficient prompts and avoid overflow.

---

## 🎭 2. Prompt Roles — System, User, Assistant
### **System Prompt**
Defines the AI’s identity, tone, rules, and constraints.

### **User Prompt**
Defines the task or question for the current turn.

### **Assistant Role**
The model’s actual response, shaped by system + user + history.

Together, these roles form the structure of every LLM interaction.

---

## 🔁 3. Multi‑Turn Conversations
- LLMs respond to the **entire conversation history**, not just the last message.  
- The system prompt remains active across all turns.  
- Context evolves like a state machine.  
- Clarifications refine the model’s understanding.  
- Multi‑turn design is essential for building reliable agents.

---

## 🔥 4. Temperature — Creativity vs Determinism
Temperature controls randomness in token selection.

- **Low temperature (0.0–0.4)** → deterministic, focused  
- **Medium (0.5–0.7)** → balanced, natural  
- **High (0.8–1.5)** → creative, exploratory  

Temperature affects *style*, not intelligence.  
Different agents require different temperatures.

---

## 🧠 5. Context Windows — How Models Remember and Forget
A context window is the maximum number of tokens the model can process at once.

It includes:
- System prompt  
- All previous messages  
- Current message  

If the total exceeds the limit, older messages are **dropped** (context truncation).  
This is why models “forget.”

Managing context is essential for:
- Long workflows  
- Multi-agent systems  
- Stable reasoning  
- Preventing drift  

---

## 🏗️ 6. Why These Concepts Matter for Agentic AI
This milestone gives you the tools to:

- Control model behavior  
- Maintain consistency across long tasks  
- Prevent forgetting  
- Balance creativity and accuracy  
- Build structured, reliable agents  
- Design prompts that scale  

These fundamentals are the backbone of every advanced LLM system you will build.

---

## ⭐ Key Takeaway
Mastering tokens, prompt roles, temperature, and context windows gives you **full control** over how an LLM thinks, responds, and behaves.  
This milestone establishes the foundation for deeper topics like reasoning patterns, memory systems, and multi-agent architectures.
