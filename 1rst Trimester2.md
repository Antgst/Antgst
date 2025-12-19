# 🎓 1er trimestre Holberton — Notes & réponses
> Document réorganisé automatiquement (titres, sections, tâches repliables, blocs de code propres).

> <span style="background:#0d1117;color:#58a6ff;border:1px solid #30363d;padding:2px 10px;border-radius:999px;">🧭 Sommaire</span> <span style="background:#0d1117;color:#3fb950;border:1px solid #30363d;padding:2px 10px;border-radius:999px;">🧩 Tâches repliables</span> <span style="background:#0d1117;color:#f2cc60;border:1px solid #30363d;padding:2px 10px;border-radius:999px;">📝 Énoncé</span> <span style="background:#0d1117;color:#c9d1d9;border:1px solid #30363d;padding:2px 10px;border-radius:999px;">✅ Réponse</span>

<a id="sommaire"></a>

## 🧭 Sommaire
- [SHELL, BASICS](#shell-basics)
- [SHELL, PERMISSIONS](#shell-permissions)
- [SHELL, I/O REDIRECTIONS AND FILTERS](#shell-i-o-redirections-and-filters)
- [SHELL, INIT FILES, VARIABLES AND EXPANSIONS](#shell-init-files-variables-and-expansions)
- [C - HELLO, WORLD](#c-hello-world)
- [C - FUNCTIONS, NESTED LOOPS](#c-functions-nested-loops)
- [C - MORE FUNCTIONS, MORE NESTED LOOPS](#c-more-functions-more-nested-loops)
- [C - POINTERS, ARRAYS AND STRINGS](#c-pointers-arrays-and-strings)
- [C - MORE POINTERS, ARRAYS AND STRINGS](#c-more-pointers-arrays-and-strings)
- [C - EVEN MORE POINTERS, ARRAYS AND STRINGS](#c-even-more-pointers-arrays-and-strings)
- [C - RECURSION](#c-recursion)
- [C - ARGC, ARGV](#c-argc-argv)
- [C - MALLOC, FREE](#c-malloc-free)
- [C - MORE MALLOC, FREE](#c-more-malloc-free)
- [C - STRUCTURES, TYPEDEF](#c-structures-typedef)
- [C - VARIADIC FUNCTIONS](#c-variadic-functions)
- [C - DOUBLY LINKED LISTS](#c-doubly-linked-lists)
- [C - FILE I/O](#c-file-i-o)
- [C - HASH TABLES](#c-hash-tables)
- [C - BINARY TREES GEORGIA](#c-binary-trees-georgia)
- [C - BINARY TREES ANTOINE](#c-binary-trees-antoine)

<a id="shell-basics"></a>

## 🐚 SHELL, BASICS

### 📌 General

- What does RTFM mean?
- What is a Shebang
- What is the Shell
- What is the shell
- What is the difference between a terminal and a shell
- What is the shell prompt
- How to use the history (the basics)

### 🧭 Navigation

- What do the commands or built-ins cd, pwd, ls do
- How to navigate the filesystem
- What are the . and .. directories
- What is the working directory, how to print it and how to change it
- What is the root directory
- What is the home directory, and how to go there
- What is the difference between the root directory and the home directory of the user root
- What are the characteristics of hidden files and how to list them
- What does the command cd - do

### 👀 Looking Around

- What do the commands ls, less, file do
- How do you use options and arguments with commands
- Understand the ls long format and how to display it
- A Guided Tour
- What does the ln command do
- What do you find in the most common/important directories
- What is a symbolic link
- What is a hard link
- What is the difference between a hard link and a symbolic link

### 🧰 Manipulating Files

- What do the commands cp, mv, rm, mkdir do
- What are wildcards and how do they work
- How to use wildcards

### 🛠️ Working with Commands

- What do type, which, help, man commands do
- What are the different kinds of commands
- What is an alias
- When do you use the command help instead of man

### 📚 Reading Man Pages

- How to read a man page
- What are man page sections
- What are the section numbers for User commands, System calls and Library functions

### ⌨️ Keyboard Shortcuts for Bash

- Common shortcuts for Bash

### 🕒 LTS

- What does LTS mean?

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 22.04 LTS
- All your scripts should be exactly two lines long ($ wc -l file should print 2)
- All your files should end with a new line (why?)
- The first line of all your files should be exactly #!/bin/bash
- A README.md file at the root of the repo, containing a description of the repository
- A README.md file, at the root of the folder of this project, describing what each script is doing
- You are not allowed to use backticks, &&, || or ;
- All your scripts must be executable. To make your file executable, use the chmod command: chmod u+x FILENAME_GOES_HERE. Later, we’ll learn more about how to utilize this command.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Where am I?</strong></summary>

**📝 Énoncé**

Write a script that prints the absolute path name of the current working directory.

**✅ Réponse**

```bash
#!/bin/bash
pwd
```

</details>

<details>
<summary><strong>🧩 1. What’s in there?.</strong></summary>

**📝 Énoncé**

Display the contents list of your current directory.

**✅ Réponse**

```bash
#!/bin/bash
ls
```

</details>

<details>
<summary><strong>🧩 2. There is no place like home</strong></summary>

**📝 Énoncé**

Write a script that changes the working directory to the user’s home directory.
You are not allowed to use any shell variables

**✅ Réponse**

```bash
#!/bin/bash
cd
```

</details>

<details>
<summary><strong>🧩 3. The long format</strong></summary>

**📝 Énoncé**

Display current directory contents in a long format

**✅ Réponse**

```bash
#!/bin/bash
ls -l
```

</details>

<details>
<summary><strong>🧩 4. Hidden files</strong></summary>

**📝 Énoncé**

Display current directory contents, including hidden files (starting with .). Use the long format.

**✅ Réponse**

```bash
#!/bin/bash
ls -la
```

</details>

<details>
<summary><strong>🧩 5. I love numbers</strong></summary>

**📝 Énoncé**

Display current directory contents.
Long format
with user and group IDs displayed numerically
And hidden files (starting with .)

**✅ Réponse**

```bash
#!/bin/bash
ls -l -n -a
```

</details>

<details>
<summary><strong>🧩 6. Welcome</strong></summary>

**📝 Énoncé**

Create a script that creates a directory named my_first_directory in the /tmp/ directory.

**✅ Réponse**

```bash
#!/bin/bash
mkdir /tmp/my_first_directory
```

</details>

<details>
<summary><strong>🧩 7. Betty in my first directory</strong></summary>

**📝 Énoncé**

Move the file betty from /tmp/ to /tmp/my_first_directory.

**✅ Réponse**

```bash
#!/bin/bash
mv /tmp/betty /tmp/my_first_directory
```

</details>

<details>
<summary><strong>🧩 8. Bye bye Betty</strong></summary>

**📝 Énoncé**

Delete the file betty.
The file betty is in /tmp/my_first_directory

**✅ Réponse**

```bash
#!/bin/bash
rm /tmp/my_first_directory/betty
```

</details>

<details>
<summary><strong>🧩 9. Bye bye My first directory</strong></summary>

**📝 Énoncé**

Delete the directory my_first_directory that is in the /tmp directory.

**✅ Réponse**

```bash
#!/bin/bash
rmdir /tmp/my_first_directory
```

</details>

<details>
<summary><strong>🧩 10. Back to the future</strong></summary>

**📝 Énoncé**

Write a script that changes the working directory to the previous one.

**✅ Réponse**

```bash
#!/bin/bash
cd -
```

</details>

<details>
<summary><strong>🧩 11. Lists</strong></summary>

**📝 Énoncé**

Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.
Be careful with the /

**✅ Réponse**

```bash
#!/bin/bash
ls -la . ..  /boot
```

</details>

<details>
<summary><strong>🧩 12. File type</strong></summary>

**📝 Énoncé**

Write a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.

**✅ Réponse**

```bash
#!/bin/bash
file /tmp/iamafile
```

</details>

<details>
<summary><strong>🧩 13. We are symbols, and inhabit symbols</strong></summary>

**📝 Énoncé**

Create a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory.

**✅ Réponse**

```bash
#!/bin/bash
ln -s /bin/ls __ls__
```

</details>

<details>
<summary><strong>🧩 14. Copy HTML files</strong></summary>

**📝 Énoncé**

Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.
You can consider that all HTML files have the extension .html

**✅ Réponse**

```bash
#!/bin/bash
cp *.html ..
```

</details>

<details>
<summary><strong>🧩 15. Let’s move</strong></summary>

**📝 Énoncé**

Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u.
You can assume that the directory /tmp/u will exist when we will run your script

**✅ Réponse**

```bash
#!/bin/bash
mv [[:upper:]]* /tmp/u
```

</details>

<details>
<summary><strong>🧩 16. Clean Emacs</strong></summary>

**📝 Énoncé**

Create a script that deletes all files in the current working directory that end with the character ~.

**✅ Réponse**

```bash
#!/bin/bash
rm *~
```

</details>

<details>
<summary><strong>🧩 17. Tree</strong></summary>

**📝 Énoncé**

Create a script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory.
You are only allowed to use two spaces (and lines) in your script, not more.

**✅ Réponse**

```bash
#!/bin/bash
mkdir -p welcome/to/school
```

</details>

- --

<a id="shell-permissions"></a>

## 🐚 SHELL, PERMISSIONS

### 🔐 Permissions

- What do the commands chmod, sudo, su, chown, chgrp do
- Linux file permissions
- How to represent each of the three sets of permissions (owner, group, and other) as a single digit
- How to change permissions, owner and group of a file
- Why can’t a normal user chown a file
- How to run a command with root privileges
- How to change user ID or become superuser

### 📖 Other Man Pages


- How to create a user
- How to create a group
- How to print real and effective user and group IDs
- How to print the groups a user is in
- How to print the effective userid

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 22.04 LTS
- All your scripts should be exactly two lines long ($ wc -l file should print 2)
- All your files should end with a new line (why?)
- The first line of all your files should be exactly #!/bin/bash
- A README.md file, at the root of the folder of the project, describing what each script is doing
- You are not allowed to use backticks, &&, || or ;
- All your files must be executable

### 🧩 Tâches

<details>
<summary><strong>🧩 0. My name is Betty</strong></summary>

**📝 Énoncé**

Create a script that switches the current user to the user betty.
You should use exactly 8 characters for your command (+1 character for the new line)
You can assume that the user betty will exist when we will run your script

**✅ Réponse**

```bash
#!/bin/bash
su betty
```

</details>

<details>
<summary><strong>🧩 1. Who am I</strong></summary>

**📝 Énoncé**

Write a script that prints the effective username of the current user.

**✅ Réponse**

```bash
#!/bin/bash
whoami
```

</details>

<details>
<summary><strong>🧩 2. Groups</strong></summary>

**📝 Énoncé**

Write a script that prints all the groups the current user is part of.

**✅ Réponse**

```bash
#!/bin/bash
groups
```

</details>

<details>
<summary><strong>🧩 3. New owner</strong></summary>

**📝 Énoncé**

Write a script that changes the owner of the file hello to the user betty.

**✅ Réponse**

```bash
#!/bin/bash
chown betty hello
```

</details>

<details>
<summary><strong>🧩 4. Empty!</strong></summary>

**📝 Énoncé**

Write a script that creates an empty file called hello.

**✅ Réponse**

```bash
#!/bin/bash
touch hello
```

</details>

<details>
<summary><strong>🧩 5. Execute</strong></summary>

**📝 Énoncé**

Write a script that adds execute permission to the owner of the file hello.

**✅ Réponse**

```bash
#!/bin/bash
chmod 750 hello
```

</details>

<details>
<summary><strong>🧩 6. Multiple permissions</strong></summary>

**📝 Énoncé**

Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
The file hello will be in the working directory

**✅ Réponse**

```bash
#!/bin/bash
chmod 754 hello
```

</details>

<details>
<summary><strong>🧩 7. Everybody!</strong></summary>

**📝 Énoncé**

Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello
The file hello will be in the working directory
You are not allowed to use commas for this script

**✅ Réponse**

```bash
#!/bin/bash
chmod ugo+x hello
```

</details>

<details>
<summary><strong>🧩 8. James Bond</strong></summary>

**📝 Énoncé**

Write a script that sets the permission to the file hello as follows:
Owner: no permission at all
Group: no permission at all
Other users: all the permissions
The file hello will be in the working directory You are not allowed to use commas for this script

**✅ Réponse**

```bash
#!/bin/bash
chmod 007 hello
```

</details>

<details>
<summary><strong>🧩 9. John Doe</strong></summary>

**📝 Énoncé**

Write a script that sets the mode of the file hello to this:
rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
The file hello will be in the working directory
You are not allowed to use commas for this script

**✅ Réponse**

```bash
#!/bin/bash
chmod 753 hello
```

</details>

<details>
<summary><strong>🧩 10. Look in the mirror</strong></summary>

**📝 Énoncé**

Write a script that sets the mode of the file hello the same as olleh’s mode.
The file hello will be in the working directory
The file olleh will be in the working directory

**✅ Réponse**

```bash
#!/bin/bash
chmod $(stat -c "%a" olleh) hello
```

</details>

<details>
<summary><strong>🧩 11. Directories</strong></summary>

**📝 Énoncé**

Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users. Regular files should not be changed.

**✅ Réponse**

```bash
#!/bin/bash
chmod -R a+x .
```

</details>

<details>
<summary><strong>🧩 12. More directories</strong></summary>

**📝 Énoncé**

Create a script that creates a directory called my_dir with permissions 751 in the working directory.

**✅ Réponse**

```bash
#!/bin/bash
mkdir -m 751 my_dir
```

</details>

<details>
<summary><strong>🧩 13. Change group</strong></summary>

**📝 Énoncé**

Write a script that changes the group owner to school for the file hello
The file hello will be in the working directory
The script must be present on the github repository and on the sandbox on the folder /tmp

**✅ Réponse**

```bash
#!/bin/bash
chgrp school hello
```

</details>

<details>
<summary><strong>🧩 14. Owner and group</strong></summary>

**📝 Énoncé**

Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.

**✅ Réponse**

```bash
#!/bin/bash
chown -R vincent:staff .
```

</details>

<details>
<summary><strong>🧩 15. Symbolic links</strong></summary>

**📝 Énoncé**

Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.
The file _hello is in the working directory
The file _hello is a symbolic link

**✅ Réponse**

```bash
#!/bin/bash
chown -h vincent:staff _hello
```

</details>

<details>
<summary><strong>🧩 16. If only</strong></summary>

**📝 Énoncé**

Write a script that changes the owner of the file hello to vincent only if it is owned by the user guillaume.
The file hello will be in the working directory

**✅ Réponse**

```bash
#!/bin/bash
chown --from=guillaume vincent hello
```

</details>

- --

<a id="shell-i-o-redirections-and-filters"></a>

## 🐚 SHELL, I/O REDIRECTIONS AND FILTERS

### 🔁 Shell, I/O Redirection

- What do the commands head, tail, find, wc, sort, uniq, grep, tr do
- How to redirect standard output to a file
- How to get standard input from a file instead of the keyboard
- How to send the output from one program to the input of another program
- How to combine commands and filters with redirections

### ✨ Special Characters

- What are special characters
- Understand what do the white spaces, single quotes, double quotes, backslash, comment, pipe, command separator, tilde and how and when to use them

### 📖 Other Man Pages

- How to display a line of text
- How to concatenate files and print on the standard output
- How to reverse a string
- How to remove sections from each line of files
- What is the /etc/passwd file and what is its format
- What is the /etc/shadow file and what is its format

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 20.04 LTS
- All your scripts should be exactly two lines long ($ wc -l file should print 2)
- All your files should end with a new line (why?)
- The first line of all your files should be exactly #!/bin/bash
- A README.md file, at the root of the folder of the project, describing what each script is doing
- You are not allowed to use backticks, &&, || or ;
- All your files must be executable
- You are not allowed to use sed or awk

### 🔎 More Info

- Read your /etc/passwd and /etc/shadow files.
- Note: You do not have to learn about fmt, pr, du, gzip, tar, lpr, sed and awk yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Hello World</strong></summary>

**📝 Énoncé**

Write a script that prints “Hello, World”, followed by a new line to the standard output.

**✅ Réponse**

```bash
#!/bin/bash
echo "Hello, World"
```

</details>

<details>
<summary><strong>🧩 1. Confused smiley</strong></summary>

**📝 Énoncé**

Write a script that displays a confused smiley "(Ôo)'.

**✅ Réponse**

```bash
#!/bin/bash
echo "\"(Ôo)'"
```

</details>

<details>
<summary><strong>🧩 2. Let's display a file</strong></summary>

**📝 Énoncé**

Display the content of the /etc/passwd file.

**✅ Réponse**

```bash
#!/bin/bash
cat /etc/passwd
```

</details>

<details>
<summary><strong>🧩 3. What about 2?</strong></summary>

**📝 Énoncé**

Display the content of /etc/passwd and /etc/hosts

**✅ Réponse**

```bash
#!/bin/bash
cat /etc/passwd /etc/hosts
```

</details>

<details>
<summary><strong>🧩 4. Last lines of a file</strong></summary>

**📝 Énoncé**

Display the last 10 lines of /etc/passwd
**Tips:** “Thinks of it as a cat, what is at the end of it?”

**✅ Réponse**

```bash
#!/bin/bash
tail -n10 /etc/passwd
```

</details>

<details>
<summary><strong>🧩 5. I'd prefer the first ones actually</strong></summary>

**📝 Énoncé**

Display the first 10 lines of /etc/passwd

**✅ Réponse**

```bash
#!/bin/bash
head -n10 /etc/passwd
```

</details>

<details>
<summary><strong>🧩 6. Line #2</strong></summary>

**📝 Énoncé**

Write a script that displays the third line of the file iacta.
- The file iacta will be in the working directory
- You’re not allowed to use sed

**✅ Réponse**

```bash
#!/bin/bash
head -n3 iacta | tail -n -1
```

</details>

<details>
<summary><strong>🧩 7. It is a good file that cuts iron without making a noise</strong></summary>

**📝 Énoncé**

Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.

**✅ Réponse**

```bash
#!/bin/bash
echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"
```

</details>

<details>
<summary><strong>🧩 8. Save current state of directory</strong></summary>

**📝 Énoncé**

Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.

**✅ Réponse**

```bash
#!/bin/bash
ls -la > ls_cwd_content
```

</details>

<details>
<summary><strong>🧩 9. Duplicate last line</strong></summary>

**📝 Énoncé**

Write a script that duplicates the last line of the file iacta
The file iacta will be in the working directory

**✅ Réponse**

```bash
#!/bin/bash
tail -n 1 iacta >> iacta
```

</details>

<details>
<summary><strong>🧩 10. No more javascript</strong></summary>

**📝 Énoncé**

Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.

**✅ Réponse**

```bash
#!/bin/bash
find . -name "*.js" -type f -delete
```

</details>

<details>
<summary><strong>🧩 11. Don't just count your directories, make your directories count</strong></summary>

**📝 Énoncé**

Write a script that counts the number of directories and sub-directories in the current directory.
The current and parent directories should not be taken into account
Hidden directories should be counted

**✅ Réponse**

```bash
#!/bin/bash
find . -mindepth 1 -type d | wc -l
```

</details>

<details>
<summary><strong>🧩 12. What’s new</strong></summary>

**📝 Énoncé**

Create a script that displays the 10 newest files in the current directory.
One file per line
Sorted from the newest to the oldest

**✅ Réponse**

```bash
#!/bin/bash
ls -t | head -n 10
```

</details>

<details>
<summary><strong>🧩 13. Being unique is better than being perfect</strong></summary>

**📝 Énoncé**

Create a script that takes a list of words as input and prints only words that appear exactly once.
Input format: One line, one word
Output format: One line, one word
Words should be sorted

**✅ Réponse**

```bash
#!/bin/bash
sort | uniq -u
```

</details>

<details>
<summary><strong>🧩 14. It must be in that file</strong></summary>

**📝 Énoncé**

Display lines containing the pattern “root” from the file /etc/passwd

**✅ Réponse**

```bash
#!/bin/bash
grep -w "root" /etc/passwd
```

</details>

<details>
<summary><strong>🧩 15. Count that word</strong></summary>

**📝 Énoncé**

Display the number of lines that contain the pattern “bin” in the file /etc/passwd

**✅ Réponse**

```bash
#!/bin/bash
grep -c "bin" /etc/passwd
```

</details>

<details>
<summary><strong>🧩 16. What's next?</strong></summary>

**📝 Énoncé**

Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.

**✅ Réponse**

```bash
#!/bin/bash
grep -A 3 "root" /etc/passwd
```

</details>

<details>
<summary><strong>🧩 17. I hate bins</strong></summary>

**📝 Énoncé**

Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.

**✅ Réponse**

```bash
#!/bin/bash
grep -L "bin" /etc/passwd
```

</details>

<details>
<summary><strong>🧩 18. Letters only please</strong></summary>

**📝 Énoncé**

Display all lines of the file /etc/ssh/sshd_config starting with a letter.
Include capital letters as well

**✅ Réponse**

```bash
#!/bin/bash
grep '^[[A:Za:z]]' /etc/ssh/sshd_config
```

</details>

<details>
<summary><strong>🧩 19. A to Z</strong></summary>

**📝 Énoncé**

Replace all characters A and c from input to Z and e respectively.

**✅ Réponse**

```bash
#!/bin/bash
tr 'Ac' 'Ze'
```

</details>

<details>
<summary><strong>🧩 20. Without C, you would live in hiago</strong></summary>

**📝 Énoncé**

Create a script that removes all letters c and C from input.

**✅ Réponse**

```bash
#!/bin/bash
tr -d 'Cc'
```

</details>

<details>
<summary><strong>🧩 21. esreveR</strong></summary>

**📝 Énoncé**

Write a script that reverse its input.

**✅ Réponse**

```bash
#!/bin/bash
rev
```

</details>

<details>
<summary><strong>🧩 22. DJ Cut Killer</strong></summary>

**📝 Énoncé**

Write a script that displays all users and their home directories, sorted by users.
Based on the the /etc/passwd file

**✅ Réponse**

```bash
#!/bin/bash
cut -d: -f1,6 /etc/passwd | sort
```

</details>

- --

<a id="shell-init-files-variables-and-expansions"></a>

## 🐚 SHELL, INIT FILES, VARIABLES AND EXPANSIONS

### 📌 General

- What happens when you type $ ls -l *.txt

Shell Initialization Files
- What are the /etc/profile file and the /etc/profile.d directory
- What is the ~/.bashrc file

Variables
- What is the difference between a local and a global variable
- What is a reserved variable
- How to create, update and delete shell variables
- What are the roles of the following reserved variables: HOME, PATH, PS1
- What are special parameters
- What is the special parameter $??

Expansions
- What is expansion and how to use them
- What is the difference between single and double quotes and how to use them properly
- How to do command substitution with $() and backticks

Shell Arithmetic
- How to perform arithmetic operations with the shell

The alias Command
- How to create an alias
- How to list aliases
- How to temporarily disable an alias

Other help pages
- How to execute commands from a file in the current shell

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 20.04 LTS
- All your scripts should be exactly two lines long ($ wc -l file should print 2)
- All your files should end with a new line (why?)
- The first line of all your files should be exactly #!/bin/bash
- A README.md file, at the root of the folder of the project, describing what each script is doing
- You are not allowed to use &&, || or ;
- You are not allowed to use bc, sed or awk
- All your files must be executable

### 🔎 More Info

- Read your /etc/profile, /etc/inputrc and ~/.bashrc files.
- Look at some files in the /etc/profile.d directory.
- Note: You do not have to learn about awk, tar, bzip2, date, scp, ulimit, umask, or shell scripting, yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. <o></strong></summary>

**📝 Énoncé**

Create a script that creates an alias.
Name: ls
Value: rm -f *

**✅ Réponse**

```bash
#!/bin/bash
alias ls="rm -f *"
```

</details>

<details>
<summary><strong>🧩 1. Hello you</strong></summary>

**📝 Énoncé**

Create a script that prints hello user, where user is the current Linux user.

**✅ Réponse**

```bash
#!/bin/bash
echo "hello $USER"
```

</details>

<details>
<summary><strong>🧩 2. The path to success is to take massive, determined action</strong></summary>

**📝 Énoncé**

Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.

**✅ Réponse**

```bash
#!/bin/bash
export PATH="$PATH:/action"
```

</details>

<details>
<summary><strong>🧩 3. If the path be beautiful, let us not ask where it leads</strong></summary>

**📝 Énoncé**

Create a script that counts the number of directories in the PATH.

**✅ Réponse**

```bash
#!/bin/bash
echo $PATH | tr ':' '\n' | grep -v '^$' | wc -l
```

</details>

<details>
<summary><strong>🧩 4. Global variables</strong></summary>

**📝 Énoncé**

Create a script that lists environment variables.

**✅ Réponse**

```bash
#!/bin/bash
printenv
```

</details>

<details>
<summary><strong>🧩 5. Local variables</strong></summary>

**📝 Énoncé**

Create a script that lists all local variables and environment variables, and functions.

**✅ Réponse**

```bash
#!/bin/bash
set
```

</details>

<details>
<summary><strong>🧩 6. Local variable</strong></summary>

**📝 Énoncé**

Create a script that creates a new local variable.
Name: BEST
Value: School

**✅ Réponse**

```bash
#!/bin/bash
BEST="School"
```

</details>

<details>
<summary><strong>🧩 7. Global variable</strong></summary>

**📝 Énoncé**

Create a script that creates a new global variable.
Name: BEST
Value: School

**✅ Réponse**

```bash
#!/bin/bash
export BEST=School
```

</details>

<details>
<summary><strong>🧩 8. Every addition to true knowledge is an addition to human power</strong></summary>

**📝 Énoncé**

Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.

**✅ Réponse**

```bash
#!/bin/bash
echo $(($TRUEKNOWLEDGE+128))
```

</details>

<details>
<summary><strong>🧩 9. Divide and rule</strong></summary>

**📝 Énoncé**

Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.
POWER and DIVIDE are environment variables

**✅ Réponse**

```bash
#!/bin/bash
echo $(($POWER/$DIVIDE))
```

</details>

<details>
<summary><strong>🧩 10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath</strong></summary>

**📝 Énoncé**

Write a script that displays the result of BREATH to the power LOVE
BREATH and LOVE are environment variables
The script should display the result, followed by a new line

**✅ Réponse**

```bash
#!/bin/bash
echo $(($BREATH**$LOVE))
```

</details>

<details>
<summary><strong>🧩 11. There are 10 types of people in the world -- Those who understand binary, and those who don't</strong></summary>

**📝 Énoncé**

Write a script that converts a number from base 2 to base 10.
The number in base 2 is stored in the environment variable BINARY
The script should display the number in base 10, followed by a new line

**✅ Réponse**

```bash
#!/bin/bash
echo $((2#$BINARY))
```

</details>

<details>
<summary><strong>🧩 12. Combination</strong></summary>

**📝 Énoncé**

Create a script that prints all possible combinations of two letters, except oo.
Letters are lower cases, from a to z
One combination per line
The output should be alpha ordered, starting with aa
Do not print oo
Your script file should contain maximum 64 characters

**✅ Réponse**

```bash
#!/bin/bash
printf '%s\n' {a..z}{a..z} | grep -v '^oo$'
```

</details>

<details>
<summary><strong>🧩 13. Floats</strong></summary>

**📝 Énoncé**

Write a script that prints a number with two decimal places, followed by a new line.
The number will be stored in the environment variable NUM.

**✅ Réponse**

```bash
#!/bin/bash
echo $NUM | printf "%.2f\n" "$NUM"
```

</details>

<details>
<summary><strong>🧩 14. Decimal to Hexadecimal</strong></summary>

**📝 Énoncé**

Write a script that converts a number from base 10 to base 16.
The number in base 10 is stored in the environment variable DECIMAL
The script should display the number in base 16, followed by a new line

**✅ Réponse**

```bash
#!/bin/bash
printf '%x\n' $DECIMAL

```
General
- What are the arithmetic operators and how to use them
- What are the logical operators (sometimes called boolean operators) and how to use them
- What the the relational operators and how to use them
- What values are considered TRUE and FALSE in C
- What are the boolean operators and how to use them
- How to use the if, if ... else statements
- How to use comments
- How to declare variables of types char, int, unsigned int
- How to assign values to variables
- How to print the values of variables of type char, int, unsigned int with printf
- How to use the while loop
- How to use variables with the while loop
- How to print variables using printf
- What is the ASCII character set
- What are the purpose of the gcc flags -m32 and -m64

Requirements
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project
- There should be no errors and no warnings during compilation
- You are not allowed to use system
- Your code should use the Betty style. It will be checked using betty-style.pl and - betty-doc.pl
```

```
</details>

<details>
<summary><strong>🧩 0. Positive anything is better than negative nothing</strong></summary>

**📝 Énoncé**

This program will assign a random number to the variable n each time it is executed. Complete the source code in order to print whether the number stored in the variable n is positive or negative.
You can find the source code here
The variable n will store a different value every time you will run this program
You don’t have to understand what rand, srand, RAND_MAX do. Please do not touch this code
The output of the program should be:
The number, followed by
if the number is greater than 0: is positive
if the number is 0: is zero
if the number is less than 0: is negative
followed by a new line

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

/**
 * main - Entry point
 * AFFICHE SUR N EST POSITIF, NEGATIF OU EGALE A 0
 * Return: Always 0 (Success)
 */

int main(void)
{
	int n;

	srand(time(0));
	n = rand() - RAND_MAX / 2;
	if (n > 0)
	{
		printf("%d is positive\n", n);
	}
	else if (n < 0)
	{
		printf("%d is negative\n", n);
	}
	else
	{
		printf("%d is zero\n", n);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 1. The last digit</strong></summary>

**📝 Énoncé**

This program will assign a random number to the variable n each time it is executed. Complete the source code in order to print the last digit of the number stored in the variable n.
You can find the source code here
The variable n will store a different value every time you run this program
You don’t have to understand what rand, srand, and RAND_MAX do. Please do not touch this code
The output of the program should be:
The string Last digit of, followed by
n, followed by
the string is, followed by
if the last digit of n is greater than 5: the string and is greater than 5
if the last digit of n is 0: the string and is 0
if the last digit of n is less than 6 and not 0: the string and is less than 6 and not 0
followed by a new line

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	int n;
	int last_digit;

	srand(time(0));
	n = rand() - RAND_MAX / 2;

	last_digit = n % 10;
	if (last_digit > 5)
	{
		printf("Last digit of %d is %d and is greater than 5\n", n, last_digit);
	}
	else if (last_digit == 0)
	{
		printf("Last digit of %d is %d and is 0\n", n, last_digit);
	}
	else
	{
		printf("Last digit of %d is %d and is less than 6 and not 0\n",
		       n, last_digit);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 2. I sometimes suffer from insomnia. And when I can't fall asleep, I play what I call the alphabet game</strong></summary>

**📝 Énoncé**

Write a program that prints the alphabet in lowercase, followed by a new line.
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
All your code should be in the main function
You can only use putchar twice in your code

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	char i = 'a';

	while (i <= 'z')
	{
		putchar (i);
		i++;
	}
	putchar ('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 3. alphABET</strong></summary>

**📝 Énoncé**

Write a program that prints the alphabet in lowercase, and then in uppercase, followed by a new line.
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
All your code should be in the main function
You can only use putchar three times in your code

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	char i;
	char m;

	i = 'a';
	while (i <= 'z')
	{
		putchar (i);
		i++;
	}
	m = 'A';
	while (m <= 'Z')
	{
		putchar (m);
		m++;
	}
	putchar ('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 4. When I was having that alphabet soup, I never thought that it would pay off</strong></summary>

**📝 Énoncé**

Write a program that prints the alphabet in lowercase, followed by a new line.
Print all the letters except q and e
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
All your code should be in the main function
You can only use putchar twice in your code

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	char i;

	i = 'a';
	while (i <= 'z')
	{
		if (i != 'q' && i != 'e')
			putchar(i);
		i++;
	}
	putchar('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 5. Numbers</strong></summary>

**📝 Énoncé**

Write a program that prints all single digit numbers of base 10 starting from 0, followed by a new line.
All your code should be in the main function

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	char i;

	for (i = 48; i < 58; i++)
	{
		putchar(i);
	}
	putchar('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 6. Numberz</strong></summary>

**📝 Énoncé**

Write a program that prints all single digit numbers of base 10 starting from 0, followed by a new line.
You are not allowed to use any variable of type char
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
You can only use putchar twice in your code
All your code should be in the main function

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
* main - Entry point
*
* Return: Always 0 (Success)
*/

int main(void)
{
	char i;

	for (i = 48; i < 58; i++)
	{
		putchar(i);
	}
	putchar('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 7. Smile in the mirror</strong></summary>

**📝 Énoncé**

Write a program that prints the lowercase alphabet in reverse, followed by a new line.
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
All your code should be in the main function
You can only use putchar twice in your code

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
* main - Entry point
*
* Return: Always 0 (Success)
*/

int main(void)
{
	char i;

	i = 'z';
	while (i >= 'a')
	{
		putchar (i);
		i--;
	}
	putchar ('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 8. Hexadecimal</strong></summary>

**📝 Énoncé**

Write a program that prints all the numbers of base 16 in lowercase, followed by a new line.
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden).
All your code should be in the main function
You can only use putchar three times in your code

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */
int main(void)
{
	char c;

	for (c = '0'; c <= '9'; c++)
	{
		putchar(c);
	}
	for (c = 'a'; c <= 'f'; c++)
	{
		putchar(c);
	}
	putchar('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 9. Patience, persistence and perspiration make an unbeatable combination for success</strong></summary>

**📝 Énoncé**

Write a program that prints all possible combinations of single-digit numbers.
Numbers must be separated by ,, followed by a space
Numbers should be printed in ascending order
You can only use the putchar function (every other function (printf, puts, etc…) is forbidden)
All your code should be in the main function
You can only use putchar four times maximum in your code
You are not allowed to use any variable of type char

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */
int main(void)
{
	int i;

	for (i = 0; i <= 9; i++)
	{
		putchar('0' + i);
		if (i != 9)
		{
			putchar(',');
			putchar(' ');
		}
	}
	putchar('\n');
	return (0);
}
```

</details>

- --

<a id="c-hello-world"></a>

## 💻 C - HELLO, WORLD

### 📌 General

- Why C programming is awesome
- Who invented C
- Who are Dennis Ritchie, Brian Kernighan and Linus Torvalds
- What happens when you type gcc main.c
- What is an entry point
- What is main
- How to print text using printf, puts and putchar
- How to get the size of a specific type using the unary operator sizeof
- How to compile using gcc
- What is the default program name when compiling with gcc
- What is the official C coding style and how to check your code with betty-style
- How to find the right header to include in your source code when using a standard library function
- How does the main function influence the return value of the program

### ✅ Requirements

C
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file at the root of the repo, containing a description of the repository
- A README.md file, at the root of the folder of this project, containing a description of the project
- There should be no errors and no warnings during compilation
- You are not allowed to use system
- Your code should use the Betty style. It will be checked using betty-style.pl and
betty-doc.pl

Shell Scripts
- Allowed editors: vi, vim, emacs
- All your scripts will be tested on Ubuntu 20.04 LTS
- All your scripts should be exactly two lines long ($ wc -l file should print 2)
- All your files should end with a new line
- The first line of all your files should be exactly #!/bin/bash

### 🔎 More Info

Betty linter
- To run the Betty linter just with command betty <filename>:
- Go to the Betty repository
- Clone the repo to your local machine
- cd into the Betty directory
- Install the linter with sudo ./install.sh
- Once saved, exit file and change permissions to apply to all users with chmod a+x betty
- Move the betty file into /bin/ directory or somewhere else in your $PATH with sudo mv betty /bin/
- You can now type betty <filename> to run the Betty linter!

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Preprocessor</strong></summary>

**📝 Énoncé**

Write a script that runs a C file through the preprocessor and save the result into another file.
The C file name will be saved in the variable $CFILE
The output should be saved in the file c

**✅ Réponse**

```bash
#!/bin/bash
gcc -E "$CFILE" -o c
```

</details>

<details>
<summary><strong>🧩 1. Compiler</strong></summary>

**📝 Énoncé**

Write a script that compiles a C file but does not link.
The C file name will be saved in the variable $CFILE
The output file should be named the same as the C file, but with the extension .o instead of .c.
**Example:** if the C file is main.c, the output file should be main.o

**✅ Réponse**

```bash
#!/bin/bash
gcc -c "$CFILE"
```

</details>

<details>
<summary><strong>🧩 2. Assembler</strong></summary>

**📝 Énoncé**

Write a script that generates the assembly code of a C code and save it in an output file.
The C file name will be saved in the variable $CFILE
The output file should be named the same as the C file, but with the extension .s instead of .c.
**Example:** if the C file is main.c, the output file should be main.s

**✅ Réponse**

```bash
#!/bin/bash
gcc -S "$CFILE"
```

</details>

<details>
<summary><strong>🧩 3. Name</strong></summary>

**📝 Énoncé**

Write a script that compiles a C file and creates an executable named cisfun.
The C file name will be saved in the variable $CFILE

**✅ Réponse**

```bash
#!/bin/bash
gcc "$CFILE" -o cisfun
```

</details>

<details>
<summary><strong>🧩 4. Hello, puts</strong></summary>

**📝 Énoncé**

Write a C program that prints exactly "Programming is like building a multilingual puzzle, followed by a new line.
Use the function puts
You are not allowed to use printf
Your program should end with the value 0

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	puts("\"Programming is like building a multilingual puzzle");
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 5. Hello, printf</strong></summary>

**📝 Énoncé**

Write a C program that prints exactly with proper grammar, but the outcome is a piece of art,, followed by a new line.
Use the function printf
You are not allowed to use the function puts
Your program should return 0
Your program should compile without warning when using the -Wall gcc option

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */
int main(void)
{
	printf("with proper grammar, but the outcome is a piece of art,\n");
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 6. Size is not grandeur, and territory does not make a nation</strong></summary>

**📝 Énoncé**

Write a C program that prints the size of various types on the computer it is compiled and run on.
You should produce the exact same output as in the example
Warnings are allowed
Your program should return 0
If you are using a linux on Vagrant you might have to install the package libc6-dev-i386 to test the -m32 gcc option (normally you dont need to do anything on your sandbox).

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Entry point
 *
 * Return: Always 0 (Success)
 */

int main(void)
{
	printf("Size of a char: %zu byte(s)\n", sizeof(char));
	printf("Size of an int: %zu byte(s)\n", sizeof(int));
	printf("Size of a long int: %zu byte(s)\n", sizeof(long int));
	printf("Size of a long long int: %zu byte(s)\n", sizeof(long long int));
	printf("Size of a float: %zu byte(s)\n", sizeof(float));
	return (0);
}
```

</details>

- --

<a id="c-functions-nested-loops"></a>

## 💻 C - FUNCTIONS, NESTED LOOPS

### 📌 General

- What are nested loops and how to use them
- What is a function and how do you use functions
- What is the difference between a declaration and a definition of a function
- What is a prototype
- Scope of variables
- What are the gcc flags -Wall -Werror -pedantic -Wextra -std=gnu89
- What are header files and how to to use them with #include

### ✅ Requirements


- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🔎 More Info

You do not have to understand the call by reference (address), stack, static variables, recursions or arrays, yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. _putchar</strong></summary>

**📝 Énoncé**

Write a program that prints _putchar, followed by a new line.
The program should return 0

**✅ Réponse**

```c
#include "main.h"

/**
 * main - Entry point
 *
 * Return: Always 0
 */
int main(void)
{
	_putchar('_');
	_putchar('p');
	_putchar('u');
	_putchar('t');
	_putchar('c');
	_putchar('h');
	_putchar('a');
	_putchar('r');
	_putchar('\n');
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 1. I sometimes suffer from insomnia. And when I can't fall asleep, I play what I call the alphabet game</strong></summary>

**📝 Énoncé**

Write a function that prints the alphabet, in lowercase, followed by a new line.
**Prototype:** void print_alphabet(void);
You can only use _putchar twice in your code

**✅ Réponse**

```c
#include "main.h"

/**
 * print_alphabet - copie l'alphabet
 *
 * Return: Always 0
 */

void print_alphabet(void)
{
	char c;

	for (c = 'a'; c <= 'z'; c++)
	{
		_putchar(c);
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 2. 10 x alphabet</strong></summary>

**📝 Énoncé**

Write a function that prints 10 times the alphabet, in lowercase, followed by a new line.
**Prototype:** void print_alphabet_x10(void);
You can only use _putchar twice in your code

**✅ Réponse**

```c
#include "main.h"

/**
 * print_alphabet_x10 - salut
 *
 * Return: Always 0 (Success)
 */

void print_alphabet_x10(void)
{
	int i;
	char c;

	for (i = 0; i < 10; i++)
	{
		for (c = 'a'; c <= 'z'; c++)
		{
			_putchar(c);
		}
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 3. islower</strong></summary>

**📝 Énoncé**

Write a function that checks for lowercase character.
**Prototype:** int _islower(int c);
Returns 1 if c is lowercase
Returns 0 otherwise
**Fyi:** The standard library provides a similar function: islower. Run man islower to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _islower - Vérifie si un caractère est une lettre minuscule ASCII.
 * @c: code du caractère à tester
 *
 * Return: 1 si @c est entre 'a' et 'z', sinon 0.
 */

int _islower(int c)
{
	if (c >= 'a' && c <= 'z')
	{
		return (1);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 4. isalpha</strong></summary>

**📝 Énoncé**

Write a function that checks for alphabetic character.
**Prototype:** int _isalpha(int c);
Returns 1 if c is a letter, lowercase or uppercase
Returns 0 otherwise
**Fyi:** The standard library provides a similar function: isalpha. Run man isalpha to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _isalpha - Vérifie si un code correspond à une lettre ASCII.
 * @c: code du caractère à tester
 *
 * Return: 1 si @c est une lettre (a–z ou A–Z), sinon 0.
 */

int _isalpha(int c)
{
	if ((c >= 'A' && c <= 'Z') || (c >= 'a' && c <= 'z'))
	{
		return (1);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 5. Sign</strong></summary>

**📝 Énoncé**

Write a function that prints the sign of a number.
**Prototype:** int print_sign(int n);
Returns 1 and prints + if n is greater than zero
Returns 0 and prints 0 if n is zero
Returns -1 and prints - if n is less than zero

**✅ Réponse**

```c
#include "main.h"

/**
 * print_sign - Affiche le signe d'un entier et retourne un indicateur.
 * @n: entier à évaluer
 *
 * Return: 1 si n > 0 (imprime '+'),
 *         0 si n == 0 (imprime '0'),
 *         -1 si n < 0 (imprime '-').
 */

int print_sign(int n)
{
	if (n > 0)
	{
		_putchar ('+');
		return (1);
	}
	else if (n < 0)
	{
		_putchar ('-');
		return (1);
	}
	else
	{
		_putchar ('0');
		return (0);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 6. There is no such thing as absolute value in this world. You can only estimate what a thing is worth to you</strong></summary>

**📝 Énoncé**

Write a function that computes the absolute value of an integer.
**Prototype:** int _abs(int);
**Fyi:** The standard library provides a similar function: abs. Run man abs to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _abs - Calcule la valeur absolue d’un entier.
 * @n: entier d’entrée
 *
 * Return: valeur absolue de @n.
 */

int _abs(int n)

{
	if (n < 0)
	{
		return (-n);
	}
	return (n);
}
```

</details>

<details>
<summary><strong>🧩 7. There are only 3 colors, 10 digits, and 7 notes; it's what we do with them that's important</strong></summary>

**📝 Énoncé**

Write a function that prints the last digit of a number.
**Prototype:** int print_last_digit(int);
Returns the value of the last digit

**✅ Réponse**

```c
#include "main.h"

/**
 * print_last_digit - Affiche le dernier chiffre d’un entier puis le renvoie.
 * @n: entier à traiter
 *
 * Return: valeur absolue du dernier chiffre (0–9).
 */

int print_last_digit(int n)
{
	int ld = n % 10;

	if (ld < 0)
	{
		ld = -ld;
	}
	_putchar(ld + '0');
	return (ld);
}
```

</details>

<details>
<summary><strong>🧩 8. I'm federal agent Jack Bauer, and today is the longest day of my life</strong></summary>

**📝 Énoncé**

Write a function that prints every minute of the day of Jack Bauer, starting from 00:00 to 23:59.
**Prototype:** void jack_bauer(void);
You can listen to this soundtrack while coding :)

**✅ Réponse**

```c
#include "main.h"

/**
 * jack_bauer - Affiche toutes les minutes de la journée, de 00:00 à 23:59.
 *
 * Return: rien.
 */

void jack_bauer(void)
{
	int minutes, hours;

	for (hours = 0; hours <= 23; hours++)
	{
		for (minutes = 0; minutes <= 59; minutes++)
		{
			_putchar((hours / 10) + '0');
			_putchar((hours % 10) + '0');
			_putchar(':');
			_putchar((minutes / 10) + '0');
			_putchar((minutes % 10) + '0');
			_putchar('\n');
		}
	}
}
```

</details>

<details>
<summary><strong>🧩 9. Learn your times table</strong></summary>

**📝 Énoncé**

Write a function that prints the 9 times table, starting with 0.
**Prototype:** void times_table(void);
Format: see example

**✅ Réponse**

```c
#include "main.h"

/**
 * times_table - Affiche la table de multiplication de 0 à 9.
 *
 * Return: rien.
 */

void times_table(void)
{
	int a, b, resultat;

	for (a = 0; a <= 9; a++)
	{
		for (b = 0; b <= 9; b++)
		{
			resultat = a * b;
			if (b != 0)
			{
				_putchar(',');
				_putchar(' ');
				if (resultat < 10)
					_putchar(' ');
			}
			if (resultat < 10)
				_putchar(resultat + '0');
			else
			{
				_putchar((resultat / 10) + '0');
				_putchar((resultat % 10) + '0');
			}
		}
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 10. a + b</strong></summary>

**📝 Énoncé**

Write a function that adds two integers and returns the result.
**Prototype:** int add(int, int);

**✅ Réponse**

```c
 #include "main.h"

/**
 * add - Additionne deux entiers.
 * @a: premier opérande
 * @b: second opérande
 *
 * Return: somme de @a et @b.
 */

int add(int a, int b)

{
	return (a + b);
}
```

</details>

<details>
<summary><strong>🧩 11. 98 Battery Street, the OG</strong></summary>

**📝 Énoncé**

Write a function that prints all natural numbers from n to 98, followed by a new line.
**Prototype:** void print_to_98(int n);
Numbers must be separated by a comma, followed by a space
Numbers should be printed in order
The first printed number should be the number passed to your function
The last printed number should be 98
You are allowed to use the standard library

**✅ Réponse**

```c
#include <stdio.h>
#include "main.h"

/**
 * print_to_98 - Imprime tous les entiers de @n à 98 inclus.
 * @n: point de départ
 *
 * Return: rien.
 */

void print_to_98(int n)
{
	if (n <= 98)
	{
		for (; n <= 98; n++)
		{
			printf("%d", n);
			if (n != 98)
			{
				putchar(',');
				putchar(' ');
			}
		}
	}
	else
	{
		for (; n >= 98; n--)
		{
			printf("%d", n);
			if (n != 98)
			{
				putchar(',');
				putchar(' ');
			}
		}
	}
	putchar('\n');
}
```

</details>

- --

<a id="c-more-functions-more-nested-loops"></a>

## 💻 C - MORE FUNCTIONS, MORE NESTED LOOPS

### 📌 General

- What are nested loops and how to use them
- What is a function and how do you use functions
- What is the difference between a declaration and a definition of a function
- What is a prototype
- Scope of variables
- What are the gcc flags -Wall -Werror -pedantic -Wextra -std=gnu89
- What are header files and how to to use them with #include

### ✅ Requirements


- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🔎 More Info

- You do not have to understand the call by reference (address), stack, static variables, recursions or arrays, yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. isupper</strong></summary>

**📝 Énoncé**

Write a function that checks for uppercase character.
**Prototype:** int _isupper(int c);
Returns 1 if c is uppercase
Returns 0 otherwise
**Fyi:** The standard library provides a similar function: isupper. Run man isupper to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _isupper - check if is upper.
 * @c : index
 * Return: 1 or 0.
 */

int _isupper(int c)
{
	if (c >= 65 && c <= 90)
	{
		return (1);
	}
	if (c >= 32 && c <= 126)
	{
		return (0);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 1. isdigit</strong></summary>

**📝 Énoncé**

Write a function that checks for a digit (0 through 9).
**Prototype:** int _isdigit(int c);
Returns 1 if c is a digit
Returns 0 otherwise
**Fyi:** The standard library provides a similar function: isdigit. Run man isdigit to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _isdigit - check if is a digit.
 * @c : index
 * Return: 1 or 0.
 */

int _isdigit(int c)
{
	if (c >= 48 && c <= 57)
	{
		return (1);
	}
	else
	{
		return (0);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 2. Collaboration is multiplication</strong></summary>

**📝 Énoncé**

Write a function that multiplies two integers.
**Prototype:** int mul(int a, int b);

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * mul - multiply
 *@a: number 1
 *@b : number 2
 * Return: the multiplication of a and b.
 */

int mul(int a, int b)
{
	return (a * b);
}
```

</details>

<details>
<summary><strong>🧩 3. The numbers speak for themselves</strong></summary>

**📝 Énoncé**

Write a function that prints the numbers, from 0 to 9, followed by a new line.
**Prototype:** void print_numbers(void);
You can only use _putchar twice in your code

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * print_numbers - Imprime les nombres
 *
 * Return: Always 0
 */

void print_numbers(void)
{
	char n;

	for (n = 48; n <= 57; n++)
	{
		_putchar(n);
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 4. I believe in numbers and signs</strong></summary>

**📝 Énoncé**

Write a function that prints the numbers, from 0 to 9, followed by a new line.
**Prototype:** void print_most_numbers(void);
Do not print 2 and 4
You can only use _putchar twice in your code

**✅ Réponse**

```c
#include "main.h"

/**
 * print_most_numbers - imprime des nombres sauf certains
 *
 * Return: Always 0.
 */

void print_most_numbers(void)
{
	char n;

	n = 48;
	while (n <= 57)
	{
		if (n != 50 && n != 52)
			_putchar(n);
		n++;
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 5. Numbers constitute the only universal language</strong></summary>

**📝 Énoncé**

Write a function that prints 10 times the numbers, from 0 to 14, followed by a new line.
**Prototype:** void more_numbers(void);
You can only use _putchar three times in your code

**✅ Réponse**

```c
#include "main.h"

/**
 * more_numbers - print 10X numbers
 *
 * Return: Always 0.
 */

void more_numbers(void)
{
	int line;
	int n;

	for (line = 0; line < 10; line++)
	{
		for (n = 0; n <= 14; n++)
		{
			if (n > 9)
			_putchar('1');
			_putchar(n % 10 + '0');
		}
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 6. The shortest distance between two points is a straight line</strong></summary>

**📝 Énoncé**

Write a function that draws a straight line in the terminal.
**Prototype:** void print_line(int n);
You can only use _putchar function to print
Where n is the number of times the character _ should be printed
The line should end with a \n
If n is 0 or less, the function should only print \n

**✅ Réponse**

```c
#include "main.h"

/**
 * print_line - check the number of lines
 *@n: number of line.
 * Return: a line.
 */

void print_line(int n)
{
	int i;
	{
		if (n > 0)
		{
			for (i = 0; i < n; i++)
				_putchar('_');
		}
	}
	_putchar ('\n');
}
```

</details>

<details>
<summary><strong>🧩 7. I feel like I am diagonally parked in a parallel universe</strong></summary>

**📝 Énoncé**

Write a function that draws a diagonal line on the terminal.
**Prototype:** void print_diagonal(int n);
You can only use _putchar function to print
Where n is the number of times the character \ should be printed
The diagonal should end with a \n
If n is 0 or less, the function should only print a \n

**✅ Réponse**

```c
#include "main.h"

/**
 * print_diagonal - print a diagonal line
 *@n: integer
 * Return: a diagonal line
 */

void print_diagonal(int n)
{
	int i;
	int j;

	if (n <= 0)
	{
		_putchar('\n');
		return;
	}
	for (i = 0; i < n; i++)
	{
		for (j = 0; j < i; j++)
			_putchar(' ');
		_putchar('\\');
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 8. You are so much sunshine in every square inch</strong></summary>

**📝 Énoncé**

Write a function that prints a square, followed by a new line.
**Prototype:** void print_square(int size);
You can only use _putchar function to print
Where size is the size of the square
If size is 0 or less, the function should print only a new line
Use the character # to print the square

**✅ Réponse**

```c
#include "main.h"

/**
 * print_square - print a square
 *@size : integer
 * Return: a square
 */

void print_square(int size)
{
	int i;
	int j;

	if (size <= 0)
	{
		_putchar('\n');
		return;
	}
	for (i = 0; i < size; i++)
	{
		for (j = 0; j < size; j++)
			_putchar('#');
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 9. Fizz-Buzz</strong></summary>

**📝 Énoncé**

The “Fizz-Buzz test” is an interview question designed to help filter out the 99.5% of programming job candidates who can’t seem to program their way out of a wet paper bag.
Write a program that prints the numbers from 1 to 100, followed by a new line. But for multiples of three print Fizz instead of the number and for the multiples of five print Buzz. For numbers which are multiples of both three and five print FizzBuzz.
Each number or word should be separated by a space
You are allowed to use the standard library

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - printa fizz buzz
 *
 * Return: always 0
 */

int main(void)
{
	int nombre;

	{
		for (nombre = 1; nombre <= 100; nombre++)
		{
			if (nombre % 3 == 0 && nombre % 5 == 0)
			printf("FizzBuzz");

			else if (nombre % 3 == 0)
			printf("Fizz");

			else if (nombre % 5 == 0)
			printf("Buzz");

			else
				printf("%d", nombre);
			if (nombre < 100)
				printf(" ");
		}
	}
	printf("\n");
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 10. Triangles</strong></summary>

**📝 Énoncé**

Write a function that prints a triangle, followed by a new line.
**Prototype:** void print_triangle(int size);
You can only use _putchar function to print
Where size is the size of the triangle
If size is 0 or less, the function should print only a new line
Use the character # to print the triangle

**✅ Réponse**

```c
#include "main.h"

/**
 * print_triangle - print a triangle
 * @size: integer
 * Return: a triangle
 */

void print_triangle(int size)
{
	{
		int i;
		int j;
		int k;

		if (size <= 0)
		{
			_putchar('\n');
			return;
		}
		for (i = 1; i <= size; i++)
		{
			for (j = 0; j < size - i; j++)
				_putchar(' ');
			for (k = 0; k < i; k++)
				_putchar('#');
			_putchar('\n');
		}
	}
}
```

</details>

- --

<a id="c-pointers-arrays-and-strings"></a>

## 💻 C - POINTERS, ARRAYS AND STRINGS

### 📌 General

- What are nested loops and how to use them
- What is a function and how do you use functions
- What is the difference between a declaration and a definition of a function
- What is a prototype
- Scope of variables
- What are the gcc flags -Wall -Werror -pedantic -Wextra -std=gnu89
- What are header files and how to to use them with #include

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🔎 More Info

- You do not have to understand the call by reference (address), stack, static variables, recursions or arrays, yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. 98 Battery st.</strong></summary>

**📝 Énoncé**

Write a function that takes a pointer to an int as parameter and updates the value it points to to 98.
**Prototype:** void reset_to_98(int *n);

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * reset_to_98 - updates the value it points.
 * @n: pointer
 * Return: 0.
 */

void reset_to_98(int *n)
{
	*n = 98;
}
```

</details>

<details>
<summary><strong>🧩 1. Don't swap horses in crossing a stream</strong></summary>

**📝 Énoncé**

Write a function that swaps the values of two integers.
**Prototype:** void swap_int(int *a, int *b);

**✅ Réponse**

```c
#include "main.h"

/**
 * swap_int - swap the value of a and b.
 * @a: pointer a
 * @b: pointer b
 * Return: a and b values.
 */

void swap_int(int *a, int *b)
{
	int tmp;

	tmp = *a;
	*a = *b;
	*b = tmp;
}
```

</details>

<details>
<summary><strong>🧩 2. This report, by its very length, defends itself against the risk of being read</strong></summary>

**📝 Énoncé**

Write a function that returns the length of a string.
**Prototype:** int _strlen(char *s);
**Fyi:** The standard library provides a similar function: strlen. Run man strlen to learn more.

**✅ Réponse**

```c
#include <stdio.h>

/**
 * _strlen - check the len of an str.
 * @s: char *
 * Return: the len.
 */

int _strlen(char *s)
{
	int len = 0;

	while (s[len] != '\0')
	{
		len++;
	}
	return (len);
}
```

</details>

<details>
<summary><strong>🧩 3. I do not fear computers. I fear the lack of them</strong></summary>

**📝 Énoncé**

Write a function that prints a string, followed by a new line, to stdout.
**Prototype:** void _puts(char *str);
**Fyi:** The standard library provides a similar function: puts. Run man puts to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _puts - updates the value it points.
 * @str: string
 * Return: 0.
 */

void _puts(char *str)
{
	int i = 0;

	while (str[i] != '\0')
	{
		_putchar(str[i]);
		i++;
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 4. I can only go one way. I've not got a reverse gear</strong></summary>

**📝 Énoncé**

Write a function that prints a string, in reverse, followed by a new line.
**Prototype:** void print_rev(char *s);

**✅ Réponse**

```c
#include "main.h"

/**
 * print_rev - reverse an str
 * @s: string
 * Return: the reversed char
 */

void print_rev(char *s)
{
	int len = 0;

	while (s[len] != '\0')
		len++;
	while (len > 0)
	{
		len--;
		_putchar(s[len]);
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 5. A good engineer thinks in reverse and asks himself about the stylistic consequences of the components and systems he proposes</strong></summary>

**📝 Énoncé**

Write a function that reverses a string.
**Prototype:** void rev_string(char *s);

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * rev_string - reverses a string in place
 * @s: pointer to the string to reverse
 *
 * Return: void
 */

void rev_string(char *s)
{
	int i = 0;
	int j = 0;
	char tmp;

	while (s[j] != '\0')
		j++;
	j--;
	while (i < j)
	{
		tmp = s[i];
		s[i] = s[j];
		s[j] = tmp;
		i++;
		j--;
	}
}
```

</details>

<details>
<summary><strong>🧩 6. Half the lies they tell about me aren't true</strong></summary>

**📝 Énoncé**

Write a function that prints every other character of a string, starting with the first character, followed by a new line.
**Prototype:** void puts2(char *str);

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * puts2 - updates the value it points.
 * @str: string
 * Return: 0.
 */

void puts2(char *str)
{
	int i = 0;

	while (str[i] != '\0')
	{
		if (i % 2 == 0)
			_putchar(str[i]);
		i++;
	}
	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 7. Winning is only half of it. Having fun is the other half</strong></summary>

**📝 Énoncé**

Write a function that prints half of a string, followed by a new line.
**Prototype:** void puts_half(char *str);
The function should print the second half of the string
If the number of characters is odd, the function should print the last n characters of the string, where n = (length_of_the_string + 1) / 2

**✅ Réponse**

```c
#include "main.h"

/**
 * puts_half - prints the second half of a string, then a newline
 * @str: pointer to the input string
 *
 * Description: If the length is odd, prints from index (len + 1) / 2
 *              to skip the middle character.
 * Return: void
 */

void puts_half(char *str)
{
	int len = 0;
	int start;
	int i;

	while (str[len] != '\0')
		len++;

	if (len % 2 == 0)
		start = len / 2;
	else
		start = (len + 1) / 2;

	for (i = start; i < len; i++)
		_putchar(str[i]);

	_putchar('\n');
}
```

</details>

<details>
<summary><strong>🧩 8. Arrays are not pointers</strong></summary>

**📝 Énoncé**

Write a function that prints n elements of an array of integers, followed by a new line.
**Prototype:** void print_array(int *a, int n);
where n is the number of elements of the array to be printed
Numbers must be separated by comma, followed by a space
The numbers should be displayed in the same order as they are stored in the array
You are allowed to use printf

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>
/**
 * print_array - print un array
 * @a: array
 * @n: length
 * Return: an array
**/

void print_array(int *a, int n)
{
	int i;

	for (i = 0; i < n; i++)
	{
		printf("%d", a[i]);
		if (i != n - 1)
			printf(", ");
	}
	printf("\n");
}
```

</details>

<details>
<summary><strong>🧩 9. strcpy</strong></summary>

**📝 Énoncé**

**Prototype:** char *_strcpy(char *dest, char *src);
Write a function that copies the string pointed to by src, including the terminating null byte (\0), to the buffer pointed to by dest.
Return value: the pointer to dest
**Fyi:** The standard library provides a similar function: strcpy. Run man strcpy to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strcpy - make a copy
 * @dest: destination
 * @src: source
 * Return: the copy
**/

char *_strcpy(char *dest, char *src)
{
	char *d = dest;

	while ((*d++ = *src++) != '\0')
		;

	return (dest);
}
```

</details>

<details>
<summary><strong>🧩 10. Great leaders are willing to sacrifice the numbers to save the people. Poor leaders sacrifice the people to save the numbers</strong></summary>

**📝 Énoncé**

Write a function that convert a string to an integer.
**Prototype:** int _atoi(char *s);
The number in the string can be preceded by an infinite number of characters
You need to take into account all the - and + signs before the number
If there are no numbers in the string, the function must return 0
You are not allowed to use long
You are not allowed to declare new variables of “type” array
You are not allowed to hard-code special values
We will use the -fsanitize=signed-integer-overflow gcc flag to compile your code.
**Fyi:** The standard library provides a similar function: atoi. Run man atoi to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _atoi - returns the length of a string
 *
 * @s: string to analyse
 *
 * Return: returns lenght;
 */

int _atoi(char *s)
{
	short boolean;
	int i, minus, result;

	i = minus = result = boolean = 0;
	minus = -1;

	while (s[i] != '\0')
	{
		if (s[i] == '-')
			minus *= -1;

		if (s[i] >= '0' && s[i] <= '9')
		{
			result *= 10;
			result -= (s[i] - '0');
			boolean = 1;
		}
		else if (boolean == 1)
			break;
		i++;
	}
	result *= minus;
	return (result);
}
```

</details>

- --

<a id="c-more-pointers-arrays-and-strings"></a>

## 💻 C - MORE POINTERS, ARRAYS AND STRINGS

### 📌 General

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🧩 Tâches

<details>
<summary><strong>🧩 0. strcat</strong></summary>

**📝 Énoncé**

Write a function that concatenates two strings.
**Prototype:** char *_strcat(char *dest, char *src);
This function appends the src string to the dest string, overwriting the terminating null byte (\0) at the end of dest, and then adds a terminating null byte
Returns a pointer to the resulting string dest
**Fyi:** The standard library provides a similar function: strcat. Run man strcat to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _strcat - concatenate 2 strings.
 * @dest: pointer to a string, inside it we add src
 * @src: pointer to the string we need to add
 * Return: ptr, a concactenate string.
 */

char *_strcat(char *dest, char *src)
{
	char *d = dest;

	while (*d != '\0')
		d++;
	while (*src != '\0')
		*d++ = *src++;
	*d = '\0';
	return (dest);
}
```

</details>

<details>
<summary><strong>🧩 1. strncat</strong></summary>

**📝 Énoncé**

Write a function that concatenates two strings.
**Prototype:** char *_strncat(char *dest, char *src, int n);
The _strncat function is similar to the _strcat function, except that
it will use at most n bytes from src; and
src does not need to be null-terminated if it contains n or more bytes
Return a pointer to the resulting string dest
**Fyi:** The standard library provides a similar function: strncat. Run man strncat to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _strncat - concatenate 2 strings.
 * @dest: pointer to a string, inside it we add src
 * @src: pointer to the string we need to add
 * @n: length of src
 * Return: ptr, a concactenate string.
 */

char *_strncat(char *dest, char *src, int n)
{
	int i = 0;
	int j = 0;

	while (dest[i] != '\0')
		i++;
	while (src[j] != '\0' && j < n)
	{
		dest[i] = src[j];
		i++;
		j++;
	}
	return (dest);
}
```

</details>

<details>
<summary><strong>🧩 2. strncpy</strong></summary>

**📝 Énoncé**

Write a function that copies a string.
**Prototype:** char *_strncpy(char *dest, char *src, int n);
Your function should work exactly like strncpy
**Fyi:** The standard library provides a similar function: strncpy. Run man strncpy to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strncpy - make a copy
 * @dest: destination
 * @src: source
 * @n: length max
 * Return: the copy
**/

char *_strncpy(char *dest, char *src, int n)
{
	int i = 0;

	for (; i < n && src[i] != '\0'; i++)
		dest[i] = src[i];
	for (; i < n; i++)
		dest[i] = '\0';
	return (dest);
}
```

</details>

<details>
<summary><strong>🧩 3. strcmp</strong></summary>

**📝 Énoncé**

Write a function that compares two strings.
**Prototype:** int _strcmp(char *s1, char *s2);
Your function should work exactly like strcmp
**Fyi:** The standard library provides a similar function: strcmp. Run man strcmp to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strcmp - compare 2 strings
 * @s1: pointer to the start of the string
 * @s2: pointer to the start of the string
 * Return: the diference
**/

int _strcmp(char *s1, char *s2)
{
	int i;

	for (i = 0; s1[i] != '\0' && s2[i] != '\0'; i++)
	{
		if (s1[i] != s2[i])
		{
			return (s1[i] - s2[i]);
		}
	}
	return (s1[i] - s2[i]);
}
```

</details>

<details>
<summary><strong>🧩 4. I am a kind of paranoid in reverse. I suspect people of plotting to make me happy</strong></summary>

**📝 Énoncé**

Write a function that reverses the content of an array of integers.
**Prototype:** void reverse_array(int *a, int n);
Where n is the number of elements of the array

**✅ Réponse**

```c
#include "main.h"

/**
 * reverse_array - reverse an array
 * @a: array
 * @n: element
 * Return: the rversed array.
 */

void reverse_array(int *a, int n)
{
	int i = 0;
	int j = n - 1;
	int temp;

	while (i < j)
	{
		temp = a[i];
		a[i] = a[j];
		a[j] = temp;
		i++;
		j--;
	}
}
```

</details>

<details>
<summary><strong>🧩 5. Always look up.</strong></summary>

**📝 Énoncé**

Write a function that changes all lowercase letters of a string to uppercase.
**Prototype:** char *string_toupper(char *);

**✅ Réponse**

```c
#include "main.h"

/**
 * string_toupper - changes all lowercase letters of a string to uppercase
 * @str: pointer to the input string
 *
 * Return: pointer to the modified string
**/

char *string_toupper(char *str)
{
	int mot;

	for (mot = 0; str[mot] != '\0'; mot++)
	{
		if (str[mot] >= 97 && str[mot] <= 122)
		{
			str[mot] = str[mot] - 32;
		}
	}
	return (str);
}
```

</details>

<details>
<summary><strong>🧩 6. Expect the best. Prepare for the worst. Capitalize on what comes</strong></summary>

**📝 Énoncé**

Write a function that capitalizes all words of a string.
**Prototype:** char *cap_string(char *);
Separators of words: space, tabulation, new line, ,, ;, ., !, ?, ", (, ), {, and }

**✅ Réponse**

```c
#include "main.h"

/**
 * cap_string - Change all firsts lettersof a word of a string to uppercase
 * @str: pointer to the input string
 *
 * Return: pointer to the modified string
**/

char *cap_string(char *str)
{
	int i;
	int j;
	char sep[] = " \t\n,;.!?\"(){}";

	if (str[0] >= 'a' && str[0] <= 'z')
		str[0] -= ('a' - 'A');
	for (i = 0; str[i] != '\0'; i++)
	{
		for (j = 0; sep[j] != '\0'; j++)
		{
			if (str[i] == sep[j])
			{
				if (str[i + 1] >= 'a' && str[i + 1] <= 'z')
					str[i + 1] -= ('a' - 'A');
				break;
			}
		}
	}
	return (str);
}
```

</details>

<details>
<summary><strong>🧩 7. Mozart composed his music not for the elite, but for everybody</strong></summary>

**📝 Énoncé**

Write a function that encodes a string into 1337.
Letters a and A should be replaced by 4
Letters e and E should be replaced by 3
Letters o and O should be replaced by 0
Letters t and T should be replaced by 7
Letters l and L should be replaced by 1
**Prototype:** char *leet(char *);
You can only use one if in your code
You can only use two loops in your code
You are not allowed to use switch
You are not allowed to use any ternary operation

**✅ Réponse**

```c
#include "main.h"

/**
 * leet - Encodes a string into 1337
 * @str: pointer to the input string
 *
 * Return: pointer to the modified string
**/

char *leet(char *str)
{
	int i;
	int j;
	char from[] = "aAeEoOtTlL";
	char to[]   = "4433007711";

	for (i = 0; str[i] != '\0'; i++)
	{
		for (j = 0; from[j] != '\0'; j++)
		{
			if (str[i] == from[j])
			{
				str[i] = to[j];
				break;
			}
		}
	}
	return (str);
}
```

</details>

- --

<a id="c-even-more-pointers-arrays-and-strings"></a>

## 💻 C - EVEN MORE POINTERS, ARRAYS AND STRINGS

### 📌 General

- What are pointers to pointers and how to use them
- What are multidimensional arrays and how to use them
- What are the most common C standard library functions to manipulate strings

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🔎 More Info

You do not need to learn about pointers to functions, arrays of structures, malloc and free - yet.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. memset</strong></summary>

**📝 Énoncé**

Write a function that fills memory with a constant byte.
**Prototype:** char *_memset(char *s, char b, unsigned int n);
The _memset() function fills the first n bytes of the memory area pointed to by s with the constant byte b
Returns a pointer to the memory area s
**Fyi:** The standard library provides a similar function: memset. Run man memset to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _memset - that fills memory with a constant byte.
 * @s: pointer to the memory area s
 * @b: constant byte b
 * @n: iteration
 * Return: the pointer
**/

char *_memset(char *s, char b, unsigned int n)
{
	unsigned int i;

	for (i = 0; i < n; i++)
	{
		s[i] = b;
	}
	return (s);
}
```

</details>

<details>
<summary><strong>🧩 1. memcpy</strong></summary>

**📝 Énoncé**

Write a function that copies memory area.
**Prototype:** char *_memcpy(char *dest, char *src, unsigned int n);
The _memcpy() function copies n bytes from memory area src to memory area dest
Returns a pointer to dest
**Fyi:** The standard library provides a similar function: memcpy. Run man memcpy to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _memcpy - copies memory area
 * @dest: destination
 * @src: source
 * @n: length max
 * Return: the copy
**/

char *_memcpy(char *dest, char *src, unsigned int n)
{
	unsigned int i;

	for (i = 0; i < n; i++)
	{
		dest[i] = src[i];
	}
	for (; i < n; i++)
	{
		dest[i] = '\0';
	}
	return (dest);
}
```

</details>

<details>
<summary><strong>🧩 2. strchr</strong></summary>

**📝 Énoncé**

Write a function that locates a character in a string.
**Prototype:** char *_strchr(char *s, char c);
Returns a pointer to the first occurrence of the character c in the string s, or NULL if the character is not found
**Fyi:** The standard library provides a similar function: strchr. Run man strchr to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strchr - Display the c's characteres, betwin c in a string
 * @s: pointer to the start of of a string
 * @c: charactere
 * Return: NULL
**/

char *_strchr(char *s, char c)
{
	int i;

	for (i = 0; s[i] != '\0'; i++)
	{
		if (s[i] == c)
		{
			return (&s[i]);
		}
	}
	if (c == '\0')
	{
		return (&s[i]);
	}

	return (NULL);
}
```

</details>

<details>
<summary><strong>🧩 3. strspn</strong></summary>

**📝 Énoncé**

Write a function that gets the length of a prefix substring.
**Prototype:** unsigned int _strspn(char *s, char *accept);
Returns the number of bytes in the initial segment of s which consist only of bytes from accept
**Fyi:** The standard library provides a similar function: strspn. Run man strspn to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strspn - gets the length of a prefix substring
 * @s: string to scan
 * @accept: string of allowed characters
 * Return: number of bytes from the start of s that are in accept
 */

unsigned int _strspn(char *s, char *accept)
{
	unsigned int count = 0;
	char *i;
	char *j;
	int match;

	for (i = s; *i != '\0'; i++)
	{
		match = 0;
		for (j = accept; *j != '\0'; j++)
		{
			if (*i == *j)
			{
				match = 1;
				break;
			}
		}
		if (match)
			count++;
		else
			break;
	}
	return (count);
}
```

</details>

<details>
<summary><strong>🧩 4. strpbrk</strong></summary>

**📝 Énoncé**

Write a function that searches a string for any of a set of bytes.
**Prototype:** char *_strpbrk(char *s, char *accept);
The _strpbrk() function locates the first occurrence in the string s of any of the bytes in the string accept
Returns a pointer to the byte in s that matches one of the bytes in accept, or NULL if no such byte is found
**Fyi:** The standard library provides a similar function: strpbrk. Run man strpbrk to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * _strpbrk - Finds the first character in s that matches any in accept
 * @s: The main string to search through
 * @accept: The string containing accepted characters
 *
 * Return: Pointer to the first matching character in s, or NULL if none found
 */

char *_strpbrk(char *s, char *accept)
{
	char *i;
	int j;
	int k;

	for (j = 0; s[j] != '\0'; j++)
	{
		for (k = 0; accept[k] != '\0'; k++)
		{
			if (s[j] == accept[k])
			{
				return (i = &s[j]);
			}
		}
	}
	return (NULL);
}
```

</details>

<details>
<summary><strong>🧩 5. strstr</strong></summary>

**📝 Énoncé**

Write a function that locates a substring.
**Prototype:** char *_strstr(char *haystack, char *needle);
The _strstr() function finds the first occurrence of the substring needle in the string haystack. The terminating null bytes (\0) are not compared
Returns a pointer to the beginning of the located substring, or NULL if the substring is not found.
**Fyi:** The standard library provides a similar function: strstr. Run man strstr to learn more.

**✅ Réponse**

```c
#include <stdio.h>

/**
 * _strstr - Locates a substring in a string
 * @haystack: The main string to search in
 * @needle: The substring to search for
 *
 * Return: Pointer to the first occurrence of needle in haystack,
 *         or NULL if needle is not found
 */

char *_strstr(char *haystack, char *needle)
{
	int i;
	int j;

	for (j = 0; haystack[j] != '\0'; j++)
	{
		for (i = 0; needle[i] != '\0'; i++)
		{
			if (haystack[j + i] != needle[i])
			{
				break;
			}
		}
		if (needle[i] == '\0')
		{
			return (&haystack[j]);
		}
	}
	return (NULL);
}
```

</details>

<details>
<summary><strong>🧩 6. Chess is mental torture</strong></summary>

**📝 Énoncé**

Write a function that prints the chessboard.
**Prototype:** void print_chessboard(char (*a)[8]);

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>

/**
 * print_chessboard - Prints an 8x8 chessboard
 * @a: Pointer to a 2D array of 8 characters per row (representing the board)
 *
 * Return: void
 **/

void print_chessboard(char (*a)[8])
{
	unsigned char rows;
	unsigned char columns;

	for (rows = 0; rows < 8; rows++)
	{
		for (columns = 0; columns < 8; columns++)
		{
			_putchar(a[rows][columns]);
		}
		_putchar('\n');
	}
}
```

</details>

<details>
<summary><strong>🧩 7. The line of life is a ragged diagonal between duty and desire</strong></summary>

**📝 Énoncé**

Write a function that prints the sum of the two diagonals of a square matrix of integers.
**Prototype:** void print_diagsums(int *a, int size);
Format: see example
You are allowed to use the standard library
Note that in the following example we are casting an int[ ][ ] into an int*. This is not something you should do. The goal here is to make sure you understand how an array of array is stored in memory.

**✅ Réponse**

```c
#include <stdio.h>

/**
 * print_diagsums - prints the sum of the two diagonals of a square matrix
 * @a: pointer to 2D array.
 * @size: which diagonal to add.
 */

void print_diagsums(int *a, int size)
{
	int i;
	int sum1;
	int sum2;

	sum1 = 0;
	sum2 = 0;

	for (i = 0; i < (size * size); i += size + 1)
		sum1 += a[i];
	for (i = size - 1; i < (size * size - 1); i += size - 1)
		sum2 += a[i];

	printf("%d, %d\n", sum1, sum2);
}
```

</details>

- --

<a id="c-recursion"></a>

## 💻 C - RECURSION

### 📌 General

- What is recursion
- How to implement recursion
- In what situations you should implement recursion
- In what situations you shouldn’t implement recursion

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- You are not allowed to use the standard library. Any use of functions like printf, puts, etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file
- You are not allowed to use any kind of loops
- You are not allowed to use static variables

### 🧩 Tâches

<details>
<summary><strong>🧩 0. She locked away a secret, deep inside herself, something she once knew to be true... but chose to forget</strong></summary>

**📝 Énoncé**

Write a function that prints a string, followed by a new line.
**Prototype:** void _puts_recursion(char *s);
**Fyi:** The standard library provides a similar function: puts. Run man puts to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _puts_recursion - Prints a string followed by a new line
 * @s: Pointer to the string to print
 *
 * Description: This function prints each character of the string
 * recursively, followed by a newline character at the end.
 *
 * Return: Nothing (void)
 */

void _puts_recursion(char *s)
{
	if (*s == '\0')
	{
		_putchar('\n');
		return;
	}
	_putchar(*s);
	_puts_recursion(s + 1);
}
```

</details>

<details>
<summary><strong>🧩 1. Why is it so important to dream? Because, in my dreams we are together</strong></summary>

**📝 Énoncé**

Write a function that prints a string in reverse.
**Prototype:** void _print_rev_recursion(char *s);

**✅ Réponse**

```c
#include "main.h"

/**
 * _print_rev_recursion - Prints a reversed string followed by a new line
 * @s: Pointer to the string to print
 *
 * Description: This function prints each character of the string in reverse
 * recursively, followed by a newline character at the end.
 *
 * Return: Nothing (void)
 */

void _print_rev_recursion(char *s)
{
	if (*s == '\0')
	{
		return;
	}
	_print_rev_recursion(s + 1);
	_putchar(*s);
}
```

</details>

<details>
<summary><strong>🧩 2. Dreams feel real while we're in them. It's only when we wake up that we realize something was actually strange</strong></summary>

**📝 Énoncé**

Write a function that returns the length of a string.
**Prototype:** int _strlen_recursion(char *s);
**Fyi:** The standard library provides a similar function: strlen. Run man strlen to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _strlen_recursion - returns the length of a string using recursion
 * @s: string to measure
 *
 * Return: length of the string
 */
int _strlen_recursion(char *s)
{
	if (*s == '\0')
		return (0);
	return (1 + _strlen_recursion(s + 1));
}
```

</details>

<details>
<summary><strong>🧩 3. You mustn't be afraid to dream a little bigger, darling</strong></summary>

**📝 Énoncé**

Write a function that returns the factorial of a given number.
**Prototype:** int factorial(int n);
If n is lower than 0, the function should return -1 to indicate an error
Factorial of 0 is 1

**✅ Réponse**

```c
#include "main.h"

/**
 * factorial - Returns the factorial of a given number
 * @n: The number to compute the factorial of
 *
 * Return: The factorial of n
 *         -1 if n is lower than 0 (error case)
 */
int factorial(int n)
{
	if (n < 0)
	{
		return (-1);
	}
	if (n == 0)
	{
		return (1);
	}
	return (n * factorial(n - 1));
}
```

</details>

<details>
<summary><strong>🧩 4. Once an idea has taken hold of the brain it's almost impossible to eradicate</strong></summary>

**📝 Énoncé**

Write a function that returns the value of x raised to the power of y.
**Prototype:** int _pow_recursion(int x, int y);
If y is lower than 0, the function should return -1
**Fyi:** The standard library provides a different function: pow. Run man pow to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * _pow_recursion - Returns the value of x raised to the power of y
 * @x: The base value
 * @y: The exponent value
 *
 * Description: Uses recursion to calculate x raised to the power y.
 *              If y is lower than 0, the function returns -1.
 *
 * Return: The result of x raised to the power of y, or -1 if y < 0
 */
int _pow_recursion(int x, int y)
{
	if (y < 0)
	{
		return (-1);
	}
	if (y == 0)
	{
		return (1);
	}
	return (x * _pow_recursion(x, y - 1));
}
```

</details>

<details>
<summary><strong>🧩 5. Your subconscious is looking for the dreamer</strong></summary>

**📝 Énoncé**

Write a function that returns the natural square root of a number.
**Prototype:** int _sqrt_recursion(int n);
If n does not have a natural square root, the function should return -1
**Fyi:** The standard library provides a different function: sqrt. Run man sqrt to learn more.

**✅ Réponse**

```c
#include "main.h"

/**
 * search_y - test for the value of y
 * @n: number to find the root of
 * @y: number to find
 *
 * Return: the value of y.
**/
int search_y(int n, int y)
{
	if (y * y == n)
	{
		return (y);
	}
	if (y * y > n)
	{
		return (-1);
	}
	return (search_y(n, y + 1));
}

/**
 * _sqrt_recursion - returns natural square root of n
 * @n: number to find the root of
 *
 * Return: square root or -1 if none
**/
int _sqrt_recursion(int n)
{
	return (search_y(n, 0));
}
```

</details>

<details>
<summary><strong>🧩 6. Inception. Is it possible?</strong></summary>

**📝 Énoncé**

Write a function that returns 1 if the input integer is a prime number, otherwise return 0.
**Prototype:** int is_prime_number(int n);

**✅ Réponse**

```c
#include "main.h"

/**
 * check_prime - Checks for a divisor of n starting from i
 * @n: The number to check
 * @i: The current divisor being tested
 *
 * Return: 1 if prime, 0 if not
 */
int check_prime(int n, int i)
{
	if (n <= 1)
	{
		return (0);
	}
	if (i * i > n)
	{
		return (1);
	}
	if (n % i == 0)
	{
		return (0);
	}
	return (check_prime(n, i + 1));
}

/**
 * is_prime_number - Returns 1 if n is a prime number, 0 otherwise
 * @n: The number to check
 *
 * Return: 1 if n is prime, 0 otherwise
 */
int is_prime_number(int n)
{
	return (check_prime(n, 2));
}
```

</details>

- --

<a id="c-argc-argv"></a>

## 💻 C - ARGC, ARGV

### 📌 General

- How to use arguments passed to your program
- What are two prototypes of main that you know of, and in which case do you use one or the other
- How to use __attribute__((unused)) or (void) to compile functions with unused variables or parameters

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file
- You are allowed to use the standard library

### 🧩 Tâches

<details>
<summary><strong>🧩 0. It ain't what they call you, it's what you answer to</strong></summary>

**📝 Énoncé**

Write a program that prints its name, followed by a new line.
If you rename the program, it will print the new name, without having to compile it again
You should not remove the path before the name of the program

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Prints the program name
 * @argc: argument count (unused)
 * @argv: argument vector (array of strings)
 *
 * Return: Always 0
 */

int main(int argc, char *argv[])
{
	(void)argc;
	printf("%s\n", argv[0]);
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 1. Silence is argument carried out by other means</strong></summary>

**📝 Énoncé**

Write a program that prints the number of arguments passed into it.
Your program should print a number, followed by a new line

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - Prints the number of arguments passed into it.
 * @argc: argument count
 * @argv: argument vector (unused)
 *
 * Return: Always 0
 */

int main(int argc, char *argv[])
{
	(void)argv;
	printf("%d\n", argc - 1);
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 2. The best argument against democracy is a five-minute conversation with the average voter</strong></summary>

**📝 Énoncé**

Write a program that prints all arguments it receives.
All arguments should be printed, including the first one
Only print one argument per line, ending with a new line

**✅ Réponse**

```c
#include <stdio.h>

/**
 * main - print all the arguments
 *
 * @argc: number of argument
 * @argv: array of argument
 *
 * Return: always 0
 */

int main(int argc, char *argv[])
{
	int i;

	for (i = 0; i < argc; i++)
	{
		printf("%s\n", argv[i]);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 3. Neither irony nor sarcasm is argument</strong></summary>

**📝 Énoncé**

Write a program that multiplies two numbers.
Your program should print the result of the multiplication, followed by a new line
You can assume that the two numbers and result of the multiplication can be stored in an integer
If the program does not receive two arguments, your program should print Error, followed by a new line, and return 1

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>

/**
 * main - get the name of the program
 *
 * @argc: number of argument
 * @argv: array of argument
 *
 * Return: always 0
 */

int main(int argc, char *argv[])
{
	int num1;
	int num2;
	int multi;

	if (argc != 3)
	{
		printf("Error\n");
	}

	else
	{
	num1 = atoi(argv[1]);
	num2 = atoi(argv[2]);
	multi = num1 * num2;

	printf("%d\n", multi);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 4. To infinity and beyond</strong></summary>

**📝 Énoncé**

Write a program that adds positive numbers.
Print the result, followed by a new line
If no number is passed to the program, print 0, followed by a new line
If one of the number contains symbols that are not digits, print Error, followed by a new line, and return 1
You can assume that numbers and the addition of all the numbers can be stored in an int

**✅ Réponse**

```c
#include <stdio.h>
#include <ctype.h>
#include <stdlib.h>

/**
 * main - get the name of the program
 *
 * @argc: number of argument
 * @argv: array of argument
 *
 * Return: always 0
 */

int main(int argc, char *argv[])
{
	int i, j;
	int somme = 0;

	if (argc == 1)
	{
		;
	}
	for (i = 1; i < argc; i++)
	{
		for (j = 0; argv[i][j] != '\0'; j++)
		{
			if (!(isdigit(argv[i][j])))
			{
			printf("Error\n");
			return (1);
			}
		}

	somme += atoi(argv[i]);
	}
	printf("%d\n", somme);
	return (0);
}
```

</details>

- --

<a id="c-malloc-free"></a>

## 💻 C - MALLOC, FREE

### 📌 General

- What is the difference between automatic and dynamic allocation
- What is malloc and free and how to use them
- Why and when use malloc
- How to use valgrind to check for memory leak

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc and free. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🔎 More Info

- You do not have to learn about calloc and realloc.

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Float like a butterfly, sting like a bee</strong></summary>

**📝 Énoncé**

Write a function that creates an array of chars, and initializes it with a specific char.
**Prototype:** char *create_array(unsigned int size, char c);
Returns NULL if size = 0
Returns a pointer to the array, or NULL if it fails

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include "main.h"

/**
 * create_array - Creates an array of chars and initializes
 *	it with a specific char
 * @size: The size of the array
 * @c: The character to initialize the array with
 *
 * Return: A pointer to the array,
 *	or NULL if size is 0 or if memory allocation fails
 */

char *create_array(unsigned int size, char c)
{
	unsigned int i;
	char *p = malloc(sizeof(c) * size);

	if (p == 0)
	{
		return (NULL);
	}
	if (size == 0)
	{
		return (NULL);
	}
	for (i = 0; i < size; i++)
	{
		p[i] = c;
	}
	return (p);
}
```

</details>

<details>
<summary><strong>🧩 1. The woman who has no imagination has no wings</strong></summary>

**📝 Énoncé**

Write a function that returns a pointer to a newly allocated space in memory, which contains a copy of the string given as a parameter.
**Prototype:** char *_strdup(char *str);
The _strdup() function returns a pointer to a new string which is a duplicate of the string str. Memory for the new string is obtained with malloc, and can be freed with free.
Returns NULL if str = NULL
On success, the _strdup function returns a pointer to the duplicated string. It returns NULL if insufficient memory was available
**Fyi:** The standard library provides a similar function: strdup. Run man strdup to learn more.

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>
#include <stdlib.h>

/**
 * _strlen - check the len of an str.
 * @s: char *
 * Return: the len.
 */

int _strlen(char *s)
{
	int len = 0;

	while (s[len] != '\0')
	{
		len++;
	}
	return (len);
}

/**
 * _strdup - Duplicates a string to a newly allocated memory space
 * @str: The string to duplicate
 *
 * Return: A pointer to the duplicated string, or NULL if str is NULL
 *         or if memory allocation fails
 */

char *_strdup(char *str)
{
	int i;
	int len;
	char *copy;

	if (str == NULL)
	{
		return (NULL);
	}

	len = _strlen(str);
	copy = malloc(len + 1);

	if (copy == NULL)
	{
		return (NULL);
	}
	for (i = 0; i < len; i++)
	{
		copy[i] = str[i];
	}
	return (copy);
}
```

</details>

<details>
<summary><strong>🧩 2. He who is not courageous enough to take risks will accomplish nothing in life</strong></summary>

**📝 Énoncé**

Write a function that concatenates two strings.
**Prototype:** char *str_concat(char *s1, char *s2);
The returned pointer should point to a newly allocated space in memory which contains the contents of s1, followed by the contents of s2, and null terminated
if NULL is passed, treat it as an empty string
The function should return NULL on failure

**✅ Réponse**

```c
#include "main.h"
#include <stdlib.h>

/**
 * _strlen - check the len of an str.
 * @s: char *
 * Return: the len.
 */

int _strlen(char *s)
{
	int len = 0;

	while (s[len] != '\0')
	{
		len++;
	}
	return (len);
}

/**
 * str_concat - Concatenates two strings into a newly allocated string
 * @s1: The first string
 * @s2: The second string
 *
 * Return: A pointer to the newly allocated concatenated string,
 *         or NULL if memory allocation fails
 *
 * Description: This function allocates enough memory to hold
 * both strings s1 and s2, copies s1 followed by s2 into the new
 * buffer, and returns a pointer to the result. The resulting string
 * is null-terminated. If either input string is NULL, it is treated
 * as an empty string.
 */

char *str_concat(char *s1, char *s2)
{
	int i;
	int j;
	char *p;
	int lens1;
	int lens2;

	if (s1 == NULL)
	{
		s1 = "";
	}
	if (s2 == NULL)
	{
		s2 = "";
	}

	lens1 = _strlen(s1);
	lens2 = _strlen(s2);
	p = malloc(lens1 + lens2 + 1);

	if (p == NULL)
	{
		return (NULL);
	}
	for (i = 0; i < lens1; i++)
	{
		p[i] = s1[i];
	}
	for (j = 0; j < lens2; j++)
	{
		p[i + j] = s2[j];
	}
	p[i + j] = '\0';

	return (p);
}
```

</details>

<details>
<summary><strong>🧩 3. If you even dream of beating me you'd better wake up and apologize</strong></summary>

**📝 Énoncé**

Write a function that returns a pointer to a 2 dimensional array of integers.
**Prototype:** int **alloc_grid(int width, int height);
Each element of the grid should be initialized to 0
The function should return NULL on failure
If width or height is 0 or negative, return NULL

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * alloc_grid - Allocates a 2D array of integers
 * @width: number of columns
 * @height: number of rows
 *
 * Return: Pointer to 2D array or NULL on failure
 */

int **alloc_grid(int width, int height)
{
	int h;
	int w;
	int **p_height;
	int *p_width;

	w = 0;

	if (width <= 0 || height <= 0)
	{
		return (NULL);
	}

	p_height = malloc(height * sizeof(int *));

	if (p_height == NULL)
	{
		return (NULL);
	}
	for (h = 0; h < height; h++)
	{
		p_width = malloc(width * sizeof(int));
		if (p_width == NULL)
		{
			while (w < h)
			{
				free(p_height[w]);
				w++;
			}
			free(p_height);
			return (NULL);
		}
		p_height[h] = p_width;
	}
	return (p_height);
}
```

</details>

<details>
<summary><strong>🧩 4. It's not bragging if you can back it up</strong></summary>

**📝 Énoncé**

Write a function that frees a 2 dimensional grid previously created by your alloc_grid function.
**Prototype:** void free_grid(int **grid, int height);
Note that we will compile with your alloc_grid.c file. Make sure it compiles.

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * free_grid - Frees a 2D array (grid) previously created by malloc
 * @grid: Pointer to the 2D array
 * @height: Number of rows in the grid
 *
 * Description: Frees each row of the grid, then frees the grid itself.
 * If grid is NULL, the function does nothing.
 */

void free_grid(int **grid, int height)
{
	int h;

	if (grid == NULL)
	{
		return;
	}
	for (h = 0; h < height; h++)
	{
		free(grid[h]);
	}
	free(grid);
}
```

</details>

- --

<a id="c-more-malloc-free"></a>

## 💻 C - MORE MALLOC, FREE

### 📌 General

- How to use the exit function
- What are the functions calloc and realloc from the standard library and how to use them

### ✅ Requirements

- Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc, free and exit. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Trust no one</strong></summary>

**📝 Énoncé**

Write a function that allocates memory using malloc.
**Prototype:** void *malloc_checked(unsigned int b);
Returns a pointer to the allocated memory
If malloc fails, the malloc_checked function should cause normal process termination with a status value of 98

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * malloc_checked - Allocates memory using malloc.
 * @b: Number of bytes to allocate.
 *
 * Return: Pointer to allocated memory, or exit with 98 on failure.
 */

void *malloc_checked(unsigned int b)
{
	void *p;

	p = malloc(b);

	if (p == NULL)
	{
		exit(98);
	}
	return (p);
}
```

</details>

<details>
<summary><strong>🧩 1. string_nconcat</strong></summary>

**📝 Énoncé**

Write a function that concatenates two strings.
**Prototype:** char *string_nconcat(char *s1, char *s2, unsigned int n);
The returned pointer shall point to a newly allocated space in memory, which contains s1, followed by the first n bytes of s2, and null terminated
If the function fails, it should return NULL
If n is greater or equal to the length of s2 then use the entire string s2
If NULL is passed, treat it as an empty string

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * _strlen - check the len of an str.
 * @s: char *
 * Return: the len.
 */

int _strlen(char *s)
{
	int len = 0;

	while (s[len] != '\0')
	{
		len++;
	}
	return (len);
}

/**
 * string_nconcat - concatenates two strings
 * @s1: first string
 * @s2: second string
 * @n: number of bytes of s2 to concatenate
 *
 * Return: pointer to new string or NULL on failure
 */

char *string_nconcat(char *s1, char *s2, unsigned int n)
{
	unsigned int i;
	unsigned int j;
	unsigned int len_s1;
	unsigned int len_s2;
	char *p;

	if (s1 == NULL)
	{
		s1 = "";
	}
	if (s2 == NULL)
	{
		s2 = "";
	}
	len_s1 = _strlen(s1);
	len_s2 = _strlen(s2);

	while (n > len_s2)
	{
		n = len_s2;
	}
	p = malloc(len_s1 + n + 1);
	if (p == NULL)
	{
		return (NULL);
	}
	for (i = 0; i < len_s1; i++)
	{ p[i] = s1[i];
	}
	for (j = 0; j < n; j++)
	{
		p[i + j] = s2[j];
	}
	p[i + j] = '\0';
	return (p);
}
```

</details>

<details>
<summary><strong>🧩 2. _calloc</strong></summary>

**📝 Énoncé**

Write a function that allocates memory for an array, using malloc.
**Prototype:** void *_calloc(unsigned int nmemb, unsigned int size);
The _calloc function allocates memory for an array of nmemb elements of size bytes each and returns a pointer to the allocated memory.
The memory is set to zero
If nmemb or size is 0, then _calloc returns NULL
If malloc fails, then _calloc returns NULL
**Fyi:** The standard library provides a different function: calloc. Run man calloc to learn more.

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * _calloc - Allocates memory for an array and sets it to zero
 * @nmemb: Number of elements in the array
 * @size: Size of each element in bytes
 *
 * Return: Pointer to the allocated memory, or NULL if failure or input is 0
 *
 * Description: This function allocates memory for an array of `nmemb`
 * elements, each of `size` bytes. All memory is initialized to 0.
 * If `nmemb` or `size` is 0, or if malloc fails, the function returns NULL.
 */

void *_calloc(unsigned int nmemb, unsigned int size)
{
	unsigned int i;
	char *p;

	if (nmemb == 0 || size == 0)
	{
		return (NULL);
	}

	p = malloc(nmemb * size);
	if (p == NULL)
	{
		return (NULL);
	}

	for (i = 0; i < nmemb * size; i++)
	{
		p[i] = 0;
	}

	return ((void *)p);
}
```

</details>

<details>
<summary><strong>🧩 3. array_range</strong></summary>

**📝 Énoncé**

Write a function that creates an array of integers.
**Prototype:** int *array_range(int min, int max);
The array created should contain all the values from min (included) to max (included), ordered from min to max
Return: the pointer to the newly created array
If min > max, return NULL
If malloc fails, return NULL

**✅ Réponse**

```c
#include <stdlib.h>

/**
 * array_range - Creates an array of integers from min to max.
 * @min: Minimum integer (inclusive).
 * @max: Maximum integer (inclusive).
 *
 * Return: Pointer to the newly allocated array, or NULL on failure.
 */
int *array_range(int min, int max)
{
	int i, len;
	int *p;

	len = max - min + 1;

	if (min > max)
	{
		return (NULL);
	}

	p = malloc(len * sizeof(int));

	if (p == NULL)
	{
		return (NULL);
	}

	for (i = 0; i < len; i++)
	{
		p[i] = min + i;
	}
	return (p);
}
```

</details>

- --

<a id="c-structures-typedef"></a>

## 💻 C - STRUCTURES, TYPEDEF

### 📌 General

- What are structures, when, why and how to use them
- How to use typedef

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are printf, malloc, free and exit.
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- Don’t forget to push your header file
- All your header files should be include guarded

#ifndef DOG_H
#define DOG_H
/**
 * struct dog - Represents information about an entity.
 * @name: Name of the entity.
 * @age: Age of the entity.
 * @owner: Name of the owner.
 */
struct dog
{
	char *name;
	float age;
	char *owner;
};
typedef struct dog dog_t;

void init_dog(struct dog *d, char *name, float age, char *owner);
void print_dog(struct dog *d);
dog_t *new_dog(char *name, float age, char *owner);
void free_dog(dog_t *d);

#endif

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Poppy</strong></summary>

**📝 Énoncé**

Define a new type struct dog with the following elements:
name, type = char *
age, type = float
owner, type = char *

**✅ Réponse**

```c
#include <stdio.h>
#include <string.h>
#include "dog.h"

/**
 * init_dog - Initializes a variable of type struct dog.
 * @d: Pointer to the dog struct to initialize.
 * @name: Name of the dog.
 * @age: Age of the dog.
 * @owner: Name of the owner.
 */
void init_dog(struct dog *d, char *name, float age, char *owner)
{
	if (d == NULL)
	return;

	d->name = name;
	d->age = age;
	d->owner = owner;
}
```

</details>

<details>
<summary><strong>🧩 1. A dog is the only thing on earth that loves you more than you love yourself</strong></summary>

**📝 Énoncé**

Write a function that initialize a variable of type struct dog
**Prototype:** void init_dog(struct dog *d, char *name, float age, char *owner);

**✅ Réponse**

```c
#include <stdio.h>
#include <string.h>
#include "dog.h"

/**
 * init_dog - Initializes a variable of type struct dog.
 * @d: Pointer to the dog struct to initialize.
 * @name: Name of the dog.
 * @age: Age of the dog.
 * @owner: Name of the owner.
 */
void init_dog(struct dog *d, char *name, float age, char *owner)
{
	if (d == NULL)
	return;

	d->name = name;
	d->age = age;
	d->owner = owner;
}
```

</details>

<details>
<summary><strong>🧩 2. A dog will teach you unconditional love. If you can have that in your life, things won't be too bad</strong></summary>

**📝 Énoncé**

Write a function that prints a struct dog
**Prototype:** void print_dog(struct dog *d);
Format: see example bellow
You are allowed to use the standard library
If an element of d is NULL, print (nil) instead of this element. (if name is NULL, print Name: (nil))
If d is NULL print nothing.

**✅ Réponse**

```c
#include <stdio.h>
#include "dog.h"

/**
 * print_dog - Prints the contents of a struct dog.
 * @d: Pointer to the dog struct to print.
 *
 * Description: If d or any of its elements are NULL, prints (nil)
 *              for those elements. Prints nothing if d is NULL.
 */
void print_dog(struct dog *d)
{
	if (d != NULL)
	{
		if (d->name != NULL)
			printf("Name: %s\n", d->name);
		else
			printf("Name: (nil)\n");

		printf("Age: %.6f\n", d->age);

		if (d->owner != NULL)
			printf("Owner: %s\n", d->owner);
		else
			printf("Owner: (nil)\n");
	}
}
```

</details>

<details>
<summary><strong>🧩 3. Outside of a dog, a book is a man's best friend. Inside of a dog it's too dark to read</strong></summary>

**📝 Énoncé**

Define a new type dog_t as a new name for the type struct dog.

**✅ Réponse**

```c
#ifndef DOG_H
#define DOG_H

/**
 * struct dog - Represents information about an entity.
 * @name: Name of the entity.
 * @age: Age of the entity.
 * @owner: Name of the owner.
 */
struct dog
{
	char *name;
	float age;
	char *owner;
};

typedef struct dog dog_t;

void init_dog(struct dog *d, char *name, float age, char *owner);
void print_dog(struct dog *d);
dog_t *new_dog(char *name, float age, char *owner);
void free_dog(dog_t *d);

#endif
```

</details>

<details>
<summary><strong>🧩 4. A door is what a dog is perpetually on the wrong side of</strong></summary>

**📝 Énoncé**

Write a function that creates a new dog.
**Prototype:** dog_t *new_dog(char *name, float age, char *owner);
You have to store a copy of name and owner
Return NULL if the function fails

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "dog.h"
char *_strcpy(char *dest, char *src);
static unsigned int _strlen(char *s);

/**
 * new_dog - Creates a new dog and stores copies of its name and owner.
 * @name: Name of the dog.
 * @age: Age of the dog.
 * @owner: Name of the owner.
 *
 * Return: Pointer to the new dog, or NULL on failure.
 */
dog_t *new_dog(char *name, float age, char *owner)
{
	dog_t *new;
	unsigned int len_name, len_owner;

	new = malloc(sizeof(dog_t));
	if (new == NULL)
		return (NULL);

	new->name = NULL;
	new->owner = NULL;
	new->age = age;

	if (name != NULL)
	{
		len_name = _strlen(name);
		new->name = malloc(len_name + 1);
		if (new->name == NULL)
		{
			free(new);
			return (NULL);
		}
		_strcpy(new->name, name);
	}

	if (owner != NULL)
	{
		len_owner = _strlen(owner);
		new->owner = malloc(len_owner + 1);
		if (new->owner == NULL)
		{
			free(new->name);
			free(new);
			return (NULL);
		}
		_strcpy(new->owner, owner);
	}

	if (new->name == NULL || new->owner == NULL)
	{
		free(new->name);
		free(new->owner);
		free(new);
		return (NULL);
	}

	return (new);
}

/**
 * _strcpy - Copies the string pointed to by src into dest.
 * @dest: Destination buffer.
 * @src: Source string.
 *
 * Return: Pointer to dest, or NULL if dest or src is NULL.
 */
char *_strcpy(char *dest, char *src)
{
	unsigned int i = 0;

	if (dest == NULL || src == NULL)
		return (NULL);
	while (src[i] != '\0')
	{
		dest[i] = src[i];
		i++;
	}
	dest[i] = '\0';
	return (dest);
}

/**
 * _strlen - Returns the length of a string.
 * @s: String to measure.
 *
 * Return: Length of the string, or 0 if s is NULL.
 */
static unsigned int _strlen(char *s)
{
	unsigned int len = 0;

	if (s == NULL)
		return (0);
	while (s[len] != '\0')
		len++;
	return (len);
}
```

</details>

<details>
<summary><strong>🧩 5. How many legs does a dog have if you call his tail a leg? Four. Saying that a tail is a leg doesn't make it a leg</strong></summary>

**📝 Énoncé**

Write a function that frees dogs.
**Prototype:** void free_dog(dog_t *d);

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include "dog.h"

/**
 * free_dog - Frees memory allocated for a dog struct.
 * @d: Pointer to the dog struct to free.
 */
void free_dog(dog_t *d)
{
	if (d == NULL)
		return;

	free(d->name);
	free(d->owner);
	free(d);
}

```
General
- What are function pointers and how to use them
- What does a function pointer exactly hold
- Where does a function pointer point to in the virtual memory

Requirements
- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc, free and exit. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called function_pointers.h
- Don’t forget to push your header file
- All your header files should be include guarded
```

```
</details>

<details>
<summary><strong>🧩 0. What's my name</strong></summary>

**📝 Énoncé**

Write a function that prints a name.
**Prototype:** void print_name(char *name, void (*f)(char *));

**✅ Réponse**

```c
#include "function_pointers.h"
#include <stddef.h>

/**
 * print_name - Calls a function to print a name
 * @name: The name to be printed
 * @f: Pointer to a function that takes a string and returns nothing
 * Return: void
**/

void print_name(char *name, void (*f)(char *))
{
	if (name != NULL)
	{
		f (name);
	}
}
```

</details>

<details>
<summary><strong>🧩 1. If you spend too much time thinking about a thing, you'll never get it done</strong></summary>

**📝 Énoncé**

Write a function that executes a function given as a parameter on each element of an array.
**Prototype:** void array_iterator(int *array, size_t size, void (*action)(int));
where size is the size of the array
and action is a pointer to the function you need to use

**✅ Réponse**

```c
#include "function_pointers.h"
#include <stddef.h>

/**
 * array_iterator - executes a function (parameter) on each element of an array
 * @size: the size of the array
 * @array: the array to execute the action
 * @action: pointer t the functio that we need to use
 * Return: void.
**/

void array_iterator(int *array, size_t size, void (*action)(int))
{
	unsigned int i;
	for (i = 0; i != size; i++)
	{
		if (array != NULL)
		{
			action(array[i]);
		}
	}
}
```

</details>

<details>
<summary><strong>🧩 2. To hell with circumstances; I create opportunities</strong></summary>

**📝 Énoncé**

Write a function that searches for an integer.
**Prototype:** int int_index(int *array, int size, int (*cmp)(int));
where size is the number of elements in the array array
cmp is a pointer to the function to be used to compare values
int_index returns the index of the first element for which the cmp function does not return 0
If no element matches, return -1
If size <= 0, return -1

**✅ Réponse**

```c
#include "function_pointers.h"

/**
 * int_index - searches for an integer.
 * @array: pointer to the index of the array
 * @size: numbers of element in the array
 * @cmp: pointer to the comparaisons functions
 * Return: the integer find
**/
int int_index(int *array, int size, int (*cmp)(int))
{
	int i;

	if (cmp == NULL || array == NULL || size == 0)
	{
		return (-1);
	}

	for (i = 0; i < size; i++)
	{
		if (cmp(array[i]))
		{
			return (i);
		}
	}
	return (-1);
}
```

</details>

<details>
<summary><strong>🧩 3. A goal is not always meant to be reached, it often serves simply as something to aim at</strong></summary>

**📝 Énoncé**

Write a program that performs simple operations.
You are allowed to use the standard library
Usage: calc num1 operator num2
You can assume num1 and num2 are integers, so use the atoi function to convert them from the string input to int
operator is one of the following:
+: addition
- : subtraction
*: multiplication
/: division
%: modulo
The program prints the result of the operation, followed by a new line
You can assume that the result of all operations can be stored in an int
if the number of arguments is wrong, print Error, followed by a new line, and exit with the status 98
if the operator is none of the above, print Error, followed by a new line, and exit with the status 99
if the user tries to divide (/ or %) by 0, print Error, followed by a new line, and exit with the status 100
This task requires that you create four different files.

3-calc.h

This file should contain all the function prototypes and data structures used by the program. You can use this structure:

/**
 * struct op - Struct op
 *
 * @op: The operator
 * @f: The function associated
 */
typedef struct op
{
    char *op;
    int (*f)(int a, int b);
} op_t;

3-op_functions.c

This file should contain the 5 following functions (not more):

op_add: returns the sum of a and b. Prototype: int op_add(int a, int b);
op_sub: returns the difference of a and b. Prototype: int op_sub(int a, int b);
op_mul: returns the product of a and b. Prototype: int op_mul(int a, int b);
op_div: returns the result of the division of a by b. Prototype: int op_div(int a, int b);
op_mod: returns the remainder of the division of a by b. Prototype: int op_mod(int a, int b);

3-get_op_func.c

This file should contain the function that selects the correct function to perform the operation asked by the user. You’re not allowed to declare any other function.

**Prototype:** int (*get_op_func(char *s))(int, int);
where s is the operator passed as argument to the program
This function returns a pointer to the function that corresponds to the operator given as a parameter. Example: get_op_func("+") should return a pointer to the function op_add
You are not allowed to use switch statements
You are not allowed to use for or do ... while loops
You are not allowed to use goto
You are not allowed to use else
You are not allowed to use more than one if statement in your code
You are not allowed to use more than one while loop in your code
If s does not match any of the 5 expected operators (+, -, *, /, %), return NULL
You are only allowed to declare these two variables in this function:

    op_t ops[ ] = {
        {"+", op_add},
        {"-", op_sub},
        {"*", op_mul},
        {"/", op_div},
        {"%", op_mod},
        {NULL, NULL}
    };
    int i;

3-main.c

This file should contain your main function only.

You are not allowed to code any other function than main in this file
You are not allowed to directly call op_add, op_sub, op_mul, op_div or op_mod from the main function
You have to use atoi to convert arguments to int
You are not allowed to use any kind of loop
You are allowed to use a maximum of 3 if statements

Compilation and examples

julien@ubuntu:~/0x0e. Function pointers$ gcc -Wall -pedantic -Werror -Wextra -std=gnu89 3-main.c 3-op_functions.c 3-get_op_func.c -o calc
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1 + 1
2
julien@ubuntu:~/0x0e. Function pointers$ ./calc 97 + 1
98
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1024 / 10
102
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1024 '*' 98
100352
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1024 '\*' 98
Error
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1024 - 98
926
julien@ubuntu:~/0x0e. Function pointers$ ./calc 1024 '%' 98
44
julien@ubuntu:~/0x0e. Function pointers$

**✅ Réponse**

```c
#ifndef CALC_H
#define CALC_H

/**
 * struct op - Struct op
 *
 * @op: The operator
 * @f: The function associated
 */
typedef struct op
{
	char *op;
	int (*f)(int a, int b);
} op_t;

int op_add(int a, int b);
int op_sub(int a, int b);
int op_mul(int a, int b);
int op_div(int a, int b);
int op_mod(int a, int b);

int (*get_op_func(char *s))(int, int);

#endif

#include "3-calc.h"
#include <stddef.h>

/**
 * get_op_func - pointer to the operatiosn functions
 * @s: pointer to a string
 * Return: the operation
**/
int (*get_op_func(char *s))(int, int)
{
	op_t ops[] = {
		{"+", op_add},
		{"-", op_sub},
		{"*", op_mul},
		{"/", op_div},
		{"%", op_mod},
		{NULL, NULL}
		};

	int i;

	while (ops[i].op && s[0] != ops[i].op[0])
	{
		i++;
	}

	if (ops[i].op && s[0] == ops[i].op[0] && s[1] == '\0')
	{
		return (ops[i].f);
	}

	return (NULL);
}

#include "3-calc.h"
#include <stddef.h>
#include <stdlib.h>
#include <stdio.h>
#include <string.h>

/**
 * main - Entry point
 * @argc: argument count
 * @argv: vector argument
 * Return: always 0.
**/
int main(int argc, char *argv[])
{
	int a, b, result;
	int (*operation)(int, int);

	if (argc > 4 || argc < 4)
	{
		printf("Error\n");
		exit(98);
	}

	a = atoi(argv[1]);
	b = atoi(argv[3]);

	operation = get_op_func(argv[2]);

	if (operation == NULL)
	{
		printf("Error\n");
		exit(99);
	}

	if ((strcmp(argv[2], "%") == 0 || strcmp(argv[2], "/") == 0) && b == 0)
	{
		printf("Error\n");
		exit(100);
	}

	result = operation(a, b);
	printf("%d\n", result);

	return (0);
}

#include "3-calc.h"

/**
 * op_add - sum of a and b
 * @a: number 1
 * @b: number 2
 * Return: the sum
**/
int op_add(int a, int b)
{
	return (a + b);
}

/**
 * op_sub - subraction of a and b
 * @a: number 1
 * @b: number 2
 * Return: the difference
**/
int op_sub(int a, int b)
{
	return (a - b);
}

/**
 * op_mul - multiplication of a and b
 * @a: number 1
 * @b: number 2
 * Return: the product
**/
int op_mul(int a, int b)
{
	return (a * b);
}

/**
 * op_div - division of a and b
 * @a: number 1
 * @b: number 2
 * Return: the quotient
**/
int op_div(int a, int b)
{
	return (a / b);
}

/**
 * op_mod - modulo of a and b
 * @a: number 1
 * @b: number 2
 * Return: the rest
**/
int op_mod(int a, int b)
{
	return (a % b);
}
```

</details>

- --

<a id="c-variadic-functions"></a>

## 💻 C - VARIADIC FUNCTIONS

### 📌 General

- What are variadic functions
- How to use va_start, va_arg and va_end macros
- Why and how to use the const type qualifier

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc, free and exit. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
- You are allowed to use the following macros: va_start, va_arg and va_end
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called variadic_functions.h
- Don’t forget to push your header file
- All your header files should be include guarded

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Beauty is variable, ugliness is constant</strong></summary>

**📝 Énoncé**

Write a function that returns the sum of all its parameters.
**Prototype:** int sum_them_all(const unsigned int n, ...);
If n == 0, return 0

**✅ Réponse**

```c
#include "variadic_functions.h"
#include <stdarg.h>

/**
 * sum_them_all - Return the sum of all its parameters
 * @n: number of arguments to sum
 *
 * Return: the sum of all the parameters, or 0 if n is 0
 */
int sum_them_all(const unsigned int n, ...)
{
	int sum = 0;
	va_list ap;
	unsigned int i;
	int value;

	if (n == 0)
	{
		return (0);
	}

	va_start(ap, n);

	for (i = 0; i < n; i++)
	{
		value = va_arg(ap, int);
		sum += value;
	}

	va_end(ap);

	return (sum);
}
```

</details>

<details>
<summary><strong>🧩 1. To be is to be the value of a variable</strong></summary>

**📝 Énoncé**

Write a function that prints numbers, followed by a new line.
**Prototype:** void print_numbers(const char *separator, const unsigned int n, ...);
where separator is the string to be printed between numbers
and n is the number of integers passed to the function
You are allowed to use printf
If separator is NULL, don’t print it
Print a new line at the end of your function

**✅ Réponse**

```c
#include "variadic_functions.h"
#include <stdarg.h>
#include <stdio.h>

/**
 * print_numbers - Prints the numbers followed by a new line
 * @separator: string to be printed between numbers
 * @n: number of integers passed to the function
 *
 * Return: nothing
 */

void print_numbers(const char *separator, const unsigned int n, ...)
{
	va_list ap;
	unsigned int i;
	int value;

	if (n == 0)
	{
		printf("\n");

		return;
	}

	va_start(ap, n);

	for (i = 0; i < n; i++)
	{
		value = va_arg(ap, int);

		printf("%d", value);

		if (separator != NULL && i < n - 1)

			printf("%s", separator);
	}

	va_end(ap);

	printf("\n");
}
```

</details>

<details>
<summary><strong>🧩 2. One woman's constant is another woman's variable</strong></summary>

**📝 Énoncé**

Write a function that prints strings, followed by a new line.
**Prototype:** void print_strings(const char *separator, const unsigned int n, ...);
where separator is the string to be printed between the strings
and n is the number of strings passed to the function
You are allowed to use printf
If separator is NULL, don’t print it
If one of the string is NULL, print (nil) instead
Print a new line at the end of your function

**✅ Réponse**

```c
#include <stdarg.h>
#include "variadic_functions.h"
#include <stdio.h>

/**
 * print_strings - Prints strings followed by a new line
 * @separator: string to be printed between strings
 * @n: number of strings passed to the function
 *
 * Return: nothing
 */

void print_strings(const char *separator, const unsigned int n, ...)
{
	va_list ap;
	unsigned int i;
	char *str;

	if (n == 0)
	{
		printf("\n");

		return;
	}

	va_start(ap, n);

	for (i = 0; i < n; i++)
	{
		str = va_arg(ap, char *);

		if (str == NULL)

			printf("(nil)");
		else
			printf("%s", str);

		if (separator != NULL && i < n - 1)
			printf("%s", separator);
	}

	va_end(ap);
	printf("\n");
}
```

</details>

<details>
<summary><strong>🧩 3. To be is a to be the value of a variable</strong></summary>

**📝 Énoncé**

Write a function that prints anything.
**Prototype:** void print_all(const char * const format, ...);
where format is a list of types of arguments passed to the function
c: char
i: integer
f: float
s: char * (if the string is NULL, print (nil) instead
any other char should be ignored
see example
You are not allowed to use for, goto, ternary operator, else, do ... while
You can use a maximum of
2 while loops
2 if
You can declare a maximum of 9 variables
You are allowed to use printf
Print a new line at the end of your function

**✅ Réponse**

```c
#include "variadic_functions.h"
#include <stdio.h>

/**
 * print_char - Print a character
 * @list: the list of arguments
 *
 * Return: void
 */
void print_char(va_list *list)
{
	printf("%c", va_arg(*list, int));
}

/**
 * print_int - Print an integer
 * @list: the list of arguments
 *
 * Return: void
 */
void print_int(va_list *list)
{
	printf("%d", va_arg(*list, int));
}

/**
 * print_float - Print a float
 * @list: the list of arguments
 *
 * Return: void
 */
void print_float(va_list *list)
{
	printf("%f", va_arg(*list, double));
}

/**
 * print_string - Print a string
 * @list: the list of arguments
 *
 * Description: if the string is NULL, print (nil)
 * Return: void
 */
void print_string(va_list *list)
{
	char *s;

	s = va_arg(*list, char *);
	if (s == NULL)
	{
		printf("(nil)");
		return;
	}

	printf("%s", s);
}

/**
 * print_all - prints anything
 * @format: a list of types of arguments
 *
 * Return: void
 */
void print_all(const char * const format, ...)
{
	type_t type_print[] = {
		{'c', print_char},
		{'i', print_int},
		{'f', print_float},
		{'s', print_string},
		{0, NULL}
	};
	va_list argument_list;
	unsigned int format_index, types_index;
	char *separator;

	separator = "";
	format_index = 0;
	va_start(argument_list, format);

	while (format != NULL && format[format_index] != '\0')
	{
		types_index = 0;
		while (type_print[types_index].types != 0)
		{
			if (format[format_index] == type_print[types_index].types)
			{
				printf("%s", separator);
				type_print[types_index].print_func(&argument_list);
				separator = ", ";
				break;
			}
			types_index++;
		}
		format_index++;
	}

	va_end(argument_list);
	printf("\n");
}

General
When and why using linked lists vs arrays
How to build and use linked lists

Requirements
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
The only C standard library functions allowed are malloc, free and exit. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
You are allowed to use _putchar
You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called lists.h
Don’t forget to push your header file
All your header files should be include guarded

More Info
Please use this data structure for this project:
/**
 * struct list_s - singly linked list
 * @str: string - (malloc'ed string)
 * @len: length of the string
 * @next: points to the next node
 *
 * Description: singly linked list node structure
 */
typedef struct list_s
{
    char *str;
    unsigned int len;
    struct list_s *next;
} list_t;
```

</details>

<details>
<summary><strong>🧩 0. Print list</strong></summary>

**📝 Énoncé**

Write a function that prints all the elements of a list_t list.
**Prototype:** size_t print_list(const list_t *h);
Return: the number of nodes
Format: see example
If str is NULL, print [0] (nil)
You are allowed to use printf

**✅ Réponse**

```c
#include "lists.h"
#include <stdio.h>

/**
* print_list - function that print a list of elements
* @h: pointer to the first node
*
* Return: the number of nodes
*/

size_t print_list(const list_t *h)
{
	size_t count = 0;

	while (h != NULL)
	/**
	 * ou while (h)
	 */
	{
		if (h->str)
		/*
		* ou if (h->str != NULL)
		*/
			printf("[%u] %s\n", h->len, h->str);

		else
			printf("[0] (nil)\n");

		count++;
		h = h->next;
	}
	return (count);
}
```

</details>

<details>
<summary><strong>🧩 1. List length</strong></summary>

**📝 Énoncé**

Write a function that returns the number of elements in a linked list_t list.
**Prototype:** size_t list_len(const list_t *h);

**✅ Réponse**

```c
#include "lists.h"

/**
* list_len - Return the number of elements in a linked list_t list
* @h: pointer to the head of the list
*
* Return: number of nodes in the list
*/

size_t list_len(const list_t *h)
{
	size_t count = 0;

	while (h)
	{
		count++;
		h = h->next;
	}
	return (count);
}
```

</details>

<details>
<summary><strong>🧩 2. Add node</strong></summary>

**📝 Énoncé**

Write a function that adds a new node at the beginning of a list_t list.
**Prototype:** list_t *add_node(list_t **head, const char *str);
Return: the address of the new element, or NULL if it failed
str needs to be duplicated
You are allowed to use strdup

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>
#include <string.h>

/**
 * add_node -  function that adds a new node at the beginning of a list_t list
 * @str: pointer to the string to be stored in the new node
 * @head: double pointer to the head of the list
 *
 * Return: Pointer to the newly added node, or NULL if memory allocation fails
*/

list_t *add_node(list_t **head, const char *str)
{
	list_t *new_node;
		unsigned int len = 0;

	new_node = malloc(sizeof(list_t));

	if (new_node == NULL)
	{
		return (NULL);
	}
	else
	/**
	 * else apparement optionnel
	 */
	{
		new_node->str = strdup(str);

		if (new_node->str == NULL)
		{
			free(new_node);
			return (NULL);
		}

		while (new_node->str[len] != '\0')
		len++;

		new_node->len = len;
		new_node->next = *head;
		*head = new_node;

	}

	return (new_node);
}
```

</details>

<details>
<summary><strong>🧩 3. Add node at the end</strong></summary>

**📝 Énoncé**

Write a function that adds a new node at the end of a list_t list.
**Prototype:** list_t *add_node_end(list_t **head, const char *str);
Return: the address of the new element, or NULL if it failed
str needs to be duplicated
You are allowed to use strdup

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>
#include <string.h>

/**
 * add_node_end - adds a new node at the end of the list_t list
 * @str: string to be duplicated and stored in the new node
 * @head: double pointer to the head of the list
 *
 * Return: the adress of the new element, or NULL if it failed
*/

list_t *add_node_end(list_t **head, const char *str)
{
	list_t *new_node;
	list_t *tmp;
	unsigned int len = 0;

	new_node = malloc(sizeof(list_t));

	if (new_node == NULL)

	return (NULL);

	new_node->str = strdup(str);

		if (new_node->str == NULL)
		{
			free(new_node);
			return (NULL);
		}

		while (str[len] != '\0')
		len++;

		new_node->len = len;
		new_node->next = NULL;

		if (*head == NULL)
		{
			*head = new_node;
		}

		else

		{
			tmp = *head;

			while (tmp->next != NULL)
			tmp = tmp->next;
			tmp->next = new_node;
		}
		return (new_node);
	}
```

</details>

<details>
<summary><strong>🧩 4. Free list</strong></summary>

**📝 Énoncé**

Write a function that frees a list_t list.
**Prototype:** void free_list(list_t *head);

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * free_list - free the list_t list
 * @head: double pointer to the head of the list
 *
 * Return : 0
 */

void free_list(list_t *head)
{
	list_t *tmp;

	while (head)
	{
		tmp = head->next;
		free(head->str);
		free(head);
		head = tmp;
	}
}
```

</details>

- --

<a id="c-doubly-linked-lists"></a>

## 💻 C - DOUBLY LINKED LISTS

### 📌 General

- What is a doubly linked list
- How to use doubly linked lists
- Start to look for the right source of information without too much help

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.5)
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc, free, printf and exit
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions should be included in your header file called lists.h
- Don’t forget to push your header file
- All your header files should be include guarded

### 🔎 More Info


Please use this data structure for this project:
/**
 * struct dlistint_s - doubly linked list
 * @n: integer
 * @prev: points to the previous node
 * @next: points to the next node
 *
 * Description: doubly linked list node structure
 *
 */
typedef struct dlistint_s
{    int n;
    struct dlistint_s *prev;
    struct dlistint_s *next;
} dlistint_t;

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Print list</strong></summary>

**📝 Énoncé**

Write a function that prints all the elements of a dlistint_t list.
**Prototype:** size_t print_dlistint(const dlistint_t *h);
Return: the number of nodes
Format: see example

**✅ Réponse**

```c
#include "lists.h"
#include <stdio.h>

/**
 * print_dlistint - print the elements of dlistint_t list
 * @h: the head of the linked list
 *
 * Return: the number of elements
 */

size_t print_dlistint(const dlistint_t *h)

{
	size_t len = 0;

	if (h == NULL)
	return (0);

	for (; h != NULL; h = h->next)
	{
		printf("%d\n", h->n);
		len++;
	}

	return (len);

}
```

</details>

<details>
<summary><strong>🧩 1. List length</strong></summary>

**📝 Énoncé**

Write a function that returns the number of elements in a linked dlistint_t list.
**Prototype:** size_t dlistint_len(const dlistint_t *h);

**✅ Réponse**

```c
#include "lists.h"

/**
 * dlistint_len - prints the number of elements
* @h: the head of the linked list
*
* Return: the number of elements printed
*/

size_t dlistint_len(const dlistint_t *h)
{
	size_t len = 0;

	if (h == NULL)
	return (0);

	for (; h != NULL; h = h->next)
	len++;

	return (len);

}
```

</details>

<details>
<summary><strong>🧩 2. Add node</strong></summary>

**📝 Énoncé**

Write a function that adds a new node at the beginning of a dlistint_t list.
**Prototype:** dlistint_t *add_dnodeint(dlistint_t **head, const int n);
Return: the address of the new element, or NULL if it failed

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * add_dnodeint - Add a new node at the beginning of a dlistint_t list
 * @head: pointer to pointer to the head of the list
 * @n: value to store inside the new node
 *
 * Return: the adress of the new element, or NULL if it failed
 */

dlistint_t *add_dnodeint(dlistint_t **head, const int n)
{
	dlistint_t *new;

	if (head == NULL)
	return (NULL);

	new = malloc(sizeof(dlistint_t));

	if (new == NULL)
	return (NULL);

	new->n = n;
	new->prev = NULL;
	new->next = *head;

	if (*head != NULL)
	(*head)->prev = new;
	(*head) = new;

	return (new);

}
```

</details>

<details>
<summary><strong>🧩 3. Add node at the end</strong></summary>

**📝 Énoncé**

Write a function that adds a new node at the end of a dlistint_t list.
**Prototype:** dlistint_t *add_dnodeint_end(dlistint_t **head, const int n);
Return: the address of the new element, or NULL if it failed

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * add_dnodeint_end - add a new node at the end a the dlistint_t list
 * @head: pointer to pointer to the head of the list
 * @n: value to store inside the new node
 *
 * Return: the address of the new element, or NULL if it failed
 */

dlistint_t *add_dnodeint_end(dlistint_t **head, const int n)
{
	dlistint_t *new;
	dlistint_t *tmp;

	if (head == NULL)
	return (NULL);

	new = malloc(sizeof(dlistint_t));
	if (new == NULL)
	return (NULL);

	new->n = n;
	new->next = NULL;

	if (*head == NULL)
	{
		new->prev = NULL;
		*head = new;
		return (new);
	}

	tmp = *head;
	while (tmp->next != NULL)
	tmp = tmp->next;

	tmp->next = new;
	new->prev = tmp;

	return (new);

}
```

</details>

<details>
<summary><strong>🧩 4. Free list</strong></summary>

**📝 Énoncé**

Write a function that frees a dlistint_t list.
**Prototype:** void free_dlistint(dlistint_t *head);

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * free_dlistint - free dlistint_t list
 * @head: pointer to the head of the list
 *
 * Return: ???
 */

void free_dlistint(dlistint_t *head)
{
	dlistint_t *tmp;

	while (head != NULL)
	{
	tmp = head;
	head = head->next;
	free(tmp);
	}

}
```

</details>

<details>
<summary><strong>🧩 5. Get node at index</strong></summary>

**📝 Énoncé**

Write a function that returns the nth node of a dlistint_t linked list.
**Prototype:** dlistint_t *get_dnodeint_at_index(dlistint_t *head, unsigned int index);
where index is the index of the node, starting from 0
if the node does not exist, return NULL

**✅ Réponse**

```c
#include "lists.h"

/**
 * get_dnodeint_at_index - return the nth node of a dlistint_t list
 * @head: pointer to the first node of the list
 * @index: position of the node to retrieve (start to 0)
 *
 * Return: a pointer to the node at the index, or NULL if it doesn't exist
 */

dlistint_t *get_dnodeint_at_index(dlistint_t *head, unsigned int index)
{
	unsigned int i = 0;

	while (head != NULL)
	{
		if (i == index)
		return (head);

		head = head->next;
		i++;
	}
	return (NULL);
}
```

</details>

<details>
<summary><strong>🧩 6. Sum list</strong></summary>

**📝 Énoncé**

Write a function that returns the sum of all the data (n) of a dlistint_t linked list.
**Prototype:** int sum_dlistint(dlistint_t *head);
if the list is empty, return 0

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * sum_dlistint - return the sum of all the n of a dlistint_t list
 * @head: pointer to the head of the list
 *
 * Return: the sum of all n, or 0 if it failed
 */

int sum_dlistint(dlistint_t *head)
{
	int sum = 0;

	while (head != NULL)
	{
		sum += head->n;
		head = head->next;
	}
	return (sum);
}
```

</details>

<details>
<summary><strong>🧩 7. Insert at index</strong></summary>

**📝 Énoncé**

Write a function that inserts a new node at a given position.
**Prototype:** dlistint_t *insert_dnodeint_at_index(dlistint_t **h, unsigned int idx, int n);
where idx is the index of the list where the new node should be added. Index starts at 0
Returns: the address of the new node, or NULL if it failed
if it is not possible to add the new node at index idx, do not add the new node and return NULL
Your files 2-add_dnodeint.c and 3-add_dnodeint_end.c will be compiled during the correction

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * insert_dnodeint_at_index - insert a new node on a position
 * @h: pointer to the head of the list
 * @idx: index where the node would be insert
 * @n: value of the new node
 *
 * Return: the adress of the new node, or NULL if it failed
 */

dlistint_t *insert_dnodeint_at_index(dlistint_t **h, unsigned int idx, int n)
{
	dlistint_t *tmp;
	unsigned int i = 0;

	if (h == NULL)
	return (NULL);

	if (idx == 0)
	return (add_dnodeint(h, n));

	tmp = *h;

	while (tmp != NULL && i < idx - 1)
	{
		tmp = tmp->next;
		i++;
	}

	if (tmp == NULL)
	return (NULL);

	if (tmp->next == NULL)
	return (add_dnodeint_end(h, n));

	{
		dlistint_t *new = malloc(sizeof(dlistint_t));

		if (new == NULL)
		return (NULL);

		new->n = n;
		new->next = tmp->next;
		new->prev = tmp;
		tmp->next->prev = new;
		tmp->next = new;

		return (new);
	}
}
```

</details>

<details>
<summary><strong>🧩 8. Delete at index</strong></summary>

**📝 Énoncé**

Write a function that deletes the node at index index of a dlistint_t linked list.
**Prototype:** int delete_dnodeint_at_index(dlistint_t **head, unsigned int index);
where index is the index of the node that should be deleted. Index starts at 0
Returns: 1 if it succeeded, -1 if it failed

**✅ Réponse**

```c
#include "lists.h"
#include <stdlib.h>

/**
 * delete_dnodeint_at_index - delete the note at the index
 * @head: pointer to the head of the list
 * @index: position of the node to delete
 *
 * Return: 1 if success, or -1 if failed
 */

int delete_dnodeint_at_index(dlistint_t **head, unsigned int index)
{
	dlistint_t *tmp = *head;
	unsigned int i = 0;

	if (head == NULL || *head == NULL)
	return (-1);

	if (index == 0)
	{
		*head = tmp->next;
		if (tmp->next != NULL)
		tmp->next->prev = NULL;
		free(tmp);
		return (1);
	}

	while (tmp != NULL && i < index)
	{
		tmp = tmp->next;
		i++;
	}

	if (tmp == NULL)
	return (-1);

	if (tmp->prev != NULL)
	tmp->prev->next = tmp->next;

	if (tmp->next != NULL)
	tmp->next->prev = tmp->prev;

	free(tmp);
	return (1);
}
```

</details>

- --

<a id="c-file-i-o"></a>

## 💻 C - FILE I/O

### 📌 General

- Look for the right source of information online
- How to create, open, close, read and write files
- What are file descriptors
- What are the 3 standard file descriptors, what are their purpose and what are their POSIX names
- How to use the I/O system calls open, close, read and write
- What are and how to use the flags O_RDONLY, O_WRONLY, O_RDWR
- What are file permissions, and how to set them when creating a file with the open system call
- What is a system call
- What is the difference between a function and a system call

### ✅ Requirements

- Allowed editors: vi, vim, emacs
- All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
- You are not allowed to use global variables
- No more than 5 functions per file
- The only C standard library functions allowed are malloc, free and exit. Any use of functions like printf, puts, calloc, realloc etc… is forbidden
- Allowed syscalls: read, write, open, close
- You are allowed to use _putchar
- You don’t have to push _putchar.c, we will use our file. If you do it won’t be taken into account
- In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
- The prototypes of all your functions and the prototype of the function _putchar should be included in your header file called main.h
- Don’t forget to push your header file
- All your header files should be include guarded
- Tip: always prefer using symbolic constants (POSIX) vs numbers when it makes sense. For instance read(STDIN_FILENO, ... vs read(0, ...

### 🧩 Tâches

<details>
<summary><strong>🧩 0. Tread lightly, she is near</strong></summary>

**📝 Énoncé**

Write a function that reads a text file and prints it to the POSIX standard output.
**Prototype:** ssize_t read_textfile(const char *filename, size_t letters);
where letters is the number of letters it should read and print
returns the actual number of letters it could read and print
if the file can not be opened or read, return 0
if filename is NULL return 0
if write fails or does not write the expected amount of bytes, return 0

**✅ Réponse**

```c
#include "main.h"
#include <fcntl.h>
#include <unistd.h>
#include <stdlib.h>

/**
 * read_textfile - Read a text file and print it to POSIX outpout
 * @filename: Name of the file to read
 * @letters: Number of letters to read and print
 *
 * Return: The number of letters, read, print, return 0 if it failed
 */

ssize_t read_textfile(const char *filename, size_t letters)
{
	int fd;
	ssize_t read2, write2;
	char *buffer;

	if (filename == NULL)
	return (0);

	fd = open(filename, O_RDONLY);
	if (fd == -1)
	return (0);

	buffer = malloc(sizeof(char) * letters);
	if (buffer == NULL)
	{
		close(fd);
		return (0);
	}

	read2 = read(fd, buffer, letters);
	if (read2 == -1)
	{
		free(buffer);
		close(fd);
		return (0);
	}

	write2 = write(STDOUT_FILENO, buffer, read2);
	free(buffer);
	close(fd);
	if (write2 != read2)
		return (0);

	return (write2);
}
```

</details>

<details>
<summary><strong>🧩 1. Under the snow</strong></summary>

**📝 Énoncé**

Create a function that creates a file.
**Prototype:** int create_file(const char *filename, char *text_content);
where filename is the name of the file to create and text_content is a NULL terminated string to write to the file
Returns: 1 on success, -1 on failure (file can not be created, file can not be written, write “fails”, etc…)
The created file must have those permissions: rw-------. If the file already exists, do not change the permissions.
if the file already exists, truncate it
if filename is NULL return -1
if text_content is NULL create an empty file

**✅ Réponse**

```c
#include "main.h"
#include <fcntl.h>
#include <unistd.h>
#include <stdlib.h>

/**
 * create_file - create a file and write inside
 * @filename: Name of the file to be created
 * @text_content: String to write inside this file
 *
 * Return: Sucess = 1, failed = -1
 */

int create_file(const char *filename, char *text_content)
{
	int fd;
	ssize_t write2;
	size_t textlen = 0;

	if (filename == NULL)
	return (-1);

	if (text_content != NULL)
	{
		while (text_content[textlen] != '\0')
		textlen++;
	}

	fd = open(filename, O_WRONLY | O_CREAT | O_TRUNC, 0600);
	if (fd == -1)
	return (-1);

	if (textlen > 0)
	{
		write2 = write(fd, text_content, textlen);
		if (write2 == -1 || (size_t)write2 != textlen)
		{
			close(fd);
			return (-1);
		}
	}
	close(fd);
	return (1);
}
```

</details>

<details>
<summary><strong>🧩 2. Speak gently, she can hear</strong></summary>

**📝 Énoncé**

Write a function that appends text at the end of a file.
**Prototype:** int append_text_to_file(const char *filename, char *text_content);
where filename is the name of the file and text_content is the NULL terminated string to add at the end of the file
Return: 1 on success and -1 on failure
Do not create the file if it does not exist
If filename is NULL return -1
If text_content is NULL, do not add anything to the file. Return 1 if the file exists and -1 if the file does not exist or if you do not have the required permissions to write the file

**✅ Réponse**

```c
#include "main.h"
#include <stdlib.h>
#include <fcntl.h>
#include <unistd.h>

/**
 * append_text_to_file - Append text at the end of a file
 * @filename: Name of the file
 * @text_content: String to append
 *
 * Return: Success = 1, Fail = -1
 */

int append_text_to_file(const char *filename, char *text_content)
{
	int fd;
	ssize_t write2;
	size_t len = 0;

	if (filename == NULL)
	return (-1);

	if (text_content != NULL)
	{
		while (text_content[len] != '\0')
		len++;
	}

	fd = open(filename, O_WRONLY | O_APPEND);
	if (fd == -1)
	return (-1);

	if (len == 0)
	{
		close(fd);
		return (1);
	}

	write2 = write(fd, text_content, len);
	if (write2 == -1 || (size_t)write2 != len)
	{
		close(fd);
		return (-1);
	}
	close(fd);
	return (1);
}
```

</details>

<details>
<summary><strong>🧩 3. cp</strong></summary>

**📝 Énoncé**

Write a program that copies the content of a file to another file.
Usage: cp file_from file_to
if the number of argument is not the correct one, exit with code 97 and print Usage: cp file_from file_to, followed by a new line, on the POSIX standard error
if file_to already exists, truncate it
if file_from does not exist, or if you can not read it, exit with code 98 and print Error: Can't read from file NAME_OF_THE_FILE, followed by a new line, on the POSIX standard error
where NAME_OF_THE_FILE is the first argument passed to your program
if you can not create or if write to file_to fails, exit with code 99 and print Error: Can't write to NAME_OF_THE_FILE, followed by a new line, on the POSIX standard error
where NAME_OF_THE_FILE is the second argument passed to your program
if you can not close a file descriptor , exit with code 100 and print Error: Can't close fd FD_VALUE, followed by a new line, on the POSIX standard error
where FD_VALUE is the value of the file descriptor
Permissions of the created file: rw-rw-r--. If the file already exists, do not change the permissions
You must read 1,024 bytes at a time from the file_from to make less system calls. Use a buffer
You are allowed to use dprintf

**✅ Réponse**

```c
#include "main.h"
#include <stdio.h>
#include <stdlib.h>
#include <fcntl.h>
#include <unistd.h>

/**
 * usage_error - prints usage message and exits with code 97
 */
void usage_error(void)
{
	dprintf(STDERR_FILENO, "Usage: cp file_from file_to\n");
	exit(97);
}

/**
 * read_error - prints read error message and exits with code 98
 * @filename: name of the file that can't be read
 */
void read_error(const char *filename)
{
	dprintf(STDERR_FILENO, "Error: Can't read from file %s\n", filename);
	exit(98);
}

/**
 * write_error - prints write error message and exits with code 99
 * @filename: name of the file that can't be written to
 */
void write_error(const char *filename)
{
	dprintf(STDERR_FILENO, "Error: Can't write to %s\n", filename);
	exit(99);
}

/**
 * close_fd - closes a file descriptor or exits with code 100
 * @fd: file descriptor to close
 */
void close_fd(int fd)
{
	if (close(fd) == -1)
	{
		dprintf(STDERR_FILENO, "Error: Can't close fd %d\n", fd);
		exit(100);
	}
}

/**
 * main - copies the content of a file to another file
 * @ac: number of arguments
 * @av: array of arguments
 *
 * Return: 0 on success
 */
int main(int ac, char **av)
{
	int fd_from, fd_to;
	ssize_t rd, wr;
	char buffer[1024];

	if (ac != 3)
		usage_error();

	fd_from = open(av[1], O_RDONLY);
	if (fd_from == -1)
		read_error(av[1]);

	fd_to = open(av[2], O_WRONLY | O_CREAT | O_TRUNC, 0664);
	if (fd_to == -1)
	{
		close_fd(fd_from);
		write_error(av[2]);
	}

	while ((rd = read(fd_from, buffer, 1024)) > 0)
	{
		wr = write(fd_to, buffer, rd);
		if (wr == -1)
		{
			close_fd(fd_from);
			close_fd(fd_to);
			write_error(av[2]);
		}
	}

	if (rd == -1)
	{
		close_fd(fd_from);
		close_fd(fd_to);
		read_error(av[1]);
	}

	close_fd(fd_from);
	close_fd(fd_to);

	return (0);
}
```

</details>

- --

<a id="c-hash-tables"></a>

## 💻 C - HASH TABLES

### 📌 General

What is a hash function
What makes a good hash function
What is a hash table, how do they work and how to use them
What is a collision and what are the main ways of dealing with collisions in the context of a hash table
What are the advantages and drawbacks of using hash tables
What are the most common use cases of hash tables

### ✅ Requirements

Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are allowed to use the C standard library
The prototypes of all your functions should be included in your header file called hash_tables.h
Don’t forget to push your header file
All your header files should be include guarded

### 🔎 More Info

Data Structures
Please use these data structures for this project:

/**
 * struct hash_node_s - Node of a hash table
 *
 * @key: The key, string
 * The key is unique in the HashTable
 * @value: The value corresponding to a key
 * @next: A pointer to the next node of the List
 */
typedef struct hash_node_s
{
     char *key;
     char *value;
     struct hash_node_s *next;
} hash_node_t;

/**
 * struct hash_table_s - Hash table data structure
 *
 * @size: The size of the array
 * @array: An array of size @size
 * Each cell of this array is a pointer to the first node of a linked list,
 * because we want our HashTable to use a Chaining collision handling
 */
typedef struct hash_table_s
{
     unsigned long int size;
     hash_node_t **array;
} hash_table_t;
Tests
We strongly encourage you to work all together on a set of tests
Python Dictionaries
Python dictionaries are implemented using hash tables. When you will be done with this project, you will be able to better understand the power and simplicity of Python dictionaries. So much is actually happening when you type d = {'a': 1, 'b': 2}, but everything looks so simple for the user. Python doesn’t use the exact same implementation than the one you will work on today though. If you are curious on how it works under the hood, here is a good blog post about how dictionaries are implemented in Python 2.7 (not mandatory).

### 🧩 Tâches

<details>
<summary><strong>🧩 0. >>> ht = { }</strong></summary>

**📝 Énoncé**

Write a function that creates a hash table.
**Prototype:** hash_table_t *hash_table_create(unsigned long int size);
where size is the size of the array
Returns a pointer to the newly created hash table
If something went wrong, your function should return NULL

**✅ Réponse**

```c
#include "hash_tables.h"
#include <stdlib.h>

/**
* hash_table_create - create an hash table
* @size: the size of the array
*
* Return: pointer to the hash table or NULL if it failed
*/

hash_table_t *hash_table_create(unsigned long int size)
{
	hash_table_t *ht;
	unsigned long int i;

	if (size == 0)
	return (NULL);

	ht = malloc(sizeof(hash_table_t));
	if (ht == NULL)
	return (NULL);

	ht->size = size;
	ht->array = malloc(sizeof(hash_node_t *) * size);
	if (ht->array == NULL)
	{
		free(ht);
		return (NULL);
	}

	for (i = 0; i < size; i++)
	ht->array[i] = NULL;

	return (ht);
}
```

</details>

<details>
<summary><strong>🧩 1. djb2</strong></summary>

**📝 Énoncé**

Write a hash function implementing the djb2 algorithm.
**Prototype:** unsigned long int hash_djb2(const unsigned char *str);
You are allowed to copy and paste the function from this page

**✅ Réponse**

```c
#include "hash_tables.h"

/**
 * hash_djb2 - implementation of the djb2 algorithm
 * @str: string used to generate hash value
 *
 * Return: hash value
 */

unsigned long int hash_djb2(const unsigned char *str)
{
	unsigned long int hash;
	int c;

	hash = 5381;
	while ((c = *str++))
	{
		hash = ((hash << 5) + hash) + c; /* hash * 33 + c */
	}
	return (hash);
}
```

</details>

<details>
<summary><strong>🧩 2. key -> index</strong></summary>

**📝 Énoncé**

Write a function that gives you the index of a key.
**Prototype:** unsigned long int key_index(const unsigned char *key, unsigned long int size);
where key is the key
and size is the size of the array of the hash table
This function should use the hash_djb2 function that you wrote earlier
Returns the index at which the key/value pair should be stored in the array of the hash table
You will have to use this hash function for all the next tasks

**✅ Réponse**

```c
#include "hash_tables.h"

/**
* key_index - the index of a key inside the hash table
* @key: the index
* @size: the size of the array
*
* Return: the index with the value that we are looking for
*/

unsigned long int key_index(const unsigned char *key, unsigned long int size)
{
	return (hash_djb2(key) % size);
}
```

</details>

<details>
<summary><strong>🧩 3. >>> ht['betty'] = 'cool'</strong></summary>

**📝 Énoncé**

Write a function that adds an element to the hash table.
**Prototype:** int hash_table_set(hash_table_t *ht, const char *key, const char *value);
Where ht is the hash table you want to add or update the key/value to
key is the key. key can not be an empty string
and value is the value associated with the key. value must be duplicated. value can be an empty string
Returns: 1 if it succeeded, 0 otherwise
In case of collision, add the new node at the beginning of the list

**✅ Réponse**

```c
#include "hash_tables.h"

/**
 * create_node - create a node
 * @key: key we add
 * @value: value inside the key
 *
 * Return: pointer to the new node, or NULL if it failed
 */

hash_node_t *create_node(const char *key, const char *value)
{
	hash_node_t *new_node;

	new_node = malloc(sizeof(hash_node_t));
	if (new_node == NULL)
	return (NULL);

	new_node->key = strdup(key);
	if (new_node->key == NULL)
	{
		free(new_node);
		return (NULL);
	}

	new_node->value = strdup(value);
	if (new_node->value == NULL)
	{
		free(new_node->key);
		free(new_node);
		return (NULL);
	}

	new_node->next = NULL;
	return (new_node);
}

/**
 * hash_table_set - Adds or updates an element in the hash table
 * @ht: Hash table
 * @key: Key
 * @value: Value inside key
 * Return: 1 on success, 0 if it failed
 */

int hash_table_set(hash_table_t *ht, const char *key, const char *value)
{
	unsigned long int idx;
	hash_node_t *tmp;
	hash_node_t *new_node;
	char *new_value;

	if (ht == NULL || key == NULL || strlen(key) == 0 || value == NULL)
	return (0);

	idx = key_index((const unsigned char *)key, ht->size);
	tmp = ht->array[idx];

	while (tmp != NULL)
	{
		if (strcmp(tmp->key, key) == 0)
		{
			new_value = strdup(value);
			if (new_value == NULL)
			return (0);

			free(tmp->value);
			tmp->value = new_value;
			return (1);
		}
		tmp = tmp->next;
	}

	new_node = create_node(key, value);
	if (new_node == NULL)
	return (0);

	new_node->next = ht->array[idx];
	ht->array[idx] = new_node;

	return (1);
}

If you want to test for collisions, here are some strings that collide using the djb2 algorithm:

- hetairas collides with mentioner
- heliotropes collides with neurospora
- depravement collides with serafins
- stylist collides with subgenera
- joyful collides with synaphea
- redescribed collides with urites
- dram collides with vivency
```

</details>

<details>
<summary><strong>🧩 4. >>> ht['betty']</strong></summary>

**📝 Énoncé**

Write a function that retrieves a value associated with a key.
**Prototype:** char *hash_table_get(const hash_table_t *ht, const char *key);
where ht is the hash table you want to look into
and key is the key you are looking for
Returns the value associated with the element, or NULL if key couldn’t be found

**✅ Réponse**

```c
#include "hash_tables.h"

/**
 * hash_table_get - find a value with a key
 * @ht: the hash table
 * @key: the key we are looking for
 *
 * Return: the value that we want with the key or NULL if it failed
 */

char *hash_table_get(const hash_table_t *ht, const char *key)
{
	unsigned long int idx;
	hash_node_t *node;

	idx = 0;
	if (ht == NULL || key == NULL || *key == '\0')
	return (NULL);

	idx = key_index((const unsigned char *)key, ht->size);
	node = ht->array[idx];

	while (node != NULL)
	{
		if (strcmp(node->key, key) == 0)
		return (node->value);
		node = node->next;
	}
	return (NULL);
}
```

</details>

<details>
<summary><strong>🧩 5. >>> print(ht)</strong></summary>

**📝 Énoncé**

Write a function that prints a hash table.
**Prototype:** void hash_table_print(const hash_table_t *ht);
where ht is the hash table
You should print the key/value in the order that they appear in the array of hash table
Order: array, list
Format: see example
If ht is NULL, don’t print anything

**✅ Réponse**

```c
#include "hash_tables.h"

/**
 * hash_table_print - Prints a hash table
 * @ht: pointer to the hash table
 */

void hash_table_print(const hash_table_t *ht)
{
	hash_node_t *node;
	unsigned long int i;
	int first = 1;

	if (ht == NULL)
	return;

	printf("{");

	for (i = 0; i < ht->size; i++)
	{
		node = ht->array[i];

		while (node != NULL)
		{
			if (!first)
			printf(", ");
			printf("'%s': '%s'", node->key, node->value);
			first = 0;
			node = node->next;
		}
	}
	printf("}\n");
}
```

</details>

<details>
<summary><strong>🧩 6. >>> del ht</strong></summary>

**📝 Énoncé**

Write a function that deletes a hash table.
**Prototype:** void hash_table_delete(hash_table_t *ht);
where ht is the hash table

**✅ Réponse**

```c
#include "hash_tables.h"

/**
 * hash_table_delete - delete the hash table
 * @ht: pointer to the hash table
 */

void hash_table_delete(hash_table_t *ht)
{
	hash_node_t *node;
	hash_node_t *tmp;
	unsigned long int i;

	if (ht == NULL)
	return;

	for (i = 0; i < ht->size; i++)
	{
		node = ht->array[i];
		while (node != 0)
		{
			tmp = node->next;
			free(node->key);
			free(node->value);
			free(node);
			node = tmp;
		}
	}

	free(ht->array);
	free(ht);
}
```

</details>

- --

/**<a id="c-binary-trees-georgia"></a>

## 💻 C - BINARY TREES GEORGIA

### 📌 General

What is a binary tree
What is the difference between a binary tree and a Binary Search Tree
What is the possible gain in terms of time complexity compared to linked lists
What are the depth, the height, the size of a binary tree
What are the different traversal methods to go through a binary tree
What is a complete, a full, a perfect, a balanced binary tree

### ✅ Requirements

Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are allowed to use the standard library
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions should be included in your header file called binary_trees.h
Don’t forget to push your header file
All your header files should be include guarded

GitHub
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

### 🔎 More Info

Data structures

Please use the following data structures and types for binary trees. Don’t forget to include them in your header file.

Basic Binary Tree
/**
 * struct binary_tree_s - Binary tree node
 *
 * @n: Integer stored in the node
 * @parent: Pointer to the parent node
 * @left: Pointer to the left child node
 * @right: Pointer to the right child node
 */
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;

Binary Search Tree

typedef struct binary_tree_s bst_t;

AVL Tree

typedef struct binary_tree_s avl_t;

Max Binary Heap

typedef struct binary_tree_s heap_t;

Note: For tasks 0 to 23 (included), you have to deal with simple binary trees. They are not BSTs, thus they don’t follow any kind of rule.

Print function
To match the examples in the tasks, you are given this function

This function is used only for visualization purposes. You don’t have to push it to your repo. It may not be used during the correction

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "binary_trees.h"

/* Original code from http://stackoverflow.com/a/13755911/5184480 */

/**
 * print_t - Stores recursively each level in an array of strings
 *
 * @tree: Pointer to the node to print
 * @offset: Offset to print
 * @depth: Depth of the node
 * @s: Buffer
 *
 * Return: length of printed tree after process
 */
static int print_t(const binary_tree_t *tree, int offset, int depth, char **s)
{
	char b[6];
	int width, left, right, is_left, i;

	if (!tree)
		return (0);
	is_left = (tree->parent && tree->parent->left == tree);
	width = sprintf(b, "(%03d)", tree->n);
	left = print_t(tree->left, offset, depth + 1, s);
	right = print_t(tree->right, offset + left + width, depth + 1, s);
	for (i = 0; i < width; i++)
		s[depth][offset + left + i] = b[i];
	if (depth && is_left)
	{
		for (i = 0; i < width + right; i++)
			s[depth - 1][offset + left + width / 2 + i] = '-';
		s[depth - 1][offset + left + width / 2] = '.';
	}
	else if (depth && !is_left)
	{
		for (i = 0; i < left + width; i++)
			s[depth - 1][offset - width / 2 + i] = '-';
		s[depth - 1][offset + left + width / 2] = '.';
	}
	return (left + width + right);
}

/**
 * _height - Measures the height of a binary tree
 *
 * @tree: Pointer to the node to measures the height
 *
 * Return: The height of the tree starting at @node
 */
static size_t _height(const binary_tree_t *tree)
{
	size_t height_l;
	size_t height_r;

	height_l = tree->left ? 1 + _height(tree->left) : 0;
	height_r = tree->right ? 1 + _height(tree->right) : 0;
	return (height_l > height_r ? height_l : height_r);
}

/**
 * binary_tree_print - Prints a binary tree
 *
 * @tree: Pointer to the root node of the tree to print
 */
void binary_tree_print(const binary_tree_t *tree)
{
	char **s;
	size_t height, i, j;

	if (!tree)
		return;
	height = _height(tree);
	s = malloc(sizeof(*s) * (height + 1));
	if (!s)
		return;
	for (i = 0; i < height + 1; i++)
	{
		s[i] = malloc(sizeof(**s) * 255);
		if (!s[i])
			return;
		memset(s[i], 32, 255);
	}
	print_t(tree, 0, 0, s);
	for (i = 0; i < height + 1; i++)
	{
		for (j = 254; j > 1; --j)
		{
			if (s[i][j] != ' ')
				break;
			s[i][j] = '\0';
		}
		printf("%s\n", s[i]);
		free(s[i]);
	}
	free(s);
}

#ifndef _BINARY_TREES_H_
#define _BINARY_TREES_H_

#include <stddef.h>

/**
 * struct binary_tree_s - Binary tree node
 *
 * @n: Integer stored in the node
 * @parent: Pointer to the parent node
 * @left: Pointer to the left child node
 * @right: Pointer to the right child node
 */
typedef struct binary_tree_s
{
	int n;
	struct binary_tree_s *parent;
	struct binary_tree_s *left;
	struct binary_tree_s *right;
} binary_tree_t;

void binary_tree_print(const binary_tree_t *);

#endif /* _BINARY_TREES_H_ */

### 🧩 Tâches

<details>
<summary><strong>🧩 0. New node</strong></summary>

**📝 Énoncé**

Write a function that creates a binary tree node
**Prototype:** binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
Where parent is a pointer to the parent node of the node to create
And value is the value to put in the new node
When created, a node does not have any child
Your function must return a pointer to the new node, or NULL on failure

**✅ Réponse**

```c
#include <stdlib.h>
#include "binary_trees.h"

/**
* binary_tree_node - Creates a binary tree node
* @parent: Pointer to the parent node of the new node
* @value: Value to store in the new node
*
* Description: Allocates memory for a new binary tree node,
* initializes its value to `value`, sets its parent to `parent`,
* and its left and right children to NULL.
*
* Return: Pointer to the newly created node, or NULL on failure
*/

binary_tree_t *binary_tree_node(binary_tree_t *parent, int value)
{
	binary_tree_t *new_node;

	new_node = malloc(sizeof(*new_node));
	if (new_node == NULL)
		return (NULL);

	new_node->n = value;
	new_node->left = NULL;
	new_node->right = NULL;
	new_node->parent = parent;

	return (new_node);
}
```

</details>

<details>
<summary><strong>🧩 1. Insert left</strong></summary>

**📝 Énoncé**

Write a function that inserts a node as the left-child of another node
**Prototype:** binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the left-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a left-child, the new node must take its place, and the old left-child must be set as the left-child of the new node.

**✅ Réponse**

```c
#include <stdlib.h>
#include "binary_trees.h"

/**
 * binary_tree_insert_left - Inserts a node as the left-child of another node
 * @parent: Pointer to the parent node
 * @value: Value to store in the new node
 *
 * Description: Creates a new node and inserts it as the left child of
 * the parent node. If the parent already has a left child, the new
 * node replaces it and the old left child becomes the left child of
 * the new node.
 *
 * Return: Pointer to the newly created node, or NULL on failure or if
 * parent is NULL
 */
binary_tree_t *binary_tree_insert_left(binary_tree_t *parent, int value)
{
	binary_tree_t *new_node;

	if (parent == NULL)
		return (NULL);

	new_node = malloc(sizeof(*new_node));
	if (new_node == NULL)
		return (NULL);

	new_node->n = value;
	new_node->left = NULL;
	new_node->right = NULL;
	new_node->parent = parent;

	if (parent->left != NULL)
	{
	new_node->left = parent->left;
	parent->left->parent = new_node;
	}
	parent->left = new_node;

	return (new_node);
}
```

</details>

<details>
<summary><strong>🧩 2. Insert right</strong></summary>

**📝 Énoncé**

Write a function that inserts a node as the right-child of another node
**Prototype:** binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value);
Where parent is a pointer to the node to insert the right-child in
And value is the value to store in the new node
Your function must return a pointer to the created node, or NULL on failure or if parent is NULL
If parent already has a right-child, the new node must take its place, and the old right-child must be set as the right-child of the new node.

**✅ Réponse**

```c
#include <stdlib.h>
#include "binary_trees.h"

/**
 * binary_tree_insert_right - Inserts a node as the right-child of another node
 * @parent: Pointer to the parent node
 * @value: Value to store in the new node
 *
 * Description: Creates a new node and inserts it as the right child of
 * the parent node. If the parent already has a right child, the new
 * node replaces it and the old right child becomes the right child of
 * the new node.
 *
 * Return: Pointer to the newly created node,
 * or NULL on failure or if parent is NULL
 */
binary_tree_t *binary_tree_insert_right(binary_tree_t *parent, int value)
{
	binary_tree_t *new_node;

	if (parent == NULL)
		return (NULL);

	new_node = malloc(sizeof(*new_node));
	if (new_node == NULL)
		return (NULL);

	new_node->n = value;
	new_node->left = NULL;
	new_node->right = NULL;
	new_node->parent = parent;

	if (parent->right != NULL)
	{
		new_node->right = parent->right;
		parent->right->parent = new_node;
	}
	parent->right = new_node;

	return (new_node);
}
```

</details>

<details>
<summary><strong>🧩 3. Delete</strong></summary>

**📝 Énoncé**

Write a function that deletes an entire binary tree
**Prototype:** void binary_tree_delete(binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to delete
If tree is NULL, do nothing

**✅ Réponse**

```c
#include "binary_trees.h"
#include <stdlib.h>

/**
* binary_tree_delete - Deletes an entire binary tree
* @tree: Pointer to the root node of the tree to delete
*
* If tree is NULL, do nothing
*/
void binary_tree_delete(binary_tree_t *tree)
{
	if (tree == NULL)
		return;

	binary_tree_delete(tree->left);

	binary_tree_delete(tree->right);

	free(tree);
}
```

</details>

<details>
<summary><strong>🧩 4. Is leaf</strong></summary>

**📝 Énoncé**

Write a function that checks if a node is a leaf
**Prototype:** int binary_tree_is_leaf(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a leaf, otherwise 0
If node is NULL, return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_is_leaf - Checks if a node is a leaf
 * @node: Pointer to the node to check
 *
 * Return: 1 if the node is a leaf, 0 otherwise
 *         Returns 0 if node is NULL
 */
int binary_tree_is_leaf(const binary_tree_t *node)
{
	if (node == NULL)
		return (0);
	if (node->left == NULL && node->right == NULL)
		return (1);
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 5. Is root</strong></summary>

**📝 Énoncé**

Write a function that checks if a given node is a root
**Prototype:** int binary_tree_is_root(const binary_tree_t *node);
Where node is a pointer to the node to check
Your function must return 1 if node is a root, otherwise 0
If node is NULL, return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_is_root - Checks if a node is a root
 * @node: Pointer to the node to check
 *
 * Return: 1 if the node is a root, 0 otherwise
 *         Returns 0 if node is NULL
 */
int binary_tree_is_root(const binary_tree_t *node)
{
	if (node == NULL)
		return (0);
	if (node->parent == NULL)
		return (1);
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 6. Pre-order traversal</strong></summary>

**📝 Énoncé**

Write a function that goes through a binary tree using pre-order traversal
**Prototype:** void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

**✅ Réponse**

```c
#include "binary_trees.h"

/**
* binary_tree_preorder - parcourt un arbre binaire en pré-ordre
* @tree: pointeur vers la racine de l'arbre à parcourir
* @func: pointeur vers la fonction à appeler pour chaque nœud
*
* Description: La fonction traverse l'arbre en pré-ordre et
* appelle la fonction `func` sur la valeur de chaque nœud.
*/
void binary_tree_preorder(const binary_tree_t *tree, void (*func)(int))
{
	if (tree == NULL || func == NULL)
		return;

	func(tree->n);
	binary_tree_preorder(tree->left, func);
	binary_tree_preorder(tree->right, func);
}
```

</details>

<details>
<summary><strong>🧩 7. In-order traversal</strong></summary>

**📝 Énoncé**

Write a function that goes through a binary tree using in-order traversal
**Prototype:** void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

**✅ Réponse**

```c
#include <stdlib.h>
#include <stdio.h>
#include "binary_trees.h"

/**
 * binary_tree_inorder - traverses a binary tree in-order
 * @tree: pointer to the root node of the tree
 * @func: function to call on each node's value
 *
 * Description: Visits nodes in in-order (left → node → right)
 * and applies func to each node. Does nothing if tree or func is NULL.
 */
void binary_tree_inorder(const binary_tree_t *tree, void (*func)(int))
{
	if (tree == NULL || func == NULL)
		return;

	binary_tree_inorder(tree->left, func);
	func(tree->n);
	binary_tree_inorder(tree->right, func);
}
```

</details>

<details>
<summary><strong>🧩 8. Post-order traversal</strong></summary>

**📝 Énoncé**

Write a function that goes through a binary tree using post-order traversal
**Prototype:** void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int));
Where tree is a pointer to the root node of the tree to traverse
And func is a pointer to a function to call for each node. The value in the node must be passed as a parameter to this function.
If tree or func is NULL, do nothing

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_postorder - traverses a binary tree in post-order
 * @tree: pointer to the root node of the tree
 * @func: function to call on each node's value
 *
 * Description: Visits nodes in post-order (left → right → node)
 * and applies func to each node. Does nothing if tree or func is NULL.
 */
void binary_tree_postorder(const binary_tree_t *tree, void (*func)(int))
{
	if (tree == NULL || func == NULL)
		return;

	binary_tree_postorder(tree->left, func);
	binary_tree_postorder(tree->right, func);
	func(tree->n);
}
```

</details>

<details>
<summary><strong>🧩 9. Height</strong></summary>

**📝 Énoncé**

Write a function that measures the height of a binary tree
**Prototype:** size_t binary_tree_height(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the height.
If tree is NULL, your function must return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_height - measures the height of a binary tree
 * @tree: pointer to the root node of the tree
 *
 * Return: height of the tree, or 0 if tree is NULL
 */
size_t binary_tree_height(const binary_tree_t *tree)
{
	size_t left_height, right_height;

	if (tree == NULL)
		return (0);

	/* Si c'est une feuille, height = 0 */
	if (tree->left == NULL && tree->right == NULL)
		return (0);

	left_height = binary_tree_height(tree->left);
	right_height = binary_tree_height(tree->right);

	if (left_height > right_height)
		return (left_height + 1);

	return (right_height + 1);
}
```

</details>

<details>
<summary><strong>🧩 10. Depth</strong></summary>

**📝 Énoncé**

Write a function that measures the depth of a node in a binary tree
**Prototype:** size_t binary_tree_depth(const binary_tree_t *tree);
Where tree is a pointer to the node to measure the depth
If tree is NULL, your function must return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
* binary_tree_depth - measures the depth of a node in a binary tree
* @tree: pointer to the node to measure
*
* Return: depth of the node, or 0 if tree is NULL
*/
size_t binary_tree_depth(const binary_tree_t *tree)
{
	size_t depth;

	if (tree == NULL)
		return (0);

	depth = 0;
	while (tree->parent != NULL)
	{
		tree = tree->parent;
		depth++;
	}

	return (depth);
}
```

</details>

<details>
<summary><strong>🧩 11. Size</strong></summary>

**📝 Énoncé**

Write a function that measures the size of a binary tree
**Prototype:** size_t binary_tree_size(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the size
If tree is NULL, the function must return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_size - measures the size of a binary tree
 * @tree: pointer to the root node of the tree
 *
 * Return: total number of nodes in the tree, or 0 if tree is NULL
 */
size_t binary_tree_size(const binary_tree_t *tree)
{
	size_t left_size;
	size_t right_size;

	if (tree == NULL)
		return (0);

	left_size = binary_tree_size(tree->left);
	right_size = binary_tree_size(tree->right);

	return (1 + left_size + right_size);
}
```

</details>

<details>
<summary><strong>🧩 12. Leaves</strong></summary>

**📝 Énoncé**

Write a function that counts the leaves in a binary tree
**Prototype:** size_t binary_tree_leaves(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of leaves
If tree is NULL, the function must return 0
A NULL pointer is not a leaf

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_leaves - counts the leaves in a binary tree
 * @tree: pointer to the root node of the tree
 *
 * Description: Counts the number of leaf nodes in a binary tree.
 * A leaf is a node with no children.
 *
 * Return: number of leaves in the tree, or 0 if tree is NULL
 */

size_t binary_tree_leaves(const binary_tree_t *tree)
{
	size_t left_leaves;
	size_t right_leaves;

	if (tree == NULL)
		return (0);

	if (tree->left == NULL && tree->right == NULL)
		return (1);

	left_leaves = binary_tree_leaves(tree->left);
	right_leaves = binary_tree_leaves(tree->right);

	return (left_leaves + right_leaves);
}
```

</details>

<details>
<summary><strong>🧩 13. Nodes</strong></summary>

**📝 Énoncé**

Write a function that counts the nodes with at least 1 child in a binary tree
**Prototype:** size_t binary_tree_nodes(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to count the number of nodes
If tree is NULL, the function must return 0
A NULL pointer is not a node

**✅ Réponse**

```c
#include "binary_trees.h"

/**
* binary_tree_nodes - counts nodes with at least one child
* @tree: pointer to the root node of the tree
*
* Return: number of nodes with at least one child, 0 if tree is NULL
*/
size_t binary_tree_nodes(const binary_tree_t *tree)
{
	size_t count = 0;

	if (tree == NULL)
		return (0);

	if (tree->left != NULL || tree->right != NULL)
		count = 1;

	count += binary_tree_nodes(tree->left);
	count += binary_tree_nodes(tree->right);

	return (count);
}
```

</details>

<details>
<summary><strong>🧩 14. Balance factor</strong></summary>

**📝 Énoncé**

Write a function that measures the balance factor of a binary tree
**Prototype:** int binary_tree_balance(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to measure the balance factor
If tree is NULL, return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_height - Measures the height of a binary tree
 * @tree: Pointer to the root node of the tree
 *
 * Description: The height is defined as the number of edges on the
 * longest path from the root node to a leaf. An empty tree has a
 * height of 0.
 *
 * Return: The height of the tree, or 0 if @tree is NULL
 */
size_t binary_tree_height(const binary_tree_t *tree)
{
	size_t left_height, right_height;

	if (tree == NULL)
		return (0);

	left_height = binary_tree_height(tree->left);
	right_height = binary_tree_height(tree->right);

	if (left_height > right_height)
		return (left_height + 1);
	else
		return (right_height + 1);
}

/**
 * binary_tree_balance - measures the balance factor of a binary tree
 * @tree: pointer to the root node of the tree
 *
 * Return: The balance of the binary tree, or 0 if tree is NULL
 */
int binary_tree_balance(const binary_tree_t *tree)
{
	int left_height, right_height;

	if (tree == NULL)
		return (0);

	left_height = binary_tree_height(tree->left);
	right_height = binary_tree_height(tree->right);

	return (left_height - right_height);
}
```

</details>

<details>
<summary><strong>🧩 15. Is full</strong></summary>

**📝 Énoncé**

Write a function that checks if a binary tree is full
**Prototype:** int binary_tree_is_full(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_is_full - checks if a binary tree is full
 * @tree: pointer to the root node of the tree
 *
 * Return: 1 if the tree is full, 0 otherwise
 */
int binary_tree_is_full(const binary_tree_t *tree)
{
	int left_tree, right_tree;

	if (tree == NULL)
		return (0);

	if (tree->left == NULL && tree->right == NULL)
		return (1);

	if (tree->left != NULL && tree->right != NULL)
	{
		left_tree = binary_tree_is_full(tree->left);
		right_tree = binary_tree_is_full(tree->right);
		if (left_tree && right_tree)
			return (1);
		else
			return (0);
	}
	return (0);
}
```

</details>

<details>
<summary><strong>🧩 16. Is perfect</strong></summary>

**📝 Énoncé**

Write a function that checks if a binary tree is perfect
**Prototype:** int binary_tree_is_perfect(const binary_tree_t *tree);
Where tree is a pointer to the root node of the tree to check
If tree is NULL, your function must return 0

**✅ Réponse**

```c
#include "binary_trees.h"

/**
* _tree_depth - measures the depth of a node in a binary tree
* @tree: pointer to the node to measure
*
* Description: Returns the depth of the node in the tree. The depth
* is defined as the number of edges from the node to the root node.
*
* Return: The depth of the binary tree
*/
size_t _tree_depth(const binary_tree_t *tree)
{
	size_t depth = 0;
	const binary_tree_t *node = tree;

	while (node->parent != NULL)
	{
		node = node->parent;
		depth++;
	}
	return (depth);
}

/**
* binary_tree_is_full - checks if a binary tree is full
* @tree: pointer to the root node of the tree
*
* Return: 1 if the tree is full, 0 otherwise
*/
int binary_tree_is_full(const binary_tree_t *tree)
{
	int left_tree, right_tree;

	if (tree == NULL)
		return (0);

	if (tree->left == NULL && tree->right == NULL)
		return (1);

	if (tree->left != NULL && tree->right != NULL)
	{
		left_tree = binary_tree_is_full(tree->left);
		right_tree = binary_tree_is_full(tree->right);
		if (left_tree && right_tree)
			return (1);
		else
			return (0);
	}
	return (0);
}

/**
* check_all_leaves_depth - checks if all leaves in a binary tree
*                          are at the same depth
* @node: pointer to the root of the subtree
* @depth_ref: reference depth to compare the leaves against
*
* Return: 1 if all leaves are at the same depth, 0 otherwise
*/
int check_all_leaves_depth(const binary_tree_t *node, size_t depth_ref)
{
	int left, right;

	if (node == NULL)
		return (1);

	if (node->left == NULL && node->right == NULL)
		return (_tree_depth(node) == depth_ref);

	left = check_all_leaves_depth(node->left, depth_ref);
	right = check_all_leaves_depth(node->right, depth_ref);

	return (left && right);
}
/**
* binary_tree_is_perfect - checks if a binary tree is perfect
* @tree: pointer to the root node of the tree
*
* Return: 1 if the tree is perfect, 0 otherwise
*/
int binary_tree_is_perfect(const binary_tree_t *tree)
{
	const binary_tree_t *node;
	size_t depth_ref;

	if (tree == NULL)
		return (0);

	if (!binary_tree_is_full(tree))
		return (0);

	node = tree;
	while (node->left != NULL)
		node = node->left;

	depth_ref = _tree_depth(node);

	return (check_all_leaves_depth(tree, depth_ref));
}
```

</details>

<details>
<summary><strong>🧩 17. Sibling</strong></summary>

**📝 Énoncé**

Write a function that finds the sibling of a node
**Prototype:** binary_tree_t *binary_tree_sibling(binary_tree_t *node);
Where node is a pointer to the node to find the sibling
Your function must return a pointer to the sibling node
If node is NULL or the parent is NULL, return NULL
If node has no sibling, return NULL

**✅ Réponse**

```c
#include "binary_trees.h"

/**
 * binary_tree_sibling - finds the sibling of a node in a binary tree
 * @node: pointer to the node to find the sibling of
 *
 * Return: pointer to the sibling node, or NULL if node is NULL,
 *         if parent is NULL, or if there is no sibling
 */
binary_tree_t *binary_tree_sibling(binary_tree_t *node)
{
	if (node == NULL || node->parent == NULL)
		return (NULL);

	if (node->parent->left == node)
		return (node->parent->right);

	return (node->parent->left);
}
```

</details>

<details>
<summary><strong>🧩 18. Uncle</strong></summary>

**📝 Énoncé**

Write a function that finds the uncle of a node
**Prototype:** binary_tree_t *binary_tree_uncle(binary_tree_t *node);
Where node is a pointer to the node to find the uncle
Your function must return a pointer to the uncle node
If node is NULL, return NULL
If node has no uncle, return NULL

**✅ Réponse**

```c
#include "binary_trees.h"

/**
* binary_tree_uncle - Finds the uncle of a node in a binary tree
* @node: Pointer to the node to find the uncle of
*
* Return: Pointer to the uncle node
*         If node is NULL or has no uncle, returns NULL
*/
binary_tree_t *binary_tree_uncle(binary_tree_t *node)
{
	binary_tree_t *parent;
	binary_tree_t *grandparent;
	binary_tree_t *uncle;

	if (node == NULL)
		return (NULL);

	parent = node->parent;
	if (parent == NULL)
		return (NULL);

	grandparent = parent->parent;
	if (grandparent == NULL)
		return (NULL);

	if (grandparent->left == parent)
		uncle = grandparent->right;
	else
		uncle = grandparent->left;

	return (uncle);
}
```

</details>

- --

<a id="c-binary-trees-antoine"></a>

## 💻 C - BINARY TREES ANTOINE

### 📌 General

What is a binary tree
What is the difference between a binary tree and a Binary Search Tree
What is the possible gain in terms of time complexity compared to linked lists
What are the depth, the height, the size of a binary tree
What are the different traversal methods to go through a binary tree
What is a complete, a full, a perfect, a balanced binary tree

### ✅ Requirements

Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
You are allowed to use the standard library
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions should be included in your header file called binary_trees.h
Don’t forget to push your header file
All your header files should be include guarded

GitHub
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

### 🔎 More Info

Data structures

Please use the following data structures and types for binary trees. Don’t forget to include them in your header file.

Basic Binary Tree
/**
 * struct binary_tree_s - Binary tree node
 *
 * @n: Integer stored in the node
 * @parent: Pointer to the parent node
 * @left: Pointer to the left child node
 * @right: Pointer to the right child node
 */
struct binary_tree_s
{
    int n;
    struct binary_tree_s *parent;
    struct binary_tree_s *left;
    struct binary_tree_s *right;
};

typedef struct binary_tree_s binary_tree_t;

Binary Search Tree

typedef struct binary_tree_s bst_t;

AVL Tree

typedef struct binary_tree_s avl_t;

Max Binary Heap

typedef struct binary_tree_s heap_t;

Note: For tasks 0 to 23 (included), you have to deal with simple binary trees. They are not BSTs, thus they don’t follow any kind of rule.

Print function
To match the examples in the tasks, you are given this function

This function is used only for visualization purposes. You don’t have to push it to your repo. It may not be used during the correction

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include "binary_trees.h"

/* Original code from http://stackoverflow.com/a/13755911/5184480 */

/**
 * print_t - Stores recursively each level in an array of strings
 *
 * @tree: Pointer to the node to print
 * @offset: Offset to print
 * @depth: Depth of the node
 * @s: Buffer
 *
 * Return: length of printed tree after process
 */
static int print_t(const binary_tree_t *tree, int offset, int depth, char **s)
{
	char b[6];
	int width, left, right, is_left, i;

	if (!tree)
		return (0);
	is_left = (tree->parent && tree->parent->left == tree);
	width = sprintf(b, "(%03d)", tree->n);
	left = print_t(tree->left, offset, depth + 1, s);
	right = print_t(tree->right, offset + left + width, depth + 1, s);
	for (i = 0; i < width; i++)
		s[depth][offset + left + i] = b[i];
	if (depth && is_left)
	{
		for (i = 0; i < width + right; i++)
			s[depth - 1][offset + left + width / 2 + i] = '-';
		s[depth - 1][offset + left + width / 2] = '.';
	}
	else if (depth && !is_left)
	{
		for (i = 0; i < left + width; i++)
			s[depth - 1][offset - width / 2 + i] = '-';
		s[depth - 1][offset + left + width / 2] = '.';
	}
	return (left + width + right);
}

/**
 * _height - Measures the height of a binary tree
 *
 * @tree: Pointer to the node to measures the height
 *
 * Return: The height of the tree starting at @node
 */
static size_t _height(const binary_tree_t *tree)
{
	size_t height_l;
	size_t height_r;

	height_l = tree->left ? 1 + _height(tree->left) : 0;
	height_r = tree->right ? 1 + _height(tree->right) : 0;
	return (height_l > height_r ? height_l : height_r);
}

/**
 * binary_tree_print - Prints a binary tree
 *
 * @tree: Pointer to the root node of the tree to print
 */
void binary_tree_print(const binary_tree_t *tree)
{
	char **s;
	size_t height, i, j;

	if (!tree)
		return;
	height = _height(tree);
	s = malloc(sizeof(*s) * (height + 1));
	if (!s)
		return;
	for (i = 0; i < height + 1; i++)
	{
		s[i] = malloc(sizeof(**s) * 255);
		if (!s[i])
			return;
		memset(s[i], 32, 255);
	}
	print_t(tree, 0, 0, s);
	for (i = 0; i < height + 1; i++)
	{
		for (j = 254; j > 1; --j)
		{
			if (s[i][j] != ' ')
				break;
			s[i][j] = '\0';
		}
		printf("%s\n", s[i]);
		free(s[i]);
	}
	free(s);
}

#ifndef _BINARY_TREES_H_
#define _BINARY_TREES_H_

#include <stddef.h>

/**
 * struct binary_tree_s - Binary tree node
 *
 * @n: Integer stored in the node
 * @parent: Pointer to the parent node
 * @left: Pointer to the left child node
 * @right: Pointer to the right child node
 */
typedef struct binary_tree_s
{
	int n;
	struct binary_tree_s *parent;
	struct binary_tree_s *left;
	struct binary_tree_s *right;
} binary_tree_t;

void binary_tree_print(const binary_tree_t *);

#endif /* _BINARY_TREES_H_ */

### 🧩 Tâches

<details>
<summary><strong>🧩 0. New node</strong></summary>

**📝 Énoncé**

But : Créer a binary tree node.

Write a function that creates a binary tree node

**Prototype:** binary_tree_t *binary_tree_node(binary_tree_t *parent, int value);
Where parent is a pointer to the parent node of the node to create
And value is the value to put in the new node
When created, a node does not have any child
Your function must return a pointer to the new node, or NULL on failure

**✅ Réponse**

```c
General
At least four different sorting algorithms
What is the Big O notation, and how to evaluate the time complexity of an algorithm
How to select the best sorting algorithm for a given input
What is a stable sorting algorithm

Requirements
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
You are not allowed to use global variables
No more than 5 functions per file
Unless specified otherwise, you are not allowed to use the standard library. Any use of functions like printf, puts, … is totally forbidden.
In the following examples, the main.c files are shown as examples. You can use them to test your functions, but you don’t have to push them to your repo (if you do we won’t take them into account). We will use our own main.c files at compilation. Our main.c files might be different from the one shown in the examples
The prototypes of all your functions should be included in your header file called sort.h
Don’t forget to push your header file
All your header files should be include guarded
A list/array does not need to be sorted if its size is less than 2.

GitHub
There should be one project repository per group. If you clone/fork/whatever a project repository with the same name before the second deadline, you risk a 0% score.

Data Structure and Functions
For this project you are given the following print_array, and print_list functions:
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
Our files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction.
Please declare the prototype of the functions print_array and print_list in your sort.h header file
Please use the following data structure for doubly linked list:

/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;

Please, note this format is used for Quiz and Task questions.
O(1)
O(n)
O(n!)
n square -> O(n^2)
log(n) -> O(log(n))
n * log(n) -> O(nlog(n))
n + k -> O(n+k)
…

Please use the “short” notation (don’t use constants). Example: O(nk) or O(wn) should be written O(n). If an answer is required within a file, all your answers files must have a newline at the end.

Tests

Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org
```

</details>

<details>
<summary><strong>🧩 0. Bubble sort</strong></summary>

**📝 Énoncé**

Write a function that sorts an array of integers in ascending order using the Bubble sort algorithm
**Prototype:** void bubble_sort(int *array, size_t size);
You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 0-O, the big O notations of the time complexity of the Bubble sort algorithm, with 1 notation per line:
in the best case
in the average case
in the worst case

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
 * bubble_sort - Sort an array of integers in ascending order
 * @array: Pointer to the array
 * @size: Number of elements
 *
 * Return: void
 */
void bubble_sort(int *array, size_t size)
{
	size_t i, j;
	int tmp;

	for (i = 0; i < size - 1; i++)
	{
		for (j = 0; j < size - i - 1; j++)
		{
			if (array[j] > array[j + 1])
			{
				tmp = array[j];
				array[j] = array[j + 1];
				array[j + 1] = tmp;

				print_array(array, size);
			}
		}
	}
}

O(n)
O(n^2)
O(n^2)
```

</details>

<details>
<summary><strong>🧩 1. Insertion sort</strong></summary>

**📝 Énoncé**

Write a function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm
**Prototype:** void insertion_sort_list(listint_t **list);
You are not allowed to modify the integer n of a node. You have to swap the nodes themselves.
You’re expected to print the list after each time you swap two elements (See example below)
Write in the file 1-O, the big O notations of the time complexity of the Insertion sort algorithm, with 1 notation per line:
in the best case
in the average case
in the worst case

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
 * insertion_sort_list - sorts a doubly linked list of integers
 *                        in ascending order using the Insertion Sort
 *
 * @list: pointer to the head of the list
 *
 * Description: Sorts a doubly linked list of integers in ascending order.
 *              Nodes must be swapped; the integer values inside nodes
 *              cannot be modified. Prints the list after each swap.
 *
 * Return: void
 */
void insertion_sort_list(listint_t **list)
{
	listint_t *head;
	listint_t *current;
	listint_t *tmp;
	listint_t *prev_node;
	listint_t *next_node;

	if (list == NULL || *list == NULL || (*list)->next == NULL)
		return;

	head = *list;
	current = head->next;

	while (current != NULL)
	{
		tmp = current->next;
		prev_node = current->prev;

		while (prev_node != NULL && current->n < prev_node->n)
		{
			next_node = current->next;

			current->prev = prev_node->prev;
			current->next = prev_node;
			prev_node->prev = current;
			prev_node->next = next_node;

			if (next_node != NULL)
				next_node->prev = prev_node;

			if (current->prev != NULL)
				current->prev->next = current;
			else
				*list = current;

			prev_node = current->prev;
			print_list(*list);
		}
		current = tmp;
	}
}

O(n)
O(n^2)
O(n^2)
```

</details>

<details>
<summary><strong>🧩 2. Selection sort</strong></summary>

**📝 Énoncé**

Write a function that sorts an array of integers in ascending order using the Selection sort algorithm
**Prototype:** void selection_sort(int *array, size_t size);
You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 2-O, the big O notations of the time complexity of the Selection sort algorithm, with 1 notation per line:
in the best case
in the average case
in the worst case

**✅ Réponse**

```c
#include <stdio.h>
#include <stdlib.h>
#include "sort.h"

/**
* selection_sort - sorts an array of integers in ascending order
*                   using the Selection sort algorithm
* @array: pointer to the array to sort
* @size: size of the array
*
* Return: void
*/
void selection_sort(int *array, size_t size)
{
	size_t i, j, min_index = 0;
	int tmp;

	if (!array || size < 2)
		return;

	for (i = 0; i < size - 1; i++)
	{
		min_index = i;
		for (j = i + 1; j < size; j++)
			if (array[j] < array[min_index])
				min_index = j;
		if (min_index != i)
		{
			tmp = array[i];
			array[i] = array[min_index];
			array[min_index] = tmp;

			print_array(array, size);
		}
	}
}

O(n^2)
O(n^2)
O(n^2)
```

</details>

<details>
<summary><strong>🧩 3. Quick sort</strong></summary>

**📝 Énoncé**

Write a function that sorts an array of integers in ascending order using the Quick sort algorithm
**Prototype:** void quick_sort(int *array, size_t size);
You must implement the Lomuto partition scheme.
The pivot should always be the last element of the partition being sorted.
You’re expected to print the array after each time you swap two elements (See example below)
Write in the file 3-O, the big O notations of the time complexity of the Quick sort algorithm, with 1 notation per line:
in the best case
in the average case
in the worst case

**✅ Réponse**

```c
#include "sort.h"
void recurs(int array[], int low, int high, size_t size);
int partition(int array[], int low, int high, size_t size);

/**
 * quick_sort - Sorts an array of integers in ascending order using Quick sort.
 * @array: Array of integers to sort.
 * @size: Size of the array.
 *
 * Description: Uses the Lomuto partition scheme.
 *              The pivot is always the last element.
 *              Prints the array after each swap.
 */
void quick_sort(int *array, size_t size)
{
	if (!array || size < 2)
		return;

	recurs(array, 0, size - 1, size);
}

/**
 * partition - Partitions the array for Quick sort.
 * @array: Array of integers to partition.
 * @low: Starting index of the partition.
 * @high: Ending index of the partition.
 * @size: Size of the array.
 *
 * Return: The index of the pivot after partitioning.
 */
int partition(int array[], int low, int high, size_t size)
{
	int pivot = array[high];
	int temp, j;
	int i = low;

	for (j = low; j < high; j++)
	{
		if (array[j] <= pivot)
		{
			if (i < j)
			{
				temp = array[i];
				array[i] = array[j];
				array[j] = temp;
				print_array(array, size);
			}
			i++;
		}
	}
	if (i != high)
	{
		temp = array[i];
		array[i] = array[high];
		array[high] = temp;
		print_array(array, size);
	}
	return (i);
}

/**
 * recurs - Recursively applies Quick sort to subarrays.
 * @array: Array of integers to sort.
 * @low: Starting index of the subarray.
 * @high: Ending index of the subarray.
 * @size: Size of the array.
 */
void recurs(int array[], int low, int high, size_t size)
{
	int index_pivot;

	if (low < high)
	{
		index_pivot = partition(array, low, high, size);
		recurs(array, low, index_pivot - 1, size);
		recurs(array, index_pivot + 1, high, size);
	}
}

O(nlog(n))
O(nlog(n))
O(n^2)
```

</details>

- --
/*
