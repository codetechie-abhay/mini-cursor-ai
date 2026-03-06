
# 🤖 Mini Cursor AI

> An AI-powered coding assistant that automatically plans software projects, designs architecture, and generates code.

Mini Cursor AI is a **multi-agent system** that converts a natural language prompt into a working project structure.
It uses specialized agents to **analyze requirements, plan architecture, and implement code automatically**.

---

# 🚀 Features

* **Automated Project Planning**
  Converts user prompts into structured project plans.

* **Architecture Design**
  Breaks down projects into detailed implementation tasks.

* **AI Code Generation**
  Creates and modifies files automatically.

* **Multi-Agent Workflow**
  Uses specialized agents for planning, architecture, and coding.

* **Tool-Based Development**
  Agents interact with the filesystem using tools.

* **Fast LLM Inference**
  Powered by Groq's high-performance inference engine.

---

# 🏗 Architecture

Mini Cursor AI uses a **three-agent pipeline**:

```
Planner Agent → Architect Agent → Coder Agent
```

### Planner Agent

Analyzes the user prompt and generates a structured project plan.

Responsibilities:

* Understand project requirements
* Suggest technology stack
* Define features
* Generate file structure

---

### Architect Agent

Transforms the project plan into implementation tasks.

Responsibilities:

* Break features into tasks
* Define dependencies between tasks
* Specify implementation details

---

### Coder Agent

Executes tasks and generates code.

Responsibilities:

* Create project files
* Write code implementations
* Modify existing files
* Use tools to interact with the filesystem

---

# 📁 Project Structure

```
coder-buddy/

main.py
pyproject.toml
.sample_env
README.md

agent/
├── graph.py
├── states.py
├── prompts.py
└── tools.py
```

### File Descriptions

**main.py**
Application entry point and CLI interface.

**graph.py**
Defines the LangGraph workflow connecting the agents.

**states.py**
Contains data models and shared state definitions.

**prompts.py**
Defines system prompts used by the agents.

**tools.py**
Contains tools for file operations used by the coder agent.

---

# 🧠 Technology Stack

* Python 3.11+
* Groq API
* LangChain
* LangGraph
* Pydantic
* python-dotenv

---

# ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/codetechie-abhay/mini-cursor-ai
cd mini-cursor-ai
```

### 2. Install dependencies

```bash
pip install -e .
```

### 3. Configure environment variables

```bash
cp .sample_env .env
```

Add your API key:

```
GROQ_API_KEY=your_api_key
```

---

# ▶️ Usage

Run the application:

```bash
python main.py
```

Example prompts:

```
Build a modern todo app using HTML, CSS, and JavaScript

Create a REST API for user management using Flask

Develop a React dashboard for data visualization
```

---

# 🔄 Workflow Example

User Prompt

```
Build a weather app using React
```

System Flow

1. Planner → Generates project plan
2. Architect → Creates task breakdown
3. Coder → Writes project files and code

Output: A generated project structure with implemented code.

---

# 🛠 Tools Used by the Coder Agent

| Tool                  | Description                    |
| --------------------- | ------------------------------ |
| read_file             | Reads file content             |
| write_file            | Creates or modifies files      |
| list_files            | Lists files in the directory   |
| get_current_directory | Returns current workspace path |

---

# 🚦 Error Handling

The system handles:

* KeyboardInterrupt (graceful cancellation)
* Validation errors
* Tool execution failures
* API/network issues

---

# 🔮 Future Improvements

* Support for multiple LLM providers
* Web-based interface
* Git integration
* Code review agent
* Plugin system for custom tools

---

# 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Open a pull request

---

# 📄 License

This project is licensed under the MIT License.

---

# 🙏 Acknowledgements

* Groq for fast LLM inference
* LangChain for LLM orchestration
* LangGraph for agent workflow management

---

✅ This version is **correct according to GitHub README standards**:

* clear structure
* no unnecessary marketing text
* clean sections
* easy to read

---
