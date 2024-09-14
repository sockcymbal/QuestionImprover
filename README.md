# 🧠 AI for Inquiry - The QuestionCrafter Agent

## Introduction

The QuestionCrafter Agent is a cutting-edge, LLM-driven "tool for thought" designed to revolutionize the way we approach inquiry. By elevating the quality and depth of user-posed questions, this agent serves as a cognitive enhancer, pushing the boundaries of how we explore complex topics and ideas.

Utilizing a novel reasoning algorithm that integrates diverse expert personas and a graph-based reasoning rhythm, QuestionCrafter systematically refines questions, making them more insightful, thought-provoking, and suited for in-depth exploration across various domains such as academic research, business strategy, or personal inquiry.

This project, which recently won 1st place at an AI for Thought Hackathon at AGI House SF, showcases the potential of AI to enhance human cognitive processes through creative techniques.

## Motivation: Navigating the Information Age Through Better Questions

In an era where we are inundated with information, the ability to ask the right questions has become more crucial than ever. QuestionCrafter is built on the premise that:

- The meta-skill of our time lies not in amassing answers, but in crafting good questions
- The caliber of our questions often dictates the value of the answers we uncover
- Well-crafted questions can be more illuminating than the answers themselves

By harnessing these principles, QuestionCrafter creates a virtuous, self-reinforcing cycle where enhanced understanding leads to ever more profound questions, fostering deeper insights and more meaningful dialogue.

## User Experience: A Journey Through QuestionCrafter

1. **Initiate Your Inquiry**: 
   - Begin by entering your initial question into the intuitive web interface.
   - The system accepts a wide range of question types, from specific queries to broad, open-ended explorations.

2. **Witness Intelligent Persona Selection**: 
   - Watch in real-time as the agent automatically selects the most relevant expert personas for your question.
   - The selection process is visualized, providing transparency into the agent's decision-making.

3. **Experience the Graph-of-Thoughts Process**: 
   - Engage with an interactive, visual representation of the reasoning process.
   - Observe as your question evolves through multiple stages of analysis and refinement.

4. **Discover Your Enhanced Question**: 
   - Receive a refined, more insightful version of your original question.
   - The enhanced question is presented alongside a detailed rationale for the refinements made.

5. **Explore Deeper Insights**: 
   - Review synthesized insights provided by the agent, offering a multi-faceted perspective on your inquiry.
   - Examine a summary of the conversation journey, highlighting key turning points in the reasoning process.

6. **Iterate for Further Refinement**: 
   - Choose to further refine your question, diving deeper into specific aspects.
   - Alternatively, explore new dimensions with different personas, broadening the scope of your inquiry.

## Components of the Agent

1. **Initial Question Input**: 
   - A user-friendly interface for submitting questions, with helpful prompts and examples.

2. **Intelligent Persona Selection**: 
   - Automatic selection of relevant expert personas from a diverse library.
   - Users can view and optionally adjust the selected personas.

3. **Graph-of-Thoughts Visualization**: 
   - An interactive visual representation of the reasoning process.
   - Users can explore different nodes to understand the evolution of ideas.

4. **Enhanced Question Output**: 
   - Clear presentation of the refined question.
   - Detailed rationale for refinements, helping users understand the transformation.

5. **Insights Section**: 
   - Display of synthesized insights from multiple perspectives.
   - A summary of the conversation journey, highlighting key developments.

6. **Iteration Options**: 
   - Buttons for further refinement or exploration of new dimensions.
   - Option to save or share refined questions and insights.

## 🧬 Agent Cybernetics: The Inner Workings

These feedback loops are iterative and dynamic, with each loop informing and shaping the subsequent ones. They create a rhythm of continuous improvement and learning, ensuring that the conversation remains adaptive, responsive to new information, and oriented toward deeper understanding and inquiry.

QuestionCrafter employs a sophisticated system of feedback loops:

1. **User Input and Response Loop**: 
   - Processes user questions and provides refined outputs.
   - Incorporates user feedback for continuous improvement.

2. **Internal Reasoning Loops**: 
   - Facilitates interactions between different persona perspectives.
   - Enables self-critique and peer evaluation among personas.
   - Supports idea expansion and interconnection of concepts.

3. **External Process Loops**: 
   - Connects different phases of the methodology for cohesive reasoning.
   - Allows for iterative refinement across multiple cycles.

## 🔗 Prompt Sequence

The QuestionCrafter Agent uses a series of carefully crafted prompts to guide the reasoning process. Here are the prompts used in the sequence:

### Prompt 1: Persona Selection
Consider the following question with careful attention to its nuances and underlying themes.
Question: {question}
Carefully select 3 expert personas from the following list. Envision how their expertise can intertwine,
forming a rich tapestry of interconnected knowledge and perspectives.
Consider the depth and breadth each brings,
and how their unique insights, when combined, could lead to groundbreaking explorations of the question.
I know you'll do great!
Available Personas: {personas}

### Prompt 2: Brainstorm
As the QuestionCrafter agent, you embody the collective intelligence of three distinct, expert personas.
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

### Prompt 3: Self<>Peer Criticism
In this phase, adopt a stance of reflective criticism.
Your role is to scrutinize both your own and your peers' initial analyses with a critical eye.
As each expert, critically examine the collective insights thus far,
aiming not just to critique but to enrich and expand upon them.
Remember, the aim here is collaborative growth.
Your critiques should pave the way for deeper exploration and a more robust collective insight.

### Prompt 4: Self<>Peer Evaluation
Reflect on the critiques received, and adapt your perspectives accordingly.
This prompt is about evolution and expansion of thought, where you reassess and reformulate ideas, creating a more
nuanced and comprehensive network of interconnected ideas and insights in relation to the question.
The objective here is to mold your perspectives into more refined, well-rounded, and insightful analyses that stand
strong under critical examination and collectively push the boundaries of understanding the question at hand.

### Prompt 5: Explore, Expand, Branch, Network
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

### Prompt 6: Convergence on Optimal Individual Answer
Now, it's time for each expert to finalize their thoughts and converge on a best answer.
Synthesize the insights and critiques into a coherent individual conclusion.
Reflect on the entire dialogue, considering how each criticism was addressed and how your thoughts evolved.
Your answer should not only represent your strongest position but also acknowledge and integrate valid and useful
insights from the other expert perspectives.
Based on all this, as each expert, what is the single best answer to the initial question: {question}?

### Prompt 7: Convergence on Optimal Holistic Answer
Facilitate a synthesis of the individual experts' answers to forge a unified, comprehensive response that
combines the best elements from each persona's insights.
This response should be a testament to the depth and complexity of the thought network,
showcasing how diverse perspectives can coalesce into a singular, insightful narrative.
The synthesized answer should not be formulated in explicit terms specific to each persona's own definition or
agenda, but rather it should be phrased in a way that seeks to inspire and uncover broad, general, deeper truths,
regardless of what personas happened to be involved in this discussion.
A great answer will transcend the limited view of any one expert.

### Prompt 8: Retrospective (Reflections, Takeaways, Purpose, Gratitude)
Now, let's engage in a thorough meta-analysis and reflection of the entire reasoning network that we've
built up so far.
Evaluate the effectiveness of the interconnected thoughts, the dynamics that have played out between
different personas, and how these elements collectively influenced the understanding and evolution of the
question.
As each expert persona, reflect on the following:

Interactions and Dynamics: Reflect on how the various stages and components of the reasoning process
interacted with each other. What synergies or conflicts emerged? How did these interactions influence the
direction and quality of the final outcome?
Adaptation and Response to Critique: Evaluate how the process adapted to new information and critiques.
How effectively did the system and the personas respond to feedback? Were there significant shifts in
perspective or approach, and what impact did they have on the reasoning process?
Confidence and Convergence: Assess your confidence in the final answer. How did the convergence phase
contribute to this confidence? Were all insights and perspectives adequately synthesized?
Meta-Learning and Future Application: Shifting focus away from the question itself and zooming out on the
holistic conversation quality, persona definitions and applicability, reasoning rhythm and overall
methodology, please identify any key learnings or specific opportunities for improvement on the meta-process
itself. Anything specific to modify that could be improved or approached differently in subsequent iterations
that would lead to an improved reasoning process, regardless of the initial question? Any specific
enhancements to any of the feedback loops?

This retrospective analysis is not just a conclusion but a stepping stone for future reasoning and inquiry.
Your reflections are invaluable for enhancing the effectiveness of this reasoning process and for enriching
our understanding of complex questions!
Copy
### Prompt 9: New Enhanced Question
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

Clarify and Focus: Examine the original question's wording and structure.
Refine it for clarity and focus, removing any ambiguities or vague terms. How can we make the question more
precise and direct?
Deepen the Inquiry: Expand the scope of the question to incorporate the key insights and perspectives
that emerged during the discussion. How can the question be rephrased to encourage deeper exploration of
these insights? Remove any unhelpful superficialities or false dichotomies present in the original question.
Encourage Comprehensive Engagement: Modify the question to stimulate more comprehensive and thoughtful
responses. Think about how the question can invite diverse relevant viewpoints and interdisciplinary
thinking.
Maintain Open-Endedness: Ensure that the revised question remains open-ended and thought-provoking. It
should encourage a range of responses, facilitating a fruitful and ongoing discussion. The improved question
should not be re-formulated in terms specific to the persona's own agenda, but rather it should be phrased
in a way that seeks to inspire and uncover broad, general, deeper truths, regardless of what kinds people
and personas explore this question in the future.
Reflect on Potential for Rich Dialogue: Contemplate the key aspects of the topic that could lead to
richer dialogue. How can the question be framed to explore these aspects more thoroughly and inspirationally?

Rationale for refinement: Upon improving the question, briefly articulate why this new version is a
significantly higher quality and more effective question. In contrast, include the most salient weaknesses
or flaws in the way the original question was formulated.

## Ideal Types of Questions for the QuestionCrafter Agent

1. **Complex, Multi-Faceted Questions**: 
   - E.g., "How might we balance technological progress with environmental sustainability?"

2. **Strategic and Decision-Making Queries**: 
   - E.g., "What factors should be considered when expanding a business into emerging markets?"

3. **Interdisciplinary and Research-Based Inquiries**: 
   - E.g., "How can insights from neuroscience inform the development of more effective educational methodologies?"

4. **Ethical and Moral Considerations**: 
   - E.g., "What are the ethical implications of using AI in healthcare decision-making?"

5. **Critical Thinking and Problem-Solving Challenges**: 
   - E.g., "How can urban planning address both housing affordability and environmental concerns?"

6. **Questions Driving Creative Exploration and Innovation**: 
   - E.g., "In what ways could biomimicry inspire solutions to energy storage challenges?"

## Future Vision

QuestionCrafter is continuously evolving. Future developments include:

- **Enhanced User Interface**: 
  - Implementing an interactive thought map for deeper exploration of the reasoning process.
  - Customizable parameters for personalized question crafting experiences.

- **Advanced Reasoning Capabilities**: 
  - Developing multi-iteration reasoning for progressively refined questions.
  - Implementing parallel reasoning graphs to explore multiple refinement paths simultaneously.

- **Expanded Persona Library**: 
  - Continuously adding diverse expert personas to broaden the knowledge base.
  - Introducing dynamic persona generation for highly specialized topics.

- **Adaptive Prompting**: 
  - Dynamically adjusting prompts based on user goals and insights from previous interactions.
  - Incorporating machine learning to optimize prompt effectiveness over time.

- **Integration with External Knowledge Bases**: 
  - Enhancing the reasoning process with verified information from reputable sources.
  - Enabling real-time fact-checking and data incorporation.

Despite being in an early phase, QuestionCrafter is already proving to be a valuable tool for deepening inquiry and enhancing cognitive processes across various fields. We invite users to explore its capabilities and contribute to its ongoing development.

### 🚀 Happy Inquiring!

