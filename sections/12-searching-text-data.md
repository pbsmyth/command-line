← [Interlude](11-interlude.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[What we've learned](13-what-weve-learned.md) →

---

# 12. Searching text data

So we've cleaned our data set, but how do we find entries that use a particular term?

Let's say I want to find all the entries in our data set that use the term "Paris."

Here we can use the `grep` command. `grep` stands for "global regular expression print." The `grep` command processes text line by line and prints any lines which match a specified pattern. Regular expressions are special strings representing a pattern to be matched in a search operation. `grep` gives us access to the power of regular expressions as we search for text.

```console
$ cat nypl_items.csv | grep -i "paris"
...
```

This will print out all the lines that contain the word "Paris." (The `-i` flag makes the command ignore capitalization.) Let's use our `wc -l` command to see how many lines that is:

```console
$ cat nypl_items.csv | grep -i "paris" | wc -l
191
```

Here we have asked `cat` to read `nypl_items.csv`, take the output and pipe it into the `grep -i` command, which will ignore capitalization and find all instances of the word `paris`. We then take the output of that `grep` command and pipe it into the word count `wc` command with the `-l` lines option. The pipeline returns `191` letting us know that "Paris" (or "paris") occurs on 191 lines of our data set.

## Challenge

Use the `grep` command to explore our `.csv` file a bit. What areas are best covered by the data set?

## Solution
If you want to get a little more milage out of the grep command, refer to [this tutorial on grep and regular expressions](https://www.digitalocean.com/community/tutorials/using-grep-regular-expressions-to-search-for-text-patterns-in-linux). Regular expressions (or regex) provide methods to search for text in more advanced ways, including specific wildcards, matching ranges of characters such as letters and numbers, and detecting features such as the beginning and end of lines. If you want to experiment with regular expressions in an easy-to-use environment, numerous regex test interfaces are available from [a simple google search](https://www.google.com/search?w&q=regex+tester), such as [RegExr](https://regexr.com/), which includes a handy cheat sheet.

## Evaluation

Let's think about the `grep` command.

- It searches the given file for lines containing a match to the given strings or words.*
- It can be combined with other commands, so as to produce a search that matches their output.*
- It produces a new file with the lines containing the strings or words you are searching.
- It delete the strings or words you are searching from a file.

---

← [Interlude](11-interlude.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[What we've learned](13-what-weve-learned.md) →