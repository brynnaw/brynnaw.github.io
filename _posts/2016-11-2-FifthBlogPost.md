---
layout: post
title:  "Fifth Blog Post"
date:   2016-10-05 
categories: ""
author: "Brynna Wainwright"
---

Hi again! Today I’m going to tell you about our assignment 4 which was to create a script that would ask the user a series of questions and save his/her answers into a CSV file. It may seem simple, but it took quite a while to figure everything out! I’ll walk you through what we did:

# Creating the Questions
First we misunderstood the assignment and thought that we were supposed to create the same 5 questions that were asked during one of our in class assignments (**oops**). Once we cleared that up, we came up with 5 new questions:

* What is your Name?
* What is your favorite color?
* What is your biggest fear?
* What is your major?
* What was the last food you ate?

# Saving User Input into a Variable
Once we got the questions down, we then made sure to save the user input into a variable. To do this, we used the command `read name`, `read color`, `read fear`, `read major`, `read food`. 

# Date Stamp
Next we needed to create a date stamp for each user that filled out the survey by saving the date they ran and answered the script into a month-date-year format. Luckily, Erin had already played around with this function during one of the class periods so we had a good idea of how to do this. We created a variable called today from a bash function using the commands 	`today() { date  +%m-%d-%Y }`. The only thing we needed to change here was taking out the `echo “Date: “ ` because we didn’t need that saved into the CSV. 

# Unique Identifier 
Now came the hard part. In order to identify each individual who answered our script, we needed to create a unique identifier. To do this, we basically just kept searching google and the documents provided in the class notes to find something that had to do with “Unique Identifier” or “UUID” or “GUID”. It took a while and we just had to do trial and error before I found something that finally worked! 

# Save into a CSV
This was tricky because we wanted to *append* an existing CSV file each time someone answered the script instead of creating a new CSV. This is something we hadn’t specifically done in class before, but we had done something similar- we had piped an existing file into a CSV formatted file using `>`.  Through more google searching, and a bunch of trial and error, we were **SO** close to figuring it out on our own! I had the idea to pipe the variables into a CSV instead of the file as a whole, so I had started typing in `cat $name, $color, $fear, $major, $food >> scriptanswers.csv`. I just needed to change cat into echo, erase the spaces in between variables, and add the date stamp and unique identifier and we would’ve been good to go! I still believe we would’ve figured it out on our own, but we ended up asking our professor for some help because we were running out of time.

#Conclusion
I learned a bunch from this exercise! First of all, I hope to go into data analytics and data science, so having some sort of idea how data files work will definitely prove useful. Also, learning the collaborative aspect of GitHub is also very useful knowledge as well as being resourceful with google! All in all, it was a successful assignment.

# Links
[Here is the link to my GitHub repository](https://github.com/brynnaw/BlueBlueGreen-Assignment-4)

