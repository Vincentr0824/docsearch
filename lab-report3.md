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
