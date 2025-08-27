--

### **Vi/Vim 30-Minute Crash Course**

**Objective:** To provide attendees with a foundational understanding of vi/Vim, its history, and the core skills needed to begin editing files confidently from the command line.

**Target Audience:** Developers, System Administrators, IT Professionals, or anyone who works in terminal environments.

**Prerequisites:** Basic familiarity with using a command line (e.g., Bash, SSH).

---

### **Slide 1: Title Slide** (1 min)

**(Visual: Clean slide with Vim logo, title, and your name/details)**

*   **Title:** Taming the Dragon: A 30-Minute Intro to vi/Vim
*   **Subtitle:** From "How do I quit?!" to "This is powerful!"
*   **Presenter:** [Your Name]
*   **Date:** [Date]

**Speaker Notes:**
"Good morning/afternoon, everyone. Welcome to 'Taming the Dragon.' How many of you have ever accidentally found yourself in a text editor in the terminal, been completely confused, and had to Google 'how to quit vim'? *(Pause for show of hands or laughs)*. You're not alone! Today, in the next 30 minutes, we're going to demystify that editor, give you the foundational skills to use it, and hopefully show you why it's still a powerhouse tool after nearly 50 years."

---

### **Slide 2: Agenda & Objectives** (1 min)

**(Visual: Bullet-point list)**

*   **What & Why:** History and Philosophy
*   **vi vs. Vim:** What's the difference?
*   **The Golden Rule:** Modes
*   **Hands-On Foundation:** The essential commands to survive and thrive.
*   **Practice Time:** Let's try it together.
*   **Resources & Q&A**

**Speaker Notes:**
"Here's our game plan for the next half hour. We'll start with a bit of history to understand why this editor is the way it is. We'll clarify the difference between `vi` and `Vim`, then jump into the single most important concept: modes. From there, it's all hands-on keyboard. We'll learn the essential commands, practice them live, and I'll point you to resources to continue your learning after this session."

---

### **Slide 3: History & Philosophy - The "Why"** (3 mins)

**(Visual: Timeline graphic)**

*   **1976:** **vi** (Visual Editor) is created by **Bill Joy** for an early BSD Unix release.
*   **The Predecessor:** `ed` (line editor) -> `ex` (extended editor) -> **vi** (visual mode of `ex`).
*   **The Constraint:** Built for slow, low-bandwidth connections (300-baud modems!). Every keystroke mattered. Hence, no mouse, no menus.
*   **1991:** **Vim** (Vi IMproved) is created by **Bram Moolenaar**. It extends vi with:
    *   Syntax highlighting
    *   Better scripting support
    *   Graphical versions (gVim)
    *   Massive portability (Windows, Mac, Linux)
*   **Philosophy:** **Modal Editing.** Different modes for different tasks (insert text vs. manipulate text). This is the key to efficiency.

**Speaker Notes:**
"Vi was born out of necessity. In an era of slow terminals, you couldn't waste keystrokes or redraw entire graphical screens. The solution was a modal editor. You wouldn't drive a car in just one gear; you have park, reverse, neutral, and drive. Vi/Vim is the same—you change modes for the task at hand. This philosophy is what makes it so powerful and efficient once you learn it."

---

### **Slide 4: vi vs. Vim** (2 mins)

**(Visual: Two-column comparison)**

| Feature | vi (The Original) | Vim (Vi IMproved) |
| :--- | :--- | :--- |
| **Availability** | On nearly every UNIX system ever made. | Must often be installed, but is ubiquitous. |
| **Syntax Highlighting** | No | **Yes** |
| **Graphical UI (GUI)** | No | **Yes** (gVim) |
| **Scripting & Plugins** | Limited | **Extensive** |
| **Ease of Use** | More austere | Better help, undo/redo, user-friendly |

**The Bottom Line:**
*   **`vi`** is a standard. You can always expect it to be there. On modern systems, `vi` is often just a symlink (shortcut) to `vim`.
*   **`vim`** is what you **should use**. It's vi with superpowers and training wheels. For this session, we are learning **Vim**.

**Speaker Notes:**
"Think of `vi` as the classic, base model car. It gets you from A to B. `Vim` is the modern version of that car with power steering, air conditioning, and a GPS. Unless you're on a deeply embedded system, you should be using `vim`. The commands we learn today work in both."

---

### **Slide 5: The Golden Rule: Modes** (3 mins)

**(Visual: Diagram showing the 3 primary modes and how they connect)**

This is the most important concept!

1.  **NORMAL MODE (Command Mode):**
    *   **What it is:** The default mode. Where you navigate, delete, copy, paste, and manipulate text. **You are not inserting text here.**
    *   **How to get there:** Press `ESC` (the "panic button"). Mash it if you're unsure what mode you're in!

2.  **INSERT MODE:**
    *   **What it is:** The mode you're used to. Keys you press are typed as text into the document.
    *   **How to get there:** From Normal mode, press `i` (for **i**nsert).

3.  **VISUAL MODE:**
    *   **What it is:** Like using your mouse to highlight text. You select blocks of text to then manipulate.
    *   **How to get there:** From Normal mode, press `v`.

**Speaker Notes:**
"You will spend most of your time switching between Normal and Insert mode. The power of Vim comes from issuing commands in Normal mode. If you remember nothing else, remember this: **If you're lost, press `ESC` to get back to Normal Mode.** It's your home base."

---

### **Slide 6: Hands-On Foundation - Part 1: Launching & Quitting** (2 mins)

**(Visual: Large, clear command examples)**

*   **Opening a file:** `vim filename.txt`
*   **Quitting (Saving the Burner Phone):**
    *   **Quit without saving:** `:q!` + `Enter` (Think: **Q**uit **!**)
    *   **Save and quit:** `:wq` + `Enter` (Think: **W**rite **Q**uit)
    *   **Just save:** `:w` + `Enter` (Think: **W**rite)

**Speaker Notes:**
"Let's get practical. To open a file, you just type `vim` and the filename. Now, the most famous problem: how to quit. All these commands are issued from Normal mode. `:q!` is your emergency exit. `:wq` is your graceful shutdown. Note the colon `:` – it means you're entering a command."

---

### **Slide 7: Hands-On Foundation - Part 2: Navigation (Normal Mode)** (4 mins)

**(Visual: Graphic of a keyboard with h,j,k,l highlighted)**

Forget the arrow keys! The true Vim way is:

*   **`h`** - left
*   **`j`** - down
*   **`k`** - up
*   **`l`** - right

**Why?** Your fingers never leave the "home row," which is much faster.

**Other Essential Navigation:**
*   **`0`** (zero) - jump to start of line
*   **`$`** - jump to end of line
*   **`gg`** - go to top of file
*   **`G`** - go to bottom of file
*   **`{N}G`** - go to line number `{N}` (e.g., `50G` goes to line 50)

**Speaker Notes:**
"This feels weird at first, but it becomes second nature. Using `h,j,k,l` means you can navigate without moving your hand across the keyboard. Let's practice this next."

---

### **Slide 8: Hands-On Foundation - Part 3: Editing (The Real Power)** (5 mins)

**(Visual: List of commands with examples)**

Editing is about **verbs** and **nouns** (e.g., `d`elete `w`ord).

*   **`i`** - **i**nsert before the cursor
*   **`a`** - **a**ppend (insert after the cursor)
*   **`o`** - open a new line **b**elow and insert
*   **`O`** - open a new line **a**bove and insert

**Deletion (Cut):**
*   **`x`** - delete character under cursor
*   **`dw`** - **d**elete a **w**ord (from cursor to end of word)
*   **`dd`** - **d**elete the entire current line

**Copy & Paste:**
*   **`yy`** - **y**ank (copy) the current line
*   **`p`** - **p**aste after the cursor
*   **`P`** - paste before the cursor

**Undo:**
*   **`u`** - **u**ndo the last change (A lifesaver!)

**Speaker Notes:**
"This is where Vim shines. `dd` deletes a line, but it also copies it. So `dd` then `p` lets you cut and paste a line incredibly quickly. `yy` and `p` is copy and paste. The combination of these simple commands is what makes experts so fast."

---

### **Slide 9: Let's Practice!** (7 mins)

**(Visual: A large, clear terminal screenshot or simply the words "YOUR TURN")**

**Instructor-Led Practice:**
1.  Open your terminal.
2.  Type: `vim practice.txt` (or `vim` alone is fine too).
3.  Press `i` to enter Insert Mode.
4.  Type a few lines of text (e.g., "Hello, this is my first Vim practice.").
5.  Press `ESC` to return to Normal Mode.
6.  **Practice:**
    *   Use `j`, `k` to move up and down.
    *   Move to a word and type `dw` to delete it.
    *   Move to a line and type `dd` to delete it.
    *   Type `u` to undo.
    *   Type `yy` to copy a line, move elsewhere, and type `p` to paste.
    *   Type `:w` to save.
    *   Type `:q!` to quit without saving your changes.

**Speaker Notes:**
"Alright, everyone, your turn! Let's all do this together. I'll walk through each step. Don't worry if you make a mistake—just press `ESC` and `u` to undo. The goal is to get the muscle memory started. I'm here to help if you get stuck."

---

### **Slide 10: How to Learn More & Resources** (1 min)

**(Visual: List of resources with logos/icons if possible)**

*   **Inside Vim:** Type `:help` or `:tutor` and press `Enter`. `vimtutor` is an excellent built-in interactive tutorial. **Do this after the session!**
*   **Online:** `https://vim-adventures.com/` (Game-based learning)
*   **Cheat Sheets:** Search for "Vim cheat sheet" – print one out!
*   **Next Steps:** Search for "Vim motions," "Vim plugins," and ".vimrc configuration."

**Speaker Notes:**
"The best way to learn is by doing. `vimtutor` is the absolute best next step—it will take you 30 minutes and reinforce everything we did today. Keep a cheat sheet handy until the commands become automatic."

---

### **Slide 11: Q&A / Thank You** (1 min)

**(Visual: Clean closing slide with your contact information)**

*   **Questions?**

*   **Thank you!**
*   **[stefan-hacks]**
*   **[Your Email]**
*   **[Your LinkedIn/Twitter]**

**Speaker Notes:**
"Thank you for your time and attention. Does anyone have any quick questions before we wrap up? Feel free to reach out if you have questions later. Now go forth and edit text with power and confidence!"
