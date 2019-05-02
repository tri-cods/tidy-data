[Next >>>](introducing-openrefine.md)

# Working with Data

> Above all, it is crucial to observe that the term "data" serves a different rhetorical function than do sister terms such as "facts" and "evidence." To put it more precisely, in contrast to these other terms, the semantic function of data is *specifically* rhetorical.

- Daniel Rosenberg, "Data Before the Fact" in *Raw Data is an Oxymoron*

> Like families, tidy datasets are all alike but every messy dataset is messy in its own way.

- Hadley Wickham, "Tidy Data," *Journal of Statistical Software*

## What is data?

It would take a long long long time to unpack such a question, so we will skip to a more salient pair of concerns: How to think of our own research in terms of structured data? How would we go about nudging our archives/notes/digital images/PDFs into forms that would enable computer analysis or visualization?

Even in a short tutorial, it's worth noting that data always comprises a slippery set of concepts, processes, technologies, and products. While Daniel Rosenberg in the above quote is most concerned with etymology, we invite you to consider how even "mechanical" processes like creating and cleaning data are rhetorical, are already engaging in argument -- before we even get to visualization or interpretation, the stages that usually get credit for revealing the story embedded in the data.

In lieu of definition, a couple of rough rules-of-thumb: By and large, the data (or rather, datasets) we create or find in the wild will be either tabular (think spreadsheet) or graph data (think tree hierarchy or network). However complicated or simple, datasets consist of values that correspond to predetermined variables. These variables, in turn, can be described as either categorical, continuous, or discontinuous. We include temporal and geographic data though these data types include special considerations in terms of comparison and mapping.

Ask for examples of different kinds of data types

## What's in a data file?

What is in a data file? The annoying retort would be *what is not in a data file?* However, in the wild, it may be helpful to provide a general taxonomy of common formats for serialized data. Note that we are *not* talking about databases here; rather we are concerned with data written to a file using text characters. As such, these files are subject to the same issues mentioned earlier with regard to other plain text files, including invisible characters like carriage returns, spaces, tabs, or other special characters added by software inadvertently.

Tabular data can be represented in terms of columns, rows, and cells. Rows represent observations or instances, which have values corresponding to column variables. Most commonly seen in proprietary formats (Excel or GoogleSheets files) or character delimited text files like CSV (comma separated values) or TSV (tab separated values).

Graph data is data that can be represented by nodes and edges, roughly speaking. Think popularized images of networks spidering out. A directed graph is data that can be represented by a tree or a hierarchy. Most commonly seen in XML or JSON formats (though these formats can represent tabular data, they are not often used for that purpose).

While we may only ever open and read spreadsheets, we interact with graph data constantly, whether using the library catalog or searching Facebook or using web-based maps.

## Tidy vs. Messy Part I

What is tidy data? To be clear we are using "tidy data" in a capacious sense. Outlined in 2014 by Hadley Wickham, a programmer and statistician, tidy data refers to applying standard ways of optimally formatting data for use with the programming language R. But with the recent tidal wave of students, journalists, humanists, artists, and/or scientists interested in engaging data in their research, "tidy data" has taken on a life of its own. Across disciplines and software and file formats awash with new sources of quantitative and qualitative data, who wouldn't want a Marie Kondo to guide us through?

Thinking tidily is helpful for anybody working with data, but particularly so for those in the humanities or qualitative social sciences who tend to be doubly challenged: First, they may not have had any prior need to think in structured ways about their sources. And second, the data they have to work with might win the prize for messiest, most complex, and least consistent.

For our purposes, tidying up means thinking about data in terms of reusable, machine-readable files. Even better: If the datasets are transparent and able to be audited.

Concretely, what does this mean? Data entered by hand is going to be inconsistent. Depending on our use case, that may be fine. If we intend to perform computational analysis or create visualizations; however, we will need to address some of that inconsistency because, well, computers are dumb. There is no ambiguity if an extra space appears in the middle of two words, for example, `N.  Lombard St`. To a machine, that value is utterly different from any other cell in which those same two words might appear, say, `N Lombard Street` or `North Lombard`.

[Next >>>](introducing-openrefine.md)