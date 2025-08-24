# Homework guidelines - Spring 2025 (NOT fall)

## Starting homework

1. **Click on the assignment link in the classmate team on GitHub.** When you follow the link and accept the assignment, GitHub will create a repo for you. The repo will be a private repo (only you, me, and the TA can see it) under the LeDataSciFi organization on GitHub. 
1. The repo will contain instructions and a rubric, and possibly starter code/data.
2. Clone the repo to your computer using GitHub desktop and follow the instructions. 

## Working on assignments / projects / taking notes 
 
[Use the GitHub workflow!](../01/03a_githubworkflow)

```{tip} 
**Fetch early, commit frequently, push often!**

This habit will help you avoid disasters, so that you get the positive features of Github without the headaches.
```

## Submitting assignments 

Submission is easy: Whatever is in your assignment repo (the online version, not your computer!!!) at the deadline is what will be graded. 

```{warning}
Again: Whatever is in your assignment repo (the online version, not your computer!!!) at the deadline is what will be graded.
```

```{warning}
Shortly after the deadline, GitHub will automatically stop you from pushing edits to the repo! So commit and push your changes often, and do not wait until minutes before the deadline. 
```

Your graders will download your repo on their computer, try to run your code, and evaluate it for accuracy and quality, based on the rubric (each assignment has a different rubric). 

## Tips for better grades (+ workproduct + repos)

```{dropdown}  **TIP #1:** Check out the rubric for the assignment
Each assignment has different grading criteria, which you'll see in the rubric within each assignment's repo.  

Generically and briefly, I'll say the important themes are:
- reproducibility (Your peers should be able to download the folder to their computer and execute the main analysis file and receive back the same results you generated)
- organization of the repo (can an outsider discern what is going on?)
- the README.md file, which should describe the repo to readers 
- the main analysis file. More on this in the next tip...
```




```{dropdown}  **TIP #2:** Before you push what you think are your final changes to the master repo...
1. Delete all temporary and output files you generated, restart the kernel (and clear output), 
2. rerun the analysis/code (as though you just started from scratch),
3. and save your notebook file when it's done running. 

This will clean up your folder for viewers (yay, professional work product!) and is a first pass at finding out if your code "works from scratch".

Did it work? If not, then the code is not reproducible. Probably, you referenced a temporary file you created outside of the flow of the code, or accidentally put an input file in the temporary file folder. Whoops! Fix it!
```



```{dropdown}  **TIP #3:** After you push what you think are your final changes to the master repo...
1. Go to the repo _**online**_. This is what your reviewers will see. The process of writing code often creates little files (like `.ipynb_checkpoints`) that you don't want in the online repo, but that you can't or don't want to delete locally. The usual solution is to add them to gitignore and purge them from the master repo. (This is easy, and I'll describe how to do it elsewhere.)
2. **A 100% solution**: Download it to your computer (click the green button, then download the zip file) **to a different spot** (say a temporary folder on your desktop), and run the analysis again, there. 

Did it work? If not, then the code is not reproducible outside the directory you built it in. 

Why did it fail? Probably, the code included absolute path references like "C:\Users\DonBowen\Documents\project1\code\extra_function.py". These are bad because they only work on my computer. (You probably won't have "DonBowen" as a folder anywhere on your computer, I hope!)  

Use relative path references instead. For example, if `main_analysis.py` uses `extra_function.py`, and `main_analysis.py` is in the "project1" folder, then "code/extra_function.py" will find the function on any computer. 
```




```{dropdown}  **TIP #4:** Make it easy for others to see the source code that executes the analysis as well as the report. 
The biggies:
1. The README.md in the main directory is what they will see first when they open it. Make it professional and helpful!  GitHub can format "Markdown" nicely (with headers, links, media, and more) and will show visitors the nicely formatted version. 
    - Create annotated links to documents graders need to access. For example, point them to your main Jupyter file, which GitHub will also render so that visitors see the output on the website without needing to run code!
    - [GitHub](https://guides.github.com/features/wikis/#Formatting-a-readme) suggests including the project name, a clear and short description (what it does and why it is important), installation tips (list packages they might need to install), and usage instructions.
2. Make sure your final analysis code shows outputs _when viewed online_! See Tip #2 above. This will help them grade faster (and faster graders are nicer graders).
```


```{dropdown}  **TIP #5:** Make it easy for others to run your code.
- At the top of the code, load all packages you need
- Under that, list parameters a user would set (you obviously choose these during your analysis, but it's nice to see them quickly in one place)
- Under that, import external files. This makes it easy for someone to see which data files are required and edit the paths if necessary. Even though I said absolute path references are bad above, there are situations where you might not keep data in the repo itself. (For example: Huge data files or sensitive data subject to privacy issues.) When this is the case and you have to use absolute path references, you want those at the top of your code so people see them!
- Again, see tip #3 above.
```


```{dropdown}  **TIP #6:** Make your work product (especially tables and figures) pretty. 
- Use good design concepts that we discuss early in the semester for figures and tables.
- I google "markdown cheat sheet" often (sometimes with "github" or "jupyter" added to it depending on what I'm writing). [This is a good start cheat sheet](https://www.markdownguide.org/cheat-sheet/) and there is so much good stuff online. 
```


