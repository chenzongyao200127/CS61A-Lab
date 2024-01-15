# Project 2: CS 61A Autocorrected Typing Software

# Introduction

In this project, you will write a program that measures typing speed. Additionally, you will implement typing autocorrect, which is a feature that attempts to correct the spelling of a word after a user types it. 
This project is inspired by typeracer.

# Final Product

Our staff solution to the project can be interacted with at cats.cs61a.org - if you'd like, try it out now! When you finish the project, you'll have implemented a significant part of this game yourself!

# Download starter files

You can download all of the project code as a zip archive. This project includes several files, but your changes will be made only to cats.py. Here are the files included in the archive:

cats.py: The typing test logic.
utils.py: Utility functions for interacting with files and strings.
ucb.py: Utility functions for CS 61A projects.
data/sample_paragraphs.txt: A file containing text samples to be typed. These are scraped Wikipedia articles about various topics.
data/common_words.txt: A file containing common English words in order of frequency.
data/words.txt: A file containing many more English words in order of frequency.
gui.py: A web server for the web-based graphical user interface (GUI).
gui_files: A directory of files needed for the graphical user interface (GUI).
images: A directory of images.
ok, proj02.ok, tests: Testing files.
The CATS GUI is an open source project on Github.

# Logistics

The project is worth 20 points. 17 points are assigned for correctness of your final code, 1 point for submitting Phase 1 by the checkpoint deadline, and 2 points for composition.

You will turn in the following files:

`cats.py`
You do not need to modify or turn in any other files to complete the project. To submit the project, run the following command:

`python3 ok --submit`

You will be able to view your submissions on the Ok dashboard.

For the functions that we ask you to complete, there may be some initial code that we provide. If you would rather not use that code, feel free to delete it and start from scratch. You may also add new function definitions as you see fit.

However, please do not modify any other functions. Doing so may result in your code failing our autograder tests. Also, please do not change any function signatures (names, argument order, or number of arguments).

Throughout this project, you should be testing the correctness of your code. It is good practice to test often, so that it is easy to isolate any problems. However, you should not be testing too often, to allow yourself time to think through problems.

We have provided an autograder called ok to help you with testing your code and tracking your progress. The first time you run the autograder, you will be asked to log in with your Ok account using your web browser. Please do so. Each time you run ok, it will back up your work and progress on our servers.

The primary purpose of ok is to test your implementations.

We recommend that you submit after you finish each problem. Only your last submission will be graded. It is also useful for us to have more backups of your code in case you run into a submission issue.

If you do not want us to record a backup of your work or information about your progress, you can run

`python3 ok --local`

With this option, no information will be sent to our course servers. If you want to test your code interactively, you can run

` python3 ok -q [question number] -i `

with the appropriate question number (e.g. 01) inserted. This will run the tests for that question until the first one you failed, then give you a chance to test the functions you wrote interactively.
You can also use the debug printing feature in OK by writing

` print("DEBUG:", x) `

which will produce an output in your terminal without causing OK tests to fail with extra output.


# Phase 1: Typing

## Problem 1 (1 pt)
Implement choose, which selects which paragraph the user will type. It takes a list of paragraphs (strings), a select function that returns True for paragraphs that can be selected, and a non-negative index k. The choose function return's the kth paragraph for which select returns True. If no such paragraph exists (because k is too large), then choose returns the empty string.

Before writing any code, unlock the tests to verify your understanding of the question.

`python3 ok -q 01 -u`

Once you are done unlocking, begin implementing your solution. You can check your correctness with:

`python3 ok -q 01`


## Problem 2 (2 pt)
Implement about, which takes a list of topic words. It returns a function which takes a paragraph and returns a boolean indicating whether that paragraph contains any of the words in topic. The returned function can be passed to choose as the select argument.

To make this comparison accurately, you will need to ignore case (that is, assume that uppercase and lowercase letters don't change what word it is) and punctuation.

Assume that all words in the topic list are already lowercased and do not contain punctuation.

Hint: You may use the string utility functions in utils.py.

Before writing any code, unlock the tests to verify your understanding of the question.

`python3 ok -q 02 -u`

Once you are done unlocking, begin implementing your solution. You can check your correctness with:

`python3 ok -q 02`
