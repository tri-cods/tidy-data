# Tidy(ish) Data

In order to begin thinking about digital methods, scholars must first make the conceptual leap toward thinking about their research as data. How do we get at the data in our research and how do we make it useful and usable by machines? What are some of the promises (and perils) of reframing research as data? By the end of the session, we’ll be introduced to strategies and tools for taking very different kinds of information and creating well-formed data, data that can then be used for analysis or visualization.

By way of introduction to working with data, we are going to focus on a) conceptually how data is structured using the tidy data framework and b) practically speaking, how to make it useable by other humans and machines with the program OpenRefine.

In this session, we will:

- install and become familiar with some of OpenRefine's features
- import data
- remove blank rows and de-duplicate
- split columns with multiple values
- export subsets in different formats

[Get Started >>>](sections/concept.md)  
[Glossary >>>](https://github.com/tri-cods/glossary) 

----- 

# Working with Data

> Above all, it is crucial to observe that the term "data" serves a different rhetorical function than do sister terms such as "facts" and "evidence." To put it more precisely, in contrast to these other terms, the semantic function of data is *specifically* rhetorical.

- Daniel Rosenberg, "Data Before the Fact" in *Raw Data is an Oxymoron*

> Like families, tidy datasets are all alike but every messy dataset is messy in its own way. Tidy datasets provide a standardized way to link the structure of a dataset (its physical layout) with its semantics (its meaning).

- Hadley Wickham, "Tidy Data," *Journal of Statistical Software*

## What is data?

It would take a long long long time to unpack such a question, so we will skip to a more salient pair of concerns: How to think of our own research in terms of structured values and variables? How would we go about manipulating our sources into forms that would enable computer analysis and visualization?

Even in a passing consideration of data as this short tutorial allows, it's worth noting that data constitutes a slippery set of concepts, processes, technologies, and products. While Daniel Rosenberg in the above quote is most concerned with etymology, we invite you to consider how even mechanical processes of transformation are rhetorical, are already engaging in argument -- before we even get to visualization or interpretation, the stages that usually get credit for revealing the story embedded in the data.

Data (or rather, datasets) are largely structured as tabular (think spreadsheet) or graph data (think tree hierarchy or network). Most of the time, values associated with variables are categorical, continuous, or discontinuous. This includes temporal and geographic data thought they have a few special considerations.

## What is OpenRefine?

OpenRefine is cross-platform open-source software that allows users to clean and transform messy data. Originally supported by Google, it is now maintained by a large user community. OpenRefine is by no means the only or best way to work with data; however, it strikes an unusual balance between working in proprietary tools for a broad audience (like Microsoft Excel or GoogleSheets) on the one hand, and on the other, straight programming for data science (R Studio, Python Notebooks).

It allows users to bring in messy data easily without requiring preliminary transformation. It allows for granular auditing of any changes, which makes provenance much simpler. It combines (relatively) easy to use suite of features with the ability to write custom scripts when needed.

A couple things to note about OpenRefine: The software was originally written for the web so it runs in the browser rather than its own window. Rather than opening and saving files, it imports data into a "project" from which we can export versions.

- Installing OpenRefine



- What is Data?
    - Where is your data?
    - Data types
    - Data structures
    - Data modeling and representation
- Importing Data
- Remove blank rows
- Split multi-value cells
- Reconciling
- De-duplicating
- Faceting
- Transformations
- Exported
- Advanced Uses
- Further Resources
    - Videos
    - Tutorials

## Resources

Videos
Tutorials
Tidy Data

-----

Session Leader: Nabil Kashyap

[![Creative Commons License](https://i.creativecommons.org/l/by-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-sa/4.0/)

[Digital Research Institute (DRI) Curriculum](http://purl.org/dc/terms/) by [Graduate Center Digital Initiatives](https://gcdi.commons.gc.cuny.edu/) is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/). Based on a work at <https://github.com/DHRI-Curriculum>. When sharing this material or derivative works, preserve this paragraph, changing only the title of the derivative work, or provide comparable attribution.