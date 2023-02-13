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

I will repeat this with some text files from another directory:

```find Fletcher -name *.txt```

This is my output:

```
Fletcher/ch1.txt
Fletcher/ch10.txt
Fletcher/ch2.txt
Fletcher/ch5.txt
Fletcher/ch6.txt
Fletcher/ch9.txt
```

Here is the link to my [source](https://www.linode.com/docs/guides/find-files-in-linux-using-the-command-line/).

This is how ```find``` can be used to get all the files of a particular extension in a directory.

### Finding file names if we dont' know the exact name

**Example 1**

We can also find a file if we know a word it contains in the name of the file (for example, I want to look for all files that contain China in the file name):

```find ./*/*/* -iname "*China*txt"```

Here is the output:

```
./travel_guides/berlitz2/China-History.txt
./travel_guides/berlitz2/China-WhatToDo.txt
./travel_guides/berlitz2/China-WhereToGo.txt
```

This is the link to my [source](https://www.redhat.com/sysadmin/linux-find-command).

**Example 2**

This command also works if I don't have an actual word. For example, even if I put "Canc" as the string to look for, it will give me all the files containing that.

```written_2:520$ find ./*/*/* -iname "*Canc*txt"```

Here is my output:

```
./travel_guides/berlitz2/Cancun-History.txt
./travel_guides/berlitz2/Cancun-WhatToDo.txt
./travel_guides/berlitz2/Cancun-WhereToGo.txt
```

This is the link to my [source](https://www.redhat.com/sysadmin/linux-find-command). This is how find can be used to get files when we don't know the exact name.

### Finding file names using the app

**Example 1**



**Example 2**

