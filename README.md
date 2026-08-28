# **Claude Agent SDK Series**

Welcome to the **Claude Agent SDK Playlist** repository!

This playlist is designed to help you understand the Claude Agent SDK from the ground up — starting with your first `query()` call, all the way to advanced topics like custom tools, MCP servers, hooks, subagents, persistent sessions, and human-in-the-loop workflows.
Each video walks you through real, practical examples so you can build production‑ready AI agents using the same agent loop that powers Claude Code.

---

## 🐍 **Install Python Using Miniconda / Miniforge**

To keep your AI projects clean and organized, it is recommended to use **conda environments**. Follow the steps below to install Miniforge and set up your environment.

---

### 🔗 **Download Miniforge for macOS (ARM64)**

Download from the official repository:
https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh

---

### 💻 **Install Miniforge**

Run the following commands:

```bash
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate
```

---

### 🧱 **Create a project-specific conda environment**

```bash
conda create --prefix ./.claude-agent-sdk-youtube-env python=3.13
conda activate ./.claude-agent-sdk-youtube-env
```

---

### 📦 **Install packages from requirements.txt**

```bash
pip install -r requirements.txt
```

Your Claude Agent SDK environment is ready to build powerful AI agents 🚀

---

# **📺 Playlist Breakdown**

### **1. Your First Claude Agent SDK Call**

- Introduction to the Claude Agent SDK and the agent loop that powers Claude Code.
- Using `query()`, the simplest entry point, to send a prompt and stream back messages.

### **2. query() vs ClaudeSDKClient — Which Should You Use?**

- Understanding `query()` for one-shot, stateless calls.
- Using `ClaudeSDKClient` for bidirectional, multi-turn conversations, custom tools, and hooks.

### **3. ClaudeAgentOptions Explained**

- Exploring the config object that controls agent behavior.
- Configuring the `model` and `system_prompt` fields.

### **4. Built-in Tools: File Editing**

- Using the built-in `Read`, `Write`, and `Edit` tools out of the box.
- No custom tool code required with default `ClaudeSDKClient` options.

### **5. Built-in Tools: Bash Execution**

- Running shell commands directly through the built-in `Bash` tool.
- Practical uses like checking file counts, running scripts, and inspecting the environment.

### **6. Built-in Tools: Web Search & Web Fetch**

- Letting the agent look up current information with `WebSearch` and `WebFetch`.
- No custom tool code needed for live web access.

### **7. Your First Custom Tool with Claude Agent SDK**

- Writing plain Python functions and exposing them as tools with `@tool`.
- Extending the agent beyond the built-in tool set.

### **8. Custom Tools Are Secretly In-Process MCP Servers**

- Understanding how `@tool` builds an MCP tool schema behind the scenes.
- Using `create_sdk_mcp_server` to wrap tools in an in-process MCP server.

### **9. Connecting Claude Agent SDK to an External MCP Server**

- Connecting to external MCP servers that run as separate processes.
- Wiring up the official filesystem MCP server via configuration.

### **10. Hooks Part 1: Pre-Tool-Use Logging**

- Understanding hooks as deterministic callbacks invoked by the application, not the model.
- Adding observability and control before a tool call executes.

### **11. Hooks Part 2: Post-Tool-Use Guardrails**

- Running logic after a tool executes but before its result reaches the model.
- Validating or scrubbing tool results, like redacting sensitive fields.

### **12. Subagents: Delegating to a Child Agent with Isolated Context**

- Delegating work to child agents with their own isolated context.
- Understanding the same subagent machinery behind Claude Code's `Task` tool.

### **13. Persistent Sessions: Save, Resume & Fork**

- Saving conversations by `session_id` and resuming them later.
- Forking sessions into independent branches that continue on their own.

### **14. Human-in-the-Loop Checkpoints — Pausing an Agent for Approval**

- Using `ClaudeAgentOptions.can_use_tool` to pause execution before sensitive tool calls.
- Building workflows where humans review and approve AI actions before they proceed.

---

# **📄 requirements.txt**

```
claude-agent-sdk
jupyter
ipykernel
python-dotenv
httpx
```

---

# **🤝 Contributing**

Got suggestions or improvements?
Feel free to open an issue or submit a pull request.

---

# **📜 License**

This project is licensed under the **MIT License**.
See the `LICENSE` file for details.

---

# **📬 Stay Connected**

- [YouTube Channel](https://www.youtube.com/@yashjainio)
- [LinkedIn](https://www.linkedin.com/in/yashjainio)

---

Thank you for checking out the **Claude Agent SDK Playlist**!
Happy building with AI 🚀
