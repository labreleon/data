This folder provides an all-encompassing working structure for empirical papers.

## Summary
0. Workflow
1. Organize your files
2. Organize your code
3. Version control
4. Abstract 
5. Comment often to explain purpose
6. Test-driven development (unit testing, refactoring, profiling)
7. References



## 0. Workflow

![](https://raw.githubusercontent.com/labreleon/paper_template/master/extra/workflow.png)



## 1: Organize your files

1. Separate directories by function.
2. Separate files into inputs and outputs
3. Make directories portable

- To see how professionals do this, check out the source code for R's [dplyr](https://github.com/tidyverse/dplyr) package
     - There are separate directories for source code (`/src`), documentation (`/man`), code tests (`/test`), data (`/data`), examples (`/vignettes`), and more

- When you use version control, it forces you to make directories portable (otherwise a collaborator will not be able to run your code)
     - Use relative filepaths (`"../input/data.csv"`) instead of (`"C:/build/input/data.csv"`).
 Run `sh setup.sh` to create symbolic links to all non-versioned folders.




## 1: Organize your files

In the main folder (root directory), place:

- A **README** file that gives a basic overview of your project.
- A **master script** that lists and runs all other scripts.


##### `/input`


- Symbolic link to non-versioned folder with input data.
- Any original data source should be included here in clean and normalized form.
- Only include cleaned files. Raw external files should be cleaned in each data source specific folder.
-  These data sets will then be manipulated and merged by the files in /code.

##### `/output`

- Versioned folder containing code that builds data and performs analyses.
- All output data should be redirected into `/output/data/`, with one data file per observation level.
- Other output files should be redirected into `/output/tables/` or `/output/figures/`.


##### `/code`
- Versioned folder containing code that builds data and performs analyses
- All output data should be redirected into /output/data/, with one data file per observation level.
- Other output files should be redirected into /output/tables/ or /output/figures/.

 ##### `/tmp`

- Symbolic link to non-versioned folder with temporary files.
- Contains any temporary file created during the manipulation of input data sets or the analysis routine.

##### `/products`

- Versioned folder containing files for preliminary results, papers, talks, and others.

 ##### `/extra`

- Contains any extra file relevant to the paper.




## 2: Organize code

1. Break programs into short scripts or functions, each of which conducts a single task.
2. Make names distinctive and meaningful.
3. Be consistent with code style and formatting.
  - Directory structure
  - Code and comment style
  - File naming conventions
  - Variable naming conventions
  - Output data structure


## 3: Version control

- Version control provides a principled way for you to easily undo changes, test out new specifications, and more

## 4: Abstract 


Don't copy-and-paste. Instead, **abstract**.

E.g. functions, loops, vectorization.

Why? Reduces scope for error.

-What if you copy-and-paste, later find a bug and correct it once, but forget the other instance?

Cost/benefit analysis with an externality to your future self

Gentzkow & Shapiro give three rules for abstraction:

1. Abstract to eliminate redundancy
2. Abstract to improve clarity
3. Otherwise, don't abstract

## 5: Comment often to explain purpose


**Basic**: Write lots of comments to explain what's going on. Comment every 5-10 lines or more.

Focus on documenting **the objectives** of the code, rather than **how** it works.

**Advanced**: Try to eliminate the need for most comments.

- Write modular code; use descriptive variable names; abstract when appropriate.

**Write self-documenting code:**

1:Use descriptive, unambiguous variable names

 - ``income_percapita`` instead of ``income_pc``
 - RStudio's autocomplete feature gives you no excuses

2: Define everything explicitly, and don't be afraid to write more code than necessary.


## 6: Test-driven development (unit testing, refactoring, profiling)

**Assume you will make mistakes**. (You will. All the time. You're a human, not a computer.)

Test-driven development (TDD) consists of a suite of tools for writing code that can be automatically tested

##### `/Unit testing`

- Unit tests are scripts that check that a piece of code does everything it is supposed to do
- When professionals write code, they also write unit tests for that code at the same time
- If code doesn't pass tests, then bugs are caught on the front end
- Test coverage determines how much of the code base is tested. High coverage rates are a must for unit testing to be useful.


##### `/Refactoring`

- Refactoring refers to the action of restructuring code without changing its external behavior or functionality. Think of it as "reorganizing"
- Example:

``estimate_ols(yvar,Xmat) = (Xmat'*Xmat)\Xmat'*yvar ``

after refactoring becomes

``estimate_ols(yvar,Xmat) = Xmat\yvar ``


- Nothing changed in the code except the number of characters in the function
- The new version may run faster, but is more readable. The output is unchanged.
- Refactoring could also mean reducing the number of input arguments


##### `/Profiling`


- Profiling refers to checking the resource demands of your code
- How much processing time does your script take? How much memory?
- Clean code should be highly performant: it uses minimal computational resources
- Profiling and refactoring go hand in hand, along with unit testing, to ensure that code is maximally optimized

## 7: References

- [Clean Code](https://raw.githack.com/OU-PhD-Econometrics/fall-2022/master/LectureNotes/01a-CleanCode/01aslides.html#1) (Ransom, 2022)
- [Best Practices for Coding & Workflows](https://raw.githack.com/msu-econ-data-analytics/course-materials/main/lecture-slides/07-Best-Practices/07-Best-Practices.html#25) (Hagerty, 2022)
- [Coding for Economists: A Language-Agnostic Guide to Programming for Economists  ](https://scholar.harvard.edu/files/ristovska/files/coding_for_econs_20190221.pdf) (Ljubica "LJ" Ristovska 2019).
- [Ricardo Dahis template](https://github.com/rdahis/paper_template)