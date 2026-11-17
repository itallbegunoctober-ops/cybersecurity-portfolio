# Lab 08 — Develop an Algorithm

**Provider:** Google Skills training activity  
**Category:** Python / Access-Control Logic  
**Status:** Completed — dated October 28, 2026

## Objective
Develop Python logic that checks whether a user is authorized to access an assigned device by comparing approved usernames and device identifiers.

## Tools and concepts
Python lists, indexing, `.append()`, `.remove()`, membership operator `in`, `.index()`, `if` / `elif` / `else`, nested conditionals and a custom function.

## Work performed
- Worked with corresponding `approved_users` and `approved_devices` lists.
- Added and removed list entries with `.append()` and `.remove()`.
- Checked whether usernames and device IDs existed using `in`.
- Used `.index()` to locate a user's corresponding position in the approved-device list.
- Compared the requested device ID with the assigned device ID.
- Implemented a `login(username, device_id)` function using conditional and nested conditional logic.
- Reviewed the example where username `sgilmore` corresponded to device ID `4n482ts`.

## Example concepts

```python
if username in approved_users:
    user_index = approved_users.index(username)
    assigned_device = approved_devices[user_index]
```

The exercise used the corresponding index in the two lists to match a username with its assigned device. This is an instructional example; production access control should use secure identity systems and robust data structures rather than relying on parallel in-memory lists.

## Skills demonstrated
Python list operations, membership checks, indexing, conditional logic, function design and basic authorization decision logic.

## Evidence to add
Add a screenshot of the completed algorithm, test cases and output, with any sensitive identifiers removed.

## Scope
A guided coding exercise, not a production authentication or access-management system.
