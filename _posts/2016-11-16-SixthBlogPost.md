---
layout: post
title:  "Sixth Blog Post"
date:   2016-10-05 
categories: ""
author: "Brynna Wainwright"
---

I’m back! And today I’m going to talk to you all about Assignment 5! The task was to create a database and a datatable within SQL that would house the answers to questions asked within a script and answered by the user. The questions were from the previous assignment, but I’ll list them here again for your convenience. 
* What is your Name?
* What is your favorite color?
* What is your biggest fear?
* What is your major?
* What was the last food you ate?

# Getting Started
First, we designated Amanda as the “Repo Czar” because her computer was in the middle of the three of us so it made sense. With that, Amanda created a new repository named “bluebluegreen” not to be mistaken for our last repository with the same group name except that one was capitalized. Then, Amanda cloned the assignment-4 into the new assignment so that we could have our old script and csv file to work with. Although this seems simple, we had trouble as a group because we didn’t realize we needed to clone assignment 4 inside of the new repository for assignment 5. After conferring with another group we realized what we did wrong and started over.

# Actually Getting Started
Then, we had to modify our script to connect to a MySQL database. At first we were pretty stumped at house to do this. We approached this problem how we usually approach coding problems, by googling for the answer. First we found one way of doing this and asked the professor what he thought. He said it looks like it could work but we may run into some issues. This is what our initial code looked like:
`IFS=,
while read UID today name color fear major food
     do
         echo "INSERT INTO scripttable (Name,Color,Fear,Major,Food,Today,UID) VALUES ('$UID', '$today', '$name', '$color', '$fear', '$major', '$food');"
done < scriptanswers.csv | mysql -u aehaney -p scriptdatabase;`

Well, he was right and we did run into issues. For some reason it was not copying the answers into the SQL table even though it was copying into the csv. After trying to fix this issue for a while we decided to look for other approaches. We found something in the class notes that we thought may work and we ended up trying that out: `mysql -u $username -p -H -e "LOAD DATA INFILE '/home/ubuntu/workspace/bluebluegreen/BlueBlueGreen-Assignment-4/scriptanswers.csv' IGNORE INTO TABLE scripttable FIELDS TERMINATED BY ',';" scriptdatabase`. **And it worked!**
BUT, we soon realized that it was replicating each answer that was already in the csv file every time we would run the script. This was an issue because the datatable had replicated entries. To fix this, we had to drop all entries in the table and edit the command to include `IGNORE` in order to ignore entries that were already included. And it worked!

# MySQL Dumping
Next, we had to figure out how to dump the MySQL database into a .sql file in our repository directory with the rest of our files after it had been modified with new data. To do this, we looked through the class notes to find where we talked about data dumping. We found the correct command which is `mysqldump -u $username -p scriptdatabase > scriptdatabase.sql` but the thing about this is that you needed to know what the user’s SQL username is! To fix this issue, we simply added another question onto the script to ask the user what their username is and saved the user input into a variable called username. This way, when we want to run the dumping command at the end of the script, we can just call the username variable that was made previously! 

# Reflections
Overall, this assignment was definitely one of the most challenging assignments thus far. We ran into many roadblocks-even more than those I mentioned just because some of them were so small! But no matter how small the issue is, it seemed to always take a fair amount of time to resolve it on our own. Additionally, the fact that I was not able to make it into class on Wednesday further complicated things. My group ended up staying late both days of class leading up to the assignment due date on Thurday, staying as late as an hour later after class! Looking back in hindsight, the issues we encountered likely shouldn’t have taken as long to resolve them as it did, but the fact that none of us have any prior experience with programming, it made each issue very difficult! In the end, I learned a lot on this assignment and I appreciate the learning material on SQL because I hope to pursue a career in some type of data analyst position, and SQL is an essential skill to have to be successful. 

# Link
[Here is the link to my GitHub repository]( https://github.com/aehaney/bluebluegreen)
