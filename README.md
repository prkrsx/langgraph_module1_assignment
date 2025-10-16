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
