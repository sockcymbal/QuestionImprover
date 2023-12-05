# AI for Inquiry - The Question Improver Agent 🧠
Reasoning agent designed to enhance the art of asking questions. This agent adopts a novel “multi-persona graph of thoughts” approach to really dig into and around the issue, ultimately crafting better questions that provoke and encourage deeper thinking and more profound analysis.

This project recently won 1st place at an AI for Thought Hackathon at AGI House SF.

#### Premise:
Effective questioning is at the heart of great thinking and decisive action. In complex situations with many trade-offs, quality questions are crucial. This tool creates a self-reinforcing cycle: deeper understanding leads to more insightful questions, which in turn fosters even deeper insights

#### User Experience: 
Input complex question -> auto-selects expert personas -> graph of thoughts reasoning -> output improved question -> Repeat as needed!

#### Components:
- Initial Problem: Complex issue with multiple trade-offs
- Persona Library: A diverse range of expert personas for simulations
- 🎶 Graph of Thoughts Reasoning Rhythm
	- Multi-Persona Expert Selection: Automatic and dynamic, based on the nature of the question
 	- Self<>Peer Criticism Round 1
 	- Evaluation Round 1
  	- Expand, Explore, Branch
  	- Convergence on Best Individual Answer
  	- Convergence on Best Collective Answer
  	- Retrospective
- Output: A refined, more insightful and though-provoking question
- Optional: Loop through this multiple times as a chain of graph of thoughts, each time iteratively improving the question until diminishing returns

#### Error Correction includes:

- **Incorporating Explicit Error Checking:** Includes a specific stage for the experts to identify potential errors in their reasoning and correct them. This is an explicit part of the criticism stages.
- **Encouraging Divergent Thinking:** During the expand, explore, and branch stage, the experts are encouraged to not only build on their current thoughts, but also to think divergently and consider entirely new lines of reasoning.
- **Adding a Retrospective Stage:** After the final convergence on the best answer, a reflection stage has been added. Here, the experts can discuss what they learned from the process, identify key takeaways, and suggest how they might approach similar problems in the future.

### **Usage Tips**
- Start with Clear and Concise Questions: Even though the agent is designed to improve question quality, starting with a well-thought-out question can lead to more insightful improvements.
- Be Specific About the Topic: The more specific you are, the better the agent can select relevant personas and generate appropriate questions.
- Utilize the Output for Broader Application: Use the improved questions as a springboard for further research, discussion, or exploration. The output can be valuable for further development, brainstorming sessions, or strategic planning.

#### Categories of questions this tool is well suited for:
1. Complex, Multi-Faceted Questions:
    - Questions that involve multiple layers or aspects, requiring a nuanced understanding and exploration of various elements.
2. Questions with Trade-Offs:
    - Questions that involve trade-offs or balancing different priorities are ideal. The agent can help explore different perspectives and outcomes associated with each choice.
3. Interdisciplinary Questions:
    - Questions that span across different fields or disciplines. The agent can leverage its diverse personas to provide insights that integrate various areas of knowledge.
4. Strategic or Decision-Making Questions:
    - Questions related to strategy formulation or decision-making in business, research, or personal contexts. The agent can help in framing the question to consider all relevant factors.
5. Ethical and Moral Questions:
    - Questions that delve into ethical dilemmas or moral considerations. The tool can aid in formulating questions that consider multiple ethical viewpoints and implications.
6. Hypothetical or Theoretical Questions:
    - Questions that are speculative or theoretical in nature, which can benefit from creative and diverse thought processes.
7. Questions Requiring Critical Thinking:
    - Questions that challenge common assumptions or standard ways of thinking. The agent can help reframe these questions to encourage deeper critical analysis.
8. Problem-Solving Questions:
    - Questions aimed at solving complex problems, where different approaches might lead to varying solutions. The tool can assist in framing these questions to cover all possible angles.
9. Research and Investigative Questions:
    - Questions that guide research projects or investigations, where a well-crafted question can set the direction for the entire inquiry.
10. Questions Seeking Holistic Understanding:
    - Questions that seek a comprehensive understanding of a topic, including its historical, cultural, and social dimensions.



# 🔗 Prompt Sequence

## Prompt 1: Persona Selection
```
Consider the following question with careful attention to its nuances and underlying themes.
Your task is to thoughtfully select 3 expert personas from the provided list, ensuring that each one
brings a distinct and relevant perspective to a deep reasoning discussion about this question.

In making your selection, consider not only the direct relevance of each persona’s expertise to the question
but also the potential for unique insights they might offer when combined. Look for synergies between the personas
that could lead to a more comprehensive and multi-dimensional exploration of the topic.
Evaluate the depth and breadth of knowledge each persona could contribute and how their viewpoints
might intersect or diverge in a way that enhances the discussion.

Your goal is to assemble a trio of personas that, together, will provide a balanced, thorough,
and insightful examination of the question at hand. I know you'll do great!

Question: {question}
Available Personas: {personas}
```

## Prompt 2: Brainstorm
```
You are a chatbot using three unique, specified personas to help reason step by step to ultimately
provide the best possible answer to a given problem/question by arriving at a final, synthesized best answer.
        
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

Appending a Retrospective phase to a reasoning process gives the LLM (and human) an opportunity to review and analyze the holistic process. This can also help inspire future iterations of more refined prompts and ways to improve the blueprint itself.

### Prompt:
```
Now let's reflect on the entire reasoning process, across all levels and abstractions.
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
please take a deep breath and refine and reformulate the original question to enhance its
clarity, depth, and engagement potential during a subsequent reasoning dialog. 
Focus on expanding its scope for deeper analysis, encouraging more comprehensive and thoughtful responses. 
Ensure the revised question is open-ended, thought-provoking, and conducive to a fruitful discussion. 
Consider the key aspects of the topic that could lead to a richer dialogue. 
Provide brief reasoning for the changes made to the original question and why it's a better question.

As a reminder, the original question was {question}
```

### Happy Experimenting! 🚀
