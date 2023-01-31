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

#### Q2: In the script, write the commands that would output the following :
#### Script running please wait ...
#### Done.

#### Q3: Quit editing and save the script

#### Q4: Display the content of the script (using a command, not from an editor)

#### Q5: Run the script
