<img src = /Images/R4R_header.png>

## Formatting problems
 
 
 | Overview | Description |
| --- | --- |
| Teaching | 20 minutes |
| Exercises | 0 minutes | 
| Question| What are some common challenges with formatting data in spreadsheets and how can we avoid them? |
| Objective | Recognize and resolve common spreadsheet formatting problems. |
| Presenters | [Gitanjali Yadav](http://www.nipgr.res.in/research/dr_gyadav.php) and [Ashley Sawle](https://www.cruk.cam.ac.uk/author/ashley-sawle) | 

* Good data organization is the foundation of your research
project. Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are very useful graphical
interfaces for designing data tables and handling very basic data
quality control functions. 




## Common Spreadsheet Errors

<p>This lesson is meant to be used as a reference for discussion as learners identify issues with the messy dataset discussed in the
previous lesson. Instructors: don’t go through this lesson except to refer to responses to the exercise in the previous lesson.</p>

<p>There are a few potential errors to be on the lookout for in your own data as well as data from collaborators or the Internet. If you are aware of the errors and the possible negative effect on downstream data analysis and result interpretation, it might motivate yourself and your project members to try and avoid them. Making small changes to the way you format your data in spreadsheets, can have a great impact on efficiency and reliability when it comes to data cleaning and analysis.</p>

<ul>
  <li><a href="#tables">Using multiple tables</a></li>
  <li><a href="#tabs">Using multiple tabs</a></li>
  <li><a href="#zeros">Not filling in zeros</a></li>
  <li><a href="#null">Using problematic null values</a></li>
  <li><a href="#formatting">Using formatting to convey information</a></li>
  <li><a href="#formatting_pretty">Using formatting to make the data sheet look pretty</a></li>
  <li><a href="#units">Placing comments or units in cells</a></li>
  <li><a href="#info">Entering more than one piece of information in a cell</a></li>
  <li><a href="#field_name">Using problematic field names</a></li>
  <li><a href="#special">Using special characters in data</a></li>
  <li><a href="#metadata">Inclusion of metadata in data table</a></li>
  <li><a href="/Documents/Day02_Dates.md">Date formatting</a></li>
</ul>

<h2 id="-using-multiple-tables"><a name="tables"></a> Using multiple tables</h2>

<p>A common strategy is creating multiple data tables within
one spreadsheet. This confuses the computer, so don’t do this!
When you create multiple tables within one
spreadsheet, you’re drawing false associations between things for the computer,
which sees each row as an observation. You’re also potentially using the same
field name in multiple places, which will make it harder to clean your data up
into a usable form. The example below depicts the problem:</p>

<p><img src="/Images/2_datasheet_example.jpg" alt="multiple tabs" /></p>

<p>In the example above, the computer will see (for example) row 4 and assume that all columns A-AF 
refer to the same sample. This row actually represents four distinct samples 
(sample 1 for each of four different collection dates - May 29th, June 12th, June 19th, and June 26th), 
as well as some calculated summary statistics (an average (avr) and standard error of measurement (SEM)) for two of those samples. Other rows are similarly problematic.</p>

<h2 id="-using-multiple-tabs"><a name="tabs"></a> Using multiple tabs</h2>

<p>But what about workbook tabs? That seems like an easy way to organize data, right? Well, yes and no. When you create extra tabs, you fail to allow the computer to see connections in the data that are there (you have to introduce spreadsheet application-specific functions or scripting to ensure this connection). Say, for instance, you make a separate tab for each day you take a measurement.</p>

<p>This isn’t good practice for two reasons:
1) you are more likely to accidentally add inconsistencies to your data if each time you take a measurement, you start recording data in a new tab, and
2) even if you manage to prevent all inconsistencies from creeping in, you will add an extra step for yourself before you analyze the
data because you will have to combine these data into a single datatable. You will have to explicitly tell the computer how to combine
tabs - and if the tabs are inconsistently formatted, you might even have to do it manually.</p>

<p>The next time you’re entering data, and you go to create another tab or table, ask yourself if you could avoid adding this tab by adding another column to your original spreadsheet. We used multiple tabs in our example of a messy data file, but now you’ve seen how you can reorganize your data to consolidate across tabs.</p>

<p>Your data sheet might get very long over the course of the experiment. This makes it harder to enter data if you can’t see your headers
at the top of the spreadsheet. But don’t repeat your header row. These can easily get mixed into the data, 
leading to problems down the road.</p>

<p>Instead you can freeze the column headers so that they remain visible even when you have a spreadsheet with many rows.</p>

<p><a href="https://support.office.com/en-ca/article/Freeze-column-headings-for-easy-scrolling-57ccce0c-cf85-4725-9579-c5d13106ca6a">Documentation on how to freeze column headers</a></p>

<h2 id="-not-filling-in-zeros"><a name="zeros"></a> Not filling in zeros</h2>

<p>It might be that when you’re measuring something, it’s
usually a zero, say the number of times a rabbit
is observed in the survey. Why bother
writing in the number zero in that column, when it’s mostly zeros?</p>

<p>However, there’s a difference between a zero and a blank cell in a spreadsheet. To the computer, a zero is actually data. You measured
or counted it. A blank cell means that it wasn’t measured and the computer will interpret it as an unknown value (otherwise known as a
null value).</p>

<p>The spreadsheets or statistical programs will likely mis-interpret blank cells that you intend to be zeros. By not entering the value of
your observation, you are telling your computer to represent that data as unknown or missing (null). This can cause problems with 
subsequent calculations or analyses. For example, the average of a set of numbers which includes a single null value is always null
(because the computer can’t guess the value of the missing observations). Because of this, it’s very important to record zeros as zeros and truly missing data as nulls.</p>

<h2 id="-using-problematic-null-values"><a name="null"></a> Using problematic null values</h2>
<p><strong>Example</strong>: using -999 or other numerical values (or zero) to represent missing data.</p>

<p><strong>Solutions</strong>:</p>

<p>There are a few reasons why null values get represented differently within a dataset.
Sometimes confusing null values are automatically recorded from the measuring device. If that’s the case, there’s not much you can do, but it can be addressed in data cleaning with a tool like <a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/">OpenRefine</a> before analysis. Other times different null values are used to convey different reasons why the data isn’t there. This is important information to capture, but is in effect using one column to capture two pieces of information. Like for <a href="#formatting">using formatting to convey information</a> it would be good here to create a new column like ‘data_missing’ and use that column to capture the different reasons.</p>

<p>Whatever the reason, it’s a problem if unknown or missing data is recorded as -999, 999, or 0.
Many statistical programs will not recognize
that these are intended to represent missing (null) values. How these values are interpreted will depend on the software you use to
analyze your data. It is essential to use a clearly defined and consistent null indicator.
Blanks (most applications) and NA (for R) are good choices. White et al, 2013, explain good choices for indicating null values for different software applications in their article:
<a href="https://peerj.com/preprints/7/">Nine simple ways to make it easier to (re)use your data.</a> Ideas in Ecology and Evolution.</p>

<p><img src="/Images/3_white_table_1.jpg" alt="White et al." /></p>

<h2 id="-using-formatting-to-convey-information"><a name="formatting"></a> Using formatting to convey information</h2>

<p><strong>Example</strong>: highlighting cells, rows or columns that should be excluded from an analysis, leaving blank rows to indicate separations in data.</p>

<p><img src="/Images/formatting.png" alt="formatting" /></p>

<p><strong>Solution</strong>: create a new field to encode which data should be excluded.</p>

<p><img src="/Images/good_formatting.png" alt="good formatting" /></p>

<h2 id="-using-formatting-to-make-the-data-sheet-look-pretty"><a name="formatting_pretty"></a> Using formatting to make the data sheet look pretty</h2>

<p><strong>Example</strong>: merging cells.</p>

<p><strong>Solution</strong>: If you’re not careful, formatting a worksheet to be more aesthetically pleasing can compromise your computer’s ability to
see associations in the data. Merged cells will make your data unreadable by statistics software. Consider restructuring your data in
such a way that you will not need to merge cells to organize your data.</p>

<h2 id="-placing-comments-or-units-in-cells"><a name="units"></a> Placing comments or units in cells</h2>

<p><strong>Example</strong>: Your data was collected, in part, by a summer student who you later found out was mis-identifying some of your species, some
of the time. You want a way to note these data are suspect.</p>

<p><strong>Solution</strong>: Most analysis software can’t see Excel or LibreOffice comments, and would be confused by comments placed within your data
cells. As described above for formatting, create another field if you need to add notes to cells. Similarly, don’t include units in
cells: ideally, all the measurements you place in one column should be in the same unit, but if for some reason they aren’t, create
another field and specify the units the cell is in.</p>

<h2 id="-entering-more-than-one-piece-of-information-in-a-cell"><a name="info"></a> Entering more than one piece of information in a cell</h2>

<p><strong>Example</strong>: You find one male, and one female of the same species. You enter this as 1M, 1F.</p>

<p><strong>Solution</strong>: Don’t include more than one piece of information in a cell. This will limit the ways in which you can analyze your data. 
If you need both these measurements, design your data sheet to include this information. For example, include one column for number of
individuals and a separate column for sex.</p>

<h2 id="-using-problematic-field-names"><a name="field_name"></a> Using problematic field names</h2>
<p>Choose descriptive field names, but be careful not to include spaces, numbers, or special characters of any kind. Spaces can be
misinterpreted by parsers that use whitespace as delimiters and some programs don’t like field names that are text strings that start
with numbers.</p>

<p>Underscores (<code class="highlighter-rouge">_</code>) are a good alternative to spaces. Consider writing names in camel case (like this: ExampleFileName) to improve
readability. Remember that abbreviations that make sense at the moment may not be so obvious in 6 months, but don’t overdo it with names
that are excessively long. Including the units in the field names avoids confusion and enables others to readily interpret your fields.</p>

<b>Examples</b> 

<table bgcolor="red"  align="left" style="width =50%; border: 1px green;">
<tr>
	<td> <b>Good Name</b></td> <br />
	<td> <b>Good Alternative </b> </td><br />
	<td> <b>Avoid </b></td><br />
</tr>
<tr>
	<td> Max_temp_C</td>
	<td> MaxTemp </td>
	<td> Maximum Temp (°C) </td>
</tr>
<tr>
	<td> Precipitation_mm</td>
	<td> Precipitation</td>
	<td> precmm </td>
</tr>	
<tr>
	<td> Mean_year_growth</td>
	<td> MeanYearGrowth </td>
	<td> Mean growth/year</td>	
</tr>	
<tr>
	<td> sex </td>
	<td> sex </td>	
	<td> M/F </td>
</tr>
<tr>	
	<td> weight </td>
	<td> weight </td>	
	<td> w.</td>	
</tr>
<tr>	
	<td> cell_type </td>
	<td> CellType </td>
	<td> Cell Type </td>
</tr>
<tr>
	<td> Observation_01 </td>
	<td> first_observation</td>
	<td> 1st Obs</td>
</tr>
</table>

<h2 id="-using-special-characters-in-data"><a name="special"></a> Using special characters in data</h2>

<p><strong>Example</strong>: You treat your spreadsheet program as a word processor when writing notes, for example copying data directly from Word or
other applications.</p>

<p><strong>Solution</strong>: This is a common strategy. For example, when writing longer text in a cell, people often include line breaks, em-dashes,
etc in their spreadsheet.  Also, when copying data in from applications such as Word, formatting and fancy non-standard characters (such
as left- and right-aligned quotation marks) are included.  When exporting this data into a coding/statistical environment or into a
relational database, dangerous things may occur, such as lines being cut in half and encoding errors being thrown.</p>

<p>General best practice is to avoid adding characters such as newlines, tabs, and vertical tabs.  In other words, treat a text cell as if
it were a simple web form that can only contain text and spaces.</p>

<h2 id="-inclusion-of-metadata-in-data-table"><a name="metadata"></a> Inclusion of metadata in data table</h2>

<p><strong>Example</strong>: You add a legend at the top or bottom of your data table explaining column meaning, units, exceptions, etc.</p>

<p><strong>Solution</strong>: Recording data about your data (“metadata”) is essential. You may be on intimate terms with your dataset while you are 
collecting and analysing it, but the chances that you will still remember that the variable “sglmemgp” means single member of group, for
example, or the exact algorithm you used to transform a variable or create a derived one, after a few months, a year, or more are slim.</p>

<p>As well, there are many reasons other people may want to examine or use your data - to understand your findings, to verify your findings,
to review your submitted publication, to replicate your results, to design a similar study, or even to archive your data for access and 
re-use by others. While digital data by definition are machine-readable, understanding their meaning is a job for human beings. The 
importance of documenting your data during the collection and analysis phase of your research cannot be overestimated, especially if your
research is going to be part of the scholarly record.</p>

<p>However, metadata should not be contained in the data file itself. Unlike a table in a paper or a supplemental file, metadata (in the 
form of legends) should not be included in a data file since this information is not data, and including it can disrupt how computer 
programs interpret your data file. Rather, metadata should be stored as a separate file in the same directory as your data file, 
preferably in plain text format with a name that clearly associates it with your data file. Because metadata files are free text format,
they also allow you to encode comments, units, information about how null values are encoded, etc. that are important to document but can
disrupt the formatting of your data file.</p>

<p>Additionally, file or database level metadata describes how files that make up the dataset relate to each other; what format are they are 
in; and whether they supercede or are superceded by previous files. A folder-level readme.txt file is the classic way of accounting for 
all the files and folders in a project.</p>

<p>(Text on metadata adapted from the online course Research Data <a href="http://datalib.edina.ac.uk/mantra">MANTRA</a> by EDINA and Data Library, University of Edinburgh. MANTRA is licensed under a <a href="https://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.)</p>

 ## Key Points
- Avoid using multiple tables within one spreadsheet.
- Avoid spreading data across multiple tabs
- Record zeros as zeros.
- Use an appropriate null value to record missing data.
- Don’t use formatting to convey information or to make your spreadsheet look pretty.
- Place comments in a separate column.
- Record units in column headers.
- Include only one piece of information in a cell
- Avoid spaces, numbers and special characters in column headers.
- Avoid special characters in your data
- Record metadata in a separate plain text file.

## End of Lesson 

---

| <a href="/Documents/Day02_Format.md"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="/Documents/Day02_Dates.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | 
  | ---- | ----|    
  
 ---
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
	
