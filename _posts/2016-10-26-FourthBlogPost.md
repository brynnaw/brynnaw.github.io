---
layout: post
title:  "Fourth Blog Post"
date:   2016-10-05 
categories: ""
author: "Brynna Wainwright"
---

Hello everyone- I’m back! So for this assignment I created a script that will convert a markdown document to a DOCX, PDF, ODT, and HTML document. It’s pretty cool if I do say so myself. 

# Abstract
The original document that I converted was an old research paper from a couple semesters ago when I was in a course titled The History of Western Art I. The paper argues that the impact of the state and its religion outweigh any stylistic choices of the individual artist on works of art. The paper cited 6 different pieces of art across cultures and time periods in which the role of the respective religion and state more prominently was shown in the work than individualistic elements. I used the subject matter, purpose, and commissioner of each piece of art as evidence of the main argument.

# Technical
The script that I used incorporated various commands which allowed the program to know what to do with the markdown document. Specifically, the following commands instructed Pandoc to change the markdown document to HTML, DOCX, ODT, and PDF respectively:
`pandoc -o ArtHistoryEssay.html ArtHistoryEssay.md`
`pandoc -o ArtHistoryEssay.docx ArtHistoryEssay.md`
`pandoc -o ArtHistoryEssay.odt ArtHistoryEssay.md`
`pandoc -o ArtHistoryEssay.pdf ArtHistoryEssay.md`
One feature that I also incorporated into the script is an If, Then Statement which ensures that the user wants to continue with the functions of the script. More specifically, I asked the user, “Would you like your markdown file to be converted? 'Yes' or 'No',” and then I saved the user’s input into a variable by using the command `read USERINPUT`. If the user input said ‘Yes’ then the script continued to run, if not, then the user is exited from the script.

# Reflection
After completing this assignment, I can honestly say I’ve learned a lot—both about pandoc and writing scripts in Bash, but also about workflow of coding. I encountered several issues when trying to complete this assignment, first of which being the if, then statement. I spent all of Wednesday’s class period to figure out why I kept getting an error when trying to run the statement. Bash would return, “./brynnaw-convert-docs.sh: line 18: [: missing `]'” for some reason. I even asked my professor what he thought and he couldn’t understand what was wrong either! I ended up doing more research and trying to replicate what other’s did to compare variables in an if then statement in bash. Eventually I had a huge epiphany moment where I realized that I was missing one single space. Amazing how such a small detail can wreak havoc on a script!

Another challenge I experienced arose when trying to find smaller pictures to link to in my table. When searching through google and user a size filter on images, I found the pictures I wanted at the sizes I wanted but unfortunately when linking to them in my markdown file, the system would return errors! I ended up searching for other images that were smaller in size, but not using the size filter!

Ultimately, this assignment helped me to better understand pandoc as well as better understand troubleshooting issues. The script which converted the documents helped to solidify the specific pandoc commands in my mind. Additionally, learning how to approach a problem when one arises by trying different things and utilizing the resources on the web is a skill that can only be learned with experience. In the end, this assignment was super fun!

# Links
If you want to better understand what the script actually does, you can get a hands-on look at the code and source/output files!

* Source file:
[ArtHistoryEssay.md](https://github.com/inls161/assignment-3-brynnaw/blob/master/ArtHistoryEssay.md)
* Output files:
[ArtHistoryEssay.docx](https://github.com/inls161/assignment-3-brynnaw/blob/master/ArtHistoryEssay.docx)
[ArtHistoryEssay.html](https://github.com/inls161/assignment-3-brynnaw/blob/master/ArtHistoryEssay.html)
[ArtHistoryEssay.odt](https://github.com/inls161/assignment-3-brynnaw/blob/master/ArtHistoryEssay.odt)
[ArtHistoryEssay.pdf](https://github.com/inls161/assignment-3-brynnaw/blob/master/ArtHistoryEssay.pdf)
[Here is the link to my Editor](https://ide.c9.io/brynnaw/assignment3)
[Here is the link to my script code](https://github.com/inls161/assignment-3-brynnaw/blob/master/brynnaw-convert-docs.sh)

