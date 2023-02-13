# Lab Report 3

## Researching Commands

In this lab report, I will look more closely at the find command and explore the different ways in which it can be used to extract information from a directory with files and other subdirectories. In general, the find command is useful for searching files or directories. We can use it to execute a variety of tasks ranging from finding files of a specific type to files with a specific name.

### Use find with the name of the file

**Example 1**

To find a file based on its name, the following command is run (all my commands are running using data from the skill-demo1-data directory and its subdirectories):

``` find -name WhatToJapan.txt```

This is the output of this command: 

```./written_2/travel_guides/berlitz1/WhatToJapan.txt```

This gave me the file path of where the file with the specified name is located. Here is a hyperlink for my [source](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)

**Example 2**

Now, I'll look for a file in some ther directory:

```find -name Bali-History.txt```

Here is the output:

```./written_2/travel_guides/berlitz2/Bali-History.txt```

Here is a hyperlink for my [source](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/). This way the ```-name``` tag can be used to look for files based on their name. 

### Using find with the extension of the file

**Example 1**

This command can also be used to find files of a single extension type. For example, if I wanted to look for all the .txt files in a directory, I could use this command:

```find Berk -name *.txt > numberTextFiles```

**Note:** This is the path for Berk (```/home/linux/ieng6/cs15lwi23/cs15lwi23aqv/skill-demo1-data/written_2/non-fiction/OUP```)

I stored all the file paths with a .txt file extension in numberTextFiles.txt. To access this information I can run ```cat numberTextFiles``` to display this information in the terminal.

```
Berk/CH4.txt
Berk/ch1.txt
Berk/ch2.txt
Berk/ch7.txt
```

Here is the link to my [source](https://www.linode.com/docs/guides/find-files-in-linux-using-the-command-line/).

**Example 2**

I will repeat this 
Here is the link to my [source](https://www.linode.com/docs/guides/find-files-in-linux-using-the-command-line/).

### THIRD COMMAND






