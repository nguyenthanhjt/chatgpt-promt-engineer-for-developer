# Section 2: Guidelines

//TODO: restructure, refactor content

## Overview

The "Guidelines" section of the course outlines essential principles for effective prompt engineering when working with Large Language Models (LLMs). This section provides practical strategies to help developers create prompts that yield more accurate and useful responses from LLMs.

## Principles of Prompting

- **The Importance of Clear Instructions:**
  - One of the most critical factors in obtaining desired outputs from LLMs is providing clear and specific instructions. Ambiguity in prompts often leads to less accurate or irrelevant responses.
  - Think of interacting with an LLM as similar to instructing a person who is knowledgeable but unfamiliar with your specific task. Clear communication is key.

### **Principle 1: Write Clear and Specific Instructions:**

- **Precision in Prompts:** The more detailed and precise your prompt, the more likely you are to get a useful response. Avoid vague instructions and instead define exactly what you need.
- **Context Matters:** Providing context within your prompts helps the LLM understand the scope and focus of the task. For example, specifying whether you want a formal summary or a casual explanation can significantly impact the quality of the output.

1. Tactic 1: Use delimiters

   - Tripple quotes: `"""`
   - Triple backticks: ```
   - Triple dashes: `---`,
   - Angle brackets: `<>`,
   - XML tags: `<tag></tag>`

   ![x](../resources/images/img-01.png)

2. Tactic 2: Ask for structured output

   - HTML, Json
   - Example: refer [02-guidelines.py](../code/02-guidelines.py)

      ```prompt
      Generate a list of three made-up book titles along with their authors and genres. Provide them in JSON format with the following keys: book_id, title, author, genre.
      ```

3. Tactic 3: Check whether conditions are satisfied

   - Check assumptions required to do the task

4. Few-shot prompting

   - Give successful examples of completing task.
   - Then ask the model to perform the task
   - Example:

    ```python
    Your task is to answer in d consistent style.

    <child>: Teach me about patience.

    ‹grandparent>: The river that carves the deepest valley flows from a modest spring; the grandest symphony originates a from a single note; the most intricate tapestry begins with a solitary thread.

    <child>: Teach me about resilience. Y
    ```

### **Principle 2: Give the model time to Think:**

- **Iterative Refinement:** Allowing the LLM to process and refine its responses by asking follow-up questions or making incremental adjustments to the prompt can lead to more refined and accurate results.
- **Patience in Interaction:** Avoid rushing through interactions with the LLM. Giving the model time to "think" and process can improve the quality of its responses.

- **Practical Application of Guidelines:**
  - These principles aren't just theoretical; they are practical tools to help you get the most out of LLMs in real-world applications. By following these guidelines, you can enhance the accuracy, relevance, and utility of the responses you receive from the model.

1. Tactic 1: Specify the steps to complete a task

   - Step 1: ...
   - Step 2: ...
   - ...
   - Step N: ...
  
2. Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion

   - Example: refer [Find the Section:[### Princle 2 - Tactic 2 - Example] here](../notebook/02-guideline.ipynb)

## Model Limitations

- Hallucination
- Makes statements that sound plausible but are not true

```txt
Tell me about AeroGlide UltraSlim Smart Toothbrush by Boie

- Reducing hallucinations:
  - First find relevant information, then answer the question based on the relevant information

```

## Summary

The "Guidelines" section emphasizes the importance of clarity, structure, and iterative refinement in prompt engineering. By being clear and specific in your instructions, structuring your prompts effectively, and allowing the LLM time to think, you can significantly improve the quality of the responses you get from these models. These principles are foundational for any developer looking to harness the full potential of LLMs in their projects.
