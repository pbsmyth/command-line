← [What Is the Command Line?](01-what-is-the-command-line.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Why is the command line useful?](03-why-is-the-command-line-useful.md) →

---

# 2. Text editors

## What is text?

Before we explain which program we'll be using for editing text, we want to give a general sense of this "text" we keep mentioning. For those of us in the humanities, whether we follow literary theorists who read any object as a "text" or we dive into philology, paleography, codicology or any of the fields [David Greetham](https://en.wikipedia.org/wiki/David_Greetham_(textual_scholar)) lays out in _Textual Scholarship_, "text" has its specific meanings. As scholars working with computers, we need to be aware of the ways plain text and formatted text differ. Words on a screen may have hidden formatting. Many of us learned to use a word processor like Microsoft Word and don't realize how much is going on behind the words shown on the screen. For the purposes of communicating with the computer and for easier movement between different programs, we need to use text without hidden formatting.

![Word Doc](../images/worddoc.png)

Users with visual disabilities, [click here](https://github.com/DHRI-Curriculum/command-line/raw/v2.0/files/WordProcessorExample.docx) to download the Word file.

If you ask the command line to read that file, this Word `.docx` file will look something like this

![Word Doc as visualized by Command Line](../images/CatWordDoc.png)

Users with visual disabilities, [click here](https://raw.githubusercontent.com/DHRI-Curriculum/command-line/v2.0/files/PK.md) to download the text file.

Word documents which look like "just words!" are actually comprised of an archive of extensible markup language (XML) instructions that only Microsoft Word can read. Plain text files can be opened in a number of different editors and can be read within the command line.

## Plain text

For the purposes of communicating with machines and between machines, we need characters to be as flexible as possible. Plain text include characters of readable material but not graphical representation.

According to the [Unicode Standard](https://www.unicode.org/versions/Unicode12.1.0/),

> Plain text is a pure sequence of character codes; plain Unicode-encoded text is therefore a sequence of Unicode character codes.

Plain text shows its cards—if it's marked up, the markup will be human readable. Plain text can be moved between programs more fluidly and can respond to programmatic manipulations. Because it is not tied to a particular font or color or placement, plain text can be styled externally.

A counterpoint to plain text is rich text (sometimes denoted by the Microsoft rich text format `.rtf` file extension) or "enriched text" (sometimes seen as an option in email programs). In rich text files, plain text is elaborated with formatting specific to the program in which they are made.

Plain text has two main properties in regard to rich text:

> plain text is the underlying content stream to which formatting can be applied. Plain text is public, standardized, and universally readable.

## Choosing a text editor

An important tool for programming and working in the command line is a text editor. A text editor is a program that allows you to edit plain text files, such as `.txt`, `.csv`, or `.md`. Text editors are not used to edit rich text documents, such as `.docx` or `.rtf`, and rich text editors should not be used to edit plain text files. This is because rich text editors will add many invisible special characters that will prevent programs from running and configuration files from being read correctly.

While it doesn't really matter which text editor you choose, you should try to become comfortable with at least one text editor.

Choosing a text editor has as much to do with personality as it does with functionality. Graphical user interfaces (GUIs), user options, and "hackability" vary from program to program.

## Default recommendation

For our workshops, we will be using [Visual Studio Code](https://code.visualstudio.com/). Not only is Visual Studio Code free and open source, but it is also consistent across macOS, Windows, and Linux systems.

You will have downloaded Visual Studio Code according to the [instructions](https://github.com/DHRI-Curriculum/install/blob/v2.0/guides/visual-studio-code.md) on the installations page. We won't be using the editor a lot in this tutorial, so don't worry about getting to know the editor now. In other workshops we will discuss syntax highlighting and version control, which Visual Studio Code supports. For now we will get back to working in the command line itself.

## Evaluation

What is the difference between a plain text document and a rich text document? (Select all that apply)

- Plain text contains no formatting, only line breaks and spacing.*
- Plain text cannot be marked up.
- Rich text is styled text, _i.e.,_ plain text completed by information such as font size, format, and colors.*
- One can't determine whether there is a difference betweeen the two without looking at their content.

What is the Command Line? How is it different from your text editor?

---

← [What Is the Command Line?](01-what-is-the-command-line.md)&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[Why is the command line useful?](03-why-is-the-command-line-useful.md) →