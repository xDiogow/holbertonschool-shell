![image](https://github.com/user-attachments/assets/7ab29922-0716-4f3d-bba2-aa1a7ee33171)

# Permissions - Shell Scripting

This directory contains a series of shell scripts that manage file and directory permissions, ownership, and group settings. The exercises cover user switching, displaying user information, modifying file modes, and more. Each script is designed to help you master file permissions and ownership management in Unix-like systems.

---

## Table of Contents

1. [My name is Betty](#my-name-is-betty)
2. [Who am I](#who-am-i)
3. [Groups](#groups)
4. [New owner](#new-owner)
5. [Empty!](#empty)
6. [Execute](#execute)
7. [Multiple permissions](#multiple-permissions)
8. [Everybody!](#everybody)
9. [James Bond](#james-bond)
10. [John Doe](#john-doe)
11. [Look in the mirror](#look-in-the-mirror)
12. [Directories](#directories)
13. [More directories](#more-directories)
14. [Change group](#change-group)
15. [Owner and group](#owner-and-group)
16. [Symbolic links](#symbolic-links)
17. [If only](#if-only)

---

## My name is Betty
**File:** `0-iam_betty`

Create a script that switches the current user to the user **betty**.  
- **Constraint:** The command must consist of exactly 8 characters (plus a newline).  
- **Example:**
  ```sh
  $ tail -1 0-iam_betty | wc -c
  9
  ```

---

## Who am I
**File:** `1-who_am_i`

Write a script that prints the effective username of the current user.  
- **Example:**
  ```sh
  $ ./1-who_am_i
  julien
  ```

---

## Groups
**File:** `2-groups`

Write a script that prints all the groups the current user is a member of.  
- **Example:**
  ```sh
  $ ./2-groups
  julien adm cdrom sudo dip plugdev lpadmin sambashare
  ```

---

## New owner
**File:** `3-new_owner`

Write a script that changes the owner of the file **hello** to the user **betty**.  
- **Note:** Use `sudo` if necessary.
- **Example:**
  ```sh
  $ sudo ./3-new_owner
  $ ls -l
  -rw-rw-r-- 1 betty  julien  0 Sep 20 14:18 hello
  ```

---

## Empty!
**File:** `4-empty`

Write a script that creates an empty file called **hello** in the working directory.

---

## Execute
**File:** `5-execute`

Write a script that adds execute permission to the owner of the file **hello**.  
- **Example:**
  ```sh
  $ ./5-execute
  $ ls -l
  -rwxrw-r-- 1 julien julien 23 Sep 20 14:25 hello
  ```

---

## Multiple permissions
**File:** `6-multiple_permissions`

Write a script that adds execute permission to the owner and the group, and read permission to others for the file **hello**.  
- **Example:**
  ```sh
  $ ./6-multiple_permissions
  $ ls -l
  -rwxr-xr-- 1 julien julien 23 Sep 20 14:25 hello
  ```

---

## Everybody!
**File:** `7-everybody`

Write a script that adds execution permission to the owner, the group, and others for the file **hello**.  
- **Constraint:** Do not use commas.
- **Example:**
  ```sh
  $ ./7-everybody
  $ ls -l
  -rwxr-x--x 1 julien julien 23 Sep 20 14:25 hello
  ```

---

## James Bond
**File:** `8-James_Bond`

Write a script that sets the permissions of the file **hello** so that:  
- Owner: no permission  
- Group: no permission  
- Others: all permissions (i.e. `-------rwx`)
- **Example:**
  ```sh
  $ ./8-James_Bond
  $ ls -l
  -------rwx 1 julien julien 23 Sep 20 14:25 hello
  ```

---

## John Doe
**File:** `9-John_Doe`

Write a script that sets the mode of the file **hello** to:  
```
-rwxr-x-wx
```
- **Constraint:** Do not use commas.
- **Example:**
  ```sh
  $ ./9-John_Doe
  $ ls -l
  -rwxr-x-wx 1 julien julien 23 Sep 20 14:25 hello
  ```

---

## Look in the mirror
**File:** `10-mirror_permissions`

Write a script that sets the mode of the file **hello** to be the same as the mode of the file **olleh**.  
- **Note:** The mode of **olleh** may vary, so your script must copy its permissions.
- **Example:**
  ```sh
  $ ./10-mirror_permissions
  $ ls -l
  (hello should match olleh’s mode)
  ```

---

## Directories
**File:** `11-directories_permissions`

Write a script that adds execute permission to all subdirectories of the current directory for the owner, group, and others. Regular files should not be modified.
- **Example:**
  ```sh
  $ ./11-directories_permissions
  $ ls -l
  (Subdirectories now have execute permission for all users)
  ```

---

## More directories
**File:** `12-directory_permissions`

Create a script that creates a directory called **my_dir** in the working directory with permissions **751**.
- **Example:**
  ```sh
  $ ./12-directory_permissions
  $ ls -l
  drwxr-x--x 2 julien julien 4096 Sep 20 14:59 my_dir
  ```

---

## Change group
**File:** `13-change_group`

Write a script that changes the group owner of the file **hello** to **school**.
- **Example:**
  ```sh
  $ sudo ./13-change_group
  $ ls -l
  -rw-rw-r-- 1 julien school 23 Sep 20 14:25 hello
  ```

---

## Owner and group
**File:** `14-change_owner_and_group`

Write a script that changes the owner to **vincent** and the group owner to **staff** for all files and directories in the current working directory.
- **Example:**
  ```sh
  $ sudo ./14-change_owner_and_group
  $ ls -l
  (All items now show vincent as owner and staff as group)
  ```

---

## Symbolic links
**File:** `15-symbolic_link_permissions`

Write a script that changes the owner and the group owner of the symbolic link **_hello** (which points to **hello**) to **vincent** and **staff**, respectively.
- **Example:**
  ```sh
  $ sudo ./15-symbolic_link_permissions
  $ ls -l
  lrwxrwxrwx 1 vincent staff  _hello -> hello
  ```

---

## If only
**File:** `16-if_only`

Write a script that changes the owner of the file **hello** to **vincent** only if its current owner is **guillaume**.
- **Example:**
  ```sh
  $ sudo ./16-if_only
  $ ls -l
  (If hello was owned by guillaume, it now shows vincent as owner)
  ```

---

Happy scripting!
