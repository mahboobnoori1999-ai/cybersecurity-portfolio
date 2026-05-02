# Commands Used

## Display Detailed File Permissions

```bash
ls -la
```

Displays detailed permissions, ownership, and hidden files within the directory.

---

## Remove Write Permission for Others

```bash
chmod o-w project_k.txt
```

Removes write access for other users from the file `project_k.txt`.

---

## Remove Read Permission for Group

```bash
chmod g-r project_m.txt
```

Removes read access for the group from the file `project_m.txt`.

---

## Update Hidden File Permissions

```bash
chmod u-w,g-w,g+r .project_x.txt
```

Modifies permissions for the hidden file:
- removes write permission for user
- removes write permission for group
- adds read permission for group

---

## Remove Execute Permission from Group

```bash
chmod g-x drafts
```

Removes execute permission for the group from the `drafts` directory to restrict unauthorized access.

---

## Verify Updated Permissions

```bash
ls -la
```

Verifies that the permission changes were successfully applied.
