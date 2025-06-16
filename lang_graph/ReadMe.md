## LangGraph Terminology
1. Agent workflows are represented as **graphs**
2. **State** represents the current sanpshot of the application.
    i. **State** is immutable
    ii.  For each filed in State, we can specify a special function called a **reducer**. This enables LangGraph to run multiple nodes concurrently and combine **State** without overwriting.
3. **Nodes** are python functions that represent agentic logic. They receive the current **State** as input, do something, and return an updated **State**.
4. **Edges** are python functions that dermine which Node to execute next based on the **State**. They can be conditional or fixed.
5. Finally:
    i. **Nodes** -> Do the work
    ii. **Edges** chose what to do next.


### Five steps to the first Graph
1. Define the **State** class
2. Start the Graph Builder
3. Create a **Node**
4. Create **Edges**
5. Compile the Graph
