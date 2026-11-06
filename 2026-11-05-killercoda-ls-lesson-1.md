Killercoda Linux Fundamentals -- Listing files with ls

Date: 2026-11-05
platform: killercoda (browser-based Linux environment)

Goal: Work through the ls command properly on a live machine --not just listing names, but formats, hidden files, and sorting by time.

What I did:
   Started with plain ls and its color output:
   --color=no, --color=yes, --color=auto.
   
   ls -l for the long listing format, and the argument conventions: one dash + one letter (-l) vs. two dashes + a full word (--color).
  •  ls -a to reveal hidden files, including . (current directory) and .. (parent directory); then ls . and ls .., and -A — almost all, everything except . and ... Combined arguments with ls -al.

  •  The detail flags: --author, -d (directories only), -i (inode numbers), -R (recursive through subdirectories), -r (reverse order).

  •  Sorting: ls sorts alphabetically by default. Learned the three timestamps — atime (last accessed), mtime (content last modified), ctime (metadata last changed) — and the date command.

  •  Sorting by time: ls -lt (newest modification first), ls -ltu (by access time), ls -ltc (by metadata change).

 •  Ran the timestamp experiment end to end: touch theNewestFile to create a file, echo "hello world!" > file-02 to change its content, chmod 444 file-01 to change its permissions — re-running ls -ltu and ls -ltc after each step to watch which timestamp each action actually moved.

 What I got wrong: Missing a certain thing for some of the commands 

 What I learned:

•  -a and -A are not the same: -A hides only the . and .. entries.

•  The three timestamps track different events — reading a file, changing its content, and changing its permissions are three separate things, and ls can sort by each one.

•  Flags combine, so stacking them lets you ask the directory a precise question instead of eyeballing a plain list.

<img width="500" alt="IMG_0553" src="https://github.com/user-attachments/assets/68eb8cfe-01d4-4a4b-9328-91591a30c10c" />

