[<<< Previous](introducing-openrefine.md) | [Next >>>](transforming-columns.md)

# Exploring an OpenRefine project

Take a moment to explore your new project. What do you notice? There are many many features, but let's start with three: sorting, filtering, and faceting.

### Sort

Select the caret to the left of the **Name** column and select sort. This is a useful way of exploring data but does not permanently rearrange the data. In order to reorder the data permanently, notice the new **Sort** option that appears in the top bar. Selecting the caret beside the new **Sort** option gives you the option to permanently apply a new order to the underlying data.

### Filter

For the column labeled **Occupation of females compensation**, select **Text filter**. In the menu in the sidebar, enter an occupation. In how many residences are there recorded female washers? How many males are employed as washers?

### Facet

For the column labeled **Rent of house**, let's filter the census data based on how much rent tenants were paying. First, we'll want to convert the column to numeric data by selecting **Edit Cells** -> **Common Transforms** -> **To number**. Note that not *all* rows were converted, why not?

From the same column, select **Facet** -> **Numeric facet**. What happens when you slide the minimum and maximum selectors that appear in the sidebar?

## Transforming cells

### Trimming whitespace

One common issue that can cause issues further on down the road are invisible characters -- like spaces, tabs, and carriage returns. This happens often enough that OpenRefine automates the process of removing extra whitespace.

For **Residence**, select **Edit Cells** -> **Common Transforms** -> **Trim leading and trailing whitespace**. Next select **Edit Cells** -> **Common Transforms** -> **Collapse consecutive whitespace**. What do you imagine that step does?

![column edit cells common transforms submenu in openrefine](openrefine-trim.jpg)

### Clustering

Whether in the 1847 handwritten entries themselves or in the process of transcribing them to a digital file, the census data we have is far from consistent. What would be great is the ability to make sure every street name and address descriptor was consistent. Across all 4,308 rows.

Where OpenRefine starts to feel powerful is how easily it lets users throw sophisticated algorithms at all cells in a column or a row. Here we are going to explore one way the program uses basic machine learning to guess at what values are most like each other in order to make values more consistent.

For **Residence**, select **Edit Cells** -> **Common Transforms** -> **Trim leading and trailing whitespace**. Next select **Edit Cells** -> **Common Transforms** -> **Collapse consecutive whitespace**.

[<<< Previous](introducing-openrefine.md) | [Next >>>](transforming-columns.md)