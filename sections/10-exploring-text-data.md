← [Pipes](09-pipes.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Interlude](11-interlude.md) →

---

# 10. Exploring Text Data

So far the only text file we've been working with is our cheat sheet. Now, this is where the command line can be a very powerful tool: let's try working with a large text file, one that would be too large to work with by hand.

Let's download the data we're going to work with:

[Download `nypl_items.csv`](https://github.com/DHRI-Curriculum/command-line/raw/v2.0/files/nypl_items.csv)

If you are using Chrome or Firefox, right click on the link above and select "Save Link As..."; make sure you name the file `nypl_items.csv`
Please note that, occasionally, [Chrome "forgets" to add the extension to your downloaded file](/images/savelinkaschrome.png); therefore, if your namefile doesn't end with `.csv`, [feel free to add it manually](/images/savelinkaschrome2.png).

Our data set is a list of public domain items from the New York Public Library. It's in `.csv` format, which is a plain text spreadsheet format. CSV stands for "comma separated values," and each field in the spreadsheet is separated with a comma. It's all still plain text, though, so we can manipulate the data using the command line.

## Move Command

Once the file is downloaded, move it from your `Downloads` folder to the `projects` folder on your desktop—either through the command line, or drag and drop in the GUI. Since this is indeed a command line workshop, you should try the former!

To move this file using the command line, you first need to navigate to your `Downloads` folder where that file is saved. Then type the `mv` command followed by the name of the file you want to move and then the file path to your `projects` folder on your desktop, which is where you want to move that file to (note that `~` refers to your home folder):

```console
$ mv nypl_items.csv ~/Desktop/projects/
```

You can then navigate to that `projects` folder and use the `ls` command to check that the file is now there.

## Viewing Data in the Command Line

Try using `cat` to look at the data. You'll find it all goes by too fast to get any sense of it. (You can click <kbd>control</kbd> + <kbd>c</kbd> on your keyboard to cancel the output if it's taking too long.)

Instead, let's use another tool, the `less` command, to get the data one page at a time:

```console
$ less nypl_items.csv
...
```

`less` gives you a paginated view of the data; it will show you contents of a file or the output from a command or string of commands, page by page.

To view the file contents page by page, you may use the following keyboard shortcuts (that should work on Windows using Git Bash or on macOS terminal):

Click the <kbd>f</kbd> key to view forward one page, or the <kbd>b</kbd> key to view back one page.

Once you're done, click the <kbd>q</kbd> key to return to the command line.

Let's try two more commands for viewing the contents of a file:

```console
$ head nypl_items.csv
...

$ tail nypl_items.csv
...
```

These commands print out the very first (the "head") and very last (the "tail") sections of the file, respectively.

## Cleaning the Data

We didn't tell you this before, but there are duplicate lines in our data! Two, to be exact. Before we try removing them, let's see how many entries are in our `.csv` file:

```console
$ cat nypl_items.csv | wc -l
100001
```

This tells us there are 100,001 lines in our file. The `wc` tool stands for "word count," but it can also count characters and lines in a file. We tell `wc` to count lines by using the `-l` flag. If we wanted to count characters, we could use `wc -m`.

To find and remove duplicate lines, we can use the `uniq` command. Let's try it out:

```console
$ cat nypl_items.csv | uniq | wc -l
99999
```

OK, the count went down by two because the `uniq` command removed the duplicate lines. But which lines were duplicated?

```console
$ cat nypl_items.csv | uniq -d
...
```

The `uniq` command with the `-d` flag prints out the lines that have duplicates.

## Challenge

Use the commands you've learned so far to create a new version of the `nypl_items.csv` file with the duplicated lines removed. (Hint: _redirects_ from the lesson when we made a [cheat sheet](https://curriculum.dhinstitutes.org/workshops/command-line/lessons/?page=8) are your friend.)

## Solution

Type `pwd` to see where on your computer you are located. If you are not in the `projects` folder we just created, navigate to that folder using the commands you learned in the [lesson on navigation](https://curriculum.dhinstitutes.org/workshops/command-line/lessons/?page=6).

Type `ls` to check whether the file `nypl_items.csv` is in your projects folder.

Type `cat nypl_items.csv | uniq > new_nypl_items.csv` to create a new version of the `nypl_items.csv` file with the duplicated lines removed.

## Evaluation

What do command line flags allow you to do?

- Flags allow you to earmark the file you are working on.
- Flags are useful to create a new version of the file you are working on, while preserving the old version for future access.
- Flags are a common way to specify options for command line programs.*

## Keywords

Do you remember the glossary terms from this section?

- [Path](https://github.com/DHRI-Curriculum/glossary/blob/v2.0/terms/path.md)

---

← [Pipes](09-pipes.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Interlude](11-interlude.md) →
