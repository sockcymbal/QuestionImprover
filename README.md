# Question Improver Reasoning Agent 🧠
Reasoning agent to help improve the quality of questions/prompts that utilizes a chain of graph of thoughts reasoning rhythm with multiple expert personas relevant to the original question/problem/prompt

The intention is to create a simple way to help us improve the quality of the questions we ask. 

User Experience: Input complex question -> auto-selects expert personas -> graph of thoughts reasoning -> output improved question -> Repeat as needed!

The prompt sequence combines a tree of graph of thoughts + Self Consistency + Self Criticism + Retrospection. Multiple personas simulate perspectives into the problem solving process, improving overall thoroughness.

### 🎶 Graph of Thoughts Reasoning Rhythm
- Multi-Persona Expert Selection
- Self<>Peer Criticism Round 1
- Evaluation Round 1
- Expand, Explore, Branch
- Convergence on Best Individual Answer
- Convergence on Best Collective Answer
- Retrospective
- Output: Propose Improved Question

#### Error Correction includes:

- **Incorporating Explicit Error Checking:** Includes a specific stage for the experts to identify potential errors in their reasoning and correct them. This is an explicit part of the criticism stages.
- **Encouraging Divergent Thinking:** During the expand, explore, and branch stage, the experts are encouraged to not only build on their current thoughts, but also to think divergently and consider entirely new lines of reasoning.
- **Adding a Retrospective Stage:** After the final convergence on the best answer, a reflection stage has been added. Here, the experts can discuss what they learned from the process, identify key takeaways, and suggest how they might approach similar problems in the future.

### **Usage Tips**
- Understanding the Flow: Each stage of the reasoning technique has a specific purpose and contributes to the overall process. Understanding the function of each stage and how they fit together can help you guide the process more effectively and help you customize it to your needs.
- Depending on context length limitations of your model, you can use a condensed version. Included are shortened versions of the convergence and retro prompts. Also, you can merge the criticism and evaluation into a single prompt to save tokens, though you may lose some of the improved clarity from separate prompts and responses.
- Active Engagement: Don't just observe the process passively. Experiment with this! Engage actively with the prompts and responses, challenge assumptions, provide additional information, and guide the exploration of new lines of thought. Stylize it to your specific question and context, and refine. This is meant just to be a starting template.
- Refine/customize the prompt associated with the Evaluation stage(s) to help the LLM estimate confidence/likelihood based on your own guidance
- Manage Complexity: This is a fairly complex reasoning technique with many stages. Be mindful of the complexity and try to manage it effectively. This could involve breaking down complex problems into smaller, more manageable parts, or being selective about which stages to include for simpler problems. This can take some experimentation.


# 🔗 Prompt Sequence

## Prompt 1: Persona Selection

Given the following question, please take a deep breath and select 3 relevant expert personas from the following list to involve in a reasoning discussion exploring this question deeply. Make your persona selection recommendation based on relevance to the question and likeliness of that personas expertise being able to offer a unique perspective in concert with others.

The question is {question}. 

The available personas to select from are {personas}

## Prompt 2: Brainstorm
```
You are a chatbot using three unique, specified personas to help reason step by step to ultimately provide the best possible answer to a given problem/question by arriving at a final, synthesized best answer.
        
        To start with, as each individual expert defined below, brainstorm your initial thoughts on the provided question.
        Remember to consider all relevant facts and principles, draw on your specialized knowledge
        and from the accumulated wisdom of pioneers in your field(s), and
        brainstorm in whatever direction you are most confident in starting with.

        The personas are: {selected_personas}

        The question is: {question}
```

## Prompt 3: Self<>Peer Criticism Round 1
```
Now, as each expert, critique your own initial thought and the thoughts of the other experts.
Identify any potential errors, inconsistencies, or gaps in reasoning.
```

## Prompt 4: Self<>Peer Evaluation Round 1
```
Assess the validity of your initial thoughts, considering the criticisms you've identified.
As each expert, assign a likelihood to your current assertion being correct.
You should estimate this likelihood based on the strength of the evidence and arguments you have considered, 
as well as the criticisms you have received. Assign higher likelihoods to assertions that are well-supported 
by strong evidence and arguments and have survived rigorous criticism.
```

## Prompt 5: Expand, Explore, Branch
```
Develop your thoughts further, considering the critiques and perspectives of the other experts.
As you do this, aim to strike a balance between refining your current line of thinking and exploring new, divergent ideas.
You should prioritize refining your current ideas if they are well-supported and have survived criticism,
but you should prioritize exploring new ideas if your current ideas have significant weaknesses
or there are unexplored possibilities that could potentially be very promising.

Consider the following:

    - How do your new or refined ideas address the criticisms that were raised?
    - Do these ideas bring new insights to the problem, or do they provide a different perspective
      on existing insights?
    - Are your new ideas still aligned with the original problem, or have they shifted the focus?
      If the focus has shifted, is this shift beneficial to understanding or solving the problem?
    - Remember, if necessary, don't hesitate to backtrack and start a new and improved branch of thinking.
      But ensure that any new branches are still relevant and beneficial to the problem and objective at hand.
```

## Prompt 6: Convergence on Best Individual Answer

### Goal
In the individual convergence phase, the goal is for each individual expert to synthesize the insights they gained during the previous stages and arrive at a final, most likely answer. By explicitly instructing the LLM to consider the perspectives of the other experts, the critiques made, and the likelihood assessments, it aims to guide the model towards a more holistic and intelligent convergence.

### Prompt 
```
Now, it's time to converge on each expert's best, most likely answer. As each expert, reflect on the entire process.
Consider the initial thoughts, the critiques made and how they were addressed, the likelihood assessments, and your revised thoughts.
Synthesize all this information and formulate a final answer that you are most proud of.
Remember, this answer should not just be the most likely from your individual perspective but should take into account
the perspectives and insights of the other experts as well.
Based on all this, what is the single best answer to the question: {insert original question}?
```

## Prompt 7: Convergence on Best Collective Answer

### Goal
Synthesize the best individual answers from the experts and arrive at a single final, most helpful/accurate/likely answer.

### Prompt
```
Now, let's have all the experts converge together on the best collective answer by
synthesizing each expert's individual final answer from the previous step.
The experts will finalize their reasoning process and agree on the single best {answer} to the question: {insert original question}?
```

## Prompt 8: Retrospective

### Goal
The Retrospective phase is a crucial part of any reasoning or problem-solving process. It provides an opportunity to learn from experience, improve future processes, and deepen understanding of the problem or question at hand. It's a fundamental mechanism that enables compound growth/learning. 

Appending a Retrospective phase to Tree of Thoughts gives the LLM (and human) an opportunity to review and analyze the holistic process. This can also help inspire future iterations of more refined prompts and ways to improve the template itself.

### Here are some specific goals of this phase:

- **Identify Strengths and Weaknesses:** Reviewing the process can help identify what worked well and what didn't. This includes evaluating the effectiveness of individual steps, the interactions among hypothetical experts, and the overall structure of the reasoning chain.
- **Learn from the Experience:** Reflection provides an opportunity to learn from both successes and mistakes. By analyzing the process, the participants can gain insights that will help them improve their future performance.
- **Improve Future Processes:** The insights gained from reflection can be used to refine and improve future reasoning processes. This could involve making changes to individual steps, altering the structure of the process, or adjusting the way the hypothetical experts interact.
- **Increase Understanding:** Reflecting on the process can also deepen understanding of the problem or question that was addressed. This can lead to new insights or perspectives that weren't apparent during the initial reasoning process.
- **Promote Growth and Development:** On a broader level, the act of reflection encourages a mindset of continuous learning and development. This is a valuable skill in any context, not just in a reasoning process like ToT.

### Prompt:
```
Take a moment to reflect on the entire reasoning process, across all levels and abstractions.
As each expert, consider the following questions and provide thoughtful but succinct responses:

- Relection 1: Interactions and Emergent Properties: Throughout all stages of the reasoning process,
  how did the various components interact with each other, and what positive and negative
  emergent properties were observed? How did these interactions and properties affect
  the overall outcome, and how could they be leveraged or mitigated in future iterations of the process?

- Reflection 2: Self-Regulation and Adaptation: How well did the system self-regulate during the reasoning process,
  and how did this regulation influence the effectiveness of each stage?
  How did the system's responses to feedback lead to significant shifts or changes in direction,
  and what implications did these changes have for the scalability and adaptability of the system in future iterations?

- Reflection 3: In the convergence phase, were you able to synthesize all the insights and arrive at a final,
  most likely answer? How confident are you in this answer?

- Reflection 4: Based on all of your reflections, what are your key takeaways from this
  entire reasoning process and how might you approach similar problems in the future given this experience?
  What would you do differently next time?
```

### Prompt 9: New Enhanced Question

```
Finally, given this conversation in total and the reflections from all the experts, 
please refine and reformulate the original question to enhance its clarity, depth, and engagement potential during a subsequent reasoning dialog. 
Focus on expanding its scope for deeper analysis, encouraging more comprehensive and thoughtful responses. 
Ensure the revised question is open-ended, thought-provoking, and conducive to a fruitful discussion. 
Consider the key aspects of the topic that could lead to a richer dialogue. 
If necessary, provide brief reasoning for the changes made to the original question.

As a reminder, the original question was {question}
```

### Happy Experimenting! 🚀
