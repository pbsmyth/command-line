# Introduction to the Command Line

## Abstract

If asked to show someone who has never seen a computer how to *do* something on your computer, many of us would explain what a screen and a cursor are, and then show how to point and click on icons. This approach relies on a graphical user interface, or GUI (pronounced "gooey!"). Today we're going to explore another way to make your computer do things: through the command line. Instead of pointing and clicking, we'll be typing in either git bash (Windows) or terminal (macOS) to tell the computer directly what task we'd like it to perform.

## Learning Objectives

- Learn common commands to create files (`touch` and `echo`)
- Learn commands to create directories (`mkdir`)
- Navigate our file structure using change directory (`cd`), print working directory (`pwd`), and list (`ls`)
- Move content from one place to another using redirects (`>`) and pipes (`|`)
- Explore a comma separated values (.csv) dataset using word and line counts, `head` and `tail`, and the concatenate command `cat`
- Search text files using the `grep` command
- Create and sort cheat sheets for the commands we learn

## Estimated time

3 hours

## Prerequisites

To complete the workshop, you will need:

- [Visual Studio Code](https://github.com/DHRI-Curriculum/install/blob/v2.0/guides/visual-studio-code.md) (recommended) You can use any plain text editor but for our purposes, Visual Studio Code ("VS Code") will be used.
- [Git Bash](https://github.com/DHRI-Curriculum/install/blob/v2.0/guides/git.md) (required) If you're using Windows, you will need to follow the instructions to install so that we can work in the cross-platform Unix command line for this session. If you're using macOS, however, you do not need to take any action. The built-in Terminal application has all the functionality we need.
- [Julia Evans's Bite Size Command Line](https://jvns.ca/blog/2018/08/05/new-zine--bite-size-command-line/) (recommended) Julia Evans's comics explain in detail (while being fun!) some of the most central Unix command line tools. It's a great zine to have on your desk next to you for this workshop, and long after.
- [Basic UNIX commands](http://mally.stanford.edu/~sr/computing/basic-unix.html) (recommended) This is another list of commonly used commands in the command line. It's useful, but can be a little overwhelming if you don't have any exposure to these things beforehand. Don't worry, we will cover the most important ones in our Introduction to Command Line workshop!

## Contexts

### Pre-reading suggestions

- [Neal Stephenson's "In the Beginning... Was the Command Line"](http://cristal.inria.fr/~weis/info/commandline.html) is a useful piece to grasp the relationship between (and the affordances of) the command line and the GUI.
- [Douglas Rushkoff's *Program or Be Programmed*](https://rushkoff.com/books/program-or-be-programmed/) offers some reflections on how using the command line allows one to communicate in a less mediated way with their machines and the importance of doing so in the current technoscape.

### Projects that use these skills

Mastering the command line will prove useful in a great number of projects. Most Python- and R-based projects will require you to have some knowledge of the command line. At a very basic level, you will be invoking a Python script and will be using values of command line arguments when creating and running your scripts.

- The command line is useful for setting up installations of server-side software (or more advanced software-as-a-service software, sometimes acronymized as SaaS). [Omeka](http://www.omeka.org) is merely one example. The command line will allow you to navigate the file structure of your server. Commands like `ls`, `mkdir`, `rmdir`, `cd`, etc. are really important. For example, `grep` could help you find a plugin directory that you might have accidentally placed in the wrong location.
- [Fair World 64: A Text-Based Game of the 1964–1965 World's Fair](https://academicworks.cuny.edu/gc_etds/3786/) A recent digital capstone project by Christofer Gass runs a Python script on the command line
- [Awesome Bash](https://github.com/awesome-lists/awesome-bash) A curated list of useful Bash scripts and resources.

### Ethical Considerations

- "The command line" is laden with masculine and military metaphors, which is reflective of the history of computing and programming. As Wendy Hui Kyong Chun discusses in ["On Software, or the Persistence of Visual Knowledge" (2004)](https://doi.org/10.1162/1526381043320741), almost all computers (as in human computers) in the US during World War II were young women. Human computers received commands from analysts——predominantly men with the military—that they then had to interpret and act upon the machine. As Chun (p. 34) argued, "computation depends on 'yes, sir' in response to short declarative sentences and imperatives that are in essence commands ... The command line is a mere operating system (OS) simulation." If commands are the ways in which a user communicates with machines, the command line (of computers today) receives these commands as text that is typed in.

## Acknowledgements

- Current Author: [Stefano Morello](https://github.com/smorello87)
- Past contributing Author: [Kelsey Chatlosh](https://github.com/kchatlosh)
- Past contributing Author: [Patrick Smyth](https://github.com/smythp)
- Past contributing Author: [Mary Catherine McKinniburgh](https://github.com/mckinniburgh)
- Past contributing Author: [Jojo Karlin](https://github.com/jojokarlin/)
- Past contributing Author: [Kalle Westerling](https://github.com/kallewesterling)
- Past reviewer: [Di Yoong](https://github.com/dyoong)
- Current editor: [Lisa Rhody](https://github.com/lmrhody)
- Current editor: [Kalle Westerling](https://github.com/kallewesterling)
