# 15.10.2026-
AI Agent - Real Task Executor on Groq APIAn autonomous, lightweight Python AI agent powered by the Groq API (openai/gpt-oss-120b). This agent bridges natural language instructions with real system actions, enabling it to manage files, execute shell commands, browse the web, perform calculations, and inspect system environments.🚀 FeaturesReal-World Execution: Interacts directly with your local machine's filesystem, shell, and browser.Autonomous Tool Selection: Uses OpenAI-compatible tool_calls schema routing to select the correct function dynamically based on user intent.Multi-Step ReAct Loop: Capable of multi-step reasoning chains (up to 8 steps by default) to solve complex nested instructions.Robust Error Handling: Safely catches exceptions across file I/O, subprocess execution, and mathematical evaluations.🛠️ Available ToolsTool NameDescriptionParameterscreate_fileCreates a new file with optional text content.filename (str), content (str)read_fileReads the first 500 characters of a file.filename (str)delete_fileDeletes a specified file from disk.filename (str)list_filesLists all contents of a target directory.folder (str, default: ".")run_commandRuns a shell/terminal command with a 15s timeout.command (str)open_websiteOpens any web URL in your default browser.url (str)calculatorEvaluates safe inline Python mathematical expressions.expr (str)get_timeRetrieves current system date and timestamp.Nonesystem_infoInspects OS details, Python version, user, and CWD.Nonewrite_noteAppends timestamped notes to a text file.note (str), filename (str)⚙️ Installation & SetupClone or save the script as agent.py.Install dependencies:pip install openai
Configure your API Key:
Make sure your Groq API key is set correctly in the script:API_KEY = "your_groq_api_key_here"
🚀 UsageRun the script from your terminal:python agent.py
Once started, type any natural language task at the interactive prompt:==================================================
   AI AGENT - REAL TASK EXECUTOR
==================================================
Try commands like:
  - create a file hello.txt with 'Hi there'
  - list all files in this folder
  - open youtube.com
  - show system info
  - what time is it
  - save note: buy milk
  - run command: dir
==================================================

Your task (or 'exit'): 
