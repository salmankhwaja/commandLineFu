Use the following commands to know which folders are the culprit.

$ du -h ~ | sort -hr | head -20

Properly remove the TRASH of linux
$ rm -rf ~/.local/share/Trash/*
