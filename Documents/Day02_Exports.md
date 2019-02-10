<img src = /Images/R4R_header.png>

## Exporting data 
 
 
 | Overview | Description |
| --- | --- |
| Teaching | 10 minutes |
| Exercises | 0 minutes | 
| Question| How can we export data from spreadsheets in a way that is useful for downstream applications?|
| Objective | Store spreadsheet data in universal file formats. |
| | Export data from a spreadsheet to a CSV file.| 
| Authors | [Gitanjali Yadav](http://www.nipgr.res.in/research/dr_gyadav.php) and [Ashley Sawle](https://www.cruk.cam.ac.uk/author/ashley-sawle) | 

* Good data organization is the foundation of your research
project. Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are very useful graphical
interfaces for designing data tables and handling very basic data
quality control functions. 


###### Q: Storing the data you’re going to work with for your analyses in Excel default file format (<code class="highlighter rouge">*.xls</code> or <code class="highlighter-rouge">*.xlsx</code> - depending on the Excel version) isn’t a good idea. Why

###### - Because it is a proprietary format, and it is possible that in the future, technology won’t exist (or will become sufficiently rare) to make it inconvenient, if not impossible, to open the file.
 
###### - Other spreadsheet software may not be able to open files saved in a proprietary Excel format.</p>
  
###### - Different versions of Excel may handle data differently, leading to inconsistencies.</p>
  
###### - Finally, more journals and grant agencies are requiring you to deposit your data in a data repository, and most of them don’t accept Excel format. It needs to be in one of the formats discussed below.</p>
 
###### *The above points also apply to other formats such as open data formats used by LibreOffice / Open Office. These formats are not static and do not get parsed the same way by different software packages.*
 

###### As an example of inconsistencies in data storage, do you remember how we talked about how Excel stores dates earlier? ###### It turns out that  there are multiple defaults for different versions of the software, and you can switch between them all. 
###### So, say you’re compiling Excel-stored data from multiple sources. There’s dates in each file- Excel interprets them as their own internally consistent serial numbers. When you combine the data, Excel will take the serial number from the place you’re importing it from, and interpret it using the rule set for the version of Excel you’re using. Essentially, you could be adding errors to your data, and it wouldn’t necessarily be flagged by any data cleaning methods if your ranges overlap.</p>

###### Storing data in a universal, open, and static format will help deal with this problem. Try tab-delimited (tab separated values or TSV) or comma-delimited (comma separated values or CSV). CSV files are plain text files where the columns are separated by commas, hence ‘comma separated values’ or CSV. The advantage of a CSV file over an Excel/SPSS/etc. file is that we can open and read a CSV file using just about any software, including plain text editors like TextEdit or NotePad. 
###### Data in a CSV file can also be easily imported into other formats and environments, such as SQLite and R. We’re not tied to a certain version of a certain expensive program when we work with CSV files, so it’s a good format to work with for maximum portability and endurance. Most spreadsheet programs can save to delimited text formats like CSV easily, although they may give you a warning during the file export.</p>

###### To save a file you have opened in Excel in CSV format:</p>

<ol>
  <li>From the top menu select ‘File’ and ‘Save as’.</li>
  <li>In the ‘Format’ field, from the list, select ‘Comma Separated Values’ (<code class="highlighter-rouge">*.csv</code>).</li>
  <li>Double check the file name and the location where you want to save it and hit ‘Save’.</li>
</ol>

###### *An important note for backwards compatibility: you can open CSV files in Excel!*

<p><img src="/Images/excel-to-csv.png" alt="Saving an Excel file to CSV" /></p>

## A Note on Cross-platform Operability

###### By default, most coding and statistical environments expect UNIX-style line endings (<code class="highlighter-rouge">\n</code>) as representing line breaks.  However, Windows uses an alternate line ending signifier (<code class="highlighter-rouge">\r\n</code>) by default for legacy compatibility with Teletype-based systems.</p>

###### As such, when exporting to CSV using Excel, your data in text format will look like this:</p>

<blockquote>
  <p>data1,data2\r\n1,2\r\n4,5\r\n</p>
</blockquote>

###### When opening your CSV file in Excel again, it will parse it as follows:</p>

<p><img width="307" alt="screen shot 2017-03-31 at 7 15 07 pm" src="https://cloud.githubusercontent.com/assets/13110354/24560663/db4a5786-1643-11e7-931a-ca2c72336878.png" /></p>

###### However, if you open your CSV file on a different system that does not parse the “\r” it will interpret your CSV file differently:</p>

###### Your data in text format then look like this:</p>

<blockquote>
  <p>data1 <br />
data2\r<br />
1<br />
2\r<br />
…</p>
</blockquote>

###### This will then in turn parse as:</p>

<p><img width="308" alt="screen shot 2017-03-31 at 7 26 42 pm" src="https://cloud.githubusercontent.com/assets/13110354/24561066/a990327c-1645-11e7-90b5-35a44e90f8d9.png" /></p>

###### thus causing terrible things to happen to your data.  For example, <code class="highlighter-rouge">2\r</code> is not a valid integer, and thus will throw an error (if you’re lucky) when you attempt to operate on it in R or Python.  Note that this happens on Excel for OSX as well as Windows, due to legacy Windows compatibility.</p>

###### There are a handful of solutions for enforcing uniform UNIX-style line endings on your exported CSV files:</p>

<ol>
  <li>When exporting from Excel, save as a “Windows comma separated (.csv)” file</li>
  <li>If you store your data file under version control using Git, edit the <code class="highlighter-rouge">.git/config</code> file in your repository to automatically translate <code class="highlighter-rouge">\r\n</code> line endings into <code class="highlighter-rouge">\n</code>.
Add the following to the file (<a href="http://nicercode.github.io/blog/2013-04-30-excel-and-line-endings">see the detailed tutorial</a>):</p>

    <div class="highlighter-rouge"><div class="highlight"><pre class="highlight"><code> [filter "cr"]
 		clean = LC_CTYPE=C awk '{printf(\"%s\\n\", $0)}' | LC_CTYPE=C tr '\\r' '\\n'
 		smudge = tr '\\n' '\\r'` 
</code></pre></div>    </div>
  </li>
</ol>

 	and then create a file <code class="highlighter-rouge">.gitattributes</code> that contains the line:

 		*.csv filter=cr

<ol>
  <li>Use <a href="http://dos2unix.sourceforge.net/">dos2unix</a> (available on OSX, *nix, and Cygwin) on local files to standardize line endings.</li>
</ol>

<h4 id="a-note-on-r-and-xlsx">A note on R and <code class="highlighter-rouge">.xlsx</code></h4>

<p>There are R packages that can read <code class="highlighter-rouge">.xls or .xlsx</code> files (as well as
Google spreadsheets). It is even possible to access different
worksheets in the <code class="highlighter-rouge">.xlsx</code> documents.</p>

<p><strong>But</strong></p>

<ul>
  <li>some of these only work on Windows</li>
  <li>this equates to replacing a (simple but manual) export to <code class="highlighter-rouge">csv</code> with
additional complexity/dependencies in the data analysis R code</li>
  <li>data formatting best practice still apply</li>
  <li>Is there really a good reason why <code class="highlighter-rouge">csv</code> (or similar) is not adequate?</li>
</ul>

<h4 id="caveats-on-commas">Caveats on commas</h4>

<p>In some datasets, the data values themselves may include commas (,). In that case, the software which you use (including Excel)
will most likely incorrectly display the data in columns. This is because the commas which are a part of the data values will be
interpreted as delimiters.</p>

<p>If you are working with data that contains commas, you likely will need to use another delimiter when working in a spreadsheet. In this
case, consider using tabs as your delimiter and working with TSV files. TSV files can be exported from spreadsheet
programs in the same way as CSV files. For more of a discussion on data formats and potential issues with commas within datasets see <a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/discuss/">the discussion page</a>.</p>


<blockquote class="keypoints">
  <h2>Key Points</h2>
  <ul>
    
    <li><p>Data stored in common spreadsheet formats will often not be read correctly into data analysis software, introducing errors into your data.</p>
</li>
    
    <li><p>Exporting data from spreadsheets to formats like CSV or TSV puts it in a format that can be used consistently by most programs.</p>
</li>
    
  </ul>
</blockquote>

</article>




## Key Points
- Never modify your raw data. Always make a copy before making any changes.
- Keep track of all of the steps you take to clean your data in a plain text file.
- Organize your data according to tidy data principles.

| <a href="../00-intro/index.html"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="../02-common-mistakes/index.html"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | 
  | ---- | ----|    
  
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
	
