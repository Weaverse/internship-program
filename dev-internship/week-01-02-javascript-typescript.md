# Week 1-2: JavaScript & TypeScript

> [!IMPORTANT]
> **DO NOT** use AI tools to write code for you. You come here to **LEARN**, the goal of this program is to build
> your programming skills through **hands-on** practice. AI assistants can help explain
> concepts or debug issues, but writing the code yourself is **essential** for learning.

---

|                 |                                                                                                             |
| :-------------- | :---------------------------------------------------------------------------------------------------------- |
| Learning Topics | Core JavaScript, ES6+ features, Functional programming, TypeScript fundamentals, Type-safe development      |
| Objectives      | Complete 30 JS exercises, Master TypeScript basics, Build a type-safe CLI task manager with full TypeScript |

## Beginner JavaScript (Skip if already familiar)
1. Complete [JavaScript Beginner Tutorial](https://www.w3schools.com/js/default.asp)

## Core JavaScript (Days 1-3)
1. Register an account on [Exercism](https://exercism.org)
2. Complete the [Javascript Track](https://exercism.org/tracks/javascript) exercises:
   - **15 Easy exercises** - Start with basics and build confidence
   - **10 Medium exercises** - Apply concepts in more complex scenarios
   - **5 Hard exercises** - Challenge yourself with advanced problems
3. Focus on understanding:
   - Variables and data types
   - Functions and scope
   - Arrays and objects
   - Control flow and loops
   - String manipulation

## Functional Programming (Days 4-5)
1. Start [LearnRx Interactive Tutorial](https://reactivex.io/learnrx/)
2. Complete exercises 1-20 (Arrays and Functions)
3. Focus on:
   - Array methods (map, filter, reduce)
   - Function composition
   - Immutability concepts
   - Promises and Async/Await

## TypeScript Fundamentals (Days 6-10)
1. Read [TypeScript Handbook - The Basics](https://www.typescriptlang.org/docs/handbook/2/basics.html)
2. Set up TypeScript environment:
   ```bash
   npm install -g typescript ts-node @types/node
   tsc --init
   ```
3. Learn essential TypeScript concepts:
   - Type annotations and inference
   - Interfaces and type aliases
   - Function types and generics basics
   - Union and intersection types
   - Enums and literal types
   - Type guards and narrowing

4. Practice with TypeScript exercises:
   ```typescript
   // Example: Type-safe task interface
   interface Task {
     id: string;
     title: string;
     completed: boolean;
     createdAt: Date;
     priority: 'low' | 'medium' | 'high';
   }

   // Type-safe function
   function filterTasksByPriority(tasks: Task[], priority: Task['priority']): Task[] {
     return tasks.filter(task => task.priority === priority);
   }
   ```

## Building Command-Line Applications (Days 11-12)

### Prerequisites - Understanding the Terminal

Before diving into CLI development, it's essential to understand what a terminal is and how to use it effectively:

1. **What is a Terminal?**
   - A terminal (also called command line or shell) is a text-based interface to interact with your computer
   - It allows you to run commands, navigate files, and execute programs without a graphical interface
   - Essential for developers as many tools and scripts are designed for terminal use

2. **Basic Terminal Commands to Practice:**

   **For macOS/Linux (bash/zsh):**
   ```bash
   # Navigation
   pwd          # Print working directory (where you are)
   ls           # List files in current directory
   ls -la       # List all files with details
   cd folder    # Change directory to 'folder'
   cd ..        # Go up one directory
   cd ~         # Go to home directory

   # File Operations
   mkdir mydir  # Create a new directory
   touch file.txt   # Create an empty file
   cp file1 file2   # Copy file1 to file2
   mv file1 file2   # Move/rename file1 to file2
   rm file.txt      # Remove a file (use carefully!)
   cat file.txt     # Display file contents

   # Useful Commands
   clear        # Clear the terminal screen
   history      # Show command history
   echo "text"  # Print text to terminal
   which node   # Find where a program is installed
   ```

   **For Windows (Command Prompt/PowerShell):**
   ```powershell
   # Navigation
   pwd          # Print working directory (PowerShell) or use 'cd' (CMD)
   dir          # List files in current directory (or 'ls' in PowerShell)
   cd folder    # Change directory to 'folder'
   cd ..        # Go up one directory
   cd %USERPROFILE%  # Go to home directory (CMD) or cd ~ (PowerShell)

   # File Operations
   mkdir mydir  # Create a new directory
   type nul > file.txt   # Create empty file (CMD) or New-Item file.txt (PowerShell)
   copy file1 file2      # Copy file1 to file2
   move file1 file2      # Move/rename file1 to file2
   del file.txt          # Remove a file (use carefully!)
   type file.txt         # Display file contents (or 'cat' in PowerShell)

   # Useful Commands
   cls          # Clear the terminal screen
   doskey /h    # Show command history (CMD) or history (PowerShell)
   echo "text"  # Print text to terminal
   where node   # Find where a program is installed
   ```

3. **Practice Exercise:**
   - Open your terminal
   - Navigate to your home directory
   - Create a new directory called "cli-practice"
   - Create a file called "hello.txt" with some content
   - List the contents of the directory
   - Remove the file and directory

### Terminal Setup

Now let's set up a modern, developer-friendly terminal environment:

**Note for Windows Users:** While the instructions below focus on Zsh and Oh My Zsh (primarily for macOS/Linux), Windows users should:
- Install [WSL2 (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) to run Linux commands natively
- After installing WSL2, you can follow the Zsh instructions below within your Linux environment
- Alternatively, use [Git Bash](https://git-scm.com/downloads) which provides Unix-like commands on Windows

1. **What is Zsh?**
   - Zsh (Z shell) is an extended version of the Bash shell with many improvements
   - More powerful auto-completion, better scripting capabilities, and enhanced customization
   - Default shell on macOS since Catalina, available on all platforms
   - Why prefer Zsh over Bash:
     - Smart tab completion (case-insensitive, partial matching)
     - Powerful globbing and pattern matching
     - Better command history search
     - Extensive theming and plugin ecosystem

2. **Install Zsh** (if not already installed):
   ```bash
   # Check if Zsh is installed
   zsh --version

   # Install on macOS (usually pre-installed)
   brew install zsh

   # Install on Ubuntu/Debian
   sudo apt update && sudo apt install zsh

   # Set Zsh as default shell
   chsh -s $(which zsh)
   ```
3. **What is Oh My Zsh?**
   - Oh My Zsh is a framework for managing Zsh configuration
   - Provides themes, plugins, and an auto-update tool
   - Makes Zsh easier to customize and extend
   - **The key difference**: Zsh is the shell itself, Oh My Zsh is a configuration framework that runs on top of Zsh

4. **Install Oh My Zsh**:
   ```bash
   # Install via curl
   sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

   # Or via wget
   sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
   ```
5. **Essential Oh My Zsh Plugins**:
   ```bash
   # Install zsh-autosuggestions for intelligent command completion
   git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

   # Install zsh-syntax-highlighting for command highlighting
   git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
   ```

6. **Configure Oh My Zsh**:
   Edit your `~/.zshrc` file:
   ```bash
   # Open the configuration file
   nano ~/.zshrc

   # Find the plugins line and update it to:
   plugins=(git zsh-autosuggestions zsh-syntax-highlighting node npm)

   # Optional: Change theme (default is robbyrussell)
   ZSH_THEME="agnoster"  # Or try "powerlevel10k/powerlevel10k"

   # Save and reload configuration
   source ~/.zshrc
   ```

7. **Verify Your Setup**:
   ```bash
   # Check shell
   echo $SHELL  # Should show /bin/zsh or similar

   # Test auto-suggestions (type a command you used before)
   # Test syntax highlighting (commands should be colored)
   # Test git plugin (type 'git' and press TAB)
   ```

### CLI Development Setup

1. Try Nodejs built-in prompt:
  ```js
  import readline from 'node:readline';

  const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
  });

  rl.question(`What's your name? `, name => {
    console.log(`Hi ${name}!`);
    rl.close();
  });
  ```

2. Install Commander.js for CLI development:
   ```bash
   npm install commander
   npm install --save-dev @types/node
   ```

3. Learn CLI basics:
   ```typescript
   // Basic CLI structure with Commander.js
   import { Command } from 'commander';

   const program = new Command();

   program
     .name('task-manager')
     .description('CLI task management application')
     .version('1.0.0');

   program
     .command('add <title>')
     .description('Add a new task')
     .option('-p, --priority <priority>', 'Set priority (low|medium|high)', 'medium')
     .action((title, options) => {
       console.log(`Adding task: ${title} with priority: ${options.priority}`);
     });

   program.parse(process.argv);
   ```

4. Essential CLI concepts:
   - Parsing command-line arguments
   - Creating interactive prompts with inquirer
   - Handling file system operations with fs/promises
   - Formatting console output with chalk
   - Creating help documentation
   - Error handling and user feedback

5. File persistence pattern:
   ```typescript
   import { promises as fs } from 'fs';
   import path from 'path';

   const DATA_FILE = path.join(process.cwd(), 'tasks.json');

   async function loadTasks(): Promise<Task[]> {
     try {
       const data = await fs.readFile(DATA_FILE, 'utf-8');
       return JSON.parse(data);
     } catch (error) {
       return []; // Return empty array if file doesn't exist
     }
   }

   async function saveTasks(tasks: Task[]): Promise<void> {
     await fs.writeFile(DATA_FILE, JSON.stringify(tasks, null, 2));
   }
   ```

## Assignment

Build a Type-Safe Task Manager CLI in TypeScript:
- [ ] Set up TypeScript project with proper tsconfig.json
- [ ] Define interfaces for Task
- [ ] Create type-safe command-line interface using Commander.js
- [ ] Implement CRUD operations with full type safety:
  - Add tasks with validation
  - Remove tasks by ID
  - Update task status and priority
  - List and filter tasks
  - Save tasks to JSON file

---

[← Back to Overview](./README.md) | [Next: Week 3-4 →](./week-03-04-dom-css-styling.md)
