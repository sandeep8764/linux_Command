
# Linux File Management Practice

A hands-on Linux command-line project to practice creating, copying, moving, renaming, and deleting files and directories.

This project is designed for beginners learning Linux commands through practical exercises.

---

## 📁 Project Folder Structure

```text
Linux_File_Management/
│
├── README.md
│
└── practice/
    │
    ├── source/
    │   └── notes.txt
    │
    ├── old_folder/
    │
    ├── destination/
    │
    └── archive/
        ├── delete-me.txt
        ├── empty-folder/
        └── delete-folder/
            ├── file1.txt
            └── file2.txt
```

---

## 🎯 Learning Objectives

By completing this practical, you will learn:

- Create files and directories.
- Copy individual files.
- Copy directories recursively.
- Move files between directories.
- Rename files and directories.
- Delete files safely.
- Remove empty directories.
- Delete directories containing files.
- Inspect directory structures.
- Understand Linux file-management commands.

---

## 1. Create the Workspace

```bash
# Create the main project directory
mkdir Linux_File_Management

# Enter the project directory
cd Linux_File_Management

# Create the practice folders
mkdir -p practice/source
mkdir -p practice/old_folder
mkdir -p practice/destination
mkdir -p practice/archive
```

---

## 2. Create Sample Files and Directories

```bash
# Create a sample file
touch practice/source/notes.txt

# Add content to the file
echo "Learning Linux File Management" > practice/source/notes.txt

# Create a file for deletion practice
touch practice/archive/delete-me.txt

# Create an empty directory
mkdir practice/archive/empty-folder

# Create a directory containing files
mkdir practice/archive/delete-folder

touch practice/archive/delete-folder/file1.txt
touch practice/archive/delete-folder/file2.txt
```

---

## 3. Copy Files Using cp

### Syntax

```bash
cp SOURCE DESTINATION
```

### Copy a file

```bash
cp practice/source/notes.txt practice/destination/notes-copy.txt
```

### Copy a directory recursively

```bash
cp -r practice/source practice/destination/source-copy
```

### Useful cp options

| Option | Description |
|---|---|
| `-r` | Copy directories recursively |
| `-i` | Ask before overwriting |
| `-v` | Display copied files |
| `-p` | Preserve file attributes |
| `-n` | Do not overwrite existing files |

---

## 4. Move Files Using mv

### Syntax

```bash
mv SOURCE DESTINATION
```

### Move a file

```bash
mv practice/source/notes.txt practice/destination/notes.txt
```

### Rename a directory

```bash
mv practice/old_folder practice/renamed_folder
```

### Useful mv options

| Option | Description |
|---|---|
| `-i` | Ask before overwriting |
| `-f` | Force overwrite without prompting |
| `-n` | Do not overwrite existing files |
| `-v` | Display moved files |

**Important:** The `mv` command is used for both moving and renaming files or directories.

---

## 5. Remove Files Using rm

### Remove a file

```bash
rm practice/archive/delete-me.txt
```

### Remove a directory recursively

```bash
rm -r practice/archive/delete-folder
```

### Remove with confirmation

```bash
rm -i practice/archive/delete-me.txt
```

### Useful rm options

| Option | Description |
|---|---|
| `-r` | Remove directories recursively |
| `-f` | Force removal |
| `-i` | Ask before each removal |
| `-I` | Ask for confirmation before certain bulk removals |
| `-v` | Display removed files |

**⚠️ Warning:** `rm` permanently deletes files in normal terminal usage. There is no standard undo command.

Always inspect the path before deleting.

---

## 6. Remove Empty Directories Using rmdir

### Syntax

```bash
rmdir DIRECTORY
```

### Example

```bash
rmdir practice/archive/empty-folder
```

**Important:** The `rmdir` command only removes empty directories.

If a directory contains files, use `rm -r` after checking its contents.

---

## 7. Verify Your Work

### Display the directory structure

```bash
find practice -print
```

### List all files and folders

```bash
ls -R practice
```

### Display detailed file information

```bash
ls -l practice/destination
```

### Check whether a file exists

```bash
test -f practice/destination/notes.txt && echo "File exists"
```

---

## 8. Expected Final Folder Structure

After completing all operations:

```text
practice/
│
├── source/
│
├── renamed_folder/
│
├── destination/
│   ├── notes-copy.txt
│   │
│   ├── notes.txt
│   │
│   └── source-copy/
│       └── notes.txt
│
└── archive/
```

---

## 9. Complete Command Summary

| Command | Purpose |
|---|---|
| `mkdir folder` | Create a directory |
| `mkdir -p a/b` | Create nested directories |
| `touch file.txt` | Create an empty file |
| `cp a.txt b.txt` | Copy a file |
| `cp -r a b` | Copy a directory |
| `mv a.txt b.txt` | Move or rename a file |
| `rm file.txt` | Remove a file |
| `rm -r folder` | Remove a directory recursively |
| `rmdir folder` | Remove an empty directory |
| `ls -l` | Display detailed listing |
| `ls -R` | Display recursive listing |
| `find . -print` | Display directory structure |
| `pwd` | Show current directory |
| `cd folder` | Change directory |

---

## 10. Practice Exercises

Try completing these tasks independently.

1. Create a directory named `backup` inside `destination`.
2. Create a file named `report.txt` inside `backup`.
3. Copy `report.txt` into `archive`.
4. Rename `report.txt` to `final-report.txt`.
5. Move `final-report.txt` into `source`.
6. Delete the copied `report.txt` from `archive`.
7. Create an empty directory named `temporary`.
8. Remove the `temporary` directory using `rmdir`.

---

## 11. Important Notes

- Use `cp` when you want to create a duplicate.
- Use `mv` when you want to move or rename.
- Use `rm` when you want to delete files.
- Use `rm -r` to delete directories containing files.
- Use `rmdir` only for empty directories.
- Use `ls` and `find` to inspect before making changes.
- Be careful with `rm -rf`; it can delete important data without confirmation.

---

## 12. Linux vs macOS

These commands are available on both Linux and macOS:

- `mkdir`
- `touch`
- `cp`
- `mv`
- `rm`
- `rmdir`
- `ls`
- `find`

Some advanced options differ because macOS uses BSD utilities while many Linux distributions use GNU utilities.

Check command documentation using:

```bash
man cp
man mv
man rm
man mkdir
man rmdir
```

---

## ✅ Project Completion

After completing this practical, you should understand the fundamentals of Linux file management.

**Topics Covered:**

- File Creation
- Directory Creation
- Copying Files
- Copying Directories
- Moving Files
- Renaming Directories
- File Removal
- Directory Removal
- Recursive Operations
- Directory Verification

**Practice Environment:** Linux Terminal / macOS Terminal

**Level:** Beginner

**Category:** Linux Command Line
