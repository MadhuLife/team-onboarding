# Step 5 — Claude Code and the Terminal

## Overview

Claude Code is the AI coding and automation tool we use to build, run, and manage everything in this project. You will use it daily — writing automations, running scripts, organizing files, managing repos, and more.

To use Claude Code, you need a **terminal**. This guide explains what a terminal is, how to install the best one (Warp), and how to install and log into Claude Code using the team account.

---

## Part 1: What Is a Terminal?

A terminal (also called a command line, shell, or console) is a text-based window where you give your computer instructions by typing commands instead of clicking buttons.

Think of it like this:

- When you click a button to open a folder, you are using a graphical interface (GUI)
- When you type `cd Documents` in a terminal to open the same folder, you are using the command line

They do the same thing — but the terminal is faster, more powerful, and lets you do things that no button or menu can do. Many professional tools (including Claude Code) run entirely through the terminal.

**You do not need to be a programmer to use a terminal.** This guide will tell you exactly what to type at every step. Treat it like following a recipe.

### Common Terminal Terms

| Word | What It Means |
|---|---|
| **Terminal / Console** | The app/window where you type commands |
| **Command** | A line of text you type and press Enter to run |
| **Directory** | A folder on your computer |
| **Run / Execute** | Press Enter after typing a command to make it happen |
| **Output** | The text the terminal prints back after you run a command |
| **Prompt** | The blinking cursor where you type — usually shows `$` or `>` |

---

## Part 2: Warp — The Terminal We Use

There are many terminals available, but we use **Warp** because it is modern, beginner-friendly, and has built-in AI assistance. Warp explains commands in plain English, catches errors, and makes the terminal far less intimidating.

### Install Warp on Windows

**System requirement:** Windows 10 version 1809 or later (most modern Windows computers qualify)

1. Open your web browser and go to [https://www.warp.dev/download](https://www.warp.dev/download)
2. Click **Download for Windows**
3. Open the downloaded installer file (`.exe`)
4. If Windows asks for permission, click **Yes**
5. Follow the installer wizard — click **Next** through the steps and then **Install**
6. Click **Finish** — Warp will open automatically
7. Warp may ask you to create a free account — you can sign up or click **Skip** to use it without an account

**Alternative — install via Windows Package Manager (for advanced users):**
Open PowerShell (search for it in the Start menu) and type:
```
winget install Warp.Warp
```
Press **Enter** and wait for it to finish.

### Install Warp on Mac

1. Go to [https://www.warp.dev/download](https://www.warp.dev/download)
2. Click **Download for macOS**
3. Open the downloaded `.dmg` file from your Downloads folder
4. Drag the **Warp** icon into your **Applications** folder
5. Eject the installer, then open Warp from Applications or Launchpad
6. If Mac says the app is from an unidentified developer: go to **System Settings → Privacy & Security** and click **Open Anyway**

### Getting Comfortable with Warp

When Warp opens, you will see a dark window with a text area at the bottom. That is where you type commands.

Some things that make Warp different from older terminals:

- **Blocks:** Each command you run and its output is grouped into a neat block — easy to read, scroll, and copy
- **AI Help:** Type a question in plain English (e.g. "how do I list all files?") and Warp will suggest the right command
- **Autocomplete:** Warp suggests completions as you type — press **Tab** to accept a suggestion
- **Command history:** Press the **Up arrow** key to bring back your last command

You do not need to memorise any commands right now. This guide tells you exactly what to type.

---

## Part 3: What Is Claude Code?

Claude Code is Anthropic's AI tool that lives in your terminal. It can:

- Read, write, and edit files on your computer
- Run scripts and automations
- Work with GitHub repositories
- Help you build and run the tools we use across the project
- Answer questions, debug problems, and complete multi-step tasks on your behalf

You communicate with Claude Code by typing in plain English, just like chatting. You can say "create a folder called leads and move all CSV files into it" and Claude Code will do it — no coding required.

Claude Code is different from the Claude.ai chat website:
- **Claude.ai** = a chat interface in your browser (like ChatGPT)
- **Claude Code** = a powerful agent that runs on your computer, has access to your files, and can take real actions

We use **Claude Code** for the project work.

---

## Part 4: Install Claude Code

### Option A — Desktop App (Easiest, recommended for beginners)

The Claude Code Desktop App lets you use Claude Code without needing the terminal at all. It runs in a window on your computer.

**On Windows:**
1. Go to [https://claude.com/download](https://claude.com/download)
2. Click **Download for Windows**
3. Open the installer (`.exe`) and follow the prompts
4. Launch Claude Code from the Start menu

**On Mac:**
1. Go to [https://claude.com/download](https://claude.com/download)
2. Click **Download for macOS**
3. Open the `.dmg` file and drag Claude Code into Applications
4. Launch it from Applications or Launchpad

---

### Option B — Terminal Version via Warp (More powerful, required for automation work)

The terminal version of Claude Code is what you will use for running our project automations, scripts, and tools. This requires Warp to be installed first (see Part 2).

**On Mac — install Claude Code in Warp:**

1. Open **Warp**
2. Type the following exactly and press **Enter**:
```
npm install -g @anthropic-ai/claude-code
```
3. Wait for it to finish — you will see text scrolling while it installs
4. When it is done, type this and press **Enter** to confirm it worked:
```
claude --version
```
You should see a version number printed back (e.g. `1.x.x`)

**On Windows — install Claude Code in Warp:**

1. Open **Warp**
2. First install Node.js if you do not have it — go to [https://nodejs.org](https://nodejs.org), download the LTS version, and install it
3. Once Node.js is installed, restart Warp
4. Type the following and press **Enter**:
```
npm install -g @anthropic-ai/claude-code
```
5. Wait for installation to complete
6. Confirm it worked by typing:
```
claude --version
```

**Alternative one-line Windows installer (PowerShell):**

Open PowerShell from the Start menu (search "PowerShell"), then paste this and press **Enter**:
```
irm https://claude.ai/install.ps1 | iex
```
This installs Claude Code without needing Node.js separately.

---

## Part 5: Log Into the Team Claude Account

We have a shared team Claude account for the project. You will be given the login credentials by Dr-mkelvo separately via the team communication channel.

### Log In via the Desktop App

1. Open the Claude Code desktop app
2. Click **Sign In**
3. Enter the team email and password provided to you
4. If prompted for two-factor authentication, check the team channel for the code or use the team authenticator app
5. Once signed in, confirm you see the correct account name in the bottom-left corner

### Log In via the Terminal (Warp)

1. Open **Warp**
2. Type the following and press **Enter**:
```
claude
```
3. Claude Code will open a browser window automatically for you to sign in
4. Sign in using the team account credentials provided by Dr-mkelvo
5. After signing in, return to Warp — you will see a confirmation that you are authenticated
6. You are now inside a Claude Code session. Type in plain English to give Claude instructions.

**If the browser does not open automatically:**
- Warp will show a URL — copy it and paste it into your browser manually
- After signing in, copy the code shown in the browser and paste it back into Warp

### Switching Between Accounts

If you have your own Claude account and the team account:
1. Inside a Claude Code session, type `/login` and press **Enter**
2. A browser window will open to re-authenticate
3. Sign in with whichever account you need

---

## Part 6: Running Claude Code for the First Time

Once installed and signed in, here is how to start a session:

1. Open **Warp**
2. Navigate to the project folder. For example, if your repos are saved in `Documents/MadhuLife`, type:

**On Mac:**
```
cd ~/Documents/MadhuLife/madhu-life
```
**On Windows:**
```
cd C:\Users\YourName\Documents\MadhuLife\madhu-life
```
Press **Enter**

3. Type `claude` and press **Enter** to start Claude Code
4. You will see the Claude Code prompt — now just type what you need in plain English. Examples:
   - `summarise all the markdown files in this folder`
   - `create a new folder called archive and move all old files into it`
   - `what is in this project?`

5. To exit a Claude Code session, type `/exit` and press **Enter**, or press `Ctrl + C`

---

## Part 7: Quick Reference

| Task | What to type in Warp |
|---|---|
| Start Claude Code | `claude` |
| Check Claude Code is installed | `claude --version` |
| Log in / switch account | `/login` (inside a Claude session) |
| Exit Claude Code | `/exit` or `Ctrl + C` |
| Go to a folder | `cd path/to/folder` |
| List files in current folder | `ls` (Mac) or `dir` (Windows) |
| Clear the terminal screen | `clear` (Mac) or `cls` (Windows) |

---

## Need Help?

If you get stuck at any step:
1. Copy the error message from Warp
2. Send it to Dr-mkelvo ([@Dr-mkelvo](https://github.com/Dr-mkelvo)) via the team channel
3. Or paste the error directly into a Claude Code session and ask: `what does this error mean and how do I fix it?`
