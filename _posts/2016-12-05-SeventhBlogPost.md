---
layout: post
title:  "Seventh Blog Post"
date:   2016-12-05
categories: ""
author: "Brynna Wainwright"
---

# Assignment Six

This assignment tasked my group and I with the objective of creating an interactive presentation to showcase all of the skills we’ve learned throughout the semester. My group included Amanda, Erin, and I and we focused on Neural Networks within Machine Learning. The organization of our presentation included an introduction of what neural networks are (what “world” we are in), followed by information about the three learning paradigms of neural networks, and then some examples to solidify the concept. 

## Who Did What

When discussing possible topics for our final project, I was eager to suggest the field of machine learning and artificial intelligence. This is due to my increased interest in the topic spurred by the first community event I attended (you can view the details of the event at my website under the tab “Community”). We decided to move forward with the concept but were hesitant at how to do so. After talking with the professor we realized that the topic was too broad and we needed to find a way to narrow in on a particular concept within Machine Learning. After doing additional research, we decided to focus on neural networks. **BUT** even after this, our topic was still too broad and we decided to focus on Reinforcement Learning within neural networks specifically. 
We split up the topics by position in the presentation, meaning Amanda gave us the initial definition and the 3 learning paradigms, Erin gave us additional details on reinforcement learning specifically, and I gave some real world examples. 

## The Process

The way we tackled this assignment was to first get the framework within cloud9 down and ready to go, then do research and get the material down, then go back and fill in our framework with content, and finally to add in our audio clips. This process was of course hindered by the occasional road blocks in which we needed to troubleshoot.

## Challenges and Associated Lightbulbs

**Challenge One**

During this assignment, my team and I encountered a good number of road blocks. I’ll try to go in order so as to aid in the understanding of the progression of the project. One of the very first road blocks that I encountered was when I created the assignment repository in the newassignment6 workspace. I realized later that I didn’t have pandoc installed for some reason even though assignment three was also in that workspace (assignment 3 was the activity where we played with pandoc and worked to convert documents between document types). When I tried to run the script with the command `./build-presentation.sh` the system would return: command not found. To remedy this issue, I looked back into the notes from the assignment 3 days and found the command to install pandoc and it worked

**Challenge Two**

Once we figured out the pandoc situation, Erin and Amanda created the repository within a workspace that already had pandoc installed so they didn’t have to mess with installing it again. Then, we looked into creating the script that builds the index.html file each time it is run. We had issues with this because we weren’t quite sure of the concept behind it. We tried to use the command as follows: `pandoc -t revealjs --template=$TEMPLATE -s --variable theme="$THEME" --variable transition="$TRANSITION" --variable revealjs-url="./" machinelearning.md -o machinelearning.html`
We realized soon that it would be a lot easier to name the file that the pandoc command converts the markdown file to `index.html` in order to better understand what was happening. We didn’t realize that each time we ran the script, pandoc would overwrite the current index.html document instead of making a new one. This made things so much easier!

**Challenge Three**

Once we finally figured out how to format the script and markdown file, we were then able to fill in our information into the markdown framework. The problem we ran into with this step, however, was how to format the audio files. We didn’t want to download the program suggested in the notes (.ogg) so instead we decided to create .mp3. This almost worked until we realized that we needed to change the audio file type in the template-index.html from .ogg to .mp3. Once we figured this out we were good to go! Once we figured out a format, we were able to just do the same thing over and over again for each slide. Generally, we had a `#` to indicate a new slide. Then we had the audio: `<section data-audio-src="audio/slide01.mp3" data-background="#56A0D3"> </section>`. Then we added any text that we needed, followed by the aside notes which contained the script that we each said on each slide using the aside tags: `<aside class="notes"></aside class="notes">`.

** Special Lightbulb Moment**

Something that I discovered while working on this project is that you can incorporate a .gif file into html in the same way you incorporate a picture! This was a special “A-ha” moment for me because it didn’t require a problem to arise before I discovering it.

**Challenge Four**

 Once we finally got this done and we previewed it, we realized that for some reason, our audio that we were hoping to play on the first slide wasn’t playing until the second, empty slide. We also realized that the audio from the example project was playing on our third slide! In order to fix this, we decided to delete all of the old example’s audio files from our directory. In addition, we moved the audio file for the introduction from the title slide to slide01. This fixed both the problem of the introductory audio playing on an empty slide as well as the old example’s audio playing. 
 
**Challenge Five**

After we got the basics of our presentation down. We decided to try to alter the theme of the whole presentation. To do this, we went to the build-presentation.sh file and altered the `THEME` section to #56A0D3, which is a shade of blue, to match the body slides. This was probably a huge mistake as it took a very long time to fix. Instead of changing all of the slides to blue, it also changed the font, font size, text placement, and picture placement of all of the slides as well as changing the background color to white! We attempted to fix this but after several failed attempts, we decided to change it back to the original. When even this didn’t work, we were at a loss! We then decided to try to revert the commit that we had made to make the change to the theme. It took several tries to get the formatting down right for the command, but we finally did it by doing `git log` to find the correct commit we were talking about, then copying the hash (the random combination of numbers and letters), and doing `git revert HASH`. This finally got our presentation back to the way it was originally! 

**Various Other Challenges**

While the challenges I listed above may seem sufficient, we actually experienced even more, I just listed the significant ones. We experienced a number of merge conflicts in which one of us forgot to pull before pushing and committing, so we became better at dealing with these issues. 

## Skills Gained from Project and How They’ll Help in Future Studies/Career

This project more than any other helped me to improve upon my troubleshooting skills. Being able to utilize available resources and become more independent when faced with problems is an essential skill when working in the “real world”. This skill is especially important as a new hire fresh out of college. Not only does troubleshooting skills help in the workforce, but also in future studies. I hope to continue onto a master program in analytics, whether it be straight out of undergrad, or after working for a couple of years. Either way, being patient and resourceful is a skill that can apply to various areas of study and will prove beneficial. 

## Conclusion

Overall, this project has proved beneficial to my development as a student and an information science minor. 

