---
title: "Getting Started"
teaching:
exercises:
questions:
- "What is a command shell and why would I use one?"
- "What programs will I be using in class?"
- "How can I find the terminal and what is it?"
objectives:
- "Access the CyVerse Discovery Environment, JupyterLab, and the terminal"
keypoints:
- "The shell gives you the ability to work more efficiently by using keyboard commands rather than a GUI."
- "Everything you need to utilize in class is housed in our JupyterLab app"
- "Login in to CyVerse and launch our class app everyday before class"
---

## What is a shell and why should I care?

A *shell* is a computer program that presents a command line interface
which allows you to control your computer using commands entered
with a keyboard instead of controlling graphical user interfaces
(GUIs) with a mouse/keyboard combination.

There are many reasons to learn about the shell:

* Many bioinformatics tools can only be used through a command line interface, or
have extra capabilities in the command line version that are not available in the GUI.
This is true, for example, of BLAST, which offers many advanced functions only accessible
to users who know how to use a shell.
* The shell makes your work _less boring_. In bioinformatics you often need to do
the same set of tasks with a large number of files. Learning the shell will allow you to
automate those repetitive tasks and leave you free to do more exciting things.
* The shell makes your work less error-prone. When humans do the same thing a hundred different times
(or even ten times), they're likely to make a mistake. Your computer can do the same thing a thousand times
with no mistakes.
* The shell makes your work more reproducible. When you carry out your work in the command-line
(rather than a GUI), your computer keeps a record of every step that you've carried out, which you can use
to re-do your work when you need to. It also gives you a way to communicate unambiguously what you've done,
so that others can check your work or apply your process to new data.
* Many bioinformatic tasks require large amounts of computing power and can't realistically be run on your
own machine. These tasks are best performed using remote computers or cloud computing, which can only be accessed
through a shell.

In this lesson you will learn how to gain access to the shell and tools we will be utilizing this semester.

## How to access the shell

On a Mac or Linux machine, you can access a shell through a program called Terminal, which is already available
on your computer. If you're using Windows, you'll need to download a separate program to access the shell or use Windows PowerShell. The problem with these methods are that they require you to access a remote server which often costs money paid by you, the institution, or a granting agency. Instead, this course has been developed using the _CyVerse Discovery Environment_ which will allow us **free** access to a terminal and server. Functionally, each method works the same.

We will spend most of our time learning about the basics of the shell
by manipulating some experimental data. Some of the data we're going to be working with is quite large, and
we're also going to be using several bioinformatic packages in later
lessons to work with this data. To avoid having to spend time
downloading the data and downloading and installing all of the software,
we're going to be working with data on a remote server already stored for you in our Discovery Environment app.

[First, you will need to create an account on CyVerse by clicking this link.](https://cyverse.org/)

Each of you will have your own username and password. This will
prevent us from accidentally changing each other's files as we work through the
exercises.

After logging in, you will see a screen showing showing three different services we can utilize.

![Image of CyVerse User Portal](../myimages/cyverseoptions.png)

Click on _LAUNCH_ for the Discovery Environment. This screen will ask you to login again utilizing the same information you just used to create your CyVerse account. Follow the onscreen prompts until you reach a screen that looks like this.

![Image of Discovery Environment Entry page](https://github.com/kbieser/shell-genomics/blob/gh-pages/_episodes/myimages/deentry.png)

Once you reach the CyVerse Discovery Environment display, click on the _Apps_ button. I will need to add you to our class team, but once added search for _DataCarpentry_Bieser_ and click _Launch Analysis_. Once you launch the _App_ you need to go back and click on the _Analyses_ button. The app you launched should appear. Move your mouse over the square with the arrow which will say _Go to analysis_ and click it. This next step can take some time especially if you are the first to launch the app that day. Be patient. When the app has loaded you should see this page which lets you know you have successfully launched the app.

![Image of JupyterLab Entry page](https://github.com/kbieser/shell-genomics/blob/gh-pages/_episodes/myimages/jupyterentry.png)

The last step is to click the _Terminal_ button on the bottom left under _Other_. If possible, complete these steps to launch your app everyday before class starts. This will enable us to use our class time most effectively.

## Data Persistence

After a few lessons, we will want to save our work from one class to the next. To do this, a _Data Persistence Jupyter notebook_ was created. At the beginning of every class, you will want to open this notebook. To do so, first click the small _data_ link and then click on _Peristence_Notebook-KB.ipynb_ which will open a new tab that is the notebook. This notebook contains commands that will allow us to save data if we run then properly.

![Image of Data Persistence Jupyter Notebook](_episodes/myimages/datapersistence.png)

A Jupyter notebook functions much like a terminal. Each section of commands is run in a cell. For our notebook, there are 2 cells that will need to be run. The first cell creates a directory so that each student will save their own data to their username. The first cell must be run at the beginning of each class. You run a cell by clicking in the cell and hitting the play button at the top of the notebook. After hitting play, switch to your terminal. Continue to follow the directions in the notebook until you reach cell 2.

~~~
$ iinit
~~~
{: .bash}

This command should generate an irods password prompt.

~~~
Enter your current iRODS password:
~~~
{: .output}

Type the same password you used to login into CyVerse and the Discovery Environment. The password will remain hidden while you are typing. When finished hit enter. If your password is accepted, the terminal will return to the normal command prompt. If you receive an error. Try again from the `iinit` command.

Return to the notebook and his the save button. We will continue with class and return to the notebook at the end of each class.

At the end of class, return to the notebook and click in cell 2. Hit the _play_ button.

If successful you should see this output. Initially the brackets will contain an _*_, but when the save is completed, you will see a number appear in the brackets. This tells you your session has been saved and it is safe to close your session.

~~~
Running recursive pre-scan... pre-scan complete... transferring data...
~~~
{: .output}

You can leave the app running for 48 hours at which point it will automatically be cancelled. For safety, return to Analyses where you launched the app, and click on the three dots to the right of the _Running_ icon. Click on _Complete and Save Outputs_. This saves the session and will allow you to relaunch from your data each subsequent session.

![Image of saving session after class](./img/closesession.png)

## Launching the app after a Data Persistence save
