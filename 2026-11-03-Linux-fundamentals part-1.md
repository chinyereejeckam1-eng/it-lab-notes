Linux Fundamentals Part 1- TryHackMe

Date: November 3, 2026 - Platfrom: TryHackMe (browser-based lab machine)

Goal: Refresh Linux command-line basics 

What I did: Navigated the filesystem with ls. cd, and pwd. read file contents with cat. searched a log file(access.log) with grep. Practiced operators: > overwrites a file, >> appends to it, && runs the next command only if the first one succeeded.

What i got wrong: I reached for a broaf sudo find across the whole filesystem when the file was in a known folder -- slower and heaver then needed.

What i learned: Navigating directly to where a file lives first, targeted navigation is faster and safer. And verify grep output matches what the task asked for before moving on.
