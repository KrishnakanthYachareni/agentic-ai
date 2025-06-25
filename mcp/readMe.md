## MCP (Model Context Protocol)

**What it's not:**
1. A framework for building agents
2. A fundamental change to how agents work
3. A way to code agents

**What it is:**
1. A protocol - a standard
2. A simple way to integrate tools, resoruces, prompts
3. "A USB-C port for AI applications"

**Reasons not to be excited**
1. It's just a standard, it's not tools themselves
2. LangChain already has big Tools ecosystem
3. You can already make any function into a Tool

**Reasone to be excited**
1. Makes it frictionless to integrate
2. It's taking off! Exploding ecosystem
3. HTML was just a standard, too.


### MCP Core Concepts
(The three components)
1. **Host** is an LLM app like Claude or our Agent architecture
2. **MCP Client** lives inside Host and connects 1:1 to MCP Server
3. **MCP Server** provides tools, context and prompts

Example:
- Fetch is an **MCP Server** that searches the web via a headless browser
- You can configure **Claude Desktop**(The host) to run an MCP CLient that then launches the Fetch **MCP Server** on your computer

**Notes:** 
1. MCP Servers most often run on your box. Connecting to Remote MCP servers are less commmon.
2. Two "Transport" mechanisms: 
    i. **Stdio** spawns and communicates via standard input/output
    ii. Other one is **SSE (Server Side Events)** uses HTTPS connections with streaming. (Server streams back the result to LLM). 
    
    iii. SSE will be useful when we use the Remote MCP Server
    iv. When working on local we can use either of **Stdio** or **SSE**


### Check out the trace

https://platform.openai.com/traces

### Now take a look at some MCP marketplaces

https://mcp.so

https://glama.ai/mcp

https://smithery.ai/

https://huggingface.co/blog/LLMhacker/top-11-essential-mcp-libraries

HuggingFace great community article:
https://huggingface.co/blog/Kseniase/mcp
