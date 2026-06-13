# 🧠 Context Windows — How LLMs Remember and Forget

## What a Context Window Is
A **context window** is the maximum amount of text (measured in tokens) that a language model can process at once.  
It includes:

- The system prompt  
- All previous user messages  
- All previous assistant messages  
- Hidden formatting tokens  
- The current user message  

If the total exceeds the model’s limit, older messages are **dropped**.  
Once dropped, the model cannot see or use them anymore.

This is the primary reason LLMs “forget” earlier parts of a conversation.

---

## Why Context Windows Matter
Understanding context windows helps you:

- Prevent accidental loss of instructions  
- Build long-running, reliable agents  
- Structure prompts for stability  
- Avoid hallucinations caused by truncation  
- Design memory systems  
- Manage multi-step workflows  

The context window is the backbone of how transformers operate.

---

## How Context Windows Work Internally
Every time you send a message, the model receives a full sequence:

