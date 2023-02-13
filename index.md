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

We can also find a file if we know a word it contains in the name of the file (for example, I want to look for all files that contain China in the file name). We can use ```-iname``` for this operation:

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

### Finding files by content

**Example 1**

Find can also be used in combination with other commands such as ```grep``` in order to execute more specific tasks. This is used when we know the contents of the file and want to know which file has it, we can carry out a command like this: If I am looking for a word such as "Eiffel" in all of the files in the berlitz1 directory, I can use a combination of ```grep``` and ```find```.

```find berlitz1 -name "*.txt" -exec grep -Hi Eiffel {} \;```

Here is the output:

```
berlitz1/HistoryFrance.txt:        pride found its perfect expression in the Eiffel Tower, thrust into the
berlitz1/IntroLasVegas.txt:        walking distance of one another, loom replicas of the Eiffel Tower, a
berlitz1/WhereToEgypt.txt:        structure in the world until the building of the Eiffel Tower in Paris
berlitz1/WhereToFrance.txt:        the Eiffel Tower, Arc de Triomphe, and Hôtel de Ville.
berlitz1/WhereToFrance.txt:        commentary — sites including the Eiffel Tower, the Palais de Chaillot
berlitz1/WhereToFrance.txt:        Invalides–Eiffel Tower
berlitz1/WhereToFrance.txt:        to look at twice, and then there is the Eiffel Tower. Monuments usually
berlitz1/WhereToFrance.txt:        but the Eiffel Tower is a monument for its own sake, a proud gesture to
berlitz1/WhereToFrance.txt:        Horloge is Rouen’s emblem, its Eiffel Tower. The ornamental gilded
berlitz1/WhereToJapan.txt:        Liberty, the Eiffel Tower, the Kremlin, the Great Wall — are man-made.
berlitz1/WhereToJapan.txt:        the Tsutenkaku Tower, a rather desperate imitation of the Eiffel Tower
berlitz1/WhereToLakeDistrict.txt:        in 1849; some think it served as the inspiration for Tour d’Eiffel in
```

This is the link to my [source](https://www.redhat.com/sysadmin/linux-find-command).

**Example 2**

I tried this with another word "Amazon". I did this with the idea of looking for a file that tallks about the Amazon river. However, the results in this case are a little bit different.

```find berlitz1 -name "*.txt" -exec grep -Hi Amazon {} \;```

Output:

```
berlitz1/WhereToFWI.txt:        though only copies of his paintings. Also in Le Carbet: the Amazona
berlitz1/WhereToLakeDistrict.txt:        book Swallows and Amazons (1930). The lake and its islands were his
```

The words "Amazona" and "Amazons" were caught as well! Thus, we can conclude that any string that is either equal to or contains the string specified will be caught by using this command.

This is the link to my [source](https://www.redhat.com/sysadmin/linux-find-command).

### Conclusion

This lab report was particularly interesting since it allowed me to explore and learn a lot of different commands which could be used while working on projects. Exploring 4 different ways in which ```find``` can be used showed me the potential of some of these Linux commands and pushed me to explore how they work in more detail. All in all, this lab report gave me the oppurtunity to implement my learnings in a practical environment and learn new things about some of these commands.
