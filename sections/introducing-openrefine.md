[<<< Previous](tidy-vs-messy.md) | [Next >>>](exploring-openrefine.md)

# What is OpenRefine?

[OpenRefine is cross-platform, open-source software](http://openrefine.org/) that allows users to clean and transform messy data. Originally supported by Google, it is now maintained by a large user community. OpenRefine is by no means the only or best way to work with data; however, it strikes an unusual balance between working in proprietary tools for a broad audience (like Microsoft Excel or GoogleSheets) on the one hand, and on the other, straight programming for data science (R Studio, Python Notebooks).

It allows users to bring in messy data easily without requiring preliminary transformation. It allows for granular auditing of any changes, which makes provenance much simpler. It combines (relatively) easy to use suite of features with the ability to write custom scripts when needed.

A couple things to note about OpenRefine: The software was originally written for the web so it runs in the browser rather than its own window. Rather than opening and saving files, it imports data into a "project" from which we can export versions of data suited to our needs.

If you haven't yet, be sure to download and install OpenRefine according to [the instructions on the installations page](https://github.com/tri-cods/install/blob/master/sections/open_refine.md).

## Importing Data

Like git, OpenRefine is not structured around discrete files that you open and save. Data is imported into a project without affecting the original file. Changes made to that data are bundled together into another file. Rather than saving over or saving multiple copies of data (i.e., `datafile_final-reallyfinal-FINAL.xls`) projects allow users to export derivative files with fine-grained control over how those derivatives should be formed.

1) From the **Create Project** option, select **Choose Files**

![openrefine: create a project screenshot](openrefine-import-1.jpg)

2) Having selected the data file, create a project name in the top bar then select **Create Project**. You may also choose from an array of options regarding how to parse that data. Note that you can import both tabular data like CSV's or Excel files as well as nested formats, like JSON or XML.

![openrefine: create a project options screenshot](openrefine-import-2.jpg)

## Importing Sample Data

For our workshop we are going to be using [historical data derived from an 1847 Quaker census of African Americans living the Philadelphia area](https://github.com/swat-ds/datasets/tree/master/1847census), found in Friends Historical Library. More context about the dataset is available in the GitHub repository and the [original published accompanying report](https://www.swarthmore.edu/Library/friends/paac1847/censusreport.html#) can be found online.

Another source of diverse data we could explore is [a spreadsheet list of new datasets](https://docs.google.com/spreadsheets/d/1wZhPLMCHKJvwOkP4juclhjFgqIY8fQFMemwKL2c64vk) circulated in newsletter called [Data is Plural](https://tinyletter.com/data-is-plural) and maintained by Jeremy Singer-Vine.

Once you've downloaded the `.csv` file, first open it in [the web application databasic.io](https://databasic.io/). What do you notice? What questions might you ask? What seems incomplete or not showing up correctly?

Now create an OpenRefine project and choose the file `1847census.csv` as the source.

In the next screen go ahead and rename the project in the top bar. For now, let's stick with the default settings and voilà, our first project.

[<<< Previous](tidy-vs-messy.md) | [Next >>>](exploring-openrefine.md)