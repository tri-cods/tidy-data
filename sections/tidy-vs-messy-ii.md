[<<< Previous](exploring-openrefine.md) | [Next >>>](transforming-columns.md)

# Tidy vs. Messy Part II

So what, again, is tidy data? More than taking a stand against error-riddled, inconsistent data, tidy refers to an attempt to standardize how we might organize data. Now that we've had a chance to explore a single research dataset in more detail, we are better equipped to explore how to apply tidy data concepts.  According to Wickham:

1. Each variable forms a column.
2. Each observation forms a row.
3. Each type of observational unit forms a table.

Messy data, on the other hand, is everything else.

## Common issues

Modeling real world phenomena in data is hard, incomplete, and often problematic. That does not preclude being able to identify large classes of issues that makes working with data significantly easier. Extrapolating from the above three concepts, five common issues are:

- Column headers should be variable names, not values.
- One column should store values for one variable.
- Variables should be stored in columns, not rows.
- Different types of observational units should appear in different tables.
- A single observational unit should appear in a single table.

Guidelines like these can be incredibly helpful for our sanity as we try to decode historical data or data created by hand. They can also be useful in guiding those of us who are not data scientists but want to create datasets from our research.

The following examples derive from widely shared examples initially used by Hadley Wickham for teaching purposes. For a fuller treatment, see [Hadley Wiksham's teaching slide deck](http://stat405.had.co.nz/lectures/18-tidy-data.pdf) as well as the  [video version of these concepts](https://vimeo.com/33727555).

### 1. Column headers should be variable names


|  | religion | <$10k | $10-20k | $20-30k | $30-40k |
|---|---|---|---|---|---|
| 1 | Agnostic | 27   | 34   | 60   | 81   |
| 2 | Atheist | 12 | 27 | 37 | 52 |
| 3 | Buddhist | 27 | 21 | 30 | 34 |
| 4 | Catholic | 418 | 617 | 732 | 670 |
| 5 | Don’t know/refused | 15 | 14 | 15 | 11 |

In this excerpted table of income distribution between religious denominations from the Pew Foundation, where might headers be actually harboring values instead of variable names?

|    | religion | income | count |
| ---- | -------- | ------ | ----- |
| 1    | agnostic | <$10k | 27   |

### 2. One column should describe one variable

| country | year | m014 | m1524 | m2534 | m3544 | m4554 | m5564 | m65  | mu | f014 | f1524 | f2534 | f3544 | f4554 | f5564 | f65 | fu |
|---------|------|------|-------|-------|-------|-------|-------|------|----|------|-------|-------|-------|-------|-------|-----|----|
| US      | 1995 | 19   | 355   | 876   | 1417  | 1121  | 742   | 1099 | NA | 26   | 280   | 579   | 499   | 285   | 202   | 591 | NA |

Variables include sex (m, f) and age (0–14, 15–25, 25–34, 35–44, 45–54, 55–64, over 65, unknown).

In this excerpt of tuberculosis dataset from the World Health Organization, where can you see multiple variable crammed into one column?

### 3. Variables should be stored in rows not columns

| id          | year | month | element | d1   | d2   | d3   | d4   | d5   | d6   | d7   | d8   | d9   | d10  | d11  | d12  | d13  | d14  | d15  | d16  | d17  | d18  | d19  | d20  | d21  | d22  | d23  | d24  | d25  | d26  | d27  | d28  | d29  | d30  | d31  |
| ----------- | ---- | ----- | ------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| MX000017004   | 2010    | 1   | TMAX  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | 278 | NA |
| MX000017004   | 2010    | 1   | TMIN  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | 145 | NA |
| MX000017004   | 2010    | 2   | TMAX  | NA  | 273 | 241 | NA  | NA  | NA  | NA  | NA  | NA  | NA  | 297 | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA  | 299 | NA  | NA  | NA  | NA  | NA  | NA  | NA  | NA |

In this excerpt of weather data from Cuernavaca, Mexico, what variable seems to appear in both a column and a row?

### 4. Different observational units should appear in different tables

| year                                                     | artist | track | time | date.entered | wk1  | wk2  | wk3  |
| -------------------------------------------------------- | ------ | ----- | ---- | ----- | ------- | ---- | ---- |
| 2000 | 2Ge+her | The Hardest Part Of ... | 3:15 | 2000-09-02| 91| 87| 92 |
| 2000 | 3 Doors | Down Kryptonite | 3:53 | 2000-04-08| 81| 70| 68 |
| 2000 | 98^0 Give | Me Just One Nig... | 3:24 | 2000-08-19| 51| 39| 34 |
| 2000 | A*Teens | Dancing Queen | 3:44 | 2000-07-08| 97| 97| 96 |
| 2000 | Aaliyah | I Don’t Wanna | 4:15 | 2000-01-29| 84| 62| 51 |
| 2000 | Aaliyah | Try Again | 4:03 | 2000-03-18| 59| 53| 38 |
| 2000 | Adams, Yolanda | Open My Heart | 5:30 | 2000-08-26| 76| 76| 74 |

Billboard Chart data from 2000 -- notice how the date is spread across different columns; however, if each row is a song is there any better way to do this?

An intermediate step is to make a new row for each song each week, like so.

| year | artist       | track                  | time | date       | week | rank |
|------|--------------|------------------------|------|------------|------|------|
| 2000 | 2Ge+her      | The Hardest Part Of... | 3:15 | 2000-09-02 | 1    | 91   |
| 2000 | 2Ge+her      | The Hardest Part Of... | 3:15 | 2000-09-09 | 2    | 87   |
| 2000 | 2Ge+her      | The Hardest Part Of... | 3:15 | 2000-09-16 | 3    | 92   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-02-26 | 1    | 87   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-03-04 | 2    | 82   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-03-11 | 3    | 72   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-03-18 | 4    | 77   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-03-25 | 5    | 87   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-04-01 | 6    | 94   |
| 2000 | 2 Pac        | Baby Don't Cry         | 4:22 | 2000-04-08 | 7    | 99   |
| 2000 | 3 Doors Down | Kryptonite             | 3:53 | 2000-04-08 | 1    | 81   |
| 2000 | 3 Doors Down | Kryptonite             | 3:53 | 2000-04-15 | 2    | 70   |
| 2000 | 3 Doors Down | Kryptonite             | 3:53 | 2000-04-22 | 3    | 68   |
| 2000 | 3 Doors Down | Kryptonite             | 3:53 | 2000-04-29 | 4    | 67   |
| 2000 | 3 Doors Down | Kryptonite             | 3:53 | 2000-05-06 | 5    | 66   |

There are still issues, though. For example, notice how many times we repeat the basic metadata of each song (year, artist, time).

The "tidy" way to address this is by considering this in terms of "observations" and differing observational units. In this case, "observational unit" mostly means the row. If we split this into two tables, one whose unit is the song and one whose unit is a song's rank from week to week, here's what it might look like.



**Billboard Table 1**

| id   | artist | track | time |
| ---- | ------ | ----- | ---- |
| 1 | 2 Pac Baby | Don’t Cry | 4:22 |
| 2 | 2Ge+her | The Hardest Part Of ... | 3:15 |
| 3 | 3 Doors Down | Kryptonite | 3:53 |
| 4 | 3 Doors Down | Loser | 4:24 |
| 5 | 504 Boyz | Wobble Wobble | 3:35 |
| 6 | 98^0 | Give Me Just One Nig... | 3:24 |
| 7 | A*Teens | Dancing Queen | 3:44 |
| 8 | Aaliyah | I Don’t Wanna | 4:15 |
| 9 | Aaliyah | Try Again | 4:03 |
| 10 | Adams, Yolanda | Open My Heart | 5:30 |

**Billboard Table 2**

| id   | date | rank |
| ---- | ---- | ---- |
| 1 | 2000-02-26 | 87 |
| 1 | 2000-03-04 | 82 |
| 1 | 2000-03-11 | 72 |
| 1 | 2000-03-18 | 77 |
| 1 | 2000-03-25 | 87 |
| 1 | 2000-04-01 | 94 |
| 1 | 2000-04-08 | 99 |
| 2 | 2000-09-02 | 91 |
| 2 | 2000-09-09 | 87 |
| 2 | 2000-09-16 | 92 |


### 5. Single observational unit should appear in a single table

Though we won't delve into this, for completeness, we'll mention that another common issue is observational units across multiple tables. Simply put, it's often the case that all the "observations" or rows may not all be in the same table. Imagine census data in which different counties are stored in separate files or the details of a historical trading voyage stored in different ledgers, possibly in different archives. The tidy way to deal with this before analysis, would be to combine them into a single table or file.

## Challenge

Looking at our 1847 census dataset, can you find an example of the first four  issues? What would it take to tidy them up?

- Column headers should be variables not values.
- One column should describe one variable.
- Variables should be in columns not rows.
- Different observational units should appear in different tables.

[<<< Previous](exploring-openrefine.md) | [Next >>>](transforming-columns.md)
