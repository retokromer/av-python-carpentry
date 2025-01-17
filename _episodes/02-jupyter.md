---
title: "Running and Quitting"
teaching: 15
exercises: 0
questions:
- "How can I run Python programs?"
objectives:
- "Launch the JupyterLab server." 
- "Create a new Python script." 
- "Create a Jupyter notebook."
- "Shutdown the JupyterLab server."
- "Understand the difference between a Python script and a Jupyter notebook."
- "Create Markdown cells in a notebook."
- "Create and run Python cells in a notebook."
keypoints:
- "Python scripts are plain text files."
- "Use the Jupyter Notebook for editing and running Python."
- "The Notebook has Command and Edit modes."
- "Use the keyboard and mouse to select and edit cells."
- "The Notebook will turn Markdown into pretty-printed documentation."
---

## Getting Started with JupyterLab

While many software developers will often use an integrated development environment (IDE) or a 
text editor to create and edit their Python programs we will be using [JupyterLab][jupyterlab] 
during this lesson. 

JupyterLab is an application with a web-based user interface from [Project Jupyter][jupyter] that 
enables one to work with documents and activities such as Jupyter notebooks, text editors, terminals,
and even custom components in a flexible, integrated, and extensible manner. JupyterLab requires a
reasonably up-to-date browser (ideally a current version of Chrome, Safari, or Firefox); Internet
Explorer versions 9 and below are *not* supported.

JupyterLab is included as part of the the Anaconda Python distribution. If you have not already 
installed the Anaconda Python distribution, see [the setup instructions]({{ page.root }}/setup/) 
for installation instructions.

Even though JupyterLab is a web-based application, JupyterLab runs locally on your machine and 
does not require an internet connection.
*   The JupyterLab server sends messages to your web browser.
*   The JupyterLab server does the work and the web browser renders the result.
*   You will type code into the browser and see the result when the web page talks to the 
    JupyterLab server.

> ## JupyterLab? What about Jupyter notebooks?
> 
> JupyterLab is the [next stage in the evolution of the Jupyter Notebook](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html#overview). If you have prior 
> experience working with Jupyter notebooks, then you will have a a good idea of what to expect 
> from JupyterLab. 
> 
> Experienced users of Jupyter notebooks interested in a more detailed discussion of the similarities and differences
> between the JupyterLab and Jupyter notebook user interfaces can find more information in the 
> [JupyterLab user interface documentation][jupyterlab-ui].
>
{: .callout}

## Starting JupyterLab

For this workshop, we start JupyterLab from Anaconda Navigator.

On Windows, click on Start and then Anaconda Navigator in the program list (or search for Anaconda in the search bar and select Anaconda Navigator). On a Mac, open up the finder, and in the Applications folder, double click on Anaconda-Navigator.

At the top of the screen, change the environment from `base` to `amia19`. Then click `Launch` on the JupyterLab tile.

## The JupyterLab Interface

JupyterLab has many features found in traditional integrated development environments (IDEs) but 
is focused on providing flexible building blocks for interactive, exploratory computing.

The [JupyterLab Interface](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) 
consists of the Menu Bar, a collapsable Left Side Bar, and the Main Work Area which contains tabs 
of documents and activities.

### Menu Bar

The Menu Bar at the top of JupyterLab has the top-level menus that expose various actions 
available in JupyterLab along with their keyboard shortcuts (where applicable). The following 
menus are included by default.

*   **File:** Actions related to files and directories such as *New*, *Open*, *Close*, *Save*, etc. The *File* menu also includes the *Quit* action used to shutdown the JupyterLab server.
*   **Edit:** Actions related to editing documents and other activities such as *Undo*, *Cut*, *Copy*, *Paste*, etc.
*   **View:** Actions that alter the appearance of JupyterLab.
*   **Run:** Actions for running code in different activities such as notebooks and code consoles (discussed below).
*   **Kernel:** Actions for managing kernels which, as mentioned above, are separate processes for running code.
*   **Tabs:** A list of the open documents and activities in the dock panel.
*   **Settings:** Common JupyterLab settings can be configured using this menu. There is also an *Advanced Settings Editor* option in the dropdown menu that provides more fine-grained control of JupyterLab settings and configuration options.
*   **Help:** A list of JupyterLab and kernel help links.

A screenshot of the default Menu Bar is provided below.

<p align='center'>
    <img alt="JupyterLab Menu Bar" src="../fig/0_jupyterlab_menu_bar.png" width="750"/>
</p>

### Left Sidebar

The left sidebar contains a number of commonly-used tabs, such as a file browser (showing the 
contents of the directory in which the JupyterLab server was launched!), a list of running kernels 
and terminals, the command palette, and a list of open tabs in the main work area. A screenshot of 
the default Left Side Bar is provided below.

<p align='center'>
    <img alt="JupyterLab Left Side Bar" src="../fig/0_jupyterlab_left_side_bar.png" width="250"/>
</p>

The left sidebar can be collapsed or expanded by selecting “Show Left Sidebar” in the View menu or 
by clicking on the active sidebar tab.

### Main Work Area

The main work area in JupyterLab enables you to arrange documents (notebooks, text files, etc.) 
and other activities (terminals, code consoles, etc.) into panels of tabs that can be resized or 
subdivided. A screenshot of the default Menu Bar is provided below.

<p align='center'>
    <img alt="JupyterLab Main Work Area" src="../fig/0_jupyterlab_main_work_area.png" width="750"/>
</p>

Drag a tab to the center of a tab panel to move the tab to the panel. Subdivide a tab panel by 
dragging a tab to the left, right, top, or bottom of the panel. The work area has a single current 
activity. The tab for the current activity is marked with a colored top border (blue by default).

## Creating a Jupyter Notebook

To open a new notebook click the Python 3 icon under the *Notebook* header in the Launcher tab in 
the main work area. You can also create a new notebook by selecting *New -> Notebook* from the *File* menu in the Menu Bar.

Additional notes on Jupyter notebooks.

  *   Notebook files have the extension `.ipynb` to distinguish them from plain-text Python programs.
  *   Notebooks can be exported as Python scripts that can be run from the command line.

Below is a screenshot of a Jupyter notebook running inside JupyterLab. If you are interested in 
more details, then see the [official notebook documentation][jupyterlab-notebook-docs].

<p align='center'>
    <img alt="Example Jupyter Notebook" src="../fig/0_jupyterlab_notebook_screenshot.png" width="750"/>
</p>

> ## How It's Stored
>
> *   The notebook file is stored in a format called JSON.
> *   Just like a webpage, what's saved looks different from what you see in your browser.
> *   But this format allows Jupyter to mix source code, text, and images, all in one file.
{: .callout}

> ## Arranging Documents into Panels of Tabs
>
> In the JupyterLab Main Work Area you can arrange documents into panels of tabs. Here is an 
> example from the [official documentation][jupyterlab].
> 
> <p align='center'>
>    <img alt="Multi-panel JupyterLab" src="../fig/0_multipanel_jupyterlab_screenshot.png" width="750"/>
> </p>
>
> First, create a text file, Python console, and terminal window and arrange then into three 
> panels in the main work area. Next, create a notebook, terminal window, and text file and 
> arrange then into three panels in the main work area. Finally, create your own combination of 
> panels and tabs. What combination of panels and tabs do you think will be most useful for your 
> workflow?
>
> > ## Solution
> >
> > After creating the necessary tabs, you can drag one of the tabs to the center of a panel to 
> > move the tab to the panel; next you can subdivide a tab panel by dragging a tab to the left, 
> > right, top, or bottom of the panel.
> >
> {: .solution}
{: .challenge}

## Use the Jupyter Notebook for editing and running Python.

*   While it's common to write Python scripts using a text editor, we are going to use the [Jupyter Notebook][jupyter] for the remainder of this workshop.
*   This has several advantages:
    *   You can easily type, edit, and copy and paste blocks of code.
    *   Tab complete allows you to easily access the names of things you are using
        and learn more about them.
    *   It allows you to annotate your code with links, different sized text, bullets, etc.
        to make it more accessible to you and your collaborators.
    *   It allows you to display figures next to the code that produces them
        to tell a complete story of the analysis.
*   Each notebook contains one or more cells that contain code, text, or images.

> ## Code vs. Text
>
> Jupyter mixes code and text in different types of blocks, called cells. We often use the term
> "code" to mean "the source code of software written in a language such as Python".
> A "code cell" in a Notebook is a cell that contains software;
> a "text cell" is one that contains ordinary prose written for human beings.
{: .callout}

## The Notebook has Command and Edit modes.

*   If you press <kbd>Esc</kbd> and <kbd>Return</kbd> alternately, the outer border of your code cell will change from gray to blue.
*   These are the **Command** (gray) and **Edit** (blue) modes of your notebook.
*   Command mode allows you to edit notebook-level features, and Edit mode changes the content of cells.
*   When in Command mode (esc/gray),
    *   The <kbd>B</kbd> key will make a new cell below the currently selected cell.
    *   The <kbd>A</kbd> key will make one above.
    *   The <kbd>X</kbd> key will delete the current cell.
    *   The <kbd>Z</kbd> key will undo your last cell operation (which could be a deletion, creation, etc).
*   All actions can be done using the menus, but there are lots of keyboard shortcuts to speed things up.

> ## Command Vs. Edit
>
> In the Jupyter notebook page are you currently in Command or Edit mode?  
> Switch between the modes. 
> Use the shortcuts to generate a new cell. 
> Use the shortcuts to delete a cell.
> Use the shortcuts to undo the last cell operation you performed.
>
> > ## Solution
> >
> > Command mode has a grey border and Edit mode has a green border. 
> > Use <kbd>Esc</kbd> and <kbd>Return</kbd> to switch between modes. 
> > You need to be in Command mode (Press <kbd>Esc</kbd> if your cell is blue).  Type <kbd>B</kbd> or <kbd>A</kbd>.
> > You need to be in Command mode (Press <kbd>Esc</kbd> if your cell is blue).  Type <kbd>X</kbd>.
> > You need to be in Command mode (Press <kbd>Esc</kbd> if your cell is blue).  Type <kbd>Z</kbd>.
> >
> {: .solution}
{: .challenge}

### Use the keyboard and mouse to select and edit cells.

*   Pressing the <kbd>Return</kbd> key turns the border blue and engages Edit mode, which allows 
    you to type within the cell.
*   Because we want to be able to write many lines of code in a single cell,
    pressing the <kbd>Return</kbd> key when in Edit mode (blue) moves the cursor to the next line 
    in the cell just like in a text editor.
*   We need some other way to tell the Notebook we want to run what's in the cell.
*   Pressing <kbd>Shift</kbd>+<kbd>Return</kbd> together will execute the contents of the cell.
*   Notice that the <kbd>Return</kbd> and <kbd>Shift</kbd> keys on the right of the keyboard are 
    right next to each other.

### The Notebook will turn Markdown into pretty-printed documentation.

*   Notebooks can also render [Markdown][markdown].
    *   A simple plain-text format for writing lists, links, 
        and other things that might go into a web page.
    *   Equivalently, a subset of HTML that looks like what you'd send in an old-fashioned email.
*   Turn the current cell into a Markdown cell by entering the Command mode (<kbd>Esc</kbd>/gray) 
    and press the <kbd>M</kbd> key.
*   `In [ ]:` will disappear to show it is no longer a code cell and you will be able to write in 
    Markdown.
*   Turn the current cell into a Code cell by entering the Command mode (<kbd>Esc</kbd>/gray) and 
    press the <kbd>Y</kbd> key.

### The Notebook will evaluate code and display results
* Running a line of code can have several outcomes:
  * Loading data for use in future code
  * Changing the state of the code environment
  * Storing information for use in future code
  * Returning the results without storing them
* Jupyter will display the results of the final line of code in a cell after executing that cell.

> ## Running Python Cells
>
> What is displayed when a Python cell in a notebook
> that contains several lines of code is executed?
> For example, what happens when this cell is executed?
>
> ~~~
> import os
> os.getcwd()
> ~~~
> {: .language-python}
> 
> > ## Solution (for Mac)
> >
> > Jupyter returns the output of only the last line.
> > ~~~
> > '/Users/your_username'
> > ~~~
> > {: .output}
> {: .solution}
{: .challenge}

> ## Running More Python Cells
>
> Why do you think that nothing is displayed when this cell is executed?
>
> ~~~
> cwd = os.getcwd()
> ~~~
> {: .language-python}
> 
> > ## Solution
> >
> > Jupyter prints the output of the last line. In this case the last line assigned a value to a variable and did not have output.
> {: .solution}
{: .challenge}

> ## Running Even More Python Cells
>
> How would you display the data stored as cwd?
> 
> > ## Solution
> > ~~~
> > cwd
> > ~~~
> > {: .language-python}
> > ~~~
> > '/Users/your_username'
> > ~~~
> > {: .output}
> >
> {: .solution}
{: .challenge}

> ## Running the Last Python Cell for this Lesson
>
> What information is stored as cwd when this cell is executed?
>
> ~~~
> os.chdir('Downloads')
> cwd = os.getcwd()
> ~~~
> {: .language-python}
> 
> > ## Solution
> > ~~~
> > cwd
> > ~~~
> > {: .language-python}
> > ~~~
> > '/Users/your_username/Downloads'
> > ~~~
> > {: .output}
> > After changing directories, `os.getcwd()` returns a different value than before.
> > This value is than stored in the variable `cwd`.
> {: .solution}
{: .challenge}

> ## Change an Existing Cell from Code to Markdown
>
> What happens if you write some Python in a code cell
> and then you switch it to a Markdown cell?
> For example,
> put the following in a code cell:
>
> ~~~
> os.getcwd()
> ~~~
> {: .language-python}
>
> And then run it with <kbd>Shift</kbd>+<kbd>Return</kbd> to be sure that it works as a code cell.
> Now go back to the cell and use <kbd>Esc</kbd> then <kbd>M</kbd> to switch the cell to Markdown
> and "run" it with <kbd>Shift</kbd>+<kbd>Return</kbd>.
> What happened and how might this be useful?
> 
> > ## Solution
> >
> > The Python code gets treated like Markdown text.
> > The lines appear as if they are part of one contiguous paragraph.
> > This could be useful to temporarily turn on and off cells in notebooks that get used for multiple purposes. 
> > ~~~
> > os.getcwd()
> > ~~~
> > {: .language-python}
> {: .solution}
{: .challenge}

> ## Python Syntax: `=`
>
> In order to parse our input, Python has rules about how it should be written.
> We can use these same rules when reading code to understand what is happening.
> As different syntaxes appear, we will point them out in these callout boxes.
>
> In Python, the equals sign `=` works a little differently than in a math class.
> `=` assigns a value to variable, like this:
> 
> ~~~
> variable = value
> ~~~
> {: .language-python}
>
> A variable is an object that can hold any value.
> We can update the value of the variable
> ~~~
> cool_file_name = 'qckitty.gif'
> ~~~
> {: .language-python}
>
> We can also create new variables.
> A variable name can include any character except space ` `, and it can't begin with a number.
> ~~~
> myFavoriteFilename = 'qckitty.gif'
> ~~~
> {: .language-python}
>
> One of the hardest parts of programming is picking good names for your variables.
> To help understand your code when you return to it in the future, try to use descriptive names.
{: .callout}

## Closing JupyterLab

*   From the Menu Bar select the "File" menu and the choose "Quit" at the bottom of the dropdown menu. You will be prompted to confirm that you wish to shutdown the JupyterLab server (don't forget to save your work!). Click "Confirm" to shutdown the JupyterLab server.
*   To restart the JupyterLab server you will need to re-run the following command from a shell.

~~~
$ jupyter lab
~~~

> ## Closing JupyerLab
>
> Practice closing and restarting the JupyterLab server.
> 
{: .challenge}
[anaconda]: https://docs.continuum.io/anaconda/install
[jupyterlab-ui]: https://jupyterlab.readthedocs.io/en/stable/user/interface.html
[jupyterlab-notebook-docs]: https://jupyterlab.readthedocs.io/en/stable/user/notebook.html
[markdown]: https://en.wikipedia.org/wiki/Markdown

{% include links.md %}