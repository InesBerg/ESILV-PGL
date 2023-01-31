# TD1

Cours Python Git Linux

## Exercise 1

#### Q1: Go to the root directory
```
cd/
```
#### Q2: Display the content of the current (root) directory
```
ls
```
#### Q3: Check your current location
```
pwd
```
#### Q4: Try to create a directory named test
```
mkdir test
```
#### Q5: Go to the general home directory (should contain folders named after each user)
```

```
#### Q6: Go to your home directory
```
cd ~
```
#### Q7: Go back to the general home directory (located "just above")
```
cd -
```
#### Q8: Go again "just above", you should be back to the root directory
```
cd ..
```
#### Q9: Go directly to your home directory (named after you). It should be a very simple command, which take no name as parameter of the path
```
cd ~
```
#### Q10: Try to create a directory named test
```
mkdir test
```
#### Q11: Go into this new directory
```
cd test
```
#### Q12: Check your current location
```
pwd
```

## Exercise 2

#### Q1: Go to your home directory (should be named after you, you might be there by default)
```
cd ~
```
#### Q2: Check your current location
```
pwd
```
#### Q3: Create a folder linux_ex_1
```
mkdir linux_ex_1
```
#### Q4: Go into this folder
```
cd linux_ex_1
```
#### Q5: Create an empty text file named [first_name]_[last_name].txt (e.g. alexis_bogroff.txt)
```
touch ines_bergaut.txt
```
#### Q6: Create a folder notes
```
mkdir notes
```
#### Q7: Move your text file into this folder
```
mv ines_bergaut.txt notes/
```
#### Q8: Rename the text file by appending the current year [first_name]_[last_name]_[current_year].txt
```
cd notes
mv ines_bergaut.txt ines_bergaut_2023.txt
```
#### Q9: Make a copy of this folder, name it notes_2022
```
cd ~
cd linux_ex_1
cp -r notes notes_2022
```
#### Q10: Delete the first folder (notes) using the verbose option
```
rm -rv notes
```

## Exercise 3

#### Q1: Create a script script_1.sh in the folder linux_ex_1
```
nano scrip_1.sh
```
#### Q2: In the script, write the commands that would output the following :
#### Script running please wait ...
#### Done.
```
echo "Script running please wait..."
echo "Done."
```
#### Q3: Quit editing and save the script
ctrl x 
Y
entrance
```
cmod +x script_1.sh   (make the script executable)
```
#### Q4: Display the content of the script (using a command, not from an editor)
```
cat script_1.sh
```
#### Q5: Run the script
```
./script_1.sh
```

## Exercise 4

### Exercise 4.1

#### Q1: Create a file credentials in the folder linux_ex_1
```
cd linux_ex_1
touch credentials.txt
```

##### (a) Write any kind of (fake) personal information within the file
```
nano credentials.txt
echo "blabla"
chmod +x credentials
cat credentials
```
##### (b) Display the file content
```
./credentials
```
##### (c) Display the current permissions
```
ls -l credentials
```
#### Q2: Change the current permissions to : read only for all users
```
chmod a-wx credentials
```
##### (a) Display the new permissions
```
ls -l credentials
```
##### (b) Modify and save the file
```
chmod u+w credentials (only user can modify)
nano credentials
echo "blabla"
```
##### (c) Display the file content
```
chmod +x credentials
./credentials 
```
#### Q3: Change the permissions back to read and write for all users
```
chmod a+w credentials
```
##### (a) Display the new permissions
```
ls -l credentials
```
##### (b) Modify and save the file
```
nano credentials
echo "blabla"
```
##### (c) Display the file content
```
chmod +x credentials
./credentials
```
#### On the same file :

#### Q1: Add the execute permission to the owner
```
chmod u+x credentials
```
##### (a) Display the new permissions
```
ls -l credentials
```
#### Q2: Remove the read permission to other users
```
chmod o-r credentials
```
##### (a) Display the new permissions
```
ls -l credentials
```
#### Q3: Change the permissions to read, write and execute for all users
```
chmod a+rwx credentials
```
##### (a) Display the new permissions
```
ls -l credentials
```

### Exercise 4.2 Access root files

#### Q1: Go to the root folder
```
cd /
```
#### Q2: Create a file in root user mode named .private_file
```
sudo touch ~/ .private_file
```
##### (a) Write some information in the file
```
ls -l credentials
```
##### (b) Display the file content
```
ls -l credentials
```
##### (c) Display all the files in the folder including hidden files
```
ls -l credentials
```
#### Q3: Modify the file in normal user mode
```
ls -l credentials
```
##### (a) Write some new information in the file
```
ls -l credentials
```
##### (b) Display the file content
```
ls -l credentials
```
#### Q4: Modify the file in root user mode
```
ls -l credentials
```
##### (a) Write some new information in the file
```
ls -l credentials
```
##### (b) Display the file content
```
ls -l credentials
```
#### Q5: Change permissions to read, write and execute for all users
```
ls -l credentials
```
##### (a) Modify the file content in normal user mode
```
ls -l credentials
```
##### (b) Display the file content
```
ls -l credentials
```
