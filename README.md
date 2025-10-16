# Module 0: Setup
1. All the necessary files have been created and keys have been setup to proceed for Module 1 learning
2. This time we are going to integrate Tavily as well and use Langgraph IDE and learn it's features in grasping more control over the agents that we build
<img width="1215" height="915" alt="image" src="https://github.com/user-attachments/assets/0b22cc0e-ff2e-432c-ab6f-c2ed4a95d346" />

# Module 1: Lesson 1 - Motivation
1. LLM applications follow a fixed controlled flow of event with inflexibility.
2. To create flexibility, agents were made with the capacity to decide the next step after step.
3. However, flexibility and control/reliability are inversely proportional and to make it the proportional LangGraph is used.
4. LangGraph represents flows as graphs, where nodes are tasks and edges define fixed or conditional paths.
5. This graph-based structure supports loops, branching in it's standalone LangGraph Studio IDE.
6. It integrates memory, streaming outputs, and tooling, as well as human inputs to enhance flexibility and reliability proportionality.
7. LangGraph thus enables creating Agents that can decide next steps over context and give the best of controlled and dynamic decisions.
<img width="1045" height="576" alt="Screenshot 2025-10-16 at 11 51 33" src="https://github.com/user-attachments/assets/249980c7-42fb-4179-980a-68dce3ab2f52" />

# Module 1: Lesson 2 - Simple Graph
<img width="1505" height="672" alt="image" src="https://github.com/user-attachments/assets/beaed683-5dfb-4ebf-a013-821b82773b51" />
Above is a simple graph with 3 nodes and 1 conditional edges.

1. State is the input schema which travels through the graph.
2. Nodes are just python functions that return a value of the State key which overrides previous value.
3. Edges are what connect the nodes; There exists Normal Node which go from node-1 to node-2 or Conditional Node which decides between n nodes upon some logic.
4. All these components make the Graph; START node through normal and conditional nodes to END node.
5. Invocation is the go to standard procedure starting from START node to END nodeCheck out the below example where I tweaked the code to toss the coin in a 60/40 bias between Heads and Tails, code uploaded as well.
<img width="1212" height="683" alt="Screenshot 2025-10-16 at 12 13 59" src="https://github.com/user-attachments/assets/d3ea36a0-cce8-402c-9647-0412d15d1794" />

# Module 1: Lesson 3 - LangSmith Studio
1. It's an IDE designed to trace and experiment with the graph, it's nodes and links.
2. You can see the flow of an event by the Agent as a graph, modify prompts and run tests on datasets.
<img width="2938" height="1662" alt="image" src="https://github.com/user-attachments/assets/e5ac5efd-fc71-405d-92a7-54ef7afcee38" />

# Module 1: Lesson 4 - Chain
1. Learnt tool calling and to use tools with graphs using a chain. This means that a tool is initialised with a list of messages, each containing a node in the graph.
2. Made my own tool calling function that returns a specific category of quotes in technology domain and tested it. I also changed up the initial messages.

# Module 1: Lesson 5 - Router
1. Learnt how to make an LLM decide whether to call a tool by interpreting input via the concept called router. A tool call is generated only when asked, otherwise the LLM responds independently.
2. Below is the example of the code tweaked:
<img width="1468" height="831" alt="image" src="https://github.com/user-attachments/assets/b986df44-6acb-414e-a818-f07cc3f764d9" />

# Module 1: Lesson 6 - Agent
1. Created an Agent that solves mathematical expressions.
2. Router Node Behaviour: Now receives and processes tools calls in a loop until a correct answer is generated.
3. Below is the example of the code tweaked to take two inputs a and b, find it's floor division then exponent and then modulo:
<img width="1170" height="888" alt="image" src="https://github.com/user-attachments/assets/7fa4bfb8-791b-4660-a789-38b1b7b79323" />

# Module 1: Lesson 7 - Agent with Memory
1. Modified the agent that solves mathematical expressions to retain memory via thread_id.
2. Here's a toy around example from LangSmith Studio:
<img width="1470" height="832" alt="image" src="https://github.com/user-attachments/assets/50fd083d-d292-4137-acf5-3acd58b8a1db" />

