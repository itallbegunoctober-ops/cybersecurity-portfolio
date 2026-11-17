# Lab 09 — Import and Parse a Text File

**Provider:** Google Skills training activity  
**Category:** Python / Log and File Handling  
**Status:** Completed training exercise (dated October 29, 2026)

## Objective
Use Python file operations to read and parse login records, append a new record and create/read an IP allow-list file.

## Tools and concepts
Python, `open()`, context managers (`with`), file modes `r`, `a`, `w`, `.read()`, `.split()` and `.write()`.

## Files used
- `login.txt` — login-related text records.
- `allow_list.txt` — IP allow-list data created during the exercise.

## Work performed
- Opened `login.txt` in read mode using a context manager.
- Read the file contents and split text into records/fields for processing.
- Opened the login file in append mode and wrote an additional record (the lab notes refer to a `jrafael...` record).
- Created/populated `allow_list.txt` in write mode.
- Reopened and read the allow-list file to inspect its contents.
- Observed that the appended record did not automatically begin on a new line when the original file lacked a trailing newline.

## Example command patterns

```python
with open("login.txt", "r") as file:
    login_data = file.read()

records = login_data.split()
```

```python
with open("login.txt", "a") as file:
    file.write(new_record)
```

```python
with open("allow_list.txt", "w") as file:
    file.write(allow_list_data)

with open("allow_list.txt", "r") as file:
    allow_list = file.read()
```

The snippets show the file modes and operations used. Consult the original exercise for the exact record format and parsing logic.

## Command explanations
- `with open(...)`: opens a file and ensures it is closed when the block ends.
- `"r"`: opens a file for reading.
- `"a"`: opens a file for appending at the end.
- `"w"`: opens a file for writing, replacing existing contents.
- `.read()`: reads file contents.
- `.split()`: splits a string into a list using whitespace by default.
- `.write()`: writes a string to the file.

## Skills demonstrated
Python file handling, context managers, reading and parsing text, appending records, creating files and working with allow-list data.

## Evidence to add
Add a sanitized code screenshot and output showing file reading, parsing, appending and allow-list creation. Remove real personal data, usernames and IP information if not intended for public release.

## Scope
A guided training exercise. Do not upload the original login data if it contains personal or sensitive information.
