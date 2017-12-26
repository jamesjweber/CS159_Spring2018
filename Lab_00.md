# Lab 0: Getting Started

## Welcome

Welcome to **CS 159**! In this class, we aim to teach you the basics of the C programming language, a powerful and widely used coding language. This class will teach you *invaluable* coding skills and etiquette that you can use for the rest of your life. 

## My take on the class

As a Junior in computer engineering, this was probably one of the most important classes I took to get me to where I am. Before college I had *never* coded before. Now I can code in `C`, `C++`, `Matlab`, `Java`, and `Swift` (the coding language for iPhones), and can pretty easily pick up languages I've never had much experience in. While this class is not perfect in many ways, I belive it is a necessary stepping stone in helping students in their coding careers. I know that coding is not everyone's cup of tea, but I hope to help make your experience as easy as possible in this class!

## Common Complaints

### C is an outdated language/This class is useless

Well yes, and no. Let me explain. Usually if you google `"Most used coding languages 2018"`, you will usually find a list like [this](https://stackify.com/popular-programming-languages-2018/) which ranks `C` as the ***second most used language*** in the world. However, if you google `"Best coding languages to learn 2018"`, [almost](http://merehead.com/blog/top-programming-languages-2018-learn/) [every](http://www.codingdojo.com/blog/7-most-in-demand-programming-languages-of-2018/) [article](https://medium.com/swlh/best-10-programming-languages-to-learn-in-2018-2d6cbc5ffc2a) you will find does ***NOT*** include `C`. This is because `C` is what is called a `low level` coding language. This means it's *extremely efficient* when it's ran. This was much more useful in the 70's and 80's when computers were just starting to take off. Since computers were so new, resources, such as memory, were very limited, so code needed to be efficient. Fast forward to 2018, we now have a [**TRILLION FOLD INCREASE**](https://gizmodo.com/the-trillion-fold-increase-in-computing-power-visualiz-1706676799) in computing power. This means that this computing power can be used for more advanced `object oriented` languages such as `Java`. These `object oriented` languages allow for much cooler applications such as `machine learning`. So, while this class will most likely not land you any sort of coding related job, it is an extremely useful to learn because a lot of these `higher level` languages (`Java`, `Matlab`, `C#`, `C++`, `Objective-C`, `Swift`, etc.) are heavily influenced by `C`. Once you learn `C` it is *very* easy to pickup a new language.

### I *hate* Putty (Read at the end of lab)

Perfect! I do too! Putty is useful because it gives you access to powerful `Command Line Tools`, but usually it's more of a nuisance than it is helpful. I've compiled two tutorials, one for [Windows](https://github.com/jamesjweber/CS159_Spring2018/blob/master/How%20to%20Install%20and%20Use%20Atom%20for%20Windows.md), one for [Mac](https://github.com/jamesjweber/CS159_Spring2018/blob/master/How%20to%20Install%20and%20Use%20Atom%20for%20Mac.md) on how to install a `text editor` to make editing your code *a lot* easier!

### I already know how to code!

Yeah sorry, this class might be a drag for you :(

## Preface (HIGHLY RECOMMENDED READ)

### WTF is going on?

Ok, so in today's lab you will setup your account for this class so that you can turn in homework and labs. This can be a very confusing lab, especially if you've never used a `command line` before. So, let's explore what a `command line` is. 

A `command line` is a tool that you can use to `textually` navigate your computer. What does `textually` navigate mean you say? Well first let's explore what it means to `graphically` navigate. 



`Graphical` navigation is primarily how you interact with your computer and your phone nowadays. You **click** on graphical objects (like an icon or the windows home button) and the computer will take different actions based on the `graphic` you **clicked**. Here I am graphically moving an example file from my Dektop to another file on my Desktop.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/graphicalNavigation.png)

So, `textual` navigation is simply navigating you computer *using only your keyboard* instead of with a mouse. You give the computer `commands` in the `command line`, and it will complete an action based on those `commands`

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/textualNavigation.png)

Note that we get the same result either way: 

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/resultNavigation.png)

The file has been moved to the folder. Now obviously it's a lot more *confusing* to use commands, which is why all computers and phones have `GUI's (Graphical User Interfaces)` now.

# Starting the Lab

## Ok I still don't know what's going on...

That's ok, you're not expected to, but hopefully I can walk you through this lab and make it pretty easy to understand.

## Step 1: Setup Putty

### What is Putty?

Putty is a `client` that allows you to connect to `ITAP's` servers that you will write all your code on. Once you have it all configured it will bring up a `command line` in which you can navigate your CS159 files for labs and homeworks.

### Open Putty

From the `Start` button select `All Programs -> Standard Software -> Telecommunications -> Putty`, and then launch the `putty .63` application.

![](http://web.ics.purdue.edu/~wcrum/cs159/images/lab00/fall15/puttyItap.png)

It should look something like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/puttyLaunchScreen.png)

### Configure and Save Your Session

#### What's a Session?

A `session` is simply a configuration to a certain server. For this class we connect to `ITAP's guru server`. This makes it easier for us so we don't have to type a complicated server name in every time

#### The Setup

1. Under **Host Name (or IP address)** enter: `guru.itap.purdue.edu`

2. Select a name for your **Saved Session**, usually we just call it `guru`

3. Press the `save` button so that you can easily load this session in the future.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/puttyGuruSetup.png)

### Apperance

This just changes how your `terminal` (`command line`) will look. You will want to use these settings to make it more readable!

#### Text Size

On the side menu, navigate to `Appearance`, which is right under `Window`. Click `Change...` and set the font size between `14`-`18`. This will make the code larger, and make your eyes less strained as you code.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/puttyTextSize1.png)

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/puttyTextSize2.png)

#### Colors

Select `Colours` (under `Window`) from the side menu. Then select the `Use system colours` checkbox. This will automatically color parts of your code. This just makes it visually easier to sift through your code.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/puttyColors.png)

### Saving Your Session

Go back to the `Session` tab from the menu. Make sure `guru` is still selected, and click `Save`.

Next time you launch `PuTTY`, you can simply click `guru` then click `Load` to load these settings again.

## Step 2: Connecting to the ITAP server

Ok, so now that you've got all your settings configured, simply press `Open` to connect to the server. (Note: You need to be connected to PAL to be able to do this).

You may get a warning like this: 

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/loginWarning.png)

Don't worry about it, just press `Yes` to continue.

### Logging In

Now, you should be at a screen that looks like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/login.png)

Input your `Purdue username` for the `login as: ` prompt. Then it will ask you for your `password`. Just type in your `Purdue password` and press `enter`. 

### VERY IMPORTANT NOTE: Your password does not show up for security measures, so if you type and nothing shows up, your computer is not broken! It's working as expected!

So once you login, you should be brought to a screen that looks like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/loginInitialPrompt.png)

Don't worry if it says something about a `VPN`. You are now in the `terminal` and the `█` charachter is where you can enter `commands`.

### Setting Up Your Account for the Semester

Now that you've successfully connected, we can setup your account using the following command (just copy and paste it, right click in putty to paste): `~cs159/student/setup`

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/loginSetupCommand.jpg)

This will setup your account so that you can use the "tools of the course" this semester including **the ability to submit your programming assignments**.

#### A few things to note:

- You do **NOT NEED TO** modify this command if you are in `CS158`

- You still **NEED TO** run this command if you have previously taken the course!

- You only have to run this command once! And that's in this first lab. So if you setup `PuTTY` on your own computer, do **NOT** run this command again! It could wipe your current work!

Once you run it, it should give you this message: 

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/setupCommandFinished.png)

### What the heck did that command do?

- A folder named after the course **CS159** has been created in your career account. Within this folder are two additional folders, one for homework assignments and another for lab assignments. Within those folders are even more folders, one for each assignment. This is done to help you organize your work. Students have made the mistake in the past of placing all source code files in the same folder and then submitting the wrong one for grading.

- Several files were copied or changed in your account to permit you to access important course tools and configurations of your `UNIX` account have been applied to make working on the server easier. You may see these files if you access your career account through another source, it is our advice that you do not delete any files that begin with a dot if you don't know why they are in your account.

### Logging Out

Either type `logout` and press enter, or just close `PuTTY` to logout. Then open `PuTTY` again, and login using the steps above.

Now it should look pretty similar, but with a welcome message that says something like **"Welcome to CS 159! Spring 2018 semester!"**

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/welcomeMessage.jpg)

### Issues?

If any problems arise while setting up your account, just raise your hand and I'll help you figure it out!

## Step 3: Navigating the Terminal

Ok now that you're all setup, we need to navigate to the first lab file. We will do that by typing in specific `commands` to help us find our way around.

### How it all works

So now that you're in your terminal, you are really just inside a folder on one of Purdue's servers. You can navigate around these folders using `commands`. This is basically the equivalent of opening `Windows Explorer` and clicking different files, the only difference is that you are using your keyboard to navigate, instead of a mouse. (See the `preface` for a more detailed description).

The first two commands we will work with are `cd` and `ls`. These are two very powerful commands that help us navigate our folders. 

### LS (listing)

`ls` is short for `listing` and will display (or list) the name of all files and folders in the folder you are currently in. So you can see below that if I go into my example CS159 folder on my computer and type `ls` it displays all the files and folders in that folder.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/ls_cd_example.png)

Hopefully this picture illustrates the parallel between the `Graphical User Interface` of your computer, and the `Text-Based User Interface` of the `terminal`.

### CD (Change Directory)

`cd` is short for `change directory`. This allows you to go from one folder to another. So for example, in the example above, I had to type `cd Desktop/CS159` to get from my `root folder` (the base folder in your computer that holds all other folders) to the `CS159` example folder.

### Putting it all together

So, let's use these commands to get to your first lab file (`lab00.c`). 

1. Type `ls` if you'd like to see all the folders in your `ITAP root directory`. You should see a folder called `CS159`. This is the folder we want to go into. 
![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/listRootDirectory.png)

2. Type `cd CS159`. This shouldn't display anything. If you want to see what's in this folder, type `ls`.

3. You should see that there are `hw/` and `labs/` folders. These are where you will save all your files for the rest of the semester.

4. Type `cd labs` to enter the `labs` folder. Type `ls` again. You should see folders for all the labs this semester.

5. Today we are interested in `lab00/`, so type `cd lab00`. Once you are in this folder `ls` to see the contents.

6. There should be a single file called `lab00.c`. This is the file we want to edit!

All in all your terminal should roughly look like this at the end:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/allCommandsLab00.png)

### Power moves only!

Obviously navigating through your folders like this is really annoying and tedious, so here's some power moves to make life a little easier.

- You can `cd` through multiple folder, so instead of doing a single `cd` command at each folder level (i.e `cd CS159`, ``cd labs`, `cd lab00`), you can put all of the folders in one line like this: `cd CS159/labs/lab00`

- Now that's still a lot of typing, you can save yourself time by typing in part of the name and pressing `tab`, it will autocomplete the folder name for. For example, you can type `cd CS` the press `tab` and it will autocomplete to `cd CS159/` for you!

- You can go back to the `root directory` by typing `cd` by itself. However, sometimes, you only want to go up one folder level, to do this, just type `cd ..` to go back one folder level!

- Terminal is really weird about spaces so make sure to never have a space in your file/folder name. Instead either concatenate the text with camel case (`sampleFile.c`), or use the underline charachter (`sample_file.c`).

- Lastly, sometimes you will want to use a command that you just typed. You can use the `up` and `down` arrows to scroll through previous commands.

[Click here](http://web.ics.purdue.edu/~wcrum/cs159/unix_vi.pdf) for a cheat sheet of `commands` that you can use.

## Step 4: Editing the lab file

So now that you are in the `lab00` folder, we need to edit the file. To enter a file, type `vi lab00.c`. `vi` is a text editor (similar to word or notepad), but it does not have a `graphical` interface (i.e. you must use a keyboard to interact with it, your mouse won't do much). This is the official way to edit your files for this course. Later on I'll talk about alternatives, but for now we'll stick with `vi`. Once you open the file, it should look like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/lab00.png)

This is the basic structure of all C programs, you aren't expected to undestand it all, but you should be able to see that it prints out `Welcome to CS 159!`

### What you need to do for this lab

All you need to do for this assignment is change the `emails` in the `header` (the blue part of the file with all the stars) to your **PURDUE** email, as well as *my email* which is **weber99@purdue.edu**.

### How to edit the file

You might notice a few things as you start to try editing the file:

When you try to scroll, it doesn't scroll the file, but it scrolls back to the terminal screen??? This is unfortunately the way `PuTTY` is. In order to scroll, you must use the `up` and `down` arrows.

When you type, you might notice that you can't put text into the file. This is because you are in `command` mode. In this mode you can only `read` text from the file, but you cannot `write to it`. In order to `edit` the file, you must go into `insert` mode. To do this press `esc`, then press `i`. The bottom of your screen should change and say `-- INSERT --`. It should look something like this:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/insertMode.png)

Now if you type, text will be entered wherever your `cursor (█)` is. Text can be deleted using `backspace`.

So now, go to the part of the file with the example logins. Replace `login1@purdue.edu` with your email, and replace `login2@purdue.edu` with my email (`weber99@purdue.edu`). If there is a third email, delete that line.

### How to exit and save

To exit, we must get *out* of `insert` mode and get back in `command` mode. To do this, simply press `esc` and the bottom line should be cleared (i.e. it shouldn't say `-- INSERT --` anymore).

Now that we are in command mode type `:wq` this should show at the bottom of the screen in the `command line` as shown here:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/writeQuitCommand.png)

#### What this command means

`:wq` is a simple command that does two things. First it `writes (w)`, or saves, your file. Then it `quits (q)` or exits your file.

## Step 5: Compile, Execute, and Submit Your Lab

### Compiling your program

#### What is compiling

Compiling basically just takes your program, written in `C` and converts it to `1's` and `0's` that your computer can use.

#### How to compile

In the `command line` (i.e not in the `lab00.c` file), enter the command: `gcc lab00.c`. `GCC (GNU C Compiler)` will compile your file and output a file that your computer can use called `a.out`. You can see this file if you use the `ls` command. `a.out` is an arbitrary file name that the compiler gives the `executable file`. It's just called that cause it's really short and easy to type.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/compiledFile.png)

### Executing your program

Once the `a.out` file has been generate simply type `a.out` to run your program. For this file, it should output `Welcome to CS 159!` to the terminal.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/fileRun.png)

### Submitting Your Code

This is *by far* the most important part of the lab. Submitting your code is the only way to get your code graded, so make sure you do it correctly!

- **Multiple submissions can made for all assignments**. The new submission will overwrite the old.

- **It is only the final submission that is retained and graded**. All previous submissions are lost and cannot be restored.

- In a lab assignment the collaborative group must designate who will be making the submissions for the group. **Only that individual must make submissions and only that person has the ability to overwrite his/her previous submissions. (Except for this lab, you will individually submit for this lab).** 

- You must be in the same directory as the file you want to submit.

- Only source code files will be submitted, `executable files (a.out)` will never be submitted.

- Submission does require you to connect to the server but you do not necessarily have to be on campus to make a submission.

Enter the `submit` command from the same directory as your `lab00.c`. You should see this prompt appear:

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/submit_1.jpg)

Type the name of the file you wish to submit (i.e. `lab00.c`). The file name **must match the expected file name** for it to sumbit properly. 

Type `lab00.c` and press enter. It will ask you if you wish to continue, as part of an academic integrity acknowlegement, just type `Y` to continue. Once you do this it should say something like `lab00.c was submitted by yourPurdueUsername`

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/submit_2.png)

You should also get a confirmation email that your file was submitted.

![](https://raw.githubusercontent.com/jamesjweber/CS159_Spring2018/master/ImageResources/emailConfirmation.png)

#### Things to check

- In the email, make sure the `Section` is **not** `99999` (like the picture above), if it is, that means your account is not setup properly!

- Check with me once you've got your email. **I need to confirm that I also got the email, so that way I can properly grade your assignments in the future!**

## You're done!

Once you've confirmed your submission with me, all you have to do is take the quiz and you are done.

Note: Depending on which professors section I'm TAing for, you may not be able to take the quiz until the end, or you may need a password. At the time of writing this, I do not know which professor I'm working for, and therefore can't tell you when the quiz will be. Just ask me in lab, I will know by then!
