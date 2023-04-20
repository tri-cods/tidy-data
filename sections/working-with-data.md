[Next >>>](tidy-vs-messy.md)

# Working with Data

> Above all, it is crucial to observe that the term "data" serves a different rhetorical function than do sister terms such as "facts" and "evidence." To put it more precisely, in contrast to these other terms, the semantic function of data is *specifically* rhetorical.

- Daniel Rosenberg, "Data Before the Fact" in *Raw Data is an Oxymoron*

> Like families, tidy datasets are all alike but every messy dataset is messy in its own way.

- Hadley Wickham, "Tidy Data," *Journal of Statistical Software*

## What is data?

It would take a long long long time to unpack such a question, so let's skip to a more salient pair of concerns: How to think of our own research in terms of structured data? How do we go about nudging our objects of study (archives/notes/digital images/PDFs) into forms that allow for computer analysis or visualization? Whether we want to use machine learning to predict patterns or simply want to share maps and digital exhibits online, we need to have some working understanding of our research as data.

Data always comprises a slippery set of concepts, processes, technologies, and products. In light of Daniel Rosenberg's comment above on the etymology of "data", consider how even "mechanical" processes like creating and cleaning data are rhetorical, are already engaging in argument -- before we even get to visualization or interpretation we are already engaged in issues of representation and modeling the world, opening up possibilities while precluding others.

By and large, the data (or rather, datasets) we create or find in the wild are either tabular (think spreadsheet) or graph data (think tree hierarchy or network). However complicated or simple, datasets consist of *values* that belong to predetermined *variables*. These variables, in turn, can describe either *categorical*, *continuous*, or *discontinuous* data. We include temporal and geographic data though these data types include special considerations in terms of comparison and mapping.

Data and datasets, in this context, are not only for quantitative research or even for research with highly structured output. Citations and library catalogs, archival finding aids and digital collections of any media, from video to journal articles -- these are all examples of data created and/or reused for research across disciplines.

What in your own research relies on grouping objects of study into meaningful categories? What might include quantitative data, whether discontinuous or continuous?

## What's in a data file?

The annoying retort would be *what is not a data file?* If we are not worried about being terribly precise, we can talk usefully about a taxonomy of common formats for sharing datasets. Note that we are *not* talking about databases here; rather we are concerned with data encoded in text characters and written to a file. As such, these files are subject to the same issues mentioned earlier with regard to other plain text files, particularly invisible characters like carriage returns, spaces, tabs, or other special characters added by software inadvertently.

**Tabular data** can be represented in terms of columns, rows, and cells. Rows represent observations or instances, which have values corresponding to column variables. Most commonly seen in proprietary formats (Excel or GoogleSheets files) or character delimited text files like CSV (comma separated values) or TSV (tab separated values).

**Graph data** is data that can be represented by nodes and edges, roughly speaking. Think [popularized images of networks spidering out](https://en.wikipedia.org/wiki/Opte_Project#/media/File:Internet_map_1024.jpg). A **directed graph** is data that can be represented by a tree or a hierarchy. Most commonly seen in XML or JSON formats (though these formats can also represent tabular data).

While some of us may only ever open and read spreadsheets, we interact with graph data constantly, whether using the library catalog or searching Facebook or using web-based maps. Websites themselves are directed graph data represented by the browse.

Why pay attention to data files? Clearly, we can save ourselves and others headache and heartbreak by being mindful with data files, by keeping folders organized, naming files sanely, having consistent, logical column headers. Beyond that, granting organizations and scholarly journals across disciplines are increasingly interested in underlying datasets. Plus you might want to visit [the European Spreadsheet Risks Interest Group](http://www.eusprig.org/) (yes, that's a thing) for a curious, sometimes comic collection of messy data horror stories.

[Next >>>](tidy-vs-messy.md)