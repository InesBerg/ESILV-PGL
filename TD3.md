## Exercise 1: Configure Git

### 1. Check that Git is installed on your environment.
```
git --version
```
### 2. Configure your name and e-mail globally.
```
git config --global user.name "inesbergaut"
git config --global user.email "inesberg06@gmail.com"

```
### 3. Check that Git has correctly recorded these two pieces of information.
```
git config --list

```
## Exercise 2: Basic workflow with a single file

### 1. Create a git repository
```
git init

```
### 2. Check that git has correctly initiliazed a repository by displaying the files wihtin your current folder
### 3. Check the current git status
```
git status

```
### 4. Create a text file named “readme.md” whose content is “# Test repository”
```
echo "# Test repository" > readme.md
```
### 5. Check the current git status
### 6. Stage the file
### 7. Check the current git status
### 8. Commit the file
### 9. Check the current git status
```
git add readme.md
git commit -m "Add readme.md"
git log
```
## Exercise 3: Basic workflow with multiple files treated separately

### 1. Create two empty python files named “main.py” and “functions.py”
```
touch main.py functions.py
```
### 2. Check the current git status
### 3. Stage only the file “main.py”
### 4. Check the current git status
### 5. Commit the file with an appropriate message
### 6. Check the current git status
### 7. Now stage and commit the file “functions.py”
```
git add main.py
git commit -m "Add main.py"
git add functions.py
git commit -m "Add functions.py"

```
### 8. Check the current git status
### 9. Check the git logs
```
git status
git log
```
## Exercise 4: Basic workflow with multiple files treated all at once

### 1. Create three empty files named “requirements.txt”, “.gitignore” and “.private”
```
touch requirements.txt .gitignore .private
```
### 2. Check the current git status
### 3. Stage all the files at once
### 4. Check the current git status
### 5. Commit the current staged files
### 6. Check the current git status
### 7. Check the git logs where each log is displayed on a single line
```
git add .
git commit -m "Add requirements.txt, .gitignore, and .private"
git log --oneline

```
## Exercise 5: Private files

### 1. Emulate a temporary empty file by creating a file named “temp.ipynb”
```
touch temp.ipynb
```
### 2. Check the current git status
### 3. Add an instruction to .gitignore to prevent git from tracking this temp file
### 4. Check the current git status
### 5. Create other temporary files named “temp.aux” and “temp.log”
### 6. Check the current git status
### 7. Change your instruction in .gitignore to prevent git from tracking any file which name starts with “temp”
### 8. Check the current git status
```
echo "temp*" >> .gitignore
touch temp.aux temp.log
git status

```
### 9. Now let’s consider your personal notes will be added to the “.private” folder. Use the “exclude” git file to prevent git from tracking this “.private” folder
```
echo ".private" >> .git/info/exclude
```

## Exercise 6: Difference between versions

### 1. Add a online description of your repository in the “readme.md” file
```
echo "This is a test repository." >> readme.md
```
### 2. Stage your “readme.md” file
### 3. Display the changes in your root directory since the last commit (not just the current status)
### 4. Commit your change
### 5. Display the changes since the last commit
### 6. Display again the changes in your root directory since the last commit
### 7. Change some words in the description of the “readme.md”
### 8. Display the changes since the last commit
```
git add readme.md
git diff --cached
git commit -m "Update readme.md with a description"
git diff

```

## Exercise 7: Undo

### 1. Suppress all your files.
```
```
### 2. Use Git to restore your files.
```
```
### 3. Backup your Git repository elsewhere (pretending a copy exists on another colleague’s computer or on a remote server).
```
```
### 4. Suppress your root directory, create a new empty one and use your backup to restore everything.
```
```
### 5. Unstage your first file
```
```
### 6. Commit your two file changes directly, without staging them.
```
```
### 7. Check your commit log history. Do you see your new commit ?
```
```
### 8. Without affecting your Git repository, set your root directory state as of the snapshot of your first commit.
```
```
### 9. Check your commit log history. You do not see all commits, do you ? How can you see all of them ?
```
```
### 10. Return to the snapshot of your your last commit.
```
```
### 11. Undo your second commit by adding a new commit that reverts it.
```
```
### 12. Check the content of your root directory. Have your previous changes disappeard ?
```
```
### 13. Check your commit log history. Do you see your revert commit ?
```
```
### 14. Remove the last 2 commits from the history.
```
```
### 15. Check the content of your root directory. Have your previous changes disappeard ?
```
```
### 16. Check your commit log history. Have you lost the last 2 commits ?
```
```
## Exercise 8: Aliases

### 1. Create a “s” alias for the git status command.
```
git config --global alias.s status
```
### 2. Create a “co” alias for the git checkout command.
```
git config --global alias.co checkout
```
### 3. Create a “b” alias for the git branch command.
```
git config --global alias.b branch
```
### 4. Create a “ci” alias for the git commit command.
```
git config --global alias.ci commit
```
### 5. Create a “dog” alias for the git log –all –decorate –oneline –graph command.
```
git config --global alias.dog "log --all --decorate --oneline --graph"
```
### 6. Create a “dag” alias for the git log –all –decorate –graph command.
```
git config --global alias.dag "log --all --decorate --graph"
```
### 7. Create a “list” alias for the git diff-tree –no-commit-id –name-only -r command.
```
git config --global alias.list "diff-tree --no-commit-id --name-only -r"
```
### 8. Create a “unstage” alias for the git reset HEAD – command.
```
git config --global alias.unstage "reset HEAD --"
```
### 9. Create a “last” alias for the git log -1 HEAD command.
```
git config --global alias.last "log -
```

## Exercise 9: Hashing

### 1. Create a root directory.
```
mkdir root_directory

```
### 2. Create a text file inside whose content is “Hello World”.
```
echo "Hello World" > root_directory/text_file.txt

```
### 3. What is the size of the file ?
```
ls -lh root_directory/text_file.txt

```
### 4. Display the file content on the screen.
```
cat root_directory/text_file.txt

```
### 5. Compute the SHA-1 hash of the file content.
```
sha1sum root_directory/text_file.txt

```
### 6. What hash would Git compute on this file ?
```
git hash-object -w root_directory/text_file.txt

```
### 7. Create a second file whose content is what Git would really consider when saving your first file.
```
echo -e "blob 11\0Hello World" > root_directory/git_file.txt

```
### 8. Compute the SHA-1 hash of this second file and check it is equal to the Git hash of your first file.
```
sha1sum root_directory/git_file.txt

```

## Exercise 10: Compressing

### 1. Create an empty Git repository in your root directory (if you have accidentally already created a Git repository in your root directory, delete it before).
```
cd root_directory
git init

```
### 2. Check that Git is aware of your 2 files but does not track them yet.
```
git status

```
### 3. Check that no object is stored yet in the objects subdirectory of your Git repository.
```
ls .git/objects

```
### 4. Create a directory inside the objects subdirectory of your Git repository, whose name is the first two characters of the SHA-1 hash computed in the previous exercise.
```
mkdir -p .git/objects/ab

```
### 5. Install the QPDF free command-line program.
```
sudo apt-get install qpdf

```
### 6. Create a file inside the directory that you have just created, whose content is the deflate compression (level 1) of your second file and whose name is the last 38 characters of the SHA-1 hash computed in the previous exercise.
```
cd .git/objects/ab
qpdf --stream-data=uncompress ../../root_directory/git_file.txt - | zlib-flate -1 > last_38_chars_of_hash

```
### 7. Check that Git successfully considers this file as one of its inner object.
```
cd ../../..
git cat-file -t ab<last_38_chars_of_hash
git cat-file -p ab<last_38_chars_of_hash

```
### 8. Backup your Git repository and create a new one.
### 9. Stage your first file in Git and check that its name and content are identical to yours.
```
cd root_directory
git init
git add text_file.txt
git commit -m "Add text_file.txt"

```
### 10. Create another text file whose content is 100 lines of “Hello Mister i” (i varying from 1 to 100).
```
echo -e "Hello Mister {1..100}\n" > text_file_100_lines.txt
git add text_file_100_lines.txt
git commit -m "Add text_file_100_lines.txt"

```
### 11. Stage this new file in Git and check that the compression ratio on this second example is better than on the first one.
```
git cat-file -s HEAD:text_file.txt
git cat-file -s HEAD:text_file_100_lines.txt

```
