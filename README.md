## 🐚 Mini-Shell – System Programming Lab (Ensimag 2A, 2023-2024)

### 🎯 Objective

The goal of this project is to gain hands-on experience with **process management** in UNIX/Linux systems by developing a small command-line interpreter (*mini-shell*).
The idea is to reimplement a subset of the core features of well-known shells such as **bash, zsh, or tcsh**, through a progressive, modular approach.

---

### 🚀 Main Features Implemented

* **Command execution** using `fork()` and `execvp()`.
* **Foreground & background process management** with `&`.
* **Built-in commands** (e.g., `jobs` to list background processes).
* **Input/output redirection** (`<`, `>`).
* **Pipes** (`|`) between two processes.
* **Process and signal handling** via `wait()` / `waitpid()`.

---

### 🔧 Advanced Features / Variants

* Wildcards and environment variables (`*`, `?`, `~`, `$PWD`, etc.).
* Multiple pipes (`cmd1 | cmd2 | cmd3 | ...`).
* Execution time limits (`ulimit`).
* Asynchronous process termination handling (`SIGCHLD`).
* Integration of an embedded **Scheme interpreter (Guile)** to execute shell commands from Scheme code.

---

### 📂 Project Structure

* **CMake + Makefile**: build, testing, and packaging.
* **Unit tests**: automated testing with `make test` and `make check`.
* **AUTHORS file**: contributor list.

---

### 🧪 Example Usage

```bash
$ ./minishell
ensishell> ls -l | grep .c > result.txt
ensishell> sleep 10 &
ensishell> jobs
[1] 12345 sleep 10
```

---

### 👨‍💻 Skills Learned

* System programming in **C**
* Process creation and management, pipes, redirections, and signals
* Debugging and unit testing
* Incremental design of a command-line interpreter
