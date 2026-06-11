## 🧩 Tokens — Understanding the Building Blocks of LLMs

## What Are Tokens?
Tokens are small pieces of text that an LLM reads or writes.  
They can be whole words, parts of words, spaces, punctuation, or symbols.  
LLMs do not process text like humans — they process **tokens**, one at a time.

---

## Tokenization Experiment
Sentence tested:  
**“I love learning about AI agents.”**

Tokenized into:
```code
["I", " love", " learning", " about", " AI", " agents", "."]
```

Token count: **7**

This simple experiment shows how LLMs break text into smaller units.

---

## How Tokenization Works
Tokenization is the process of breaking text into small pieces (tokens) that an LLM can understand.  
Different models use different tokenization algorithms, but the goal is the same:  
**convert raw text into numerical units the model can process.**

### 🔹 Byte Pair Encoding (BPE)
One of the most common tokenization methods used in modern LLMs.

How it works:
- Starts with individual characters  
- Finds the most frequent pairs of characters  
- Merges them into larger units  
- Repeats until a vocabulary is built  

Example (conceptual):
- "u" + "n" → "un"  
- "believ" + "able" → "believable"  

Why BPE is useful:
- Efficient for English  
- Handles rare words by breaking them into subwords  
- Keeps vocabulary size manageable  

### 🔹 WordPiece
Used by models like BERT.

How it works:
- Similar to BPE but uses a **probability-based** approach  
- Chooses merges that maximize the likelihood of the training data  

Example:
- "un" + "##believable"  
(“##” indicates continuation of a word.)

Why WordPiece is useful:
- Great for languages with many word forms  
- Handles unknown words gracefully  

### 🔹 SentencePiece
Used by models like T5 and many multilingual models.

How it works:
- Treats the entire input as a raw stream of characters  
- Does not rely on whitespace  
- Works well for languages without spaces (e.g., Japanese, Chinese)  

Why SentencePiece is useful:
- Language‑agnostic  
- Ideal for multilingual models  

### 🔹 Why Tokenization Exists
LLMs cannot read raw text.  
They only understand **numbers**, so tokenization converts:

**text → tokens → numerical IDs**

Example (conceptual):

---

## Why Tokens Matter
- **Context window limits:** Models can only read a fixed number of tokens  
- **Cost:** More tokens = higher cost (for paid models)  
- **Output length:** Token limits control how long responses can be  

---

## Examples — Token Counts for Different Sentences

### 🔹 Example 1
Sentence:  
"I love learning about AI agents."

Tokens:  
["I", " love", " learning", " about", " AI", " agents", "."]

Token count: **7**

---

### 🔹 Example 2
Sentence:  
"Hello world!"

Tokens:  
["Hello", " world", "!"]

Token count: **3**

---

### 🔹 Example 3
Sentence:  
"Unbelievable performance by the model."

Tokens (approximate):  
["Un", "believ", "able", " performance", " by", " the", " model", "."]

Token count: **8**

---

### 🔹 Example 4
Sentence:  
"Large Language Models are transforming the world."

Tokens (approximate):  
["Large", " Language", " Models", " are", " transforming", " the", " world", "."]

Token count: **8**

---

### 🔹 Example 5
Sentence:  
"Tokenization affects cost, context, and output length."

Tokens (approximate):  
["Token", "ization", " affects", " cost", ",", " context", ",", " and", " output", " length", "."]

Token count: **11**

---

### 🔹 What These Examples Show
- Short sentences can still have many tokens  
- Long words often break into multiple subword tokens  
- Spaces and punctuation matter  
- Token counts vary by tokenizer (BPE, WordPiece, SentencePiece)  

---

## Experiments — My Tokenization Tests
Use this section to document any additional tokenization tests you run in the future.

---

## Key Takeaways
- LLMs read **tokens**, not words  
- Even simple sentences break into multiple tokens  
- Tokenization affects cost, memory, and prompt design  
- Understanding tokens helps you write better prompts  


