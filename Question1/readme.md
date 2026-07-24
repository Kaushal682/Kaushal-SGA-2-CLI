# Question 1 - Linux Shell Scripting

## Objective

This shell script performs the following tasks:

- Identifies duplicate student submissions.
- Creates a backup of unique submissions.
- Generates a report containing:
  - Number of files processed
  - Number of duplicate files
  - Number of backed-up files
- Stores all error messages separately in an error log.

---

## Files Included

### submissions/

Contains sample student submission files.

- student1.txt
- student2.txt
- student3.txt (Duplicate of student1.txt)
- student4.txt

### backup/

Stores only unique files after script execution.

### process_submissions.sh

Main shell script.

### report.txt

Contains the summary report.

### errors.log

Contains all runtime errors.

---

## Linux Commands Used

| Command | Purpose |
|---------|---------|
| mkdir | Creates directories |
| cp | Copies unique files |
| md5sum | Generates file hash |
| awk | Extracts MD5 hash |
| chmod | Gives execute permission |
| cat | Displays file contents |
| ls | Lists files |

---

## Redirection Operators

- > Overwrites a file
- >> Appends to a file
- 2>> Appends error messages

---

## File Handling Technique

The script reads each file from the submissions folder and calculates its MD5 hash. If the hash already exists, the file is treated as a duplicate. Otherwise, the file is copied to the backup folder. Finally, a report and error log are generated.

---

## Output

Files Processed : 4

Duplicate Files : 1

Files Backed Up : 3
