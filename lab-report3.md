Chosen Command: ```find```

The first command tested that uses find is:

```find technical/ -mmin -60```

The output of this command is:

```
technical/
technical//911report
technical//911report/chapter-1.txt
```

This command checks for files which have been modified in the last 60 minutes. For example purposes, I went in and changed a line in the chapter-1.txt file and that resulted in the file path being the output for the command. This would be useful incase a team was working on certain files, and didn't want to modify other files. The team would be able to check if any files that weren't supposed to be touched were modified. 

Here is another example of this command being used:

```find technical/biomed/ -mmin -60```

The output of this command is:

```
technical/biomed/
technical/biomed//1468-6708-3-1.txt
```

The reason why this was the output is because I went in and modified the 1468-6708-3-1.txt file in the biomed folder. The reason why the chapter-1.txt file path didn't appear is because instead of writing on ```technical/``` for the path, I specified ```technical/biomed/```. This command is useful as it will help with keeping track of changes in larger scale projects with multiple folders. 

The source of this command is the following website: https://www.tecmint.com/35-practical-examples-of-linux-find-command/



The second command tested is:

```find technical/ -type f -name "chapter-1.txt" -exec rm -f {} \;```

The output of this command is:

```There is no actual output in the terminal!```

While it may be hard to tell from first glance, this command actually removes specific files based on their name. Without an output, the specific file is simply removed after the command is executed. This is rather useful for removing junk files, or files that are no longer needed for a project. It is important to know that in certain applications such as vs code, the file can actually be brought back to life if it is still open, simply saving it again will return it to its original place. 

Here is another example of this command being used:

```find technical/biomed/ -type f -name "1468-6708-3-1.txt" -exec rm -f {} \;```

The output of this command is:

```Once again, there is no output!```

Once again, this example removes specific files from specific paths based on the file name given. In this example, the path is further specific and removes the file from that specific path. This version is useful incase certain file names are similar to each other, but are in different folders. This will help with avoiding an accidental removal of a possibly important file with a similar name in another folder. 

The source of this command is the following website: https://www.tecmint.com/35-practical-examples-of-linux-find-command/



The third command tested is:

```find technical/ -type f -empty```

The output of this command is:

```technical//911report/chapter-1.txt

The reason why this path was the output of the command is because the command searches for empty files in specific directories, and I deleted the contents of the chapter-1.txt file. The reason why this is useful is because there may be unwanted empty text files that can be found with this command and removed in combination with the previous command we covered. 

Here is another example of this command being used:

```find technical/biomed/ -type f -empty```

The output of this command is:

```technical/biomed//1468-6708-3-1.txt

The reason why this path was the output of the command is because it is another file with it's contents deleted by me. Another reason as to why this command is useful is because there may have been a mistake where the contents of a file have been deleted which would result in an error, and the mistake can be easily identified using this command. 

The source of this command is in the following website: https://www.tecmint.com/35-practical-examples-of-linux-find-command/
