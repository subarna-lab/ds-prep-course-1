# Data Science Prep Course Repository

Welcome to Data Science Prep Course repository. Here is you'll find all information needed to setup your environment and the
workflow you'll use during the Prep Course.

1. [Initial Setup](#initial-setup)
    1. [Windows Setup](#Windows-Setup) Miguel (up for review)
    1. [Setup _Git_/_GitHub_](#setup-_git__github_) Hugo
    1. [Setup your Workspace Repository](#setup-your-workspace-repository) Hugo
    1. [Get the Learning Material](#get-the-learning-material) Hugo
    1. [Running a Learning Unit](#running-and-submitting-a-learning-unit) Hugo
1. [Learning Unit Workflow](#learning-unit-workflow) Hugo
1. [Updates to Learning Units](#updates-to-learning-units) Miguel (up for review)
1. [Help](#help) Miguel
    1. [Learning Unit Workflow](#learning-unit-workflow) Miguel
    1. [Other](#other) Miguel (up for review)

## Initial Setup

**IMPORTANT**
Before the bootcamp you will have to complete these instructions, this is 
essential.

Once you complete the setup mark yourself as such on [this spreadsheet](CREATE A SPREADSHEET WITH STUDENTS' NAMES).
Make sure that you complete the setup by the 30th of March, as the course will begin on that day. If you are struggling to install any of the software to be mentioned below, tell us ASAP! The course by itself will be very intensive, so we do not want to you waste 5 hours on the setting up part!! 

By completing this you will setup and learn about all the tools you'll be
using during the academy. We will also be able to identify any problems in time to figure out a solution.


### Windows Setup

This section deals with setting up either Windows Subsystem for Linux (WSL)
or VMWare. 
If you are using MacOS or Linux you can skip this section.

Follow [this guide](guides/Windows_Subsystem_for_Linux_Installation_Guide_for_Windows_10.md) if you are running Windows 10.

If you are running Windows 7, follow the guide bellow on running Ubuntu with Windows 7 with VMware Player. You'll be required to download VMware and Ubuntu 18, for that please use the links provided bellow.
* [VMware download link](https://www.vmware.com/go/getplayer-win)
* [Ubuntu download link](https://ubuntu.com/download/desktop/thank-you?version=18.04.4&architecture=amd64)
* Follow this guide: [How To Run Ubuntu in Windows 7 with VMware Player](https://www.howtogeek.com/howto/11287/how-to-run-ubuntu-in-windows-7-with-vmware-player/)

### Setup _Git_/_GitHub_

CHANGE SCREENSHOT INTO PREP COURSE-SPECIFIC REPO

Having a _GitHub_ account and knowing the basics of committing and pushing 
changes are mandatory.
By the end of this setup you will have accomplished both.

1. Install [_git_](https://git-scm.com/)
If you're on Windows or OS X, [_GitHub Desktop_](https://desktop.github.com/) is 
probably easiest.
1. [Sign up](https://github.com/join) for a _GitHub_ account if you don't 
already have one.

If you plan on using the terminal and not _GitHub_ desktop it might be a good
idea to [set up ssh keys](https://help.github.com/articles/connecting-to-github-with-ssh/)
for _GitHub_.

### Setup your Workspace Repository

It's good practice to store your work with version control. 
In this academy that is a requirement as it is how you will make your work
available to us.

#### Creating the Workspace

CHANGE THIS PART INTO CLONING THE REPO

1. Log into _GitHub_
1. Create a new **private** _GitHub_ repository called *batch3-workspace*, see 
[Creating a new repository](https://help.github.com/en/articles/creating-a-new-repository). 
**IMPORTANT** The repo **MUST** be named *batch3-workspace*! 
If you name it anything else, you will be unable to submit any of your work!
    1. You need to explicitly select Private - This is your work and nobody else's. 
    You will be graded based upon the merits of what you are able to do here 
    so this should not be open to the world while you are working
    on it. 
    Maybe after the course is completed, you can open-source it but not this 
    time.
    1. Initialize with a README. 
    This is mostly just so that you don't initialize an empty repo.
    1. Add a Python `.gitignore`.
    This step is insanely important. If you don't do this, you may
    end up checking things into the repo that make it un-gradeable by our 
    grading system.
    ADD THE `.gitignore` PLEASE!!!! <--- 4 * `!` isn't enough

![Create Repository](assets/create_repository.png "Create Repository")


#### Cloning the Workspace

1. Open a Terminal or Git Bash, the next steps are on this terminal
1. Clone your _<username>/batch3-workspace_ repository
```bash
git clone https://github.com/<username>/batch3-workspace.git
```

Or if you have your ssh keys set up:
```bash
git clone git@github.com:<username>/batch3-workspace.git
```

### Get the Learning Material

You will be cloning the [batch3-students](https://github.com/LDSSA/batch3-students) 
repository.
All of the learning material you need will be made available on this repo
as the academy progresses.

1. Open a Terminal or Git Bash, the next steps are on this terminal
1. Clone the students repository 
[batch3-students](https://github.com/LDSSA/batch3-students)
```bash
git clone https://github.com/LDSSA/batch3-students.git
```
Or if you have your ssh keys set up:

```bash
git clone git@github.com:LDSSA/batch3-students.git
```

### Running Learning Unit

In the `batch3-students` repository that you just cloned there is a sample
learning unit.
It's used to give instructors guidelines to produce the learning units.
We are also using it to ensure that you are able to run and submit a learning 
unit.

So go ahead and copy the sample directory `sample/SLU00 - LU Tutorial` from the `
batch3-students` repository to your repository (named `batch3-workspace`).
![Sample learning unit](assets/sample_learning_unit.png "Sample learning unit")

The grader only requires you to have the contents in a directory starting with
the learning unit's ID, but we highly advise to keep the same directory 
structure as the students repository.
All learning units are organized as: 
```
<specialization ID> - <specialization name>/<learning unit ID> - <learnin unit name>
```
Doing so will help you keep organized and ease copying data from the students
repository to yours.

#### Creating Python Virtual Environment

TODO

#### Working on the Learning Unit

All learning units come as a set of Jupyter Notebooks (and some links to
presentations).
Notebooks are documents that can contain text, images and live code that you
can run interactively.

In this section we will launch the Jupyter Notebook application.
The application is accessed through the web browser.

Once you have the application open feel free to explore the sample learning
unit structure.
It will give you a handle on what to expect and what rules the instructors
follow (and the effort they put) when creating a learning unit.

So let's start the Jupyter Notebook app.

1. Activate the environment and run jupyter notebook
```bash
conda activate slu00
jupyter notebook
```

##### The Exercise Notebook

Every learning unit contains an exercise notebook with exercises you will
work on.
So let's have a look at the sample Learning Unit. 
1. On the Jupyter Notebook UI in the browser open the exercise notebook
![Open exercise notebook](assets/jupyter_exercise_notebook.png "Open exercise notebook")
1. Follow the instructions provided in the notebook

Besides the exercises and the cells for you to write solutions you will see
other cells with a series of `assert` statements.
This is how we (and you) will determine if a solution is correct.
If all `assert` statements pass, meaning you dont get an `AssertionError` or
any other kind of exception, the solution is correct.

Once you've solved all of the notebook we recommend the following this simple 
checklist to avoid unexpected surprises.
1. Save the notebook (again)
1. Run "Restart & Run All"
![Restart & Run All](assets/jupyter_clear_and_run.png "Restart & Run All")
1. At this point the notebook should have run without any failing assertions

If you want to submit your notebook before it is all the way done to
check intermediate progress, feel free to.

If you are able to go through the entire process and get a passing grade on 
the sample LU you'll have a good understanding of the same flow that you'll use
for all LUs throughout the academy.

#### Commit and Push

Now you have worked on the sample learning unit and you have some uncommitted 
changes.
It's time to commit the changes, which just means adding them to your `batch3-workspace`
repository history, and pushing this history to you remote on _GitHub_.

1. Using the terminal commit and push the changes
```bash
git add .
git commit -m 'Testing the sample notebook'
git push
```

## Learning Unit Workflow

Learning units will be announced in the academy's _#annoucements_ channel.
At this point they are available in the 
[batch3-students](https://github.com/LDSSA/batch3-students) 
repository.

The steps you followed during the initial setup are exactly what you are going
to be doing for each new learning unit.
Here's a quick recap:
1. Once a new learning unit is available pull the changes from the 
[batch3-students](https://github.com/LDSSA/batch3-students) repo.
1. Copy the unit to your `batch3-workspace` repo
1. Work
1. Once all tests pass or once you're happy, commit the changes and push
1. Profit

## Updates to Learning Units

As much as we try and have processes in place to prevent errors and bugs in 
the learning units some make it through to you.
If the problem is not in the exercise notebook you can just pull the new 
version from the ds-prep-course repo and replace the file.
The problem is if the correction is in the exercise notebook, you can't just
replace the file because your work is there and you'll lose it!

When a new version of the exercise notebook is released (and announced) you will have to merge the work you've already done into the new version of the
notebook.

At the moment our suggestion to merge the changes is: 
1. Rename the old version
1. Copy the new exercise notebook over
1. Open both and copy paste your solutions to the new notebook

We understand it's not ideal and are working on improving this workflow.

## Help

During the prep-course you will surely run into problems and have doubts about the
material.
We provide you with some different channels to ask for help.

### Learning Unit

If you feel something is not clear enough or there is a bug in the learning
material please follow [these steps](https://github.com/LDSSA/wiki/wiki/How-to-ask-for-and-give-help). Remember, there is no such thing as a dumb question, and by asking questions publically you will help others! 

If you have more conceptual questions about the materials or how to approach a problem you can also
reach out to the instructors on slack.
You can find the main contact for the learning unit in the
[_XXXX) this instructor can help you out or redirect you to someone that is available at the moment.


### Other

If your problem doesn't fit in any  of the previous categories head over to
slack and ask.
Someone will surely point you in the right direction.

If you're looking for some specific part of our organization head over to the
[Member Directory](https://github.com/LDSSA/wiki/wiki/Member-Directory)
and search for the area of responsibility you're looking for.

