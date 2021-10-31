# Command-Challenges-Writeups
Writeups For https://cmdchallenge.com/ 

***Challenge 1*** :

<kbd>Your first challenge is to print "hello world" on the terminal in a single command.</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  echo "hello world
  ```
</details>

***Challenge 2*** :

<kbd>Print the current working directory.</kbd>
<details>
  <summary> <b>View Solution </b></summary>
  
```
  pwd
  ```
</details>

***Challenge 3*** :

<h><kbd>List names of all the files in the current directory, one file per line</kbd></h>
<details>
  <summary> <b>View Solution </b></summary>
  
```
  ls
  ```
</details>

***Challenge 4*** :

<kbd>There is a file named access.log in the current directory. Print the contents.</kbd>
<details>
  <summary> <b>View Solution </b></summary>
  
 ```
  cat access.log
  ```
 </details>
 
 ***Challenge 5*** :
 
 <kbd>Print the last 5 lines of "access.log".</kbd>
<details>
  <summary> <b>View Solution </b></summary>
  
```
  cat access.log | tail -n 5
  ```
</details>

 ***Challenge 6*** :
 
 <kbd>Create an empty file named take-the-command-challenge in the current working directory.</kbd>
<details>
  <summary> <b>View Solution </b></summary>
  
```
  > take-the-command-challenge
  ```
</details>

 ***Challenge 7*** :
 
 <kbd>Create a directory named tmp/files in the current working directory</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  mkdir -p tmp/files
  ```
</details>
 
 ***Challenge 8*** :
 
 <kbd>Copy the file named take-the-command-challenge to the directory tmp/files</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  cp take-the-command-challenge  tmp/files
  ```
</details>

***Challenge 9***: 

<kbd>Move the file named take-the-command-challenge to the directory tmp/files</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  mv take-the-command-challenge  tmp/files
  ```
</details>

***Challenge 10***: 

<kbd>Create a symbolic link named take-the-command-challenge that points to the file tmp/files/take-the-command-challenge</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  ln -s tmp/files/take-the-command-challenge take-the-command-challenge
  ```
</details>

***Challenge 11***:

<kbd>Delete all of the files in this challenge directory including all subdirectories and their contents</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  rm -rf .* ./*
  ```
</details>

***Challenge 12***

<kbd>There are files in this challenge with different file extensions. Remove all files with the .doc extension recursively in the current working directory.</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  rm -f **/*.doc
  ```
</details>

***Challenge 13***

<kbd>There is a file named access.log in the current working directory. Print all lines in this file that contains the string "GET".</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  cat access.log | grep -i "GET"
  ```
</details>

***Challenge 14***

<kbd>Print all files in the current directory, one per line (not the path, just the filename) that contain the string "500".</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  grep -Rli "500"
  ```
</details>

***Challenge 15***

<kbd>Print the relative file paths, one path per line for all filenames that start with "access.log" in the current directory.</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  ls -r
  ```
</details>

***Challenge 16***

<kbd>Print all matching lines (without the filename or the file path) in all files under the current directory that start with "access.log" that contain the string "500".</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  find ./ -type f -name access.* -exec grep -i "500" "{}" ";"
  ```
</details>

***Challenge 17***

<kbd>Extract all IP addresses from files that start with "access.log" printing one IP address per line.</kbd>

<details>
  <summary> <b>View Solution </b></summary>
  
```
  
  ```
</details>







