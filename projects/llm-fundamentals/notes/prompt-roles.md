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

