[<<< Previous](introducing-openrefine.md) | [Next >>>](transforming-columns.md)

# Exploring an OpenRefine project

Take a moment to explore your new project. What do you notice?

Let's start with three common functions: sorting, filtering, and faceting.


### Sort

Select the caret to the left of the **Name** column and select sort. This is a useful way of exploring data but does not permanently rearrange the data. In order to reorder the data permanently, notice the new **Sort** option that appears in the top bar. Selecting the caret beside the new **Sort** option gives you the option to permanently apply a new order to the underlying data.

### Filter

For the column labeled **Occupation of females compensation**, select **Text filter**. In the menu in the sidebar, enter an occupation. In how many residences are there recorded female washers? How many males are employed as washers?

### Facet

For the column labeled **Rent of house**, let's filter the census data based on how much rent tenants were paying. First, we'll want to convert the column to numeric data by selecting **Edit Cells** -> **Common Transforms** -> **To number**. Note that not *all* rows were converted, why not?

From the same column, select **Facet** -> **Numeric facet**. What happens when you slide the minimum and maximum selectors that appear in the sidebar?

[<<< Previous](introducing-openrefine.md) | [Next >>>](transforming-columns.md)