[<<< Previous](working-with-data.md) | [Next >>>](introducing-openrefine.md)

# Tidy vs. Messy Part I

What is tidy data? To be clear we are using "tidy data" in a capacious sense. [Outlined in 2014 by Hadley Wickham](https://www.jstatsoft.org/article/view/v059i10/), a programmer and statistician, tidy data refers to applying standard ways of optimally formatting data for use with the programming language R. But with the recent tidal wave of students, journalists, humanists, artists, and/or scientists interested in engaging data in their research, "tidy data" has taken on a life of its own. Across disciplines and software and file formats awash with new sources of quantitative and qualitative data, who wouldn't want a Marie Kondo to guide us through?

Thinking tidily is helpful for anybody working with data, but particularly so for those in the humanities or qualitative social sciences who tend to be doubly challenged: First, they may not have had any prior need to think in structured ways about their sources. And second, the data they have to work with might win the prize for messiest, most complex, and least consistent.

For our purposes, tidying up means thinking about data in terms of reusable, machine-readable files. Even better: If the datasets are transparent and able to be audited.

Concretely, what does this mean? Data entered by hand is going to be inconsistent. Depending on our use case, that may be fine. If we intend to perform computational analysis or create visualizations; however, we will need to address some of that inconsistency because, well, computers are dumb. There is no ambiguity if an extra space appears in the middle of two words, for example, `N.  Lombard St`. To a machine, that value is utterly different from any other cell in which those same two words might appear, say, `N Lombard Street` or `North Lombard`.

[<<< Previous](working-with-data.md) | [Next >>>](introducing-openrefine.md)