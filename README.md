# Python-Task-3
# Research Plan: Evaluating Open Source AI Model for Student Competence Analysis

## Approach to Identifying and Evaluating Models

To tackle the problem of analyzing student-written Python code and generating meaningful competence assessment prompts, I focused on open-source large language models (LLMs) available on Hugging Face. These models can process natural language and code-related data effectively. I selected **GPT-Neo 1.3B** by EleutherAI as the primary candidate because it is open-source, widely used, and provides the flexibility to generate natural language outputs from code inputs.

My evaluation strategy involves creating a simple prototype where the model takes a Python code snippet written by a student as input and outputs thoughtful prompts. Example prompts include:
- "What is the role of this function in the overall program?"
- "Can you explain the purpose of the loop condition here?"
- "Do you think this implementation covers all edge cases?"

I would test its applicability by running sample experiments using both correct and buggy Python code written by students. The generated prompts would be manually evaluated for relevance, depth, and the ability to probe conceptual understanding without giving direct solutions.

---

## Reasoning and Decision-Making

### What makes a model suitable for high-level competence analysis?
A suitable model should understand both code structure and semantics well enough to generate prompts that challenge the student’s conceptual understanding rather than merely pointing out syntax errors. It should encourage students to think critically about their implementation.

### How would I test whether a model generates meaningful prompts?
I would run controlled experiments using sample Python code examples covering various difficulty levels. I would evaluate outputs based on criteria such as:
- Relevance of prompts to the code.
- Whether prompts are general enough to apply to similar coding problems.
- Whether prompts are encouraging rather than technical or vague.

### Trade-offs between accuracy, interpretability, and cost
- Accuracy: Larger models like GPT-Neo can better understand context but require more computational resources.
- Interpretability: It is easier to interpret prompts than model internals, but results may sometimes be vague.
- Cost: Running large models is expensive in terms of memory and compute time, but GPT-Neo is open-source and reasonably optimized.

### Why I chose GPT-Neo
I chose GPT-Neo 1.3B because it provides a good balance of accessibility (open-source, Hugging Face hosting), versatility (it understands both code and language), and community support. Its limitation is that it may lack the precision of fine-tuned educational models designed specifically for code analysis, but it serves well for prototype-level competence assessment without additional costs.

---

## References
- GPT-Neo 1.3B by EleutherAI:  
https://huggingface.co/EleutherAI/gpt-neo-1.3B
