[<<< Previous](working-with-data.md) | [Next >>>](introducing-openrefine.md)

# Tidy vs. Messy Part I

What is tidy data? To be clear we are using "tidy data" in a capacious sense. [Outlined in 2014 by Hadley Wickham](https://www.jstatsoft.org/article/view/v059i10/), a programmer and statistician, tidy data refers to applying standard ways of optimally formatting data for use with the programming language R. With the recent tidal wave of students, journalists, humanists, artists, and/or scientists interested in engaging data in their research, "tidy data" has taken on a life of its own. Across disciplines and software and file formats awash with new sources of quantitative and qualitative data, who wouldn't want a Marie Kondo to guide us through?

Thinking tidily is helpful for anybody working with data, but particularly so for those in some humanities and social sciences who may not have had prior need to think in structured ways about their sources. With little practice, these researchers are often thrown into some of the messiest, most inconsistent, and otherwise challenging data to work with. Having a few rules of thumb can be invaluable.

For our purposes, tidying up means thinking about data in terms of reusable, machine-readable files. Even better: If the datasets are transparent and able to be audited.

Concretely, what does this mean? Data entered by hand is going to be inconsistent. Depending on our use case, that may be fine. If we intend to perform computational analysis or create visualizations; however, we will need to address some of that inconsistency because, well, computers are dumb. There is no ambiguity if an extra space appears in the middle of two words, for example, `N.  Lombard St`. To a machine, that value is utterly different from any other cell in which those same two words might appear, say, `N Lombard Street` or `North Lombard`. But as this example might suggest, how can we generalize when "each dataset is messy in its own way", often requiring context and data specific remediation?

[<<< Previous](working-with-data.md) | [Next >>>](introducing-openrefine.md)