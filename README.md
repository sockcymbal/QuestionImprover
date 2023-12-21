# AI for Inquiry - The Question Improver Agent 🧠
The purpose of the Question Improver Agent is to enhance the quality and depth of questions posed by users. Utilizing a sophisticated algorithm that incorporates a diverse range of expert personas, the agent systematically refines and restructures initial questions. Through this process, it produces more insightful, thought-provoking, and comprehensive questions that are better suited for in-depth exploration and discussion in various domains, such as academic research, business strategy, or personal inquiry. This tool aims to foster deeper understanding and more meaningful dialogue by elevating the art of questioning.

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
 	- Self<>Peer Criticism
 	- Evaluation
  	- Expand, Explore, Branch, Network
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
        
Embody each expert persona and articulate your initial analysis of the question.
Detail your perspective, drawing on specific knowledge, experiences, and pioneering concepts from your field.
Aim to uncover new angles and dimensions of the question, demonstrating how your unique expertise contributes to a multifaceted understanding.

The personas are: {selected_personas}

The question is: {question}
```

## Prompt 3: Self<>Peer Criticism
```
Adopt a critical lens as each expert. Evaluate and challenge your own initial analysis and the analyses provided by your peers.
Focus on identifying potential biases, logical fallacies, or gaps in reasoning.
Offer constructive feedback that encourages deeper exploration and refinement of ideas.
```

## Prompt 4: Self<>Peer Evaluation
```
Reassess the credibility and robustness of your initial thoughts in light of the critiques received.
For each assertion, estimate its likelihood of accuracy and helpfulness,
considering the strength of your arguments, the quality of evidence, and the nature of the criticisms.

Prioritize assertions that are well-supported, constructive and resilient to scrutiny.
```

## Prompt 5: Expand, Explore, Branch, Network
```
Deepen and diversify your thinking, integrating critiques and alternative perspectives.
Explore both the refinement of current ideas and the generation of novel concepts.
Assess whether new ideas address criticisms effectively, bring fresh insights, and remain aligned with the core problem.
If necessary, pivot to new, more promising lines of reasoning.
```

## Prompt 6: Convergence on Best Individual Answer

### Goal
In the individual convergence phase, the goal is for each individual expert to synthesize the insights they gained during the previous stages and arrive at a final, most likely answer. By explicitly instructing the LLM to consider the perspectives of the other experts, the critiques made, and the likelihood assessments, it aims to guide the model towards a more holistic and intelligent convergence.

### Prompt 
```
Now, it's time for each expert to finalize their thoughts and converge on a best answer.
Synthesize the insights and critiques into a cohesive and compelling answer from each expert's viewpoint.

Reflect on the entire dialogue, considering how each criticism was addressed and how your thoughts evolved.
Your answer should not only represent your strongest position but also acknowledge and integrate valid and useful insights from the other expert perspectives.
        
Based on all this, as each expert, what is the single best answer to the question: {question}?
```

## Prompt 7: Convergence on Best Collective Answer

### Goal
Synthesize the best individual answers from the experts and arrive at a single final, most helpful/accurate/likely answer.

### Prompt
```
Facilitate a synthesis of the individual experts' answers to forge a unified, comprehensive and impressive response. 
This collective answer should encapsulate the most salient points from each expert, demonstrating a 
harmonious integration of diverse perspectives. Aim for a conclusion that is not only insightful but 
also balanced and representative of the collective expertise.

The synthesized answer should not be formulated in explicit terms specific to each persona's own agenda, 
but rather it should be phrased in a way that seeks to inspire and uncover broad, general, deeper truths, 
regardless of what personas happened to be involved in this discussion. 
A great answer will transcend the limited view of any one expert, so the answer shouldn't be phrased as such.
```

## Prompt 8: Retrospective

### Goal
The Retrospective phase is a crucial part of any reasoning or problem-solving process. It provides an opportunity to learn from experience, improve future processes, and deepen understanding of the problem or question at hand. It's a fundamental mechanism that enables compound growth/learning. 

Appending a Retrospective phase to a reasoning process gives the LLM (and human) an opportunity to review and analyze the holistic process. This can also help inspire future iterations of more refined prompts and ways to improve the blueprint itself.

### Prompt:
```
Now let's engage in a reflective analysis of the entire reasoning journey we've just undertaken. 
As each expert persona, consider the following aspects, ensuring your responses are thoughtful and encompassing:

1. Interactions and Dynamics: Reflect on how the various stages and components of the reasoning process interacted 
with each other. What synergies or conflicts emerged? How did these interactions influence the direction and 
quality of the final outcome?

2. Adaptation and Response to Critique: Evaluate how the process adapted to new information and critiques. 
How effectively did the system and the personas respond to feedback? Were there significant shifts in 
perspective or approach, and what impact did they have on the reasoning process?

3. Confidence and Convergence: Assess your confidence in the final answer. How did the convergence phase 
contribute to this confidence? Were all insights and perspectives adequately synthesized?

4. Learning and Future Application: Identify the key learnings from this reasoning process. 
What insights have you gained about the topic, and how might these insights influence your approach to 
similar problems in the future? Are there aspects of the process that could be improved or approached differently 
in subsequent iterations?

This retrospective analysis is not just a conclusion but a stepping stone for future reasoning and inquiry. 
Your reflections are invaluable for enhancing the effectiveness of this process and for enriching 
our understanding of complex questions!
```

### Prompt 9: New Enhanced Question

```
After thorough analysis and reflection on the entire discussion, let's now focus on the final and crucial task of proposing a much-enhanced version the original question. 
After going through the following reflection process, please take a deep breath and generate a far better version of the original question.
As we do this, keep in mind the insights gained, the perspectives shared, and the critiques addressed during our reasoning journey.

Here are some thoughts to consider before you propose the final improved question:

1. Clarify and Focus: Examine the original question's wording and structure.
Refine it for clarity and focus, removing any ambiguities or vague terms.
How can we make the question more precise and direct?

2. Deepen the Inquiry: Expand the scope of the question to incorporate the key insights and perspectives that emerged during the discussion.
How can the question be rephrased to encourage deeper exploration of these insights?
Remove any unhelpful superficialities or false dichotomies present in the original question.

3. Encourage Comprehensive Engagement: Modify the question to stimulate more comprehensive and thoughtful responses.
Think about how the question can invite diverse relevant viewpoints and interdisciplinary thinking.

4. Maintain Open-Endedness: Ensure that the revised question remains open-ended and thought-provoking.
It should encourage a range of responses, facilitating a fruitful and ongoing discussion. 
The improved question should not be re-formulated in terms specific to the persona's own agenda, 
but rather it should be phrased in a way that seeks to inspire and uncover broad, general, deeper truths, 
regardless of what kinds people and personas explore this question in the future. 

5. Reflect on Potential for Rich Dialogue: Contemplate the key aspects of the topic that could lead to richer dialogue.
How can the question be framed to explore these aspects more thoroughly and inspirationally?

6. Justify the Refinement: After reformulating the question, provide a brief explanation of the changes made.
Why is this revised question more effective in eliciting insightful and comprehensive responses?
How does it better capture the complexities and nuances of the topic?
After reflection, please include the most salient weaknesses or flaws in the way the original question was formulated.

This final step is not just about modifying the question, but also about encapsulating the essence of our collaborative thought process.
It’s about transforming the question into a tool that can unlock deeper understanding and more meaningful dialogue and inspired action in subsequent discussions.

As a reminder, the original question was {question}

OUPUT - IMPROVED QUESTION:
```

### Happy Inquiring! 🚀
