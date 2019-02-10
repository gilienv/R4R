<img src = /Images/R4R_header.png>

## Formatting data tables in Spreadsheets
 
 
 | Overview | Description |
| --- | --- |
| Teaching | 15 minutes |
| Exercises | 20 minutes | 
| Question| How do we format data in spreadsheets for effective data use? |
| Objective | Describe best practices for data entry and formatting in spreadsheets |
| Presenters | [Gitanjali Yadav](http://www.nipgr.res.in/research/dr_gyadav.php) and [Ashley Sawle](https://www.cruk.cam.ac.uk/author/ashley-sawle) | 
 
* The most common mistake made is treating spreadsheet programs like lab notebooks, that is,
relying on context, notes in the margin,
spatial layout of data and fields to convey information. As humans, we
can (usually) interpret these things, but computers don’t view information the same way, and
unless we explain to the computer what every single thing means (and
that can be hard!), it will not be able to see how our data fits
together.</p>

* Using the power of computers, we can manage and analyze data in much more 
effective and faster ways, but to use that power, we have to set up
our data for the computer to be able to understand it (and computers are very 
literal).</p>

* This is why it’s extremely important to set up well-formatted
tables from the outset - before you even start entering data from
your very first preliminary experiment. Data organization is the
foundation of your research project. It can make it easier or harder
to work with your data throughout your analysis, so it’s worth
thinking about when you’re doing your data entry or setting up your
experiment. You can set things up in different ways in spreadsheets,
but some of these choices can limit your ability to work with the data in other programs or
have the you-of-6-months-from-now or your collaborator work with the
data.</p>

<blockquote>
  <p>Note: the best layouts/formats (as well as software and
interfaces) for data entry and data analysis might be
different. It is important to take this into account, and ideally
automate the conversion from one to another.</p>
</blockquote>

<h3 id="keeping-track-of-your-analyses">Keeping track of your analyses</h3>

<p>When you’re working with spreadsheets, during data clean up or analyses, it’s
very easy to end up with a spreadsheet that looks very different from the one
you started with. In order to be able to reproduce your analyses or figure out
what you did when Reviewer #3 asks for a different analysis, you should</p>

<ul>
  <li>create a new file with your cleaned or analyzed data. Don’t modify
the original dataset, or you will never know where you started!</li>
  <li>keep track of the steps you took in your clean up or analysis. You should track 
these steps as you would any step in an experiment. We recommend that you 
do this in a plain text file stored in the same folder as the data file.</li>
</ul>

<p>This might be an example of a spreadsheet setup:</p>

<p><img src=/Images/spreadsheet1.png alt="spreadsheet setup" /></p>

<p>Put these principles in to practice today during your Exercises.</p>

<blockquote>
  <p>Note: This is out of scope for this lesson, but for information on how to maintain version control over your data, look at our lesson on <a href="http://swcarpentry.github.io/git-novice/">‘Git’</a>.</p>
</blockquote>

<h3 id="structuring-data-in-spreadsheets">Structuring data in spreadsheets</h3>

<p>The cardinal rules of using spreadsheet programs for data:</p>

<ol>
  <li>Put all your variables in columns - the thing you’re measuring,
like ‘weight’ or ‘temperature’.</li>
  <li>Put each observation in its own row.</li>
  <li>Don’t combine multiple pieces of information in one
cell. Sometimes it just seems like one thing, but think if that’s
the only way you’ll want to be able to use or sort that data.</li>
  <li>Leave the raw data raw - don’t change it!</li>
  <li>Export the cleaned data to a text-based format like CSV (comma-separated values) format. This
ensures that anyone can use the data, and is required by
most data repositories.</li>
</ol>

<p>For instance, we have data from a survey of small mammals in a desert
ecosystem. Different people have gone to the field and entered data into a spreadsheet. They keep track of things like species, plot,
weight, sex and date collected.</p>

<p>If they were to keep track of the data like this:</p>

<p><img src=/Images/multiple-info.png alt="multiple-info example" /></p>

<p>the problem is that species and sex are in the same field. So, if they wanted to 
look at all of one species or look at different weight distributions by sex, 
it would be hard to do this using this data setup. If instead we put sex and species 
in different columns, you can see that it would be much easier.</p>

<h3 id="columns-for-variables-and-rows-for-observations">Columns for variables and rows for observations</h3>

<p>The rule of thumb, when setting up a datasheet, is columns =
variables, rows = observations, cells = data (values).</p>

<p>So, instead we should have:</p>

<p><img src="/Images/single-info.png" alt="single-info example" /></p>

## Discussion
- If not already discussed, introduce the dataset that will be used in this lesson, and in the other ecology lessons, the <a href="http://www.datacarpentry.org/ecology-workshop/data/">Portal Project Teaching Dataset</a>
- The data used in the ecology lessons are observations of a small mammal community in southern Arizona. This is part of a project studying the effects of rodents and ants on the plant community that has been running for almost 40 years. The rodents are sampled on a series of 24 plots, with different experimental manipulations controlling which rodents are allowed to access which plots.
- This is a real dataset that has been used in over 100 publications. We’ve simplified it just a little bit for the workshop, but you can download the full dataset and work with it using exactly the same tools we’ll learn about today.
 
 ## Exercise
- We’re going to take a messy version of the survey data and describe how we would clean it up.
	- Download the data by clicking <a href="https://ndownloader.figshare.com/files/2252083">here</a> to get it from FigShare.
	- Open up the data in a spreadsheet program.</li>
	- You can see that there are two tabs. Two field assistants conducted the surveys, one in 2013 and one in 2014, and they both kept track of the data in their own way. Now you’re the person in charge of this project and you want to be able to 
start analyzing the data.</li>
	- With the person next to you, identify what is wrong with this spreadsheet. Also discuss the steps you would need to take to clean up the 2013 and 2014 tabs, and to put them all together in one spreadsheet.
	- Important:  Do not forget our first piece of advice: to create a new file (or tab) for the cleaned data, never modify your original (raw) data.
	- After you go through this exercise, we’ll discuss as a group what was wrong with this data and how you would fix it.</p>


## Reference
* An excellent reference, in particular with regard to R scripting is Hadley Wickham, <em>Tidy Data</em>, Vol. 59, Issue 10, Sep 2014, Journal of Statistical Software. <a href="http://www.jstatsoft.org/v59/i10">http://www.jstatsoft.org/v59/i10</a>


## Key Points
- Never modify your raw data. Always make a copy before making any changes.
- Keep track of all of the steps you take to clean your data in a plain text file.
- Organize your data according to tidy data principles.

---

| <a href="/Documents/Day02_Intro.md"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="/Documents/Day02_Problems.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | <a href="/Documents/Day02_Sol1.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Solution to Exercise</span></a> 
  | ---- | ----| ----| 
  
---
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
	
