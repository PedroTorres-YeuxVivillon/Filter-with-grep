# 🔍 Linux Command Line: Filtering Files and Text with `grep`

This repository documents my hands-on lab using the `grep` command and piping. As a beginner in cybersecurity and data analysis, learning to efficiently search through files and text is a critical skill for log analysis and data retrieval.

## 📖 Project Overview

This lab simulated a common task for IT and security professionals: sifting through log files and user reports to find specific information. I used the `grep` command to search inside files and to filter the list of files themselves.

### **What I Learned & Practiced**

*   Using `grep` to search for specific text patterns *within* a file.
*   Using the pipe operator (`|`) to send the output of one command (like `ls`) as input to `grep`.
*   Using `grep` to filter *file names* based on a specific string.

## 🛠️ Lab Tasks & My Solutions

### **Task 1: Find Error Messages in a Log File**

**Goal:** Navigate to a logs directory and find all error entries in the `server_logs.txt` file.

**My Solution:**
First, I changed to the correct directory, then used `grep` to find every line containing the word "error".
```bash
cd /home/analyst/logs
grep "error" server_logs.txt
```

**Result:** The command returned Six lines containing error messages. This skill is vital for quickly identifying problems in system logs.

### **Task 2: Find Files with Specific Names**

**Goal:** Navigate to a user reports directory and find files containing specific strings in their names.

**My Solution:**
I used the ls command to list all files and then piped (|) that list to grep to filter it.

**Part 1: Find files with "Q1" in the name**

```bash
cd /home/analyst/reports/users
ls | grep "Q1"
```
**Result:** This command listed Three files that contained "Q1" in their names.

**Part 2:** Find files with "access" in the name
```bash
ls | grep "access"
```
**Result:** This command listed Four files that contained "access" in their names.

### Task 3: Search for Specific User Information

**Goal:** Search inside user data files to find specific usernames and departmental information.

**My Solution:**

**Part 1: Find the username jhill**
I used grep to search inside the Q2_deleted_users.txt file for the exact string.

```bash
grep "jhill" Q2_deleted_users.txt
```

**Result:** Yes, the username jhill was found in the Q2_deleted_users.txt file.

**Part 2:** Count users added to the Human Resources department
I searched the Q4_added_users.txt file for lines containing the department name.

```bash
grep "Human Resources" Q4_added_users.txt
```

**Result:** The command returned **Three** users who were added to the Human Resources department.

### ✅ Conclusion
This lab was an excellent introduction to the power of grep and piping on the Linux command line. I successfully learned how to:

- Quickly scan log files for critical entries like errors.

- Filter long lists of files to find the ones I need based on their names.

- Extract specific pieces of information, like usernames and department data, from text files.
