---
output:
  html_document: default
  pdf_document: default
---
# Using the RStudio server




## Introduction

RStudio is a complete environment for working with the R language. Once you have got used to it you will find that it makes working with R far more productive than using the R console version. However some of the concepts involved in using RStudio may be new. 
RStudio provides an interface for working with R code, rather than an interface for running analyses directly. 

## Getting started with the RStudio server

The RStudio server version runs directly through any web browser. **There is no need to install any software on your laptop, PC or tablet**

Access to the server is through the following URL. This works both on and off campus.

http://r.bournemouth.ac.uk:8789/


<div class="rmdbu">
<p><a href="http://r.bournemouth.ac.uk:8789/" class="uri">http://r.bournemouth.ac.uk:8789/</a></p>
</div>

### Log into the RStudio server

1. Click on the URL http://r.bournemouth.ac.uk:8789/ in a browser. Use Firefox or Chrome.
2. You will see a log in page.
3. Log in using the username and the password you have been provided

## RStudio server concepts

The RStudio server is an integrated platform for doing the following ... 

1. Saving and sharing data files
2. Running analyses
3. Compiling reports
4. Connecting to data stores
5. Sharing analyses with others.

Advanced features can be used without any programming skills through sharing scripts. However you do need to become familiar with some new concepts in order to use the server. 
The RStudio server is ideal for collaborative work. You have your own permanent space on the server for saving your own work and building up a portfolio of useful analyses. Only one person can be logged in at any one time under your username. However I can always log into your user space at any time in order to help correct any errors and to give you advice on the analysis. 

## Finding your way around the interface

Once you are logged in you will see three sections of the interface by default. This will change to four sections when you begin using scripts in the interface.


<div class="figure">
<img src="images/rstudio.gif" alt="Animated gif tour of the Rstudio interface."  />
<p class="caption">(\#fig:unnamed-chunk-3)Animated gif tour of the Rstudio interface.</p>
</div>



Look carefully at the interface and learn to recognise the sections.

1. The RConsole. This is showing up on the left hand side when you first log in. The console can be used for running R code interactively. There is a tab showing up labelled "terminal" as well. You won't use this, as it is for more advanced programming.
2. The environment, history and connections pane is at the top right of the screen. The environment tab is the one that is most used. This tab will show the data that is in the active workspace in R. The concept will only become clear after beginning to use R.  
3. The files, plots, packages, help and viewer tab at the bottom right. The files tab is the most important to understand at this stage. There will be no files in your home directory yet, nor will there be any folders.

A key concept to understand when using the server is that your home directory on the server is like a directory (folder) on your PC. It is rather like the university H drive. However it is all "encapsulated" on the server, which is also running R. So it is distinct from your H drive and it is not directly linked.  In order to move data files and scripts into your home directory you must **upload** them. You will see buttons labelled **New Folder, Upload, Delete, Rename and More**. If you click on the **More** button you will also find an option to **Export** your files. The **upload** and the **export** buttons are frequently used to move files onto the server and to directly move files off the server. It is **very important** to be aware of this concept. Files saved on the server will always be available for use later. In contrast active analyses that take place in the server memory, as opposed to the server's hard disk space, will be temporary and will be lost between sessions.

## Using projects in RStudio

You can use Rstudio without opening projects. However, projects make organising your work much simpler. A project is a set of instructions to restore the server to the same state that it was in when you closed the project. So if you are analysing a range of data sets you can use one project per data set to keep your work organised. 

To form a new project and add a new folder

1. Click on the file menu at the top left of the interface.
2. Go to New Project
3. You will see a window with three options to create a project. Choose the first option labelled **New Directory** 
4. The next window will show a range of  advanced options. Ignore them and just select **New Project**
5. You will now see a window with a prompt for the Directory name (and some other options). In this example the project will contain data on sleep in mammals, so "sleep" could be used as the directory name.
6. Click create project
7. Look at the files pane in the bottom right corner. You will now see that after Home there is the word sleep. You can also see a file called sleep.Rproj in the folder.
8. Click on home. You can see a folder called sleep in your home directory. So .. you have created a new project and placed the project file within the folder. 


<div class="figure">
<img src="images/ss_1.gif" alt="Animated gif showing the steps taken when opening a new project. (Note the gif will be static in a PDF version of this document)"  />
<p class="caption">(\#fig:unnamed-chunk-4)Animated gif showing the steps taken when opening a new project. (Note the gif will be static in a PDF version of this document)</p>
</div>


## Uploading data

The course material generally uses data that is already placed on the server. However in order in order to conduct your own data analyses you will need to upload data files to your folders. The easiest way to ensure that the data and the data analysis are kept unified is to upload the data into the same folder you opened for the analysis project.  That way there will be no need to specify a path when the data are read into R.

Although R can read data from many different formats, the data files that you upload must be in some form of conventional format. The easiest format to use is to save each table as a single comma separated variable (.csv) file. The first line should contain short variable names with no spaces. The variable definitions should be kept separately and referred to when writing figure labels and captions, but not used in the column headers.

Data files are added to the project using the upload button in the files pane (bottom right). If you want to upload multiple files at once (e.g shapefiles) you should first compress them into a zip file. The zip file will expand when uploaded.

![](images/ss_2.gif)<!-- -->




## Working with markdown documents.

This course will concentrate on the use of markdown documents as a way of running R code. There are many advantages of using markdown.

1. Embedded code can be either revealed to other users to show how the results were obtained or hidden to simply produce a report with embedded figures and statistics.
2. Annotation of the results of an analysis can be embedded around the results to explain the key results.
3. Very limited knowledge of the R language and syntax is necessary to adapt markdown documents in order to analyse your own data.
4. With a little more knowledge and experience of R complex methods can be applied by altering markdown found on-line.

## Forming a markdown document.

1. Go to file on the top menu bar
2. Choose "New file"
3. Choose "R Markdown"
4. You will now see a window in which you can type in a name for the title of your analysis. By default the name is "untitled". Change that to some title that makes sense for the analysis you are going to run. It is easy to change the title later.
5. You will now see an untitled markdown document added to the top pane in RStudio. Rather confusingly it is still untitled, even though you've just typed a title! The reason for this is that the title you typed is used as the first line of the data report, but so far you still have not saved the file as a named document.
6. Click on save to save the report.  Now give the file itself a name.

The steps are shown in the animated gif below


![](images/ss_3.gif)<!-- -->



Now try pressing the "knit" button on the top right pane. You will see the default demonstration document that was produced as a template "knit" into a simple data report. This is not yet using your data of course.


<div class="figure">
<img src="images/ss_4.gif" alt="Compiling the demonstration markdown document."  />
<p class="caption">(\#fig:unnamed-chunk-7)Compiling the demonstration markdown document.</p>
</div>



The steps above will always produce the default "demo" markdown document. Every time you start a new markdown Rstudio will start off with this one. 
You should take a look at the logic of the demo document carefully. It consists of "chunks" of R code that produce output in the form of tables and figures embedded in text. The R code automatically produces output and adds it to the document after knitting. So if you have R code available that will run an analysis that you are interested in you don't have to remember any other steps in order to run it. Simply ensure that the data that is being added to the analysis is appropriate for the type of analysis being run and you can obtain the same results with your own data. This will be the way R is used in this course.



<div class="figure">
<img src="images/ss_5.gif" alt="Removing the default text from a new markdown document"  />
<p class="caption">(\#fig:unnamed-chunk-8)Removing the default text from a new markdown document</p>
</div>

## Reading in your data

If you are new to R you may be tempted to look around for a button on the RStudio interface to "load" the data file. You won't find one. Although there is a way to load data interactively you really **must not** do this.

<div class="rmdwarn">
<p>Always make sure that you include a line of code that loads the data at the start of your R script. Do not load data using the import data feature when building a markdown document. It will not work, as the data will not be loaded when you compile.</p>
</div>



In this case the working directory that R is using coincides with the project directory. So there is no need to include the path to the data file. This line will read the file into R and assign the data to a data frame called "d". 


```r
d<-read.csv("sleep.csv")
```

To form a code chunk click on the button on the interface labelled "Insert". Alternatively the keyboard short-cut control alt I will work.  Then type the code very carefully into the chunk. Make sure that the code sits within the body of the chunk and that you do not disturb the dashes that separate the chunk from the rest of the document. 

You should type the line into a single block of code that loads the data. Some  types of data, such as GIS layers or SPSS data files require packages to be loaded first. You should include a code chunk to load these packages first if you need them.

<div class="rmdnote">
<p>When conducting an analysis with just a single data frame I often call the data object &quot;d&quot;. This is just for brevity. As there are no other data objects present there is no ambiguity. If you load several data frames you should give them more informative names.</p>
</div>

![](images/ss_6.gif)<!-- -->


When you have finished typing the line of code to load the data, click on the run button of the chunk. You will see a data object appear in the environment pane in the top right corner of the RStudio server. If you click on this object it will open as a spreadsheet like table in the main panel.

<div class="figure">
<img src="images/ss_7.gif" alt="Clicking on the name of the data frame in the Environment tab opens up a spreadsheet like interface to inspect the data"  />
<p class="caption">(\#fig:unnamed-chunk-12)Clicking on the name of the data frame in the Environment tab opens up a spreadsheet like interface to inspect the data</p>
</div>

## Adding analysis chunks

Once you have the data loaded you can begin to build up an analysis. You should use a separate chunk for each step and write some text between each chunk that explains what you are doing.  Code from the course documents and crib sheets will form the basis for most of your analyses. It is very important to run all the code in the right order. Code chunks often depend on actions that are taken previously. For example in fig \@ref(fig:rstudio10) the animated gif shows that two code chunks have been added after the data were  loaded. The first produces a new variable which is the log transformed body weight. The second inspects the relationship between mean time spent sleeping and the log transformed variable. If the code were not run in order the last chunk would not work. The downward facing button on a code chunk runs all the chunks above it. You should use this frequently in order to check that everything is in the right order.

<div class="figure">
<img src="images/ss_8.gif" alt="Building up an analysis in a markdown document. Notice how the run all chunks above button is used to ensure that all the necessary code is being run"  />
<p class="caption">(\#fig:rstudio10)Building up an analysis in a markdown document. Notice how the run all chunks above button is used to ensure that all the necessary code is being run</p>
</div>

## Compiling a report

Once you have written all the code needed for your analysis and tested it by stepping through each chunk in the correct order you can compile your report into a document. This whole book has been written and compiled in this way. The idea of using markdown is to ensure that all the code to produce an analysis is reproducible and that the results of the analysis are annotated with comments that explain them both as a reminder to yourself and potentially as a report read by others. 


<div class="figure">
<img src="images/ss_9.gif" alt="Knitting the markdown into an HTML document"  />
<p class="caption">(\#fig:unnamed-chunk-13)Knitting the markdown into an HTML document</p>
</div>







