# Command-Challenges-Writeups Part Two
Writeups For https://cmdchallenge.com/ 

***Challenge 21*** :

<kbd>The file split-me.txt contains a list of numbers separated by a ; character. Split the numbers on the ; character, one number per line.
</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
cat split-me.txt | tr ";" "\n" 
  ```
</details>

***Challenge 22*** :

<kbd>Print the numbers 1 to 100 separated by spaces.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
echo  {1..100} 
  ```
</details>

***Challenge 23*** :

<kbd>This challenge has text files (with a .txt extension) that contain the phrase "challenges are difficult". Delete this phrase from all text files recursively.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
find . -type f -name "*.txt" -exec  sed -i 's/challenges are difficult//g' "{}" ";"
  ```
</details>

***Challenge 24*** :

<kbd>The file sum-me.txt has a list of numbers, one per line. Print the sum of these numbers.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
echo $( cat sum-me.txt | tr "\n" "+" | sed 's/+$//' ) | bc 

  ```
</details>

***Challenge 25*** :

<kbd>Print all files in the current directory recursively without the leading directory path.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
find . -type f -exec basename  "{}" ";"
  ```
</details>

***Challenge 26*** :

<kbd>Rename all files removing the extension from them in the current directory recursively.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
for i in $(find . -type f ); do mv $i $(echo $i | sed 's/\.[a-z]//g' ) ;done 
  ```
</details>

***Challenge 27*** :

<kbd>The files in this challenge contain spaces. List all of the files (filenames only) in the current directory but replace all spaces with a '.' character.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
ls | tr " " "." 

  ```
</details>

***Challenge 28*** :

<kbd>In this challenge there are some directories containing files with different extensions. Print all directories, one per line without duplicates that contain one or more files with a ".tf" extension.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
find ./ -type f -name "*.tf" -exec dirname "{}" ";" | uniq    
  ```
</details>


***Challenge 29*** :

<kbd>There are a mix of files in this directory that start with letters and numbers. Print the filenames (just the filenames) of all files that start with a number recursively in the current directory.

</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
find . -type f -exec basename "{}" ";" | egrep "^[0-9]+"
  ```
</details>

***Challenge 30*** :

<kbd>Print the 25th line of the file faces.txt

<details>
  <summary> <b>View Solution </b></summary>
  
```
cat faces.txt | sed -n "25p" 
  ```
</details>

***Challenge 31*** :

<kbd>Print the lines of the file reverse-me.txt in this directory in reverse line order so that the last line is printed first and the first line is printed last.
  </kbd>
<details>
  <summary> <b>View Solution </b></summary>
  
```
cat reverse-me.txt | tac
  ```
</details>


