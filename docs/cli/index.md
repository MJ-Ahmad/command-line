# MJ Command-Line — Documentation Hub

**Maintained by**: Sovereign Architect (MJ Ahmad)  
**Purpose**: To provide a step-by-step guide for deploying MJ smart contracts to Mainnet or Testnet environments

---

## Git

1. **Initialize a repo**  
   `git init` — start a new repository.

2. **Clone a repo**  
   `git clone <url>` — copy an existing repository.

3. **Stage changes**  
   `git add <file>` or `git add .` — prepare files for commit.

4. **Commit changes**  
   `git commit -m "message"` — save changes with a message.

5. **Switch branches**  
   `git switch <branch>` — move between branches.

6. **Create a branch**  
   `git switch -c <branch>` — start a new branch.

7. **View history**  
   `git log --oneline` — see a compact commit history.

8. **Compare changes**  
   `git diff` — check differences before committing.

9. **Push changes**  
   `git push origin main` — send commits to remote.

10. **Pull updates**  
    `git pull` — fetch and merge changes from remote.

---

**Initialize GitHub repo**

1. `git init`
2. `git add .`
3. `git commit -m "Initial commit"`
4. `git branch -M main`
5. `git remote add origin https://github.com/<your-username>/<repo-name>.git`
6. `git push -u origin main`

---

### 🔑 Main Points

- **Getting Started**
  - Initialize a repository: `git init`
  - Clone an existing repository: `git clone <url>`

- **Prepare to Commit**
  - Stage files: `git add <file>` or `git add .`
  - Remove or move files: `git rm`, `git mv`
  - Unstage changes: `git reset`

- **Make Commits**
  - Commit with a message: `git commit -m "message"`
  - Commit staged + tracked changes: `git commit -am "message"`

- **Branching**
  - Switch branches: `git switch <branch>` or `git checkout <branch>`
  - Create new branch: `git switch -c <branch>`
  - Delete branch: `git branch -d <branch>` (force with `-D`)

- **Diff & History**
  - Compare changes: `git diff`
  - Show commit details: `git show <commit>`
  - View logs: `git log`, `git log --oneline`
  - Blame file lines: `git blame <file>`

- **Undo & Restore**
  - Discard changes: `git restore <file>` or `git reset --hard`
  - Stash changes: `git stash`
  - Amend last commit: `git commit --amend`

- **Merge & Rebase**
  - Merge branches: `git merge`
  - Rebase: `git rebase`
  - Cherry-pick commits: `git cherry-pick <commit>`

- **Remote Operations**
  - Add remote: `git remote add <name> <url>`
  - Push changes: `git push origin main`
  - Pull changes: `git pull`

- **Configuration**
  - Set username/email: `git config user.name "Name"`, `git config user.email "Email"`
  - Global config: `git config --global ...`
  - Aliases: `git config alias.st status`

- **Important Files**
  - Local config: `.git/config`
  - Global config: `~/.gitconfig`
  - Ignore list: `.gitignore`  

---

### `gh`

---

## mkdocs 

`Commands & Project Scripts`

### `Command`

**Install mkdocs**

`pip install mkdocs`

**install a theme like Material**

`pip install mkdocs-material`

Create project folder

`mkdir learning-project`

`cd learning-project`

**Initialize mkdocs**

`mkdocs new .` - This will generate mkdocs.yml and a docs/ folder.

**Run local server**

`mkdocs serve` - Visit: `http://127.0.0.1:8000`

**Deploy to GitHub Pages**

`git init`

`git add .`

`git commit -m "Initial commit"`

`git branch -M main`

`git remote add origin https://github.com/<your-username>/<repo-name>.git`

`git push -u origin main`

**Deploy with MKDocs:**

`mkdocs gh-deploy`

**Workflow Summary**

Write docs → in `docs/` folder.  

Preview locally → `mkdocs serve`.  

Commit changes → `git add . && git commit -m "update"`.  

Deploy → `mkdocs gh-deploy`.  

---

### `Project Scripts`

Design a **complete MKDocs project** for “Learning Project” that covers **.NET, ML.NET, Python, Blockchain, etc.** and walk through **setup, build, and deployment to GitHub Pages** step by step.

---

**Project Structure (Folder Tree)**

Here’s a clean structure you can start with:

```
learning-project/
│
├── docs/                     # All documentation lives here
│   ├── index.md              # Home page
│   ├── dotnet/
│   │   ├── intro.md
│   │   ├── tutorials.md
│   │   └── projects.md
│   ├── mlnet/
│   │   ├── intro.md
│   │   ├── examples.md
│   │   └── projects.md
│   ├── python/
│   │   ├── intro.md
│   │   ├── venv.md
│   │   └── projects.md
│   ├── blockchain/
│   │   ├── intro.md
│   │   ├── basics.md
│   │   └── projects.md
│   └── about.md
│
├── mkdocs.yml                # MKDocs configuration file
├── requirements.txt          # Python dependencies
└── README.md                 # Project overview
```

---

**Step 1: Install MKDocs**

Open **PowerShell 7** (since you were checking that earlier):

```powershell
# Install mkdocs
pip install mkdocs

# Optional: install a theme like Material
pip install mkdocs-material
```

---

**Step 2: Initialize Project**

```powershell
# Create project folder
mkdir learning-project
cd learning-project

# Initialize mkdocs
mkdocs new .
```

This will generate `mkdocs.yml` and a `docs/` folder.

---

**Step 3: Configure mkdocs.yml**

Edit `mkdocs.yml`:

```yaml
site_name: Learning Project
theme:
  name: material

nav:
  - Home: index.md
  - .NET:
      - Introduction: dotnet/intro.md
      - Tutorials: dotnet/tutorials.md
      - Projects: dotnet/projects.md
  - ML.NET:
      - Introduction: mlnet/intro.md
      - Examples: mlnet/examples.md
      - Projects: mlnet/projects.md
  - Python:
      - Introduction: python/intro.md
      - Virtual Environments: python/venv.md
      - Projects: python/projects.md
  - Blockchain:
      - Introduction: blockchain/intro.md
      - Basics: blockchain/basics.md
      - Projects: blockchain/projects.md
  - About: about.md
```

---

**Step 4: Build & Preview Locally**

```powershell
# Run local server
mkdocs serve
```

Visit: `http://127.0.0.1:8000`

---

**Step 5: Deploy to GitHub Pages**

1. Initialize GitHub repo:

```powershell
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

2. Deploy with MKDocs:

```powershell
mkdocs gh-deploy
```

This will build the site and push it to the `gh-pages` branch automatically.

---

**Workflow Summary**

1. **Write docs** → in `docs/` folder.  
2. **Preview locally** → `mkdocs serve`.  
3. **Commit changes** → `git add . && git commit -m "update"`.  
4. **Deploy** → `mkdocs gh-deploy`.  

---

👉 Tip: Since you’re learning multiple technologies, keep each topic modular. For example, add **projects.md** in each section where you document hands-on mini-projects (like a Python script, ML.NET model, or Blockchain demo).

Would you like me to also **create a ready-to-use mkdocs.yml file** with Material theme and navigation already set up for your topics so you can copy-paste directly?


---

👉 These ten cover the **core workflow**: start a repo, make changes, commit, branch, review, and sync with remotes.  

Next, create a **visual workflow diagram** showing how these commands connect in a typical project cycle

---

I see exactly what’s happening, Abdul. The warnings you’re seeing break down into two separate issues:

---

### 1. ⚠️ Material Theme Warning
- The **Material for MkDocs team** is warning about **MkDocs 2.0** (still experimental).
- They’re saying it’s **not production-ready** and may break plugins/themes.
- **Solution:** Stick with **MkDocs 1.x** for now. You can downgrade safely:

```powershell
pip install "mkdocs<2.0"
pip install mkdocs-material
```

That way you’ll avoid instability until MkDocs 2.0 stabilizes.

---

### 2. ⚠️ Missing Documentation Files
All those `WARNING - A reference to 'dotnet/intro.md' ... not found` mean your **mkdocs.yml navigation points to files that don’t exist yet**.

### Fix:
Create the missing files inside your `docs/` folder:

```powershell
mkdir docs\dotnet
mkdir docs\mlnet
mkdir docs\python
mkdir docs\blockchain

# Create empty files
ni docs\dotnet\intro.md
ni docs\dotnet\tutorials.md
ni docs\dotnet\projects.md

ni docs\mlnet\intro.md
ni docs\mlnet\examples.md
ni docs\mlnet\projects.md

ni docs\python\intro.md
ni docs\python\venv.md
ni docs\python\projects.md

ni docs\blockchain\intro.md
ni docs\blockchain\basics.md
ni docs\blockchain\projects.md

ni docs\about.md
```

*(Here `ni` = `New-Item` in PowerShell. You can also just create them manually in VS Code.)*

Once those files exist, the warnings will disappear.

---

### ✅ Next Steps
1. **Downgrade MkDocs** to 1.x for stability.  
2. **Create the missing files** so your navigation works.  
3. Run again:

```powershell
mkdocs serve
```

Now your site should build cleanly and serve at `http://127.0.0.1:8000`.

---

👉 Tip: You don’t need to fill all those `.md` files right away. Even empty files will satisfy MkDocs. Later, you can add content gradually for each topic (.NET, ML.NET, Python, Blockchain).

Would you like me to **generate starter content** (like a template intro for each section) so your pages don’t look blank when you first open them?

---

Great, Abdul — since you’ve already downgraded MkDocs to 1.x, let’s automate the creation of all those missing files with a **Python script**. This way, you can just run one `.py` file and it will generate the folder tree and starter content for each section.

---

### 📜 Python Script: `create_docs_structure.py`

Save this file in your project root (`C:\Dev\learn`) and run it with your virtual environment:

```python
import os

# Define the folder structure and files with starter content
structure = {
    "dotnet": {
        "intro.md": "# .NET Introduction\nWelcome to the .NET section.",
        "tutorials.md": "# .NET Tutorials\nStep-by-step guides for learning .NET.",
        "projects.md": "# .NET Projects\nDocument your .NET projects here."
    },
    "mlnet": {
        "intro.md": "# ML.NET Introduction\nOverview of ML.NET for machine learning in .NET.",
        "examples.md": "# ML.NET Examples\nCode samples and use cases.",
        "projects.md": "# ML.NET Projects\nDocument your ML.NET projects here."
    },
    "python": {
        "intro.md": "# Python Introduction\nGetting started with Python.",
        "venv.md": "# Python Virtual Environments\nGuide to creating and using venv.",
        "projects.md": "# Python Projects\nDocument your Python projects here."
    },
    "blockchain": {
        "intro.md": "# Blockchain Introduction\nBasics of blockchain technology.",
        "basics.md": "# Blockchain Basics\nCore concepts explained.",
        "projects.md": "# Blockchain Projects\nDocument your blockchain projects here."
    }
}

# Root docs folder
docs_root = "docs"

# Ensure docs root exists
os.makedirs(docs_root, exist_ok=True)

# Create About page
about_path = os.path.join(docs_root, "about.md")
if not os.path.exists(about_path):
    with open(about_path, "w", encoding="utf-8") as f:
        f.write("# About\nThis project covers .NET, ML.NET, Python, and Blockchain learning resources.")

# Create index page
index_path = os.path.join(docs_root, "index.md")
if not os.path.exists(index_path):
    with open(index_path, "w", encoding="utf-8") as f:
        f.write("# Welcome\nThis is the Learning Project documentation site.")

# Loop through structure and create folders/files
for folder, files in structure.items():
    folder_path = os.path.join(docs_root, folder)
    os.makedirs(folder_path, exist_ok=True)
    for filename, content in files.items():
        file_path = os.path.join(folder_path, filename)
        if not os.path.exists(file_path):
            with open(file_path, "w", encoding="utf-8") as f:
                f.write(content)

print("✅ Documentation structure created successfully!")
```

---

### ⚙️ How to Run

1. Save the script as `create_docs_structure.py` in your project root.  
2. Run it inside your virtual environment:

```powershell
(.mjenv) PS C:\Dev\learn> python create_docs_structure.py
```

3. It will:
   - Create all missing folders (`dotnet`, `mlnet`, `python`, `blockchain`).  
   - Add starter `.md` files with headings and placeholder content.  
   - Generate `index.md` and `about.md` if missing.  

---

### 🎯 Result

After running, your `docs/` folder will look like this:

```
docs/
├── index.md
├── about.md
├── dotnet/
│   ├── intro.md
│   ├── tutorials.md
│   └── projects.md
├── mlnet/
│   ├── intro.md
│   ├── examples.md
│   └── projects.md
├── python/
│   ├── intro.md
│   ├── venv.md
│   └── projects.md
└── blockchain/
    ├── intro.md
    ├── basics.md
    └── projects.md
```

---

👉 This way, you won’t see any more “file not found” warnings when running `mkdocs serve`.  

Would you like me to also extend this script so it **auto-populates each file with a learning roadmap** (like bullet points for topics to cover in .NET, ML.NET, Python, Blockchain), instead of just placeholder text?

---

Excellent, Abdul — the script ran perfectly and your docs structure is now in place. That means all those “file not found” warnings are gone, and you’ve got a solid foundation for your Learning Project.

---

### 🔑 What You’ve Achieved
- **MkDocs downgraded to 1.x** → stable environment.  
- **Python automation script executed** → created all missing folders and `.md` files with starter content.  
- **Docs tree ready** → matches your `mkdocs.yml` navigation.  

---

### 📌 Next Steps: Build & Deploy Workflow

Here’s the complete workflow you can follow every time you update your docs:

### 1. Preview Locally
```powershell
mkdocs serve
```
- Opens at `http://127.0.0.1:8000`  
- Lets you check formatting, navigation, and content before publishing.

---

### 2. Build Static Site
```powershell
mkdocs build
```
- Generates a `site/` folder with HTML, CSS, JS.  
- This is the version that gets deployed.

---

### 3. Push to GitHub
```powershell
git add .
git commit -m "Update docs"
git push origin main
```

---

### 4. Deploy to GitHub Pages
```powershell
mkdocs gh-deploy
```
- Builds the site and pushes it to the `gh-pages` branch.  
- GitHub Pages will serve it at:  
  `https://<your-username>.github.io/<repo-name>/`

---

### 🎯 Suggested Enhancements
- Add **learning roadmaps** in each section (`intro.md`, `projects.md`) with bullet points for topics.  
- Use **Material theme features**:  
  - Search bar  
  - Code highlighting  
  - Tabs and admonitions (`!!! note`, `!!! warning`)  
- Add a **README.md** in the repo root to explain the project purpose.

---

👉 You now have a **repeatable workflow**: write → preview → commit → deploy.  

Would you like me to extend your Python script so it **auto-populates each file with a roadmap outline** (like “Topics to Learn in .NET”, “Python Roadmap”, “Blockchain Essentials”), instead of just placeholder text? That way, you’ll have a structured syllabus ready to expand.

---

Perfect, Abdul — let’s extend your automation so you can generate a **CLI documentation section** automatically. We’ll create a Python script that builds a new file `docs/cli.md` and fills it with structured content for Git CLI, Python CLI, .NET CLI, ML.NET CLI, PowerShell, etc.

---

### 📜 Python Script: `create_cli_docs.py`

Save this in your project root and run it. It will generate `docs/cli.md` with organized headings and starter content.

```python
import os

# Root docs folder
docs_root = "docs"
os.makedirs(docs_root, exist_ok=True)

cli_file = os.path.join(docs_root, "cli.md")

cli_content = """# Command Line Interfaces (CLI)

This section documents common CLIs used in development: Git, Python, .NET, ML.NET, and PowerShell.

---

## Git CLI
### Manual
Overview of Git commands and usage.

### Release Notes
Track Git release updates.

### Getting Started
Basic Git setup and initialization.

### GitHub CLI (gh)
Work seamlessly with GitHub from the command line.

#### Core Commands
- gh auth
- gh browse
- gh codespace
- gh gist
- gh issue
- gh org
- gh pr
- gh project
- gh release
- gh repo
- gh skill

#### GitHub Actions Commands
- gh cache
- gh run
- gh workflow

#### Additional Commands
- gh agent-task
- gh alias
- gh api
- gh attestation
- gh completion
- gh config
- gh copilot
- gh extension
- gh gpg-key
- gh label
- gh licenses
- gh preview
- gh ruleset
- gh search
- gh secret
- gh ssh-key
- gh status
- gh variable

#### Options
--version : Show gh version

#### Examples
```bash
$ gh issue create
$ gh repo clone cli/cli
```

---

## Python CLI

### Manual
Python interpreter and command-line options.

### Common Commands
- python --version
- python -m venv env
- python -m pip install <package>
- python -m unittest

---

## .NET CLI
### Manual
.NET Core command-line interface.

### Common Commands
- dotnet new
- dotnet build
- dotnet run
- dotnet test
- dotnet publish

---

## ML.NET CLI
### Manual
ML.NET Model Builder CLI.

### Common Commands
- mlnet auto-train
- mlnet generate-code
- mlnet evaluate
- mlnet predict

---

## PowerShell (PS)
### Manual
Windows PowerShell and cross-platform PowerShell Core.

### Common Commands
- Get-Help
- Get-Process
- Get-Service
- Set-ExecutionPolicy
- Install-Module
"""

### Write file
with open(cli_file, "w", encoding="utf-8") as f:
    f.write(cli_content)

print("✅ CLI documentation created at docs/cli.md")
```

---

## ⚙️ How to Run

```powershell
(.mjenv) PS C:\Dev\learn> python create_cli_docs.py
```

This will generate `docs/cli.md` with structured sections for Git, Python, .NET, ML.NET, and PowerShell.

---

### 🎯 Result

Your `docs/cli.md` will look like:

```
docs/
└── cli.md
```

Containing headings, subsections, and command lists for each CLI.

---

👉 Next step: add `CLI` to your `mkdocs.yml` navigation:

```yaml
nav:
  - Home: index.md
  - CLI: cli.md
  - .NET: ...
  - ML.NET: ...
  - Python: ...
  - Blockchain: ...
  - About: about.md
```

---

Would you like me to **expand the script further** so each CLI section (Git, Python, .NET, ML.NET, PS) gets its own **subfolder with multiple `.md` files** (like `cli/git.md`, `cli/python.md`, etc.), instead of one big `cli.md`? That way, you can grow each CLI topic separately.

---

Got it, Abdul — let’s automate your **CLI documentation** so you don’t have to manually type out all those commands. We’ll make a Python script that generates a **`docs/cli/` folder** with separate markdown files for each CLI (Git, Python, .NET, ML.NET, PowerShell). This way, you’ll have a clean structure instead of one giant `cli.md`.

---

### 📜 Python Script: `create_cli_structure.py`

Save this in your project root and run it. It will create a `docs/cli/` folder with organized files.

```python
import os

# Root docs folder
docs_root = "docs"
cli_root = os.path.join(docs_root, "cli")

# Ensure CLI folder exists
os.makedirs(cli_root, exist_ok=True)

# Define CLI sections and starter content
cli_sections = {
    "git.md": """# Git CLI
Git command-line interface for version control.

## Manual
Basic Git usage and setup.

## Common Commands
- git init
- git clone <repo>
- git status
- git add .
- git commit -m "message"
- git push
- git pull

## GitHub CLI (gh)
Work seamlessly with GitHub from the command line.

### Core Commands
- gh auth
- gh browse
- gh codespace
- gh gist
- gh issue
- gh org
- gh pr
- gh project
- gh release
- gh repo
- gh skill

### Options
--version : Show gh version

### Examples
```bash
$ gh issue create
$ gh repo clone cli/cli
```""",

    "python.md": """# Python CLI
Python interpreter and command-line options.

## Common Commands
- python --version
- python -m venv env
- python -m pip install <package>
- python -m unittest
""",

    "dotnet.md": """# .NET CLI
.NET Core command-line interface.

## Common Commands
- dotnet new
- dotnet build
- dotnet run
- dotnet test
- dotnet publish
""",

    "mlnet.md": """# ML.NET CLI
ML.NET Model Builder CLI.

## Common Commands
- mlnet auto-train
- mlnet generate-code
- mlnet evaluate
- mlnet predict
""",

    "powershell.md": """# PowerShell CLI
Windows PowerShell and cross-platform PowerShell Core.

## Common Commands
- Get-Help
- Get-Process
- Get-Service
- Set-ExecutionPolicy
- Install-Module
"""
}

# Create each CLI file
for filename, content in cli_sections.items():
    file_path = os.path.join(cli_root, filename)
    if not os.path.exists(file_path):
        with open(file_path, "w", encoding="utf-8") as f:
            f.write(content)

print("✅ CLI documentation structure created at docs/cli/")
```

---

### ⚙️ How to Run

```powershell
(.mjenv) PS C:\Dev\learn> python create_cli_structure.py
```

---

### 📂 Resulting Structure

```
docs/
└── cli/
    ├── git.md
    ├── python.md
    ├── dotnet.md
    ├── mlnet.md
    └── powershell.md
```

---

### 🔗 Update mkdocs.yml

Add this to your navigation:

```yaml
nav:
  - Home: index.md
  - CLI:
      - Git: cli/git.md
      - Python: cli/python.md
      - .NET: cli/dotnet.md
      - ML.NET: cli/mlnet.md
      - PowerShell: cli/powershell.md
  - .NET: ...
  - ML.NET: ...
  - Python: ...
  - Blockchain: ...
  - About: about.md
```

---

👉 This way, each CLI has its own dedicated page, and you can expand them independently as you learn more.  

Would you like me to also **auto-populate Git CLI with the full command list you pasted** (like `gh issue create`, `gh repo clone`, etc.) so it’s all structured into subsections automatically?

---

Perfect, Abdul — let’s supercharge your CLI documentation automation. Since you want **all Git CLI commands you pasted** structured into Markdown files, here’s a Python script that will generate a **`docs/cli/` folder** with separate `.md` files for Git, Python, .NET, ML.NET, and PowerShell. The Git section will be fully populated with the long command list you provided.

---

### 📜 Python Script: `create_cli_full.py`

```python
import os

# Root docs folder
docs_root = "docs"
cli_root = os.path.join(docs_root, "cli")

# Ensure CLI folder exists
os.makedirs(cli_root, exist_ok=True)

# Git CLI content (expanded with your full command list)
git_content = """# Git CLI
Git command-line interface for version control.

## Manual
Basic Git usage and setup.

## Release Notes
Track Git release updates.

## Getting Started
Basic Git setup and initialization.

---

## GitHub CLI (gh)
Work seamlessly with GitHub from the command line.

### Core Commands
gh auth  
gh browse  
gh codespace  
gh gist  
gh issue  
gh org  
gh pr  
gh project  
gh release  
gh repo  
gh skill  

### GitHub Actions Commands
gh cache  
gh run  
gh workflow  

### Additional Commands
gh agent-task  
gh alias  
gh api  
gh attestation  
gh completion  
gh config  
gh copilot  
gh extension  
gh gpg-key  
gh label  
gh licenses  
gh preview  
gh ruleset  
gh search  
gh secret  
gh ssh-key  
gh status  
gh variable  

### Options
--version : Show gh version

### Examples
```bash
$ gh issue create
$ gh repo clone cli/cli
```

---

### Other Git Commands
- git init
- git clone <repo>
- git status
- git add .
- git commit -m "message"
- git push
- git pull
"""

### Other CLI content
python_content = """# Python CLI
Python interpreter and command-line options.

### Common Commands
- python --version
- python -m venv env
- python -m pip install <package>
- python -m unittest
"""

dotnet_content = """# .NET CLI
.NET Core command-line interface.

### Common Commands
- dotnet new
- dotnet build
- dotnet run
- dotnet test
- dotnet publish
"""

mlnet_content = """# ML.NET CLI
ML.NET Model Builder CLI.

### Common Commands
- mlnet auto-train
- mlnet generate-code
- mlnet evaluate
- mlnet predict
"""

powershell_content = """# PowerShell CLI
Windows PowerShell and cross-platform PowerShell Core.

### Common Commands
- Get-Help
- Get-Process
- Get-Service
- Set-ExecutionPolicy
- Install-Module
"""

### Write files
cli_files = {
    "git.md": git_content,
    "python.md": python_content,
    "dotnet.md": dotnet_content,
    "mlnet.md": mlnet_content,
    "powershell.md": powershell_content,
}

for filename, content in cli_files.items():
    file_path = os.path.join(cli_root, filename)
    with open(file_path, "w", encoding="utf-8") as f:
        f.write(content)

print("✅ Full CLI documentation created at docs/cli/")
```

---

## ⚙️ How to Run

```powershell
(.mjenv) PS C:\Dev\learn> python create_cli_full.py
```

---

### 📂 Resulting Structure

```
docs/
└── cli/
    ├── git.md        # Full Git + GitHub CLI commands
    ├── python.md     # Python CLI basics
    ├── dotnet.md     # .NET CLI basics
    ├── mlnet.md      # ML.NET CLI basics
    └── powershell.md # PowerShell basics
```

---

### 🔗 Update mkdocs.yml

```yaml
nav:
  - Home: index.md
  - CLI:
      - Git: cli/git.md
      - Python: cli/python.md
      - .NET: cli/dotnet.md
      - ML.NET: cli/mlnet.md
      - PowerShell: cli/powershell.md
  - .NET: ...
  - ML.NET: ...
  - Python: ...
  - Blockchain: ...
  - About: about.md
```

---

👉 This gives you a **complete CLI syllabus** with Git fully populated, and placeholders for Python, .NET, ML.NET, and PowerShell that you can expand later.  

Would you like me to also **auto-generate subfolders** (like `cli/git/commands.md`, `cli/git/examples.md`) so each Git topic is split into smaller pages instead of one giant `git.md`?

---

Here’s a **complete `mkdocs.yml`** you can drop straight into your project root. It integrates all your learning sections (.NET, ML.NET, Python, Blockchain), plus the new **CLI documentation** with subpages for Git, Python, .NET, ML.NET, and PowerShell.

---

### 📄 mkdocs.yml

```yaml
site_name: Learning Project
site_description: Documentation site for learning .NET, ML.NET, Python, Blockchain, and CLI tools
site_author: Abdul
theme:
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - search.suggest
    - search.highlight
    - content.code.copy
    - content.tabs.link

nav:
  - Home: index.md
  - CLI:
      - Git: cli/git.md
      - Python: cli/python.md
      - .NET: cli/dotnet.md
      - ML.NET: cli/mlnet.md
      - PowerShell: cli/powershell.md
  - .NET:
      - Introduction: dotnet/intro.md
      - Tutorials: dotnet/tutorials.md
      - Projects: dotnet/projects.md
  - ML.NET:
      - Introduction: mlnet/intro.md
      - Examples: mlnet/examples.md
      - Projects: mlnet/projects.md
  - Python:
      - Introduction: python/intro.md
      - Virtual Environments: python/venv.md
      - Projects: python/projects.md
  - Blockchain:
      - Introduction: blockchain/intro.md
      - Basics: blockchain/basics.md
      - Projects: blockchain/projects.md
  - About: about.md

markdown_extensions:
  - admonition
  - codehilite
  - footnotes
  - meta
  - toc:
      permalink: true
  - pymdownx.details
  - pymdownx.superfences
  - pymdownx.tabbed
  - pymdownx.tasklist
  - pymdownx.highlight
  - pymdownx.inlinehilite
  - pymdownx.keys
  - pymdownx.mark
  - pymdownx.critic
  - pymdownx.caret
  - pymdownx.tilde
```

---

### ✅ What This Gives You
- **Material theme** with advanced features (tabs, search, copy code buttons).  
- **Navigation tree** with all your learning topics and CLI subpages.  
- **Markdown extensions** for rich formatting (admonitions, tabs, task lists, syntax highlighting).  

---

### 🚀 Next Steps
1. Save this as `mkdocs.yml` in your project root.  
2. Run locally to preview:

```powershell
mkdocs serve
```

3. Deploy to GitHub Pages:

```powershell
mkdocs gh-deploy
```

---

👉 This setup makes your documentation modular and scalable. Each CLI has its own page, and your learning topics are neatly grouped.  

Would you like me to also **add a “Projects” section under CLI** (e.g., “Git CLI Projects”, “Python CLI Projects”) so you can document hands-on exercises for each tool?

---

### Updated mkdocs.yml

```yaml
site_name: Learning Project
site_description: Documentation site for learning .NET, ML.NET, Python, Blockchain, and CLI tools
site_author: Abdul
theme:
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - search.suggest
    - search.highlight
    - content.code.copy
    - content.tabs.link

nav:
  - Home: index.md
  - CLI:
      - Git: cli/git.md
      - Python: cli/python.md
      - .NET: cli/dotnet.md
      - ML.NET: cli/mlnet.md
      - PowerShell: cli/powershell.md
  - .NET:
      - Introduction: dotnet/intro.md
      - Tutorials: dotnet/tutorials.md
      - Projects: dotnet/projects.md
  - ML.NET:
      - Introduction: mlnet/intro.md
      - Examples: mlnet/examples.md
      - Projects: mlnet/projects.md
  - Python:
      - Introduction: python/intro.md
      - Virtual Environments: python/venv.md
      - Projects: python/projects.md
  - Blockchain:
      - Introduction: blockchain/intro.md
      - Basics: blockchain/basics.md
      - Projects: blockchain/projects.md
  - PowerShell:
      - Introduction: powershell/intro.md
      - Basics: powershell/basics.md
      - Projects: powershell/projects.md
  - About: about.md

markdown_extensions:
  - admonition
  - codehilite
  - footnotes
  - meta
  - toc:
      permalink: true
  - pymdownx.details
  - pymdownx.superfences
  - pymdownx.tabbed
  - pymdownx.tasklist
  - pymdownx.highlight
  - pymdownx.inlinehilite
  - pymdownx.keys
  - pymdownx.mark
  - pymdownx.critic
  - pymdownx.caret
  - pymdownx.tilde
```

---

### Create the PowerShell pages (quick commands)

**PowerShell: create files if missing**

```powershell
mkdir docs\powershell -ErrorAction SilentlyContinue
ni docs\powershell\intro.md -Force
ni docs\powershell\basics.md -Force
ni docs\powershell\projects.md -Force

# Optional: add starter content
Set-Content docs\powershell\intro.md "# PowerShell Introduction`nOverview of PowerShell and cross-platform usage."
Set-Content docs\powershell\basics.md "# PowerShell Basics`nCommon cmdlets and usage examples."
Set-Content docs\powershell\projects.md "# PowerShell Projects`nHands-on exercises and scripts."
```

Run `mkdocs serve` to verify there are no nav warnings and preview the site.

---


### GitHub CLI `gh repo` documentation:

```markdown
# GitHub CLI: `gh repo`

The `gh repo` command in GitHub CLI allows you to manage repositories directly from the command line.  
It includes subcommands for creating, cloning, viewing, forking, and deleting repositories.

---

## 📥 Clone a Repository
```bash
gh repo clone owner/repository-name
```
This will clone the specified repository into your current directory.

---

### 🆕 Create a Repository
```bash
gh repo create my-repo --public --clone
```
Creates a new public repository named `my-repo` and immediately clones it locally.

---

### 🔎 View Repository Details
```bash
gh repo view owner/repository-name --web
```
Opens the repository details in your web browser.

---

### 🍴 Fork a Repository
```bash
gh repo fork owner/repository-name --clone
```
Forks the repository and clones the fork locally.

---

### 🗑️ Delete a Repository
```bash
gh repo delete owner/repository-name --confirm
```
Deletes the specified repository.  
⚠️ **Be cautious**: this action is destructive and cannot be undone.

---

### 💡 Key Considerations
- Use `--help` with any subcommand for detailed options (e.g., `gh repo create --help`).
- Ensure you are authenticated with GitHub CLI (`gh auth login`) before using these commands.
- Be careful with destructive actions like `delete`.

---

## 📚 Learn More
- [GitHub CLI Documentation](https://cli.github.com)
- [GitHub CLI Repo Management](https://cli.github.com/manual/gh_repo)
```

---

This version is clean, structured, and MKDocs-ready:
- Uses headings and sections for clarity.
- Includes fenced code blocks for commands.
- Adds icons/emojis for quick scanning.
- Provides official documentation links at the end.

Would you like me to also create a **Mermaid diagram** showing the lifecycle of `gh repo` commands (create → clone → view → fork → delete) to visually complement this page?

---