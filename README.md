# organize
A bash script to organize markdown todos with todo.txt using gsed (gnu-sed) on MacOS

I keep notes on all my projects in separate markdown files in Atom.  The conventional marker for a "todo" item in markdown is `- [ ]`.  In a subdirectory of my project files directory, I maintain todo.txt files.  Mostly as an exercise in learning how to `grep` and `sed`, I wrote a script to scrape all occurrences of the `- [ ]` token in *.md files in the same directory as the script, re-format them into todo.txt format (with an (I) priority for "Inbox"), and change all of the todos in the markdown files to `- [>]` to signify they have been promoted to the todo.txt file.  (This borrows, some what, from Bullet Journal notation.)

Once harvested into the todo.txt file, the tasks can be manipulated natively or with [todotxt/todo.txt-cli](https://github.com/todotxt/todo.txt-cli).

## Requirements:

- GNU `sed`.  This was written for MacOS, so I installed the GNU version with `brew install gnu-sed`.  If you're using Linux already, just change `gsed` to `sed` where the former appears in the script.  BSD `sed` is...unpredictable.

- The `organize` script should sit in the same directory with the .md files, and the traditional todo.txt files (done.txt, report.txt, todo.txt) should occupy a subdirectory named `todo`.  

That's it.  Happy organizing.

P.S. It took me two days to learn how to use `sed` even this much, and I was sufficiently proud of myself that I created my first repo commemorating the occasion.
