<h1> This module's exercises </h1>

- Writing in Markdown
- Using the DH Box command line
- Converting files with the command line
- Setting up GitHub
- Interacting with GitHub from the command line

<h2> Writing in Markdown </h2>

The [markdown cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links) is a useful resource that I am sure I will be referring back to continually; this is what I used today:

- To make text *italic*, wrap text with *

- To make text **bold**, wrap text with **

- To make text ***both italic and bold***, wrap text with ***

- To link a post, use [this text](to hyperlink this webpage)

- To add an image, use: 
![alt text] (IMAGE LINK GOES HERE "Hover Text Goes Here")

- To create bulleted list, use - or + or * at the beginning.

<h2> Using DH Box Command Line</h2>

Installing pandec, numo, sudo using the command line was interesting. I wasn't exactly sure what I was doing, but I was typing random commands, and it was making things work, and that was really very rewarding.

Notes to remember:

- The $ history command allows me to create a record of all the commands I type to that point;
- The $ ls is a useful command because I can use it to double check that there was nothing I missed;
- The DHBox program recommends changes if something doesn't go right with the typed command; not always, but sometimes - not 
sure what it can and can't help with
- I had to reinstall Nano because it didn't work initially; use $ sudo apt-get install nano to install Nano, and in the same
way, use the apt-get command with sudo to install an app through sudo. 

<h2>Converting files with the command line</h2>

In converting files, I requested Pandoc to create an output file ( the -o) called todayscommands.docx 
from dhbox-work-today.md.
Using this command; $ pandoc -o todayscommands.docx dhbox-work-today.md, I converted it to word file, but changing docx to 
html makes it an html file. This is easy enough.

<h2> Github and the command line </h2>
I had already set up my Github previously, for my fail log, however, after creating my own Hist 3814o depository, I was able
to move the converted html file from the previous exercise to the depository. 
