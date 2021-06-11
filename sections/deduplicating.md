[<<< Previous](tidy-vs-messy-ii.md) | [Next >>>](exporting-data.md)

# Deduplicating rows

## Identifying duplicate rows

We would normally use **Facets**->**Customized facets**->**Duplicates facet** in order to identify duplicate rows; however, no single column in this set is a unique identifier. Some residences have the same name. Some have the same address. How to identify and delete duplicate rows when there is no identifier? Admittedly, this process is convoluted and is decidedly not the slickest feature of OpenRefine.

One way to approximate an identifier is to glob the values of a row together. Unique residences may have the same name. They may even have the same street address as another residence. But they would not have the same "Name" + "Residence" + "Number in family" + ... + "Remarks".

## Create a row based on other columns

Under the **Name** column, select **Edit column** -> **Add column based on this column...**. Name this column **temp**.

Using GREL, we can access the value of other cells in the current row by using the `cells` variable and indicating which column, i.e., `cells['Residence']`. This object has multiple attributes, so we'll want to specify that we want the string value, as in `cells['Residence'].value`.

To smoosh together several values, we can literally just "add" them together:
 `cells['Name'].value + cells['Residence'].value + cells['Number in family'].value + cells['Remarks'].value`.

Sort on this new column. In order to reorder the underlying data, select **Sort** -> **Reorder rows permanently** from the top bar menu.

Now we blank cells with the same values in our new **temp** column by selecting **Edit cells** -> **Blank down**.

Now facet on blank values by selecting **Facet** -> **Customized facets** -> **Facet by blank**. Then select the 'true' in the sidebar to limit to blank values.

Now let's mark all these rows temporarily. OpenRefine let's us star any row or rows in order to mark them for further action. Select **All** -> **Edit rows** -> **Star rows**. Now go ahead and clear all facets in the left sidebar.

Finally, to actually remove duplicate rows, select **All** -> **Facet** ->**Facet by star**. Now select **All** -> **Edit rows** -> **Remove all matching rows**.

## Creating an identifier

Once we've deduplicated, let's not lose track of our unique rows or "observations." As we learned in the last section, something fundamental to tidying data is being able to consistently identify observations (i.e., rows) across different tables. As we also learned in the last section, what we thought of as one table, if we are thinking to tidily, should be split into several according the question we'd like to answer.

Under the **Name** column, select **Edit column** -> **Add column based on this column...**

To access the index of the current row, we can use the `row` variable and get the `index` value, i.e., `row.index`.

Optionally, if you want to ensure each identifier is a four digit number, we can apply the fancier formula: `"0000"[0,4-row.index.length()] + row.index`

Now select **Edit column** and move this new column to the beginning of the table.

[<<< Previous](tidy-vs-messy-ii.md) | [Next >>>](exporting-data.md)