# 🧠 AI for Inquiry - The Question Improver Agent
The Question Improver Agent is an LLM-driven "tool for thought" designed to elevate the quality and depth of user-posed questions. It utilizes a novel reasoning algorithm integrating diverse expert personas and a graph-based reasoning rhythm to systematically refine questions, making them more insightful, thought-provoking and suited for in-depth exploration across various domains, such as academic research, business strategy, or personal inquiry.

This tool aims to elevate the art of inquiry, fostering a cycle of deepened understanding, more meaningful dialog and progressively insightful questioning.

This project recently won 1st place at an AI for Thought Hackathon at AGI House SF, showcasing how we can enhance cognitive processes using creative AI techniques.

### Motivation: 
> How to navigate the Information Age through better questions

The premise for this agent is that in an age where information inundates and overwhelms us, the ability to ask the right questions is more crucial than ever.
- the meta-skill and art lies not in amassing answers, but in crafting good questions
- the caliber of questions often dictates the value of the answers we uncover
- the right questions can even be more illuminating than the answers

The QuestionImprover Agent harnesses this principle, creating a virtuous self-reinforcing cycle where enhanced understanding leads to ever more profound questions, thereby fostering even deeper insights.

This repo consists of 
- a persona library that I've started to define
- all the prompts used so you can try this with your own questions in a UI like ChatGPT
- simple python example in a Jupyter notebook implementation using Langchain to help orchestrate the prompt engineering

#

### Table of Contents
1. [**Introduction**](#ai-for-inquiry---the-question-improver-agent-🧠)
- Overview of the QuestionImprover Agent
- The Necessity of Quality Questioning in Today's World
2. [**Motivation**](#motivation)
- The Art of Crafting Profound Questions
- Creating a Cycle of Deepened Understanding
3. [**User Experience: Journey Through the Agent**](#user-experience)
- Step-by-Step Guide: From Initial Inquiry to Enhanced Question
4. [**Components of the Agent**](#components-of-the-agent)
- Initial Problem Assessment
- Persona Library and Expert Integration
- Graph-of-Thoughts Reasoning Rhythm
- Enhanced Question Output and Iterative Refinement
5. [**Agent Cybernetics: The Inner Workings**](#agent-cybernetics-the-inner-workings)
- The Role of Feedback Loops
- Insight, Evaluation, and Adaptation Loops
- Synthesis, Reflection, and Refinement Loops
6. [**The Agent's Prompt Sequence**](#🔗-prompt-sequence)
- Detailed Breakdown of Each Prompt in the Reasoning Process
7. [**Types of Questions Ideal for the Agent**](#ideal-types-of-questions-for-the-questionimprover-agent)
- Range of Queries Ideal for the Agent’s Capabilities
8. [**Future Development**](#future-vision)
- Plans for Enhancements and New Features
- UI Development and Automation Strategies

#
### User Experience: 
Step 1: Initiate with Your Inquiry
- Begin by presenting your current question to the system. This could be any topic or dilemma you're keen to explore more deeply. It's the starting point of your journey into enhanced understanding.

Step 2: Intelligent Persona Selection
- Based on your question, the agent automatically selects the most relevant expert personas from a diverse pool. Feel free to fine-tune this selection, adding or removing personas to better fit the nuances of your question.

Step 3: Experience the Graph-of-Thoughts Reasoning Process
-  Engage with the agent's distinctive 'Graph-of-Thoughts' reasoning process. This is where the magic happens – your question is dissected, analyzed, and reimagined through multiple expert perspectives, evolving with each insightful interaction.

Step 4: Discover Your Enhanced Question
- What emerges from this process is a question that’s not just an improvement but a revelation – more insightful, probing, and designed to unlock deeper understanding. It's a testament to the power of collaborative intelligence and thoughtful refinement.

Step 5: Embark on Iterative Exploration for Deeper Insights
- Don't stop there! Use the newly improved question as a launchpad for further discovery. Begin again with the new question and repeat the process. Each iteration allows you to dive deeper, continually refining the question and exploring new dimensions with different personas.

#
### Components of the Agent:
1. **Initial Problem Assessment** 
- Tackles complex issues with multiple trade-offs, setting the stage for a thorough inquiry process.
2. **Persona Library**
- Features a diverse collection of expert personas for simulation, each embodying unique perspectives and specialized knowledge. These personas contribute distinct angles of expertise, enriching the question refinement process with a breadth of insights.
3. **🎶 Graph-of-Thoughts Reasoning Rhythm** 
- A harmonious and methodical process that orchestrates collaborative reasoning, featuring several key stages:
    - **Dynamic Multi-Persona Expert Selection**: Intelligently combines expert personas in a way that aligns with the unique facets of each question, ensuring a tailored and relevant approach to question elevation.
    - **Self<>Peer Critique**: Engages personas in a critical analysis phase, where they scrutinize and challenge both their own insights and those of their peers, fostering a culture of constructive feedback and continuous improvement.
    - **Self<>Peer Evaluation**: Involves careful consideration of the various critiques and viewpoints presented, deepening the understanding and expanding the horizons of the original question.
    - **Expansion, Branching, Exploration**: Encourages expansive thinking, inviting personas to venture into new realms of ideas, discover unseen connections, and explore innovative perspectives.
    - **Synthesis of Individual Insights**: Each persona distills their collective wisdom, refining it into a singular, comprehensive insight.
    - **Fusion of Collective Insight**: Integrates the most potent elements from each persona's input, forming a unified, powerful, and insightful response.
    - **Reflective Retrospective**: A phase dedicated to evaluating the effectiveness of the reasoning process, extracting lessons and insights to optimize future inquiries.
4. Enhanced Question Output
- Delivers a significantly refined, deeper, and more thought-provoking version of the original question, elevating the inquiry to new levels of sophistication and insight.
5. Iterative Refinement (Optional)
- Option to re-engage with the reasoning process multiple times, further enriching the question with each cycle. This iterative approach allows for continuous improvement, reaching deeper layers of understanding until a point of maximum insight is achieved.

#
## 🧬 Agent Cybernetics: The Inner Workings

> These feedback loops are iterative and dynamic, with each loop informing and shaping the subsequent ones. They create a rhythm of continuous improvement and learning, ensuring that the conversation remains adaptive, responsive to new information, and oriented toward deeper understanding and inquiry.

1. **Initial Insight and Critique Loop**: Each persona provides initial insights specific to their expertise, laying the foundation for the reasoning process. This loop establishes the primary perspectives and sets the stage for the conversation. This is followed by a critique phase, where each persona critically evaluates their own and others' insights. This loop of insight and critique ensures that each perspective is not only articulated but also challenged and refined.

2. **Adaptation and Expansion Loop**: After receiving critiques, each persona adapts their insights to incorporate this feedback. This loop focuses on evolution, where personas reassess and reformulate their ideas, creating a more nuanced and comprehensive network of interconnected thoughts.

3. **Integration and Synthesis Loop**: The personas then synthesize their evolved thoughts into individual conclusions, striving to converge on the best answer. This loop involves distilling the collective wisdom into coherent positions that reflect the integration of all perspectives.

4. **Convergence and Divergence Loop**: The process then moves into a phase where personas explore new, divergent ideas stimulated by the previous feedback loops, followed by a convergence phase where these ideas are brought together into a unified, comprehensive response. This loop allows for the exploration of novel concepts and the integration of diverse thoughts into a cohesive narrative.

5. **Meta-Analysis and Reflection Loop:** The conversation crescendos in a meta-analysis, where each persona reflects on the effectiveness of the interconnected thoughts, the dynamics between personas, and the adaptation to critiques. This loop is critical for evaluating the reasoning process itself and identifying opportunities for future improvements.

6. **Question Refinement and Enhancement Loop:** Finally, the initial question is refined based on the insights gained through the networked reasoning process. This loop focuses on transforming the question into a more insightful and universally engaging form, encapsulating the essence of the collaborative thought process.

### There are three primary layers of feedback loops:

1. **User Input and Response Feedback Loop**:
    - Initial Input: The user starts by posing a question to the system.
    - Agent Processing and Output: The AI processes the question through its multi-layered reasoning rhythm, outputting a refined question.
    - User Evaluation and Feedback: The user evaluates the refined question, assessing its depth, relevance, and clarity. Users can modify the agent's prompts to better suit their specific context or inquiry goals.

2. **Internal Layer Feedback Loops**: These occur within each major phase or component of the methodology. Examples include:
	- The interaction and critique within the expert persona selection and interaction phase.
	- The process of self and peer criticism, where personas evaluate and refine their own and each other's insights.
	- The evaluation and expansion phase, where feedback leads to the exploration of new ideas and the refinement of existing ones.
	- The idea integration and network building within each persona's thought process.

3. **External Layer Feedback Loops**: These are the loops that connect different phases of the methodology, ensuring that insights and improvements from one phase inform and enhance subsequent phases. Examples include:
	- The convergence and synthesis loop, where the insights from individual and collective convergence phases are used to refine the question and the process itself.
	- The retrospective and iterative improvement loop, which reflects on the entire process and informs improvements for future iterations.
	- Iterative Refinement via Chain-of-Graph-of-Thoughts: Based on the user's goals, iterate through the reasoning process again from the beginning, inputting the recently improved question to make it even better. This chains together individual Graph-of-Thoughts rhythms, where the outcome of one cycle informs the starting point of the next.

These layers of feedback loops interact with each other, creating a dynamic, interconnected system. The internal loops ensure depth and rigor within each phase, while the external loops ensure that the entire process is cohesive, adaptive, continually improving, and aligned with human goals.

#
# 🔗 Prompt Sequence

### Prompt 1: Persona Selection
```
Consider the following question with careful attention to its nuances and underlying themes.

Question: {question}

Carefully select 3 expert personas from the following list. Envision how their expertise can intertwine,
forming a rich tapestry of interconnected knowledge and perspectives. 

Consider the depth and breadth each brings,
and how their unique insights, when combined, could lead to groundbreaking explorations of the question.

I know you'll do great!

Available Personas: {personas}
```

### Prompt 2: Brainstorm
```
As the QuestionImprover agent, you embody the collective intelligence of three distinct, expert personas. 
Your ultimate task is to collaboratively refine a user-posed question through an iterative prompting rhythm,
drawing upon the diverse expertise of these personas.

Each persona will begin this process now by contributing their initial insights on the user's original question. 
Draw upon your unique knowledge base, experiences, and innovative concepts specific to your field. 
Your goal is to uncover new perspectives and dimensions of the question, showcasing how your 
expertise enriches a multi-layered understanding.

In subsequent reasoning stages, we will integrate these perspectives into a cohesive thought network. 
This overall collaborative synthesis aims to evolve the original question into one that is more comprehensive, 
insightful, and multidimensional.

Persona Contributions:{selected_personas}

Original Question: {question}

Please articulate each persona's initial response to the question, one by one, to initiate this 
multifaceted and iterative exploration.
```

### Prompt 3: Self<>Peer Criticism
```
In this phase, adopt a stance of reflective criticism.
Your role is to scrutinize both your own and your peers' initial analyses with a critical eye.

As each expert, critically examine the collective insights thus far,
aiming not just to critique but to enrich and expand upon them. 

Remember, the aim here is collaborative growth.
Your critiques should pave the way for deeper exploration and a more robust collective insight.
```

### Prompt 4: Self<>Peer Evaluation
```
Reflect on the critiques received, and adapt your perspectives accordingly. 

This prompt is about evolution and expansion of thought, where you reassess and reformulate ideas, creating a more
nuanced and comprehensive network of interconnected ideas and insights in relation to the question.

The objective here is to mold your perspectives into more refined, well-rounded, and insightful analyses that stand
strong under critical examination and collectively push the boundaries of understanding the question at hand.
```

### Prompt 5: Explore, Expand, Branch, Network
```
This stage is about creating a vibrant tapestry of ideas, weaving together the various
critiques and perspectives into an interconnected web of thought.

Focus on how new ideas can interconnect with and enhance existing thoughts. 
Explore the potential of novel concepts to form new nodes in this thought network. 

Push the boundaries of conventional thinking. Each persona explores new, divergent ideas, stimulated by the feedback loop. 

Critically assess how these ideas not only address previous criticisms but also contribute fresh insights, creating a
richer and more intricate web of understanding, or introducing new dimensions to the question.

Consider pivoting to new lines of reasoning that promise to add valuable connections to this evolving thought network.

The aim here is to foster a dynamic and evolving landscape of ideas, where each thought is connected,
contributing to a deeper, more nuanced understanding of the original question.
```

### Prompt 6: Convergence on Optimal Individual Answer

### Goal
In the individual convergence phase, the goal is integrative synthesis. Each individual expert will reflect on the insights gained during the previous stages and arrive at a final, best answer. By explicitly instructing the LLM to consider the perspectives of the other experts, the critiques made, and any likelihood assessments, it aims to guide the model towards a more holistic and intelligent convergence.

### Prompt 
```
Now, it's time for each expert to finalize their thoughts and converge on a best answer. 
Synthesize the insights and critiques into a coherent individual conclusion.

Reflect on the entire dialogue, considering how each criticism was addressed and how your thoughts evolved. 

Your answer should not only represent your strongest position but also acknowledge and integrate valid and useful
insights from the other expert perspectives.
        
Based on all this, as each expert, what is the single best answer to the initial question: {question}?
```

### Prompt 7: Convergence on Optimal Holistic Answer

### Goal
Synthesize the best individual answers from the experts and arrive at a single final, most helpful/accurate/likely answer.

### Prompt
```
Facilitate a synthesis of the individual experts' answers to forge a unified, comprehensive response that
combines the best elements from each persona's insights.

This response should be a testament to the depth and complexity of the thought network, 
showcasing how diverse perspectives can coalesce into a singular, insightful narrative.

The synthesized answer should not be formulated in explicit terms specific to each persona's own definition or
agenda, but rather it should be phrased in a way that seeks to inspire and uncover broad, general, deeper truths,
regardless of what personas happened to be involved in this discussion.
A great answer will transcend the limited view of any one expert.
```

### Prompt 8: Retrospective (Reflections, Takeaways, Purpose, Gratitude)

### Goal
The Retrospective phase is a crucial part of any reasoning or problem-solving process. It provides an opportunity to learn from experience, improve future processes, and deepen understanding of the problem or question at hand. It's a fundamental mechanism that enables compound growth/learning. 

Appending a Retrospective phase to a reasoning process gives the LLM (and human) an opportunity to review and analyze the holistic process. This can also help inspire future iterations of more refined prompts and ways to improve the blueprint itself.

### Prompt:
```
Now, let's engage in a thorough meta-analysis and reflection of the entire reasoning network that we've
built up so far. 

Evaluate the effectiveness of the interconnected thoughts, the dynamics that have played out between
different personas, and how these elements collectively influenced the understanding and evolution of the
question.

As each expert persona, reflect on the following:

1. Interactions and Dynamics: Reflect on how the various stages and components of the reasoning process
interacted with each other. What synergies or conflicts emerged? How did these interactions influence the
direction and quality of the final outcome?

2. Adaptation and Response to Critique: Evaluate how the process adapted to new information and critiques.
How effectively did the system and the personas respond to feedback? Were there significant shifts in
perspective or approach, and what impact did they have on the reasoning process?

3. Confidence and Convergence: Assess your confidence in the final answer. How did the convergence phase
contribute to this confidence? Were all insights and perspectives adequately synthesized?

4. Meta-Learning and Future Application: Shifting focus away from the question itself and zooming out on the
holistic conversation quality, persona definitions and applicability, reasoning rhythm and overall
methodology, please identify any key learnings or specific opportunities for improvement on the meta-process
itself. Anything specific to modify that could be improved or approached differently in subsequent iterations
that would lead to an improved reasoning process, regardless of the initial question? Any specific
enhancements to any of the feedback loops?

This retrospective analysis is not just a conclusion but a stepping stone for future reasoning and inquiry.
Your reflections are invaluable for enhancing the effectiveness of this reasoning process and for enriching
our understanding of complex questions!
```

### 💡 Prompt 9: New Enhanced Question

```
As we conclude our collaborative journey and after thorough analysis and reflection on the entire
discussion, let's now focus on the final objective - to vastly elevate the original question into a more
insightful and universally engaging form. 

After going through the following thoughts, please take a deep breath and generate a far higher quality
version of the original question.

Reformulate the initial question by weaving in the rich insights gained through this networked reasoning
process. 

The new question should be deeper, clearer, and designed to catalyze more curiosity and invite more
comprehensive exploration.

Here are some thoughts to consider before you propose an improved version of the question:

1. Clarify and Focus: Examine the original question's wording and structure.
Refine it for clarity and focus, removing any ambiguities or vague terms. How can we make the question more
precise and direct?

2. Deepen the Inquiry: Expand the scope of the question to incorporate the key insights and perspectives
that emerged during the discussion. How can the question be rephrased to encourage deeper exploration of
these insights? Remove any unhelpful superficialities or false dichotomies present in the original question.

3. Encourage Comprehensive Engagement: Modify the question to stimulate more comprehensive and thoughtful
responses. Think about how the question can invite diverse relevant viewpoints and interdisciplinary
thinking.

4. Maintain Open-Endedness: Ensure that the revised question remains open-ended and thought-provoking. It
should encourage a range of responses, facilitating a fruitful and ongoing discussion. The improved question
should not be re-formulated in terms specific to the persona's own agenda, but rather it should be phrased
in a way that seeks to inspire and uncover broad, general, deeper truths, regardless of what kinds people
and personas explore this question in the future. 

5. Reflect on Potential for Rich Dialogue: Contemplate the key aspects of the topic that could lead to
richer dialogue. How can the question be framed to explore these aspects more thoroughly and inspirationally?

Rationale for refinement: Upon improving the question, briefly articulate why this new version is a
significantly higher quality and more effective question. In contrast, include the most salient weaknesses
or flaws in the way the original question was formulated.

Proposed personas for further exploration: After generating the new improved question, please propose 1-3
other ideal expert personas that would be useful to invoke in subsequent collaboration for even deeper
exploration of the question. Include a rationale for each proposed persona.

This final step is not just about modifying the question, but also about encapsulating the essence of our
collaborative thought process. It’s about transforming the question into a tool that can unlock deeper
understanding and more meaningful dialogue and inspired action in subsequent discussions.

As a reminder, the original question was {question}

Please format your output like:

**Initial Question**: Present the user's original question.
**QuestionImprover Output - Enhanced Question**: Display the refined question that the agent has generated.
**Rationale for Refinement**: Explain the thought process behind how the initial question was refined. This
helps the user understand why certain changes or focuses were made. Explain the weaknesses or limitations of
the initial question.
**Proposed Personas for Wider Exploration**: Suggest expert personas or perspectives that could further
deepen the exploration of the enhanced question, including the rationale for each suggestion. This guides
the user on what additional angles or expertise to consider next.
**Potential Exploration Pathways**: Offer possible directions or sub-questions for further exploration based
on the enhanced question. This helps to spark more specific avenues of inquiry.
**Further Reading/Resources**: Include links or references to relevant literature, articles, people of
interest, or studies that can provide more context or information related to the enhanced question.

```

### Prompt 10: Harmony Seeking Loop

```
Identify a fundamental principle that all personas can agree upon. 

How did this shared foundation influence the collective reasoning process?
``````
#

### Ideal Types of Questions for the QuestionImprover Agent
1. Complex, Multi-Faceted Questions
- Ideal for queries involving various layers and dimensions of trade-offs, requiring an intricate understanding and exploration.
  The agent excels in unpacking and refining these layered questions, bringing clarity and depth to multifaceted topics.
2. Strategic and Decision-Making Queries
- Tailored for questions related to strategy development or critical decision-making, whether in business, academic research, or personal scenarios. The agent aids in structuring these questions to consider all vital factors and potential outcomes.
3. Interdisciplinary and Research-Based Inquiries
- Perfect for questions that cross disciplinary boundaries or are central to research projects. The agent's diverse personas
  contribute insights from different fields, fostering an integrated and comprehensive exploration.
4. Ethical and Moral Considerations
- Suitable for probing into ethical dilemmas or moral issues. The agent assists in framing these questions to encompass various
  ethical perspectives and implications, ensuring a balanced and thorough examination.
5. Critical Thinking and Problem-Solving Challenges
- Designed for questions that demand critical thinking or are aimed at resolving complex problems. The agent helps in reshaping
  these questions to challenge assumptions and explore diverse solution pathways.
6. Questions Driving Creative Exploration and Innovation
- Well suited for inquiries aimed at driving creative thinking. The agent adeptly aids in formulating questions that challenge
  conventional perspectives and inspire new paths of thought, making it a valuable tool for those looking to venture beyond
  traditional boundaries.

#
That's it! For now. I'm constantly modifying these prompts and iterating them in various ways for specific use-cases (and encourage you to do the same), but these are a good starting point because they set the right foundation for what this agent is trying to achieve. In the spirit of continuous improvement and being best in class, this agent's reasoning process should improve over time and incorporate the best reasoning techniques out there that are valid for this context. This is all an exercise in trial and error to develop heuristics that unlock cognitive potential. 

Despite being in a super early developmental phase, this agent is already pratical and helpful enough for me to personally use in all kinds of useful ways.


### 🔮 Future Vision

Lots of experiments and improvements in the works! The python example was created quickly for a hackathon, so there's a bunch to refactor there. Essentially I've been honing the backend, logic, prompt engineering and persona library first to make sure this is actually useful. It is! I use it all the time now and it improves the depth of my thinking. Next I'm working on a few UI ideas, a question quality scoring system, alternate prompting techniques, and adding the option for a user to input a goal for the inquiry process that can help align the reasoning and question reformulation process to be more suitable for that goal.

**Optimization and Expansion of Core Functionalities**

- Rhythm and Logic Refinement: Continuing to refine the backend and logic for more efficient processing and accurate reasoning.
- Enhanced Prompt Engineering: Further developing the prompt engineering process to ensure more nuanced, helpful and contextually relevant responses.
- Persona Library Development: Expanding the persona library to encompass a wider range of expertise and viewpoints.

**Create a User Interface!**

- Simple User Interaction: Designing a user-friendly interface where users can easily input questions and receive enhanced versions.
- Interactive Thought Map: Visual representation of the Graph-of-Thoughts reasoning, allowing users to explore different aspects of the reasoning process in detail.
- Customizable Parameters: Adjustable settings to control the number of expert personas, iteration loops, and other parameters for a tailored experience.

**Inquiry Goal Alignment**

Goal-Oriented Reasoning: Incorporating the option for users to define a specific goal for their inquiry, aligning the reasoning process to generate more targeted questions.

**Increase Agentic Usefulness and Automation**

- Multi-Iteration Reasoning: Automating the reasoning sequence to loop multiple times, using a broader range of experts to refine the question progressively, based on predefined quality levels or stopping criteria.
- Parallel Reasoning Graphs: Running multiple reasoning sequences in parallel with the same initial question, comparing and deciding the best-refined question based on a quality assessment methodology.
- Dynamic Persona Generation: Creating new personas on-the-fly for subsequent iterations to introduce fresh perspectives.
- Adaptive Prompting: Dynamically adjusting prompts in subsequent iterations, guided by the user's specified goals and insights from previous retrospectives.
 
Let me know of any awesome question reformulations you come across during your own testing!


### 🚀 Happy Inquiring!
