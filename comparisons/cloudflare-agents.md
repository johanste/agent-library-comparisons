### **Nouns (Entities)**

1. **Agent**:
   - Represents an AI-powered entity capable of performing tasks autonomously.
   - Properties:
     - Built-in state management with automatic synchronization.
     - Supports WebSockets for real-time communication.
     - Can execute asynchronous workflows and schedule tasks.
     - Integrates with SQL databases for persistent state.

2. **State**:
   - The built-in state associated with an agent.
   - Properties:
     - Automatically synchronized between the agent and clients.
     - Can trigger events on state changes.
     - Readable and writable via the agent's SQL database.

3. **Task**:
   - Represents a unit of work performed by an agent.
   - Properties:
     - Can run for seconds, minutes, or hours, depending on the task's requirements.
     - Supports asynchronous execution and retries.

4. **Workflow**:
   - A sequence of tasks or operations managed by an agent.
   - Properties:
     - Ensures guaranteed execution with automatic retries.
     - Can persist state for extended durations (e.g., days or weeks).

5. **Event**:
   - Represents triggers or actions within an agent's lifecycle.
   - Properties:
     - Initiates specific operations or transitions.
     - Responds to state changes or external inputs.

6. **WebSocket**:
   - A communication channel for real-time updates between agents and clients.
   - Properties:
     - Streams updates for long-running tasks or asynchronous workflows.
     - Enables low-latency interactivity.

7. **Durable Object**:
   - A stateful micro-server that hosts agents.
   - Properties:
     - Scales to handle millions of requests.
     - Runs close to users for low-latency interactions or near data for high throughput.

8. **SQL Database**:
   - A persistent storage mechanism for agents.
   - Properties:
     - Stores agent state and task-related data.
     - Enables querying and updating state directly.

9. **AI Gateway**:
   - A Cloudflare service for managing AI applications.
   - Properties:
     - Provides caching, rate limiting, and request retries.
     - Supports model fallback for robust AI workflows.

10. **Vectorize**:
    - A vector database for semantic search and memory.
    - Properties:
      - Enables tasks like recommendations, anomaly detection, and context storage.
      - Provides memory for agents interacting with LLMs.

### **Verbs (Actions)**

1. **Create Agent**:
   - Defines a new agent by extending the `Agent` class.
   - Includes methods for state management, scheduling, and task execution.

2. **Set State**:
   - Updates the agent's state.
   - Automatically synchronizes changes with clients.

3. **Schedule Task**:
   - Schedules a task to be executed by the agent.
   - Supports delayed or recurring execution.

4. **Run Workflow**:
   - Executes a sequence of tasks managed by the agent.
   - Ensures guaranteed execution with retries and state persistence.

5. **Trigger Event**:
   - Initiates specific actions or transitions in response to state changes or external inputs.

6. **Stream Updates**:
   - Sends real-time updates to clients via WebSockets.
   - Handles long-running tasks or asynchronous workflows.

7. **Query State**:
   - Reads the agent's state from the SQL database.
   - Enables clients to retrieve task-related data.

8. **Write State**:
   - Writes data to the agent's SQL database.
   - Ensures persistent storage for workflows and tasks.

9. **Deploy Agent**:
   - Deploys an agent to Cloudflare's Durable Objects.
   - Ensures scalability and low-latency interactions.

10. **Integrate AI Gateway**:
    - Configures the AI Gateway for caching, rate limiting, and retries.
    - Supports robust AI workflows with model fallback.

### **Key Relationships**
- **Agents and State**:
  - Agents manage state that is automatically synchronized with clients.
  - State changes can trigger events or workflows.

- **Agents and Workflows**:
  - Workflows consist of tasks executed by agents.
  - Agents ensure guaranteed execution with retries and persistence.

- **Agents and WebSockets**:
  - WebSockets enable real-time communication between agents and clients.
  - Streams updates for long-running tasks or asynchronous workflows.

- **Agents and Durable Objects**:
  - Durable Objects host agents and provide scalability.
  - Enable agents to run close to users or data for optimal performance.

- **Agents and SQL Databases**:
  - SQL databases store agent state and task-related data.
  - Provide persistent storage for workflows and tasks.
