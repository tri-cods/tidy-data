[<<< Previous](tidy-vs-messy-ii.md) | [Next >>>](exporting-data.md)

# Deduplicating rows

## Identifying duplicate rows

We would normally use **Facets**->**Customized facets**->**Duplicates facet** in order to identify duplicate rows; however, no column in this set is a unique identifier. Some residences have the same name. Some have the same address. How to identify and delete duplicate rows when there is no identifier? Admittedly, this process is convoluted and is decidedly not the slickest feature of OpenRefine.

One way to approximate an identifier is to glob the values of a row together. Unique residences may have the same name. They may even have the same street address as another residence. But they would not have the same "Name" + "Residence" + "Number in family" + ... + "Remarks".

Under the **Name** column, select **Edit column** -> **Add column based on this column...**.

 `cells['Name'] + cells['Residence'] + cells['Number in family'] + cells['Remarks'] `

Sort on this new column. We will also select **Sort** -> **Reorder rows permanently** from the top bar menu.

**Edit cells** -> **Blank down**

**Facet** -> **Customized facets** -> **Facet by blank**

Select true. Select **All** -> **Edit rows** -> **Star rows**. Clear facets. **All** -> **Facet** ->**Facet by star**. **All** -> **Edit rows** -> **Remove all matching rows**.

## Creating an identifier

Once we've deduplicated, let's not lose track of our unique rows or "observations." As we learned in the last section, something fundamental to tidying data is being able to consistently identify observations (i.e., rows) across different tables. As we also learned in the last section, what we thought of as one table, if we are thinking to tidily, should be split into several according the question we'd like to answer.

Under the **Name** column, select **Edit column** -> **Add column based on this column...**.

`“0000”[0,4-row.index.length()] + row.index()`

Now move this new column to the beginning of the table.

[<<< Previous](tidy-vs-messy-ii.md) | [Next >>>](exporting-data.md)