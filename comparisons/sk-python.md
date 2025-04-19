### **Nouns (Entities)**

1. **Agent**:
   - An autonomous actor that drives goal-oriented behavior.
   - Properties:
     - Integrates planning, reflection, function execution, and memory.
     - Completes complex tasks in a multi-turn workflow.
     - Can manage multiple concurrent conversations simultaneously.
     - Built on the Semantic Kernel framework for advanced, autonomous behaviors.

2. **Goal**:
   - The objective or end state that the agent is designed to achieve.
   - Properties:
     - Helps the agent determine which functions or skills to invoke.
     - Guides the agent in moving the conversation or task forward.
     - Enables alignment with user-defined objectives.

3. **Planner**:
   - A dedicated component that decomposes high-level goals into actionable steps.
   - Properties:
     - Converts broad objectives into a sequence of function calls or "plan steps."
     - Enables iterative execution of plans by the agent.
     - Leverages the Semantic Kernel's capabilities for structured planning.

4. **Chain-of-Thought**:
   - The internal log or reasoning trail representing the agent’s iterative thought process.
   - Properties:
     - Captures how the agent refines its plan through reflective reasoning.
     - Tracks the reasoning process before each action.
     - Provides transparency into the agent's decision-making process.

5. **Memory**:
   - A persistent storage area for context, prior results, reflections, and relevant data.
   - Properties:
     - Ensures continuity across interactions.
     - Informs subsequent decisions and planning cycles.
     - Supports dynamic adaptability by retaining historical context.

6. **Skill / Tool**:
   - Modular units consisting of semantic functions (prompt templates and LLM completions) or native functions.
   - Properties:
     - Serve as building blocks for performing discrete tasks.
     - Enable the agent to achieve its goals.
     - Can dynamically interact with external services or execute complex tasks.

7. **Context**:
   - The dynamic state passed along through each iteration.
   - Properties:
     - Includes inputs, intermediate outputs, and additional data.
     - Informs planning and execution.
     - Aligns with Semantic Kernel's unified structure for communication.

8. **Execution Trace**:
   - A record of the actions and decisions made during the agent’s lifecycle.
   - Properties:
     - Encapsulates invoked functions, their results, and adjustments made during reflection.
     - Provides a detailed log for debugging and optimization.

9. **Kernel**:
   - The core object in the Semantic Kernel ecosystem that drives AI operations and interactions.
   - Properties:
     - Manages state, processes instructions, and invokes AI services.
     - Acts as the foundation for creating and managing agents.
     - Provides consistency across various agent implementations.

### **Verbs (Actions)**

1. **Initialize / Instantiate**:
   - Creates and configures an agent.
   - Includes setting the goal, attaching skills, connecting to memory, and preparing the planner.
   - Automatically creates a Kernel instance if none is provided.

2. **Plan**:
   - Generates a sequence of actions to achieve the goal.
   - Delegates planning to the planner, which outputs structured steps based on the current context.
   - Leverages Semantic Kernel's planning capabilities.

3. **Reflect**:
   - Evaluates previous actions and outcomes.
   - Enables the agent to assess progress, reconsider strategies, and update plans.
   - Incorporates insights from the execution trace.

4. **Decide / Select**:
   - Chooses the next action or skill invocation.
   - Determines the best function to advance toward the goal based on the current context.
   - Aligns with the agent's reasoning and planning.

5. **Invoke / Execute**:
   - Calls a semantic or native function from a registered skill.
   - Performs specific operations or transformations.
   - Dynamically interacts with external services or APIs.

6. **Update / Modify**:
   - Incorporates new data into the agent’s context or memory after each action.
   - Refines the agent’s state for subsequent planning cycles.
   - Ensures adaptability to changing conditions.

7. **Iterate / Loop**:
   - Repeats the cycle of planning, reflecting, and execution.
   - Continues until the goal is sufficiently met or a stopping criterion is reached.
   - Supports multi-turn workflows.

8. **Conclude / Finalize**:
   - Finalizes the task when the goal is achieved.
   - Summarizes outcomes or presents the final results.
   - Provides a seamless transition to subsequent tasks or interactions.

### **Key Relationships**
- **Agents and Goals**:
  - Agents are driven by goals, which define their purpose and guide their actions.
  - Goals align with user-defined objectives and inform planning.

- **Planner and Skills**:
  - The planner decomposes goals into actionable steps, which are executed using skills.
  - Skills enable agents to perform discrete tasks and interact with external services.

- **Memory and Context**:
  - Memory ensures continuity, while context dynamically informs each iteration.
  - Both are critical for maintaining state and enabling adaptability.

- **Kernel and Agents**:
  - The Kernel provides the foundational context and capabilities for agents.
  - Acts as the engine for processing instructions and managing state.

- **Execution Trace**:
  - Tracks the agent’s lifecycle, including decisions, actions, and reflections.
  - Provides transparency and aids in debugging and optimization.