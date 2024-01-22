# Problem Set 2
### Due Friday, January 26, 2024, at 11:59pm EST


### Accessing and submitting the problem set

As with PS1, you will be accessing and submitting this problem set using GitHub Classroom. As a reminder, here's how that goes:

1. Accept the invitation you found on Canvas in Problem Set 2 (which you have already done if you are here).

2. [Read PS1 Part 4 to review how to clone a problem set repository using GitHub Desktop and how to work on it locally.](https://github.com/CSCI1090-S24/ps1/blob/main/README.md#part-4-clone-your-copy-of-the-repository-to-your-own-machine) **As described in PS1, you need to remember where you cloned your repo to on your own machine!**

3. Edit the files on your computer in this repository as described in the sections below.

4. [Reead PS1 Part 9 to review how to submit your work using GitHub Desktop from your local machine up to GitHub on the internet.](https://github.com/CSCI1090-S24/ps1/blob/main/README.md#part-9-commit-your-work-to-github-classroom-using-the-github-desktop-app). Remember that you can commit and push your work as many times as you like. I recommend doing it often so that you have a backup of your work in case your computer breaks!

**NOTE: This respository is nearly empty. That's because you will be creating Python programs yourself, putting them (or creating them) in this directory, and pushing and committing them to GitHub.**

### Deliverables

1. `ps2-part1.py` (Part 1)
2. `ps2-part2.py` (Part 2)
3. `ps2-part3.py` (Part 3)
4. `ps2-part4.py` (Part 4)

### Important Guidelines
* Your problem set must be submitted with GitHub. If you are struggling to use GitHub, the TAs can help!
* You do not need to do error checking. You can assume the user will always enter the kind of iput you ask for.
* Comments are not required yet, but they are strongly encouraged so that we can give you extra credit.
* Points will be deducted if your output does not match the required format.
* Points will be deducted if your files are not named as required.
* Points will be deducted if your files are not in the correct location (i.e., in the top-level directory where you see the `README`.)

---

## Part 1: Math with user input

First, you are going to create a Python file in IDLE. Here's how to do that. You will be doing this for parts 2, 3, and 4, as well, so pay attention.

1. Launch IDLE.
2. Go to `File -> New file`. A new window will open.
3. Go to `File -> Save`. A dialog window will pop up where you can enter the name of the Python file and where you want to save it:

<img src="img/savefile1.png" width="500">

5. Enter the file name `ps2-part1.py` in the `Save As` box.

6. Within the dialog box, you now have to navigate to wherever you decided to clone this PS2 repository.  If you're on a Mac and it's giving you limited options where to save your file, click the little arrow circled in the screenshot below. That will give you a real Finder-type window where you can navigate to wherever you saved the repo.

<img src="img/savefile2.png" width="500">

**Recall that I suggest cloning all your GitHub problem set repos to a folder called `DataScience` or `CSCI1090` on your Desktop or in your Documents folder. You can go look in GitHub Desktop to where you actually cloned this repository.**

6. Now you have a Python program you can edit! This is what you should make your program do.

* Ask the user for an integer between 10 and 100. Save that to a variable called `firstnum`.
* Ask the user for a second integer that is less than 4. Save that to a variable called `secondnum`.
* Repeat back to the user the two numbers that they entered.
* Print out their sum and product.
* Print out the first number raised to the power of the second number.
* Print out the remainder you get when you divide the first number by the second number.

7. When you run your program (`Run -> Run module`), your output must look like the example below. We wil take off points if the words, spacing, capitlization are not the same as the output below. The only thing that will vary will be the information after the colon, which is either provided by the user or is the result of a mathematical operation.

**IMPORTANT: Save your file and test it after each line of code that you write. When you get an error message, it will be easier to determine exactly when and where you introduced an error if you are only testing a small amount of new code.** 

## Part 2: Math with user input using a function

Create a new file called `ps2-part2.py` just as you did above. This program will do what you did in Part 1, but this time you will write your own function to do the math work. Here's how it will go:

1. Write a function called `number_fun()` that takes two integer parameters, `a` and `b`. The function should everything you did above **except** get the input from the user, namely:
* Repeat back to the user the two integers that they entered.
* Print out their sum and product.
* Print out the first number raised to the power of the second number.
* Print out the remainder you get when you divide the first number by the second number.

2. **Outside** (after) the function definition, type code to:

* Ask the user for an integer between 10 and 100. Save that to a variable called `firstnum`.
* Ask the user for a second integer that is less than 4. Save that to a variable called `secondnum`.
* Call the `number_fun()` function, passing in `firstnum` and `secondnum` as the arguments.

When you run your program, your output should look exactly like the output of your program in Part 1.

## Part 3: Target heart rate calculator
In this problem, you will ask a user to provide their age and to choose between two fitness goals. You will then tell them what their target heart rate should be for that fitness goal given their age. Your code will go in a file called `ps2-part3.py`, which you will create as you did for the other problems, above. Here's how your code should work:

1. Write a function, `heart_rate()` that takes two parameters: `age` (an integer) and `goal` (a character, `S` for speed or `E` for endurance). The function should do the following:
* Subtract the user's age from 220 to give their max heart rate, saved as a variable called `max_heart_rate`.
* Print out the user's max heart rate.
* Print out their target heart rate range given their goal.
  - If the `goal` value is `S`, their target heart rate range is 80\% to 100\% of `max_heart_rate`.
  - If the `goal` value is `E`, their target heart rate range is 60\% to 80\% of `max_heart_rate`.
* See the example output below for the exact wording of your output and a few examples.

2. **Outside** (after) the function definition, type code to
* Ask the user their age, which you should save as a variable called `user_age`. See the example output below for the required wording.
* Ask the user if they want to improve speed (`S`) or endurance (`E`). Save the input as `user_goal`. See the example output below for the required wording.
* Call the `heart_rate()` function you wrote above, passing in `user_age` and `user_goal` as the arguments.

When you run your program (`Run -> Run module`), your output must look like the example output below. We wil take off points if the words, spacing, capitlization are not the same as the output below. The only thing that will vary will be the information provided by the user and the result of the mathematical operations.

## Part 4: Recidivism calculator
Recidivism risk scores are used to assess the risk of committing another crime after arrest and are used in bail and early parole decisions.  In Cynthia Rudin’s article [Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead](https://www.nature.com/articles/s42256-019-0048-x) (Nature Machine Intelligence, 2019), Rudin shows how the following simple model based on conditionals is almost as accurate as more complex machine learning models.

<img src="img/reccidivism.png" width="500">

Following the structure you used for Part 2 and Part 3, write a Python program called `ps2-part4.py`. Here's are a few sample runs of the program. Remember that your output must match this output in terms of words, spacing, formatting, etc.

---

## Deadline: Friday, January 26, 2024, at 11:59pm EST

## Deliverables

1. `ps2-part1.py` (Part 1)
2. `ps2-part2.py` (Part 2)
3. `ps2-part3.py` (Part 3)
4. `ps2-part4.py` (Part 4)

## Reminder: Important Guidelines
* Your problem set must be submitted with GitHub. If you are struggling to use GitHub, the TAs or I can help during office hours.
* You do not need to do error checking of user input. You can assume the user will always enter the kind of iput you ask for.
* Comments are not required yet, but they are strongly encouraged so that we can give you extra credit.
* Points will be deducted if your output does not match the requires format.
* Points will be deducted if your files are not named as required.
* Points will be deducted if your files are not in the correct location (i.e., in the top-level directory where you see the `README`.)
