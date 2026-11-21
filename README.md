# Linux File Management Practice

Practice removing, renaming, copying, and moving files and folders in this workspace.

## Folder layout

- `practice/source/` — files used for copy and move exercises
- `practice/old_folder/` — folder to rename
- `practice/destination/` — folder for copied and moved files
- `practice/archive/` — folder for removal practice

## Safe commands

```bash
# Copy a file
cp practice/source/notes.txt practice/destination/notes-copy.txt

# Copy a folder recursively
cp -r practice/source practice/destination/source-copy

# Move a file
mv practice/source/notes.txt practice/destination/notes.txt

# Rename a folder
mv practice/old_folder practice/renamed_folder

# Remove a file
rm practice/archive/delete-me.txt

# Remove an empty folder
rmdir practice/archive/empty-folder

# Remove a folder and its contents
rm -rf practice/archive/delete-folder
```

> Always check with `ls` first. Use `rm -ri` or `rm -rfi` when you want confirmation before deleting.
