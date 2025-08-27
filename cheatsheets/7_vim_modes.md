# Vim Modes


## Introduction

Vim (Vi iMproved) essentially differs from other editors by its use of “modes” inherited from vi. Each mode serves a different purpose like editing text, inserting text, running commands, and so on. It is therefore important to understand what they do, how to switch between them, and how they may influence or change the behavior of Vim’s predefined hotkeys. We’ll cover the 7 most frequently used modes any developer should know:

- Normal
- Insert
- Visual
- Command-line
- Replace
- Binary
- Org

---
## Normal mode

The Normal mode is the default mode when launching Vim. It is the one you’ll spend the most time using as it allows you to navigate the text, copy/cut/paste characters, words and lines, but also roll-back actions, and so on.

![](:/d744fea05c744146a2524c984e43608a)

The fastest way to get back to the Normal mode from any mode you are currently in is to press on the &lt;Esc&gt; key twice, which should cause the screen to flash or the bell to ring.

---
## Insert mode

The Insert mode is the one you should be the most familiar with. It allows you to modify the text buffer by typing and removing characters, the same way you would do in most modern text editors.

![](:/d35b956cfc9c4617a0799bb0526ec8b4)

There are 3 ways to enter the Insert mode from the default Normal mode:

- Pressing i (for *insert*) will directly switch to Insert mode.
- Pressing a (for *append*) will switch to Insert mode and move the cursor after the current character.
- Pressing o will switch to Insert mode and insert a new line below the line the cursor is on.

---
## Visual mode

The Visual mode allows you to visually highlight (select) specific text areas and run commands on them.

To enter the Visual mode from the Normal mode, you can press on v—which will mark the beginning of the selection—and then use the arrow keys to move the cursor to the desired end of the selection. You can then use any of the commands available in the Normal mode for cutting, copying, pasting, and so on.

![](:/40b9a4b3faf3493b8b335a3be1d218c5)

Alternatively, you can also use:

V (for *Visual Line* mode) which will automatically select entire lines.

![](:/b1f74b7fd359451c8ca5f2470f0c5c5d)

&lt;Ctrl&gt; + v (for *Block Visual* mode) which will select rectangular regions of the text.

![](:/a692cde370e54e8096cea90cff3d8a8b)

---
## Command-line mode

The Command-line mode offers a more advanced way of executing commands that are cumbersome or impossible to perform through the Normal mode. For example searching and replacing, or saving and quitting.

To enter the Command-line mode, you can press on :, which will cause the cursor to move at the bottom of the window in the command box. You can then write any command you like and press enter to execute it.
