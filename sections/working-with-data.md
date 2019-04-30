[Next >>>](introducing-openrefine.md)

# Working with Data

> Above all, it is crucial to observe that the term "data" serves a different rhetorical function than do sister terms such as "facts" and "evidence." To put it more precisely, in contrast to these other terms, the semantic function of data is *specifically* rhetorical.

- Daniel Rosenberg, "Data Before the Fact" in *Raw Data is an Oxymoron*

> Like families, tidy datasets are all alike but every messy dataset is messy in its own way.

- Hadley Wickham, "Tidy Data," *Journal of Statistical Software*

## What is data?

It would take a long long long time to unpack such a question, so we will skip to a more salient pair of concerns: How to think of our own research in terms of structured data? How would we go about nudging our archives/notes/digital images/PDFs into forms that would enable computer analysis or visualization?

Even in a passing consideration of data as this short tutorial allows, it's worth noting that data constitutes a slippery set of concepts, processes, technologies, and products. While Daniel Rosenberg in the above quote is most concerned with etymology, we invite you to consider how even mechanical processes of transformation are rhetorical, are already engaging in argument -- before we even get to visualization or interpretation, the stages that usually get credit for revealing the story embedded in the data.

In lieu of definition, a couple of rough rules-of-thumb: By and large, the data (or rather, datasets) we create or find in the wild will be either tabular (think spreadsheet) or graph data (think tree hierarchy or network). However complicated or simple, datasets consist of values that correspond to predetermined variables. These variables, in turn, can be described as either categorical, continuous, or discontinuous. This includes temporal and geographic data though these data types include special considerations.

## What's in a data file?

What is in a data file? The annoying retort would be *what is not in a data file?* However, in the wild, it may be helpful to provide a general taxonomy of common formats for serialized data. Note that we are *not* talking about databases here; rather we are concerned with data written to a file using text characters. As such, these files are subject to the same issues mentioned earlier with regard to other plain text files, including differing newline characters or special characters added by software inadvertently.

Data files that we use in research for analysis or visualization largely fall under either tabular or graph data.

Tabular data can be represented in terms of columns, rows, and cells. Rows represent observations or instances, which have values corresponding to column variables. Most commonly seen in proprietary formats (Excel or GoogleSheets files) or character delimited text files like CSV (comma separated values) or TSV (tab separated values).

Graph data is data that can be represented by nodes and edges, roughly speaking, what is popularly visualized as network diagrams. Directed graph describes data that can be represented by a tree or a hierarchy. Most commonly seen in XML or JSON formats (though these formats can represent tabular data, they are not often used for that purpose).

[Next >>>](introducing-openrefine.md)