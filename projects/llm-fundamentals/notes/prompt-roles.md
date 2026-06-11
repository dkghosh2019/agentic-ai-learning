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

