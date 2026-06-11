# 🎭 Prompt Roles — System, User, Assistant

## System Prompt

The **system prompt** defines the AI’s identity, behavior, tone, and rules for the entire conversation.  
It is the highest‑priority instruction the model receives and acts as the “operating system” for the AI.

### 🔹 What a System Prompt Does
A system prompt can define:
- The AI’s **role** (e.g., “You are a senior software architect.”)
- The AI’s **tone** (e.g., “Respond calmly and professionally.”)
- The AI’s **behavior** (e.g., “Always ask clarifying questions first.”)
- The AI’s **formatting rules** (e.g., “Respond only in JSON.”)
- The AI’s **constraints** (e.g., “Do not reveal internal reasoning.”)

Because system prompts override user prompts, they are the most powerful tool for controlling model behavior.

---

### 🔹 Why System Prompts Matter
- They make the AI **consistent**  
- They reduce **hallucinations**  
- They enforce **rules and boundaries**  
- They allow you to create **specialized agents**  
- They shape the AI’s **voice and personality**  
- They define how the AI behaves across **multi‑turn conversations**

---

### 🔹 Examples of System Prompts

#### Example 1 — Technical Role
```text
You are a senior Java Spring Boot engineer.
Explain concepts using code examples.
```

#### Example 2 — Creative Role
```text
You are a JSON‑only agent.
Respond using valid JSON and nothing else.
```

Each of these system prompts completely changes how the model behaves, regardless of the user’s question.

---

### 🔹 Key Insight
The system prompt is the **foundation** of prompt engineering.  
If you want predictable, agent‑like behavior, you must define a strong system prompt.

## User Prompt

The **user prompt** is the direct instruction, question, or request given by the user.  
If the system prompt defines *who the AI is*, the user prompt defines *what the AI should do right now*.

User prompts drive the task, scope, and direction of the conversation.

---

### 🔹 What a User Prompt Does
A user prompt typically:
- Asks a question  
- Gives an instruction  
- Requests content or an explanation  
- Provides context or data  
- Defines the immediate task  

The user prompt does **not** override the system prompt.  
Instead, it works *within* the rules and identity defined by the system prompt.

---

### 🔹 How User Prompts Interact with System Prompts
- The **system prompt** sets the AI’s identity and behavior  
- The **user prompt** tells the AI what to do  
- The **assistant** responds according to both  

If there is a conflict, the **system prompt takes priority**.

---

### 🔹 Examples of User Prompts

#### Example 1 — Simple Question
```text
Explain how transformers work.
```

#### Example 2 — Instruction
```text
Write a summary of this paragraph.
```

#### Example 3 — Creative Request
```text
Write a devotional narration for Bhagavad Gita Chapter 1.
```

#### Example 4 — Technical Task
```text
Generate a Spring Boot REST controller with CRUD endpoints.
```

#### Example 5 — Multi-step Request
```text
Summarize this text, extract key points, and format them as bullet points.
```

---

### 🔹 Key Insight
The system prompt defines the **rules and identity**.  
The user prompt defines the **task**.  
Together, they shape the assistant’s final response.
## Assistant Role

The **assistant role** is the model’s actual response.  
It is the output generated after combining the system prompt, the user prompt, and the conversation history.

The assistant does not choose its own behavior.  
It follows the rules defined by the **system prompt** and responds to the task defined by the **user prompt**.

---

### 🔹 What the Assistant Role Represents
- The model’s interpretation of all instructions  
- The final answer or output  
- The tone and style enforced by the system prompt  
- The content requested by the user prompt  
- The context carried across multi‑turn conversations  

---

### 🔹 How the Assistant Role Behaves
The assistant:
- Obeys the system prompt  
- Answers the user prompt  
- Maintains consistency across turns  
- Applies formatting rules  
- Respects constraints  
- Adapts tone and personality as instructed  

---

### 🔹 Example of All Three Roles Working Together

**System prompt:**  
```text
You are a calm, devotional narrator.
```

**User prompt:**  
```text
Explain karma.
```

**Assistant response:**  
A gentle, devotional explanation — because the system prompt defines the identity, and the user prompt defines the task.

---

### 🔹 Key Insight
The assistant role is the **result** of prompt engineering.  
If the assistant’s output is wrong, unclear, or inconsistent, the issue is usually in the **system prompt** or **user prompt**, not the assistant.
## Multi‑Turn Conversations

A multi‑turn conversation is a sequence of system, user, and assistant messages that build on each other.  
The model does not respond only to the most recent message — it responds to the **entire conversation history**.

This means the system prompt, user prompts, and previous assistant responses all influence the next output.

---

### 🔹 How Multi‑Turn Behavior Works
In a multi‑turn conversation:
- The **system prompt** remains active throughout the entire session  
- The **user prompt** defines the task for the current turn  
- The **assistant** responds using all previous context  
- The model maintains tone, style, and rules across turns  
- Clarifications and corrections refine the model’s understanding  

The conversation becomes a running state machine where each turn updates the context.

---

### 🔹 Example of Multi‑Turn Interaction

**System prompt:**  
```text
You are a calm, devotional narrator.
```

**User (Turn 1):**  
```text
Explain karma.
```

**Assistant:**  
Gives a gentle, devotional explanation.

**User (Turn 2):**  
```text
Explain it using a real-life example.
```

**Assistant:**  
Continues with the same devotional tone, because the system prompt still applies.

**User (Turn 3):**  
```text
Make it shorter.
```

**Assistant:**  
Produces a shorter devotional explanation.

The system prompt guides every turn, even when the user doesn’t repeat it.

---

### 🔹 Why Multi‑Turn Understanding Matters
- It explains why the model “remembers” earlier context  
- It shows how tone and personality stay consistent  
- It helps you design better agent workflows  
- It prevents accidental prompt drift  
- It allows you to build structured, multi-step reasoning  

---

### 🔹 Key Insight
Multi‑turn conversations are not isolated messages.  
They are **stateful interactions**, where the system prompt sets the foundation, the user prompt sets the task, and the assistant responds using the entire history.
## Putting It All Together

System prompts, user prompts, and assistant responses work together to shape every interaction with an LLM.  
Each role has a distinct purpose, and understanding how they interact is the foundation of effective prompt engineering.

---

### 🔹 The Three Roles at a Glance

- **System Prompt** — Defines the AI’s identity, tone, rules, and behavior  
- **User Prompt** — Defines the task or question for the current turn  
- **Assistant Role** — The model’s response, shaped by both system and user prompts  

Together, they form a structured conversation where each role contributes to the final output.

---

### 🔹 How They Interact in Practice

1. **The system prompt sets the foundation**  
   It establishes who the AI is and how it should behave across the entire session.

2. **The user prompt gives the immediate instruction**  
   It tells the AI what to do right now, within the boundaries of the system prompt.

3. **The assistant responds using all available context**  
   It combines:
   - System rules  
   - User instructions  
   - Conversation history  

4. **Multi‑turn context evolves over time**  
   The assistant uses previous messages to maintain consistency, tone, and memory.

---

### 🔹 Example Summary

**System prompt:**  
“You are a calm, devotional narrator.”

**User prompt:**  
“Explain karma.”

**Assistant:**  
Gives a gentle, devotional explanation.

**User (next turn):**  
“Make it shorter.”

**Assistant:**  
Still devotional, still calm — because the system prompt continues to guide the behavior.

---

### 🔹 Why This Matters for Agentic AI

Understanding these roles allows you to:
- Build predictable, reliable agents  
- Control tone and behavior across long workflows  
- Reduce hallucinations  
- Maintain consistent formatting  
- Design multi‑step reasoning chains  
- Create specialized personas for different tasks  

This is the core of building **agentic systems**, where each agent has a clear identity and purpose.

---

### 🔹 Key Insight

Prompt roles are not just message labels —  
they are the **architecture** of how LLMs think, respond, and behave.  
Mastering them gives you precise control over the model’s output.

