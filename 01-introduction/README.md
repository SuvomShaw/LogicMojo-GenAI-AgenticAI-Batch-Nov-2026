# Welcome to the Generative AI and Agentic AI batch

Over the next 4–5 months, we will move from Python basics to building AI products. We will learn how data and machine learning work, then explore transformers, large language models (LLMs), retrieval augmented generation (RAG), LangChain, LangGraph, tools, agents and multi-agent systems. We will practise through exercises, projects and a final capstone.

You do not need to understand all these terms today. We will learn them one step at a time.

## 1. Install Python

Python is the programming language we will use throughout the course. Use Python **3.11 or 3.12** for this batch to make it easier to work with course libraries.

- **macOS:** Open [Python downloads for macOS](https://www.python.org/downloads/macos/), choose a stable Python 3.12 release, download the macOS installer and follow its instructions. Open Terminal and run `python3 --version`.
- **Windows:** Open [Python downloads for Windows](https://www.python.org/downloads/windows/), choose a stable Python 3.12 release and run its installer. If shown, select **Add Python to PATH**. Open PowerShell and run `py -3.12 --version` (or `python --version`).

If the command is not found, close and reopen the terminal. Ask your instructor for help if needed.

## 2. Install VS Code

[Download VS Code](https://code.visualstudio.com/download) for your operating system and install it. Open VS Code, click **Extensions** on the left, and install **Python** and **Jupyter** by Microsoft. Open your course folder using **File → Open Folder**.

## 3. What is a Jupyter notebook?

A notebook (`.ipynb`) combines text, code and results in one file. It is useful for learning, experimenting and explaining data. Each piece is a **cell**: a Markdown cell holds notes, and a code cell runs Python. Run a selected cell with **Shift + Enter**. The **kernel** is the Python process that runs your code. Cells share state, so run them in order; after restarting the kernel, run earlier cells again.

## 4. Create a notebook in VS Code

1. Open your course folder in VS Code. Create a file named `practice.ipynb`.
2. Open it, click **Select Kernel**, then select your Python environment (see section 6). If prompted, install `ipykernel`.
3. Add a code cell, type `print("Hello, AI!")`, and press **Shift + Enter**.
4. Add a Markdown cell for your notes. Save with **Ctrl+S** on Windows or **Command+S** on macOS.

See [VS Code notebook documentation](https://code.visualstudio.com/docs/datascience/jupyter-notebooks) if the interface looks different.

## 5. Use Google Colab

[Google Colab](https://colab.research.google.com/) lets you run notebooks in a browser. Sign in with a Google account, choose **New notebook**, type code in a cell and press **Shift + Enter**. Use **File → Save a copy in Drive** to keep your work, or **File → Download → Download .ipynb** to save it locally. You can upload an existing `.ipynb` from the Colab opening screen. Colab runs in a separate temporary environment: local files and locally installed packages are not automatically available there.

## 6. Create a virtual environment

A virtual environment keeps the packages for one project separate from other projects. Open the course folder in VS Code and open **Terminal → New Terminal**.

**macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install ipykernel
```

**Windows PowerShell:**

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install ipykernel
```

If PowerShell blocks activation, use **Command Prompt** in VS Code and run `.venv\Scripts\activate.bat`. In VS Code use **Python: Select Interpreter** from the Command Palette and choose `.venv`; for a notebook also use **Select Kernel → Python Environments → .venv**. Run `python --version` in the activated terminal to check. `deactivate` exits the environment. Reopen the terminal and activate it again when needed. The instructor will share additional packages for later lessons.

## 7. Keep your course work organised

Use one course folder and add a numbered folder for each topic. For example:

```text
genai-agentic-course/
├── .venv/                 # local packages; do not upload
├── 01-introduction/
├── 02-python-basics/
│   ├── python_basics.ipynb
│   └── practice.ipynb
├── 03-python-functions/
├── 04-ml-basics/
├── 05-llms-and-rag/
├── 06-agents/
├── assignments/
├── projects/
├── .gitignore
└── README.md
```

This is a suggested layout, not a fixed class schedule. Add folders as the course progresses. Keep your own practice separate from the original lesson. Each larger project can have its own `.venv` and dependency list.

## 8. Git and GitHub

**Git** tracks changes to files on your computer. **GitHub** hosts Git repositories online, making it easier to back up and share work.

1. Create an account at [github.com](https://github.com/signup) and verify your email.
2. Install Git from [git-scm.com](https://git-scm.com/downloads); on macOS follow the installer or Command Line Tools prompt. On Windows run the installer with the recommended options.
3. Restart the terminal and check `git --version`. Set your name and email once:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

Use an email associated with your GitHub account if you want commits linked to your profile. To get a course repository shared by your instructor, copy its HTTPS URL and run `git clone REPOSITORY_URL` in the parent folder. Open the cloned folder in VS Code. If you are starting your own repository, use `git init` in your course folder, then create a repository on GitHub and follow its instructions to connect the remote.

GitHub requires authentication to push: use the browser sign-in offered by VS Code or Git Credential Manager, or follow [GitHub authentication guidance](https://docs.github.com/en/authentication). Your GitHub account password is not used as a Git password over HTTPS. Do not commit `.venv`, API keys or `.env` files. A starter `.gitignore` can contain:

```gitignore
.venv/
__pycache__/
.ipynb_checkpoints/
.env
```

Review `git status` and your changes before committing and pushing. The instructor will demonstrate this workflow.

## 9. Install Ollama

[Ollama](https://ollama.com/) lets you download and run supported open models locally. Download and install it from [ollama.com/download](https://ollama.com/download) for macOS or Windows, then open the app. In a new terminal, check `ollama --version`. To try a small example model, run:

```bash
ollama run llama3.2:1b
```

The first run downloads the model and needs internet and disk space. Ask a question after the prompt appears; use `/bye` to leave. Performance and model compatibility depend on your computer's memory and hardware. Local models can be slow; we will also learn hosted options later. See the [Ollama quickstart](https://docs.ollama.com/quickstart) for help.

## Ready for class?

Check that Python starts, VS Code opens your folder, and you can run `print("Hello, AI!")` in a notebook. If local setup takes longer, use Colab for the first practice and ask for help with the local setup.
