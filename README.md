# AutoGen Multi-Agent System Project

A comprehensive collection of AutoGen examples and implementations showcasing multi-agent systems, custom tools, human-in-the-loop interactions, and a literature review assistant with Streamlit frontend.

## 📋 Project Overview

This repository contains various AutoGen implementations including:

- **Multi-Agent Systems**: Examples of agent collaboration and communication patterns
- **Custom Tools Integration**: Demonstrations of custom function tools and third-party APIs
- **Human-in-the-Loop**: Interactive agent systems with human feedback mechanisms  
- **Literature Review Assistant**: A specialized two-agent system for academic paper research
- **Streamlit Frontend**: Web interface for the literature review functionality
- **Jupyter Notebooks**: Educational examples and tutorials

## 🗂️ Project Structure

```
autogen/
├── README.md                    # This file
├── requirements.txt             # Python dependencies
├── .env                        # Environment variables (API keys)
├── autogen3/                   # Virtual environment
├── streamlit_app.py            # Streamlit web interface
├── autogen_backend.py          # Literature review backend logic
├── 
├── # Core Examples
├── 9.1 human in the loop.py    # Human interaction examples
├── 9.2 Human in the loop after Run.py
├── 10.1 Custom Tools Function.py # Custom tool implementations
├── 10.2 InbuiltTool.py         # Built-in tool usage
├── 10.3 Third-PartyTools.py    # External API integrations
├──
├── # Jupyter Notebooks
├── 1. Understanding MultiAgent Systems.ipynb
├── 2. SelectorGroupChat.ipynb
├── 5 Configuring LLMs.ipynb
├── Agents in Autogen.ipynb
├── Multi-Model Capabilities with Autogen Agent.ipynb
└── Understanding MultiAgent Systems with termination condition.ipynb
```

##  Quick Start

### Prerequisites

- Python 3.8 or higher
- OpenAI API key
- Git (for cloning)

### 1. Environment Setup

```bash
# Clone the repository
git clone <your-repo-url>
cd autogen

# Create and activate virtual environment
python -m venv autogen3
source autogen3/bin/activate  # On Windows: autogen3\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Configuration

Create or update the `.env` file with your API key:

```bash
echo "OPENAI_API_KEY='your-openai-api-key-here'" > .env
```

### 3. Run Examples

#### Basic Agent Example
```bash
python "10.1 Custom Tools Function.py"
```

#### Human-in-the-Loop Example
```bash
python "9.1 human in the loop.py"
```

#### Literature Review Assistant (CLI)
```bash
python autogen_backend.py
```

#### Web Interface (Streamlit)
```bash
streamlit run streamlit_app.py
```

## 🛠️ AutoGen Studio Setup

AutoGen Studio provides a visual interface for building multi-agent workflows.

### Installation

```bash
# Ensure virtual environment is activated
source autogen3/bin/activate  # Windows: autogen3\Scripts\activate

# Install AutoGen Studio
pip install autogenstudio

# Verify installation
autogenstudio --help
```

### Starting AutoGen Studio

```bash
# Method 1: Command line
autogenstudio ui --host 0.0.0.0 --port 8081

# Method 2: Python module
python -m autogenstudio.ui.main --host 0.0.0.0 --port 8081

# Method 3: Direct execution
autogenstudio ui
```

### Access AutoGen Studio

1. Open your web browser
2. Navigate to: `http://localhost:8081`
3. Start building your multi-agent workflows!

### AutoGen Studio Features

- **Visual Workflow Builder**: Drag-and-drop interface for agent creation
- **Agent Templates**: Pre-built agent configurations
- **Model Management**: Support for multiple LLM providers
- **Chat Interface**: Test your agents in real-time
- **Export Functionality**: Generate code from visual workflows

## 📚 Key Components

### Literature Review System

The `autogen_backend.py` implements a two-agent system:

- **Search Agent**: Queries arXiv and retrieves academic papers
- **Summarizer Agent**: Creates comprehensive literature reviews
- **Streamlit Frontend**: Web interface in `streamlit_app.py`

### Custom Tools Examples

- **String Reversal**: Basic custom function tool
- **HTTP Integration**: External API calls (Cat Facts API)
- **arXiv Search**: Academic paper retrieval

### Human-in-the-Loop Patterns

- **Input Functions**: Real-time human input during conversations
- **Approval Workflows**: Human approval before agent actions
- **Interactive Chat**: Console-based human-agent interaction

## 🔧 Configuration

### Environment Variables

Required in `.env` file:
```
OPENAI_API_KEY='your-openai-api-key'
```

### Model Configuration

Default models used:
- `gpt-4o-mini`: Cost-effective for most tasks
- `gpt-4o`: Higher capability tasks

### Customization Options

- **Agent Personalities**: Modify `system_message` parameters
- **Tool Integration**: Add custom functions via `FunctionTool`
- **Termination Conditions**: Control conversation flow
- **Model Selection**: Switch between OpenAI models

## 🧪 Testing Examples

### Run Individual Components

```bash
# Test custom tools
python "10.1 Custom Tools Function.py"

# Test API integrations  
python "10.2 InbuiltTool.py"

# Test human interaction
python "9.1 human in the loop.py"

# Test literature review backend
python autogen_backend.py
```

### Web Interface Testing

```bash
# Start Streamlit app
streamlit run streamlit_app.py

# Navigate to: http://localhost:8501
# Enter research topic and test the system
```

## 📖 Learning Resources

### Jupyter Notebooks

Start with these notebooks for learning:

1. `1. Understanding MultiAgent Systems.ipynb` - Fundamentals
2. `Agents in Autogen.ipynb` - Agent creation and configuration
3. `5 Configuring LLMs.ipynb` - Model setup and optimization

### Key Concepts Covered

- **Agent Communication Patterns**: Round-robin, selector-based
- **Tool Integration**: Custom functions and external APIs  
- **Termination Conditions**: Conversation flow control
- **Model Selection**: Choosing appropriate LLMs
- **Human Integration**: Interactive agent systems

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Add your examples or improvements
4. Test thoroughly
5. Submit a pull request

## 📝 License

This project is for educational purposes. Please respect OpenAI's usage policies and API rate limits.

## 🆘 Troubleshooting

### Common Issues

**Module Import Errors**
```bash
# Ensure virtual environment is activated
source autogen3/bin/activate
pip install -r requirements.txt
```

**API Key Issues**
```bash
# Check .env file exists and contains valid key
cat .env
# Reload environment
source .env
```

**Port Conflicts**
```bash
# Use different port for Streamlit
streamlit run streamlit_app.py --server.port 8502

# Use different port for AutoGen Studio  
autogenstudio ui --port 8082
```

**AutoGen Studio Not Found**
```bash
# Reinstall AutoGen Studio
pip uninstall autogenstudio
pip install autogenstudio

# Verify installation
which autogenstudio
```

### Getting Help

- Check the [AutoGen Documentation](https://microsoft.github.io/autogen/)
- Review the Jupyter notebooks for examples
- Examine the Python files for implementation patterns

---

## 🚀 Quick Commands Reference

```bash
# Setup
python -m venv autogen3
source autogen3/bin/activate
pip install -r requirements.txt

# Run Examples
python "10.1 Custom Tools Function.py"
python "9.1 human in the loop.py"

# Web Interfaces
streamlit run streamlit_app.py
autogenstudio ui --port 8081

# Access URLs
# Streamlit: http://localhost:8501
# AutoGen Studio: http://localhost:8081
```

Happy coding with AutoGen! 🤖✨