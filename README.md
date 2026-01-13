Activity 4: Data visualization 2: Customizing plots
================

# Overview

Welcome! Today’s activity is all about the basics of customizing plots.
We will continue using `ggplot2` and will use two built-in datasets for
this activity (no reading in data is necessary today!).

You will submit two outputs for this activity:

1.  A **PDF** of a rendered Quarto document with all of your R code (see
    below). Please include all of the code that appears in this
    document, in addition to adding your own code in the “Q#” sections.

2.  A plot and research question from the final section

A note about submitting code:

As a general practice, it is good to **use headers to denote which
section of the homework** you are in and **add in your own comments
about what each line is actually doing** - this is excellent practice
for organizing your own big R scripts in the future. The biggest way
that you will code for probably the first few years of your coding
career will consist of you revisiting old R scripts and copying/pasting
code and/or adapting that code to your current problems. I promise you,
your future self will be thrilled with your current self if you take the
extra few minutes to 1) organize your code in a nice way and 2) provide
detailed comments about what each line is doing (as well as what
questions you have about it).

Also, don’t be afraid to use lots of blank lines! It is MUCH nicer for
your future self to look at code that has a few blank lines in between
sections of code than a bajillion lines in a row of straight code.

*From here on, please put headers (either as comments in the code or as
Quarto headers) to denote which question you are answering (e.g. “Q1:”)
and precede your code with comments that describe what that code does.*

# 1) Penguins!

## Setting up

First, let’s load our packages. You should already have the `here` and
`ggplot2` packages installed; read them in from the library in your
code. Also install and read in the `palmerpenguins` package, which
contains built-in data.

``` r
# install.packages("palmerpenguins")
library(ggplot2)
library(here)
library(palmerpenguins)
```

We just installed a package which has data built into it. We are going
to go ahead and store the `penguins` data frame as a data object anyway
(not technically necessary because it’s already built-in, but this
reinforces storing dataframes).

``` r
# Read in the palmer penguins data
penguins <- penguins
```

Next, let’s navigate to the help page of this dataset. Doing so provides
information on the dataset and its various columns. We can learn that
this dataset “includes measurements for penguin species, island in
Palmer Archipelago, size (flipper length, body mass, bill dimensions),
and sex”. Read on to learn about each column in the dataset.

``` r
# Putting a "?" in front of a function (or built-in dataset) will automatically bring up its help page!
?penguins
```

## Start with a question

Let’s start by forming a research question. Let’s ask: How are bill
length and bill depth associated, and how does this vary by species of
penguin?

Let’s create a basic graph to begin, but plotting `bill_length_mm` on
the x-axis and `bill_depth_mm` on the y-axis.

``` r
ggplot(data = penguins, aes(x = bill_length_mm, y = bill_depth_mm)) +
  geom_point()
```

    Warning: Removed 2 rows containing missing values or values outside the scale range
    (`geom_point()`).

![](README.markdown_github_files/figure-markdown_github/unnamed-chunk-3-1.png)

### Q1.1: Do you see a relationship?

Does it look like there is a relationship between these variables?
Describe the relationship.

### Q2.2: Color the points by species of penguin

That previous graph only addresses part of our question: we asked not
only “how are bill length and bill depth associated”, but also “**how
does this vary by species of penguin**?”

Next, 1) change the aesthetics of this plot to color the points by the
species of penguin and 2) interpret the graph by describing if this
changes your answer to the previous question.

The take-home message here is to be thorough with how you look at your
data! If you ignore certain variables, you might miss important patterns
(this is also crucial when deciding what statistical models we should
run on our data, but more on that in a few weeks!).

Ok, now let’s jump into some fun data visualization!

## 

# 2) CO2 Uptake in Grass Plants Data

Next, it’s time to practice what you’ve learned again! R has a number of
built-in datasets. The dataset `CO2` provides the data from an
experiment on the cold tolerance of a grass species. Familiarize
yourself with the dataset by reading the help page for this dataset

``` r
# Putting a "?" in front of a function (or built-in dataset) will automatically bring up its help page!
?CO2
```

### Q2.1: Write a research question that you would like to answer

Once you have a sense of what is in the dataset, write a research
question that you would like to answer. There are many options with
varying complexity!

### Q2.2: Choose a graph to answer your question

What graph would be appropriate to answer this question? Think about the
kinds of graphs we’ve used so far and whether your variables are
continuous or categorical.

### Q2.3: Create your graph
