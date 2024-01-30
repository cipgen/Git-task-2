## Creating a New Directory Under Git Version Control

## Git Challenge: Creating, Hashing, and Managing a File

1. Initialize a New Git Directory

Create a new directory named `git_challenge` and initialize it with Git:
```bash
mkdir git_challenge
cd git_challenge
git init
```
2. Create and Write to challenge.txt
In the git_challenge directory, create a file named challenge.txt and write a specific line of text to it:

echo "This is my Git challenge file." > challenge.txt
3. Hash the Contents of challenge.txt
Use the Git command to hash the contents of challenge.txt. Save the command output to a file named hash.txt:

git hash-object -w challenge.txt > hash.txt
4. Display File Contents Using the Hash
Use the Git system command to display the contents of challenge.txt using the hash saved in hash.txt, and append the command output to hash.txt:

git cat-file -p $(cat hash.txt) >> hash.txt

5. Add challenge.txt to the Git Index
Use the update-index command to add challenge.txt to the Git index:

git update-index --add challenge.txt
6. View Staged Contents of the Git Index
Use the git ls-files command to view the staged contents of the Git index. Append the result to hash.txt:

git ls-files --stage >> hash.txt


This markdown block provides a step-by-step guide for your Git challenge, from directory creation to advanced Git commands.
