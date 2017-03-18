# Programming

It might seem strange that programming is listed here before things like statistics or domain knowledge, but the reality is that you can’t do anything without knowing how to code. Theoretical statistics is useful, as is knowledge of campaigns, but in order to be analyst, you need to know how to produce scalable, replicable work.[^1]

## Core Skills

A handy metric that for how well do you know something is "how much Googling does it take for you to do something?" 

Core skills are things that you should be able to get within 3 Googles or less, i.e., they’re something that you’re basically able to do off-the-cuff but might need some reminder on the details.

Note: in the following section, when I refer to data or a dataset, you should picture something like an individual-level dataset where every row is an individual and the columns are things like first name, last name, gender, age, etc.

### Data Munging

* Data Input/Output (IO): read in data, export data, and transform data into different file types

* Subset to a part of the data by some condition, i.e. drop observations. For example, subset the dataset so that only women are left in it.

* Clean up a messy column of data. For example, maybe a variable should be coded as 1 through 6, but there are 99s in the data. Could you recode all of the 99s to 0s or something?

* Merge datasets together based on an arbitrary number of columns and check to make sure that your merge worked correctly

* Recode columns from strings to numbers or vice versa

* Generate new columns by combining old columns. Maybe this means you’re multiplying two variables together, or you’re going to create a new column that returns a TRUE/FALSE value for if you’re a 65+ woman based on your age and gender columns

* Reformat your data from [wide to long format](http://www.ats.ucla.edu/stat/r/faq/reshape.htm) and vice versa

### Basic Analysis and Graphing

* Print frequency counts of a column or multiple columns (i.e., print every unique value and the counts of those values)

* Find the mean, median, mode, and various percentiles of a column

* You should know how to generate histograms, bar plots, scatter plots, and line plots. Ideally, you should be able to generate plots that include multiple categories (i.e., scatterplot of age vs. income with different colors for men vs women).

* You should be able to clean up your plots, i.e., label your axes, add titles, change colors, etc. 

### Coding best practices

* Document your code.[^3] Help your reader understand what you're trying to do. Your future self will thank you.

* Follow style guides. Google has quite [lovely style guides](https://github.com/google/styleguide/) for most major languages. Use them (or something similar).

* You should understand the appropriate places for `for` loops and `if/else` statements.

* Write DRY (Don't Repeat Yourself) code and use functions. A rule of thumb that’s often used is that you can copy things twice, but once you’re writing things three times, you should be wrapping it into a function.

### Finding Your Own Answers

If you only learn one thing in this programming section, let it be the ability to find your own answers.

There’s this site called [Let Me Google That For You](http://lmgtfy.com/). If your colleagues are sending you links from that site, things are very, very bad. If they’re sending you links from Google directly, they’re just being polite.

As a junior analyst, you're going to have lots of questions, and you need to figure out how to get answers to those questions without asking your boss or colleagues all the time. If you run into an error message, throw it into Google and see what pops out. There’s an art to figuring out the key terms that you should be Googling, but the only way to learn it is to throw a bunch of stuff at the wall.

In general, here are some tips for debugging code/troubleshooting:

* Drop your error message right into Google or Stack Exchange.

* Remind yourself what the objective is. Abstract away from your specific problem and try to figure out the general principle of what you’re trying to accomplish. Then, google that.

* Write things down using pen and paper.

* Break down your code and write small "tests". Take a few lines at a time---is the output what you expect it is?

* Check stupid syntax things. Are your commas in the right place, etc.?[^2]

## Core Tools

### SQL

Before I get into other languages, I feel compelled to highlight Structured Query Language, or SQL (pronounced either "si-kwel" or saying the letters S-Q-L). SQL is how you interact with large databases, e.g. a voter file. As an analyst, you won’t be doing a lot of data manipulation in SQL because SQL doesn’t support statistics very well, but you will be using SQL heavily in order to access data. I sometimes joke that SQL is the lingua franca of progressive politics beacuse it's the one language that everyone from analysts to data managers to database engineers will actually know.

Here are some basic things that you should expect to know how to do in SQL by the end of your first six months in this industry. It’s okay not to know any of this going in, but SQL is pretty easy to learn if you know another programming language.

* SELECT statements to select data

* WHERE clauses to add conditions on the data that you select

* use CASE WHEN statements because SQL doesn’t believe in "if" statements

* JOINing tables together (and understand the difference between LEFT and INNER joins)

* How to CREATE and DROP tables

* How to GROUP BY a column and calculate aggregates

Good tutorials include [SQLZOO](http://sqlzoo.net/), [Codecademy](https://www.codecademy.com/learn/learn-sql), [ModeAnalytics SQL School](https://sqlschool.modeanalytics.com/toc/), and [w3 Schools](http://www.w3schools.com/sql/).

### Excel

If SQL is the common language of progressive data, then Excel is the common tool. People will get snobby about Excel at times, but if you need to do a fast, simple analysis, then Excel is probably the best tool for you.

Here are the basic things you should know how to do in Excel:

* INDEX-MATCH (old-school Excel whizzes will tell you to use VLOOKUP, but INDEX-MATCH is strictly superior)

* Pivot Tables

* IF-Statements

* Removing duplicates

* SUM and SUM-IF statements

* CONCATENATE strings together

* Basic graphing and data visualization

I honestly haven't found great resources for Excel, but [Chandoo](http://chandoo.org/wp/excel-tutorial/) looks pretty comprehensive.

### General-Purpose Programming Languages

You should learn a general-purpose programming language like R or Python to be taken seriously.[^4] Yes, there will always be organizations who are willing to take a chance on folks who know nothing, but your search will be so much easier if you already know one of these languages. (If you stay in the industry long enough, odds are good that you’ll end up learning both, so it doesn’t really matter which one you learn first.)

#### R

Depending on whom you ask, R is either a wildly popular language for statistics or an awful language put together by statisticians who couldn’t code their way out of a paper bag. R is built on matrices, so if you can keep that in your head, then you’ll probably be fine. That said, R is definitely a more annoying language than Python for writing any type of software: managing dependencies and testing is way harder. (But as an entry-level analyst, these words don’t need to mean much to you.)

Useful packages to learn[^5]:

* dplyr (for data munging)

* stats (for stats)

* ggplot (for plotting)

You might want to download RStudio in addition to R, which will make your workspace a bit easier to manager.

There are lots of resources for learning R, but [swirL](http://swirlstats.com/), [Code School](http://tryr.codeschool.com/), [Roger Peng’s Coursera course](https://www.coursera.org/learn/r-programming), [David Robinson’s RData course](http://varianceexplained.org/RData/), and [Functional Programming in R](https://www.dropbox.com/sh/gf30g4mhj7vs78y/AACKtUckmSmSES-dEwS3EQzNa/1-functions.pdf?dl=0) are my favorites.

#### Python[^6]

Python is one of the most popular computing languages in the world, which is both good and bad. It’s written by and for software developers, so it does lots of things easily that R struggles with (classes, testing, and virtual environments come to mind immediately). It’s also arguably more (human-)readable than most languages: Python forces your code to look nice. That said, there are fewer statistical tools written in Python than R, so if you’re working in analytics, you’ll probably end up writing extensions from Python to R.

Useful packages to learn:

* pandas (for data-munging)

* numpy (for math)

* statsmodels (for stats/econometrics)

* scikit-learn (for machine learning)

* matplotlib, seaborn, or ggplot (for plotting)

You should consider doing all of this in [jupyter notebook](http://pgbovine.net/ipython-notebook-first-impressions.htm), which ties together your code and visualizations nicely.

Like R, there are lots of good resources for learning Python. Some of my favorites include [Learn Python the Hard Way](http://learnpythonthehardway.org/), [Think Python](http://www.greenteapress.com/thinkpython2/index.html), [Python for Social Scientists](http://www.pythonforsocialscientists.org/), and [A list of Python Tutorials for Social Scientists](http://nealcaren.github.io/python-tutorials/).

Berkeley PoliSci offers a good [course on computational tools for social research](https://github.com/ribernhard/PS239T) that covers a lot of this stuff for R and Python. The Python section has neater code than the R section, so if you're relying on this for R, you might want to also look at a [style guide](http://adv-r.had.co.nz/Style.html).

#### A Note on Stata and SPSS

If you don’t know Stata or SPSS, skip this section, and thank your statistics professors.

Stata is a statistical program used largely by economists and political scientists.[^7] It is not open-source, and a license costs thousands of dollars per year for organizations. As a result, it’s an expensive investment for organizations, and, worse, many of the cutting-edge statistical algorithms/packages are no longer written in Stata. SPSS is also a proprietary statistical program and suffers from many of the same drawbacks as Stata.

Because Stata and SPSS are fundamentally designed to be *programs *and not *languages* (even if both have a scripting option), there are things that are literally impossible (or very, very difficult) in Stata or SPSS that are easy in R or Python, e.g., web-scraping, text analysis, network analysis, Bayesian modeling, and most of the topics listed below under advanced scripting.

That said, there are a number of strategy polling firms and even some analytics firms who still use Stata or SPSS. I wouldn’t recommend taking time to learn either of them, but if you know them, they might be helpful. But you should realize that Stata is a poor signaling device. If you’ve been a student (undergraduate or graduate) in the last 2-3 years and want to be serious about data analysis, then you need to learn something more--not just to get hired but to actually do the work.

## Advanced Skills

These aren’t skills that you need to have going in, but you have any one of them, they’ll be useful. Make sure to highlight them in your resume. Many of them *are *skills that you should reasonably be expected to learn in 1-2 years, though. If the senior analysts at your organization don’t have these types of skills, you should think seriously about how technical the organization is and how technical you want it to be.

### Version Control

Create a GitHub account. Learn to use version control in the context of larger collaborative projects, i.e. using branching and merging.

[tryGit](https://try.github.io) is a good tutorial.

### Command Line Interfaces

You should be able to do basic things in the command line like move in and out of directories, find files, edit files on the command line (using either nano, vim, or emacs), move files, copy files, and delete files.

More advanced users should be able to do analysis and data munging on the command line using commands like awk. This is really useful when you’re working with large files, where command line tools will enable you to work with larger datasets than can normally fit in memory.

[Code Academy](https://www.codecademy.com/learn/learn-the-command-line) has some great tutorials. For a more unorthodox approach, try [Over the Wire Wargames](http://overthewire.org/wargames/), which teaches you command line tools by having you hack into servers.

### Advanced Scripting

Advanced scripting is a pretty generic category, but here are some useful skills to learn: 

* How to write your own packages and modules. Regardless of what language you’re working in, you will probably want to create some sort of centralized package that is used to distribute key functions.

* Bash Scripting. Write programs that run off the command line! Really useful because it can mash together scripts from a bunch of different languages

* APIs. You should understand how to hit APIs to gather information. If you want practice, the [Sunlight Foundation](https://sunlightfoundation.com/api/) has some particularly nice APIs with really fun datasets.

* Web scraping. Take data from the internet and turn it into a machine-readable format by parsing HTML, XML, and JSON formats

* Server administration and database management. Ideally, you’ll always work at an organization with an IT department and a Dev-Ops team. (They’re like the black magic of technology organizations: no one really knows what they do, but they make things run.) In practice, you should know how to set up basic databases like SQLITE, Postgres, or MongoDB on your own. Amazon Web Services offers a [1-year free tier](http://aws.amazon.com/free‎) where you can play around on a server.

* Web Development. Learn to make your own web-apps (perhaps on [Heroku](https://www.heroku.com/)). Know your away around the basics of HTML/CSS (and for the love of God, don’t reinvent the wheel. Just use [Bootstrap](http://getbootstrap.com/))

### Reporting and Advanced Graphing

Your analysis is only useful if other people can understand it. And that often means producing lots of charts and graphs. Also, the extraordinary influx of data has meant that decision-makers like reports. Even when those reports are totally pointless. You’ll still have to learn how to make them.

When you do this stuff, though, you should be prepared to do this stuff *over and over *again. So...try to set up reports that can be updated easily.

Some popular graphing tools:

* Tableau is a pretty horrendous graphing package, but if you’re a junior analyst, you probably have to deal with it anyway! There’s a free version of Tableau that you can download. Play around with it for a day or two and build a dashboard. Then, slap it on your resume.[^8]

* Statistical plotting in R or Python. In R, you can use the default graphics (often called "Base R") or you can use the ggplot package. The ggplot package and syntax also exists in Python. Other options for Python include matplotlib and seaborn. Note that these tools are mostly used for static visualizations (the stuff that goes into reports and powerpoint decks).

* D3.js (Javascript). This is hard[^9] but potentially a worthwhile one to learn if you like data visualization and *want to do much more of it*. If you don’t like data visualization, then don’t bother. What’s great about D3.js is that you can make interactive graphics. All of the cool charts in the New York Times, for example, are made in D3.js.

### Mapping

You might consider mapping a subset of plotting, but maps are often particularly useful in politics in a way that’s not true generally. Geography is so prominent in politics that being able to make a great-looking map is actually a non-trivial skill. 

Here are some things you might use for mapping: 

* Google Fusion tables

* GIS (ARCGIS or QGIS)

* R or Python

* D3.js

[^1]: There are some organizations where you can get away with writing one-off pieces of code, but it likely means that the organization is inefficient. You should be striving to write good, clean code that can be used over and over again. But it’s okay if you’re starting off with one-off pieces of code, or if you’re using that for prototypes. But eventually, if you want your work to be useful, it needs to be replicable and scaleable, so you should be asking yourself how to modify your code to accomplish that.

[^2]: I can’t tell you the number of times I’ve gotten JavaScript code to work by chucking random commas everywhere.

[^3]: Seriously, organizations have been known to automatically throw out candidates who don’t add comments to their code.

[^4]: Note that this advice applies to analytics in particular. If you’re looking for a job as a data manager, then you probably won’t need these particular programming languages, but many of the advanced programming skills will apply to you.

[^5]: Really, anything by Hadley Wickham, who is a god among men.

[^6]: At the risk of starting a flame war, learn Python 3 (not Python 2). Anaconda is a good installation. Jupyter notebooks are excellent for beginners.

[^7]: If you want a career in social science academia, then Stata and SPSS may suffice for you. But if you're working at an organization that needs to do analysis at scale, you need to learn another language.

[^8]: There’s literally no such thing as a Tableau expert, so just fake it til you make it (or get promoted to the point where you never have to think about it again)

[^9]: The way I like to describe D3.js to folks is through the Carl Sagan quote "in order to make an apple pie, you must first create the universe." Well, in order to make a freaking scatterplot, you first need to decide the width of your plot, make your axes, map your data onto the axes, which gets mapped to the width of the plot, then add points, etc. 
