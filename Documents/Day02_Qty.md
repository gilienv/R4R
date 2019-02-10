<img src = /Images/R4R_header.png>

## Quality control
 
 
 | Overview | Description |
| --- | --- |
| Teaching | 15 minutes |
| Exercises | 3 minutes | 
| Question| What are basic principles for using spreadsheets for good data organization? |
| Objective | Describe best practices for organizing data so computers can make the best use of data sets |
| Authors | [Gitanjali Yadav](http://www.nipgr.res.in/research/dr_gyadav.php) and [Ashley Sawle](https://www.cruk.cam.ac.uk/author/ashley-sawle) | 

* Good data organization is the foundation of your research
project. Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are very useful graphical
interfaces for designing data tables and handling very basic data
quality control functions. 




## Key Points
- Never modify your raw data. Always make a copy before making any changes.
- Keep track of all of the steps you take to clean your data in a plain text file.
- Organize your data according to tidy data principles.

| <a href="../00-intro/index.html"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="../02-common-mistakes/index.html"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | 
  | ---- | ----|    
  
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>





<article>
<div class="row">
  <div class="col-md-1">
  </div>
  <div class="col-md-10">
    <h1 class="maintitle">Quality control</h1>
  </div>
  <div class="col-md-1">
  </div>
</div>


<blockquote class="objectives">
  <h2>Overview</h2>

  <div class="row">
    <div class="col-md-3">
      <strong>Teaching:</strong> 20 min
      <br/>
      <strong>Exercises:</strong> 0 min
    </div>
    <div class="col-md-9">
      <strong>Questions</strong>
      <ul>
	
	<li><p>How can we carry out basic quality control and quality assurance in spreadsheets?</p>
</li>
	
      </ul>
    </div>
  </div>

  <div class="row">
    <div class="col-md-3">
    </div>
    <div class="col-md-9">
      <strong>Objectives</strong>
      <ul>
	
	<li><p>Apply quality control techniques to identify errors in spreadsheets and limit incorrect data entry.</p>
</li>
	
      </ul>
    </div>
  </div>

</blockquote>

<p>Authors:<strong>Christie Bahlai</strong>, <strong>Aleksandra Pawlik</strong><br /></p>

<p>When you have a well-structured data table, you can use several simple
techniques within your spreadsheet to ensure the data you enter is
free of errors. These approaches include techniques that are
implemented prior to entering data (quality assurance) and
techniques that are used after entering data to check for errors
(quality control).</p>

<h1 id="quality-assurance">Quality Assurance</h1>

<p>Quality assurance stops bad data from ever being entered by checking to see if
values are valid during data entry. For example, if research is being conducted
at sites A, B, and C, then the value V (which is right next to B on the
keyboard) should never be entered. Likewise if one of the kinds of data being
collected is a count, only integers greater than or equal to zero should be
allowed.</p>

<p>To control the kind of data entered into a a spreadsheet we use Data Validation
(Excel) or Validity (Libre Office Calc), to set the values that can be entered
in each data column.</p>

<p>1. Select the cells or column you want to validate</p>

<p>2. On the <code class="highlighter-rouge">Data</code> tab select <code class="highlighter-rouge">Data Validation</code></p>

<p><img src="../fig/data_validation.png" alt="Image of Data Validation button on Data tab" /></p>

<p>3. In the <code class="highlighter-rouge">Allow</code> box select the kind of data that should be in the
   column. Options include whole numbers, decimals, lists of items, dates, and
   other values.</p>

<p><img src="../fig/data_validation_window.png" alt="Image of Data Validation window" /></p>

<p>4. After selecting an item enter any additional details. For example, if you’ve
   chosen a list of values, enter a comma-delimited list of allowable
   values in the <code class="highlighter-rouge">Source</code> box.</p>

<p>Let’s try this out by setting the plot column in our spreadsheet to only allow
plot values that are integers between 1 and 24.</p>

<ol>
  <li>Select the <code class="highlighter-rouge">plot_id</code> column</li>
  <li>On the <code class="highlighter-rouge">Data</code> tab select <code class="highlighter-rouge">Data Validation</code></li>
  <li>In the <code class="highlighter-rouge">Allow</code> box select <code class="highlighter-rouge">Whole number</code></li>
  <li>Set the minimum and maximum values to 1 and 24.</li>
</ol>

<p><img src="../fig/plot_validation.png" alt="Image of Data Validation window for validating plot values" /></p>

<p>Now let’s try entering a new value in the plot column that isn’t a valid
plot. The spreadsheet stops us from entering the wrong value and asks us if we
would like to try again.</p>

<p><img src="../fig/invalid_value.png" alt="Image of error when trying to enter invalid data" /></p>

<p>You can also customize the resulting message to be more informative by entering
your own message in the <code class="highlighter-rouge">Input Message</code> tab</p>

<p><img src="../fig/input_message.png" alt="Image of Input Message tab" /></p>

<p>or allow invalid data to result in a warning rather than an error by modifying the <code class="highlighter-rouge">Style</code>
option on the <code class="highlighter-rouge">Error Alert</code> tab.</p>

<p><img src="../fig/error_alert.png" alt="Image of Error Alert tab" /></p>

<p>Quality assurance can make data entry easier as well as more robust. For
example, if you use a list of options to restrict data entry, the spreadsheet
will provide you with a drop-downlist of the available items. So, instead of
trying to remember how to spell <em>Dipodomys spectabilis</em>, you can select the
right option from the list.</p>

<p><img src="../fig/drop_down_list.png" alt="Image of drop-down menu" /></p>

<h1 id="quality-control">Quality Control</h1>

<p>Tip: <em>Before doing any quality control operations, save your original file with the formulas and a name indicating it is the original
data. Create a separate file with appropriate naming and versioning, and ensure your data is stored as values and not as formulas. 
Because formulas refer to other cells, and you may be moving cells around, you may compromise the integrity of your data if you do not
take this step!</em></p>

<p>readMe (README) files: As you start manipulating your data files, create a readMe document / text file to keep track of your files and
document your manipulations so that they may be easily understood and replicated, either by your future self or by an independent
researcher. Your readMe file should document all of the files in your data set (including documentation), describe their content and
format, and lay out the organizing principles of folders and subfolders. For each of the separate files listed, it is a good idea to
document the manipulations or analyses that were carried out on those data. 
<a href="https://data.research.cornell.edu/content/readme">Cornell University’s Research Data Management Service Group</a> provides detailed
guidelines for how to write a good readMe file, along with an adaptable template.</p>

<h2 id="sorting">Sorting</h2>
<p>Bad values often sort to the bottom or top of the column. For example, if your data should be numeric, then alphabetical and null data
will group at the ends of the sorted data. Sort your data by each field, one at a time. Scan through each column, but pay the most
attention to the top and the bottom of a column. 
If your dataset is well-structured and does not contain formulas, sorting should never affect the integrity of your dataset.</p>

<p><strong>Remember</strong> to expand your sort in order to prevent data corruption. Expanding your sort ensures that the all the data in one row move together instead of only sorting a single column in isolation. Sorting by only a single column will scramble your data - a single row will no longer represent an individual observation.</p>

<blockquote class="challenge">
  <h2 id="exercise">Exercise</h2>

  <p>We’ve combined all of the tables from the messy data into a single table in a single tab. Download this semi-cleaned data file to your computer: <a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/blob/gh-pages/data/survey_sorting_exercise.xlsx?raw=true">survey_sorting_exercise</a></p>

  <p>Once downloaded, sort the <code class="highlighter-rouge">Weight_grams</code> column in your spreadsheet program from <code class="highlighter-rouge">Largest to Smallest</code>.</p>

  <p>What do you notice?</p>

  <blockquote class="solution">
    <h2 id="solution">Solution</h2>

    <p>Click the Sort button on the data tab in Excel. A pop-up will appear. Make sure you select <code class="highlighter-rouge">Expand the selection</code>.</p>

    <p class="output"><img src="../fig/sorting_button.png" alt="quality_control0, exercise1" /></p>

    <p>The following window will display, choose the column you want to sort as well as the sort order.</p>

    <p class="output"><img src="../fig/sorting_example.png" alt="quality_control1, exercise1" /></p>

    <p><strong>Note</strong> how the odd values sort to the top and bottom of the tabular data. 
The cells containing no data values sort to the bottom of the tabular data, while the cells where the letter “g” was included can be found towards the top. This is a powerful way to check your data for outliers and odd values.</p>

    <p class="output"><img src="../fig/sorting_solution_1.png" alt="quality_control2, exercise1" /></p>

    <p class="output"><img src="../fig/sorting_solution_2.png" alt="quality_control3, exercise1" /></p>

  </blockquote>
</blockquote>

<h2 id="conditional-formatting">Conditional formatting</h2>
<p>Conditional formatting basically can do something like color code your values by some
criteria or lowest to highest. This makes it easy to scan your data for outliers.</p>

<p>Conditional formatting should be used with caution, but it can be a great way to flag inconsistent values when entering data.</p>

<blockquote class="challenge">
  <h2 id="exercise-1">Exercise</h2>
  <ol>
    <li>In the main Excel menu bar, click <code class="highlighter-rouge">Home</code> &gt; <code class="highlighter-rouge">Conditional Formatting...</code> choose a formatting rule.</li>
    <li>Apply a <code class="highlighter-rouge">2-Color Scale</code> formatting rule with the lowest values set to orange and the highest values set to yellow.</li>
    <li>Now we can scan through and different colors will stand out. Do you notice any strange values?</li>
  </ol>

  <blockquote class="solution">
    <h2 id="solution-1">Solution</h2>

    <p class="output">Cells that contain non-numerical values are not colored. This includes both the cells where the letter “g” was included and the empty cells. 
<img src="../fig/conditional_formating.png" alt="quality_control4, exercise2" /></p>

  </blockquote>
</blockquote>

<p>It is nice to do be able to do these scans in spreadsheets, but we also can do these
checks in a programming language like R, or in OpenRefine or SQL.</p>


<blockquote class="keypoints">
  <h2>Key Points</h2>
  <ul>
    
    <li><p>Always copy your original spreadsheet file and work with a copy so you don’t affect the raw data.</p>
</li>
    
    <li><p>Use data validation to prevent accidentally entering invalid data.</p>
</li>
    
    <li><p>Use sorting to check for invalid data.</p>
</li>
    
    <li><p>Use conditional formatting (cautiously) to check for invalid data.</p>
</li>
    
  </ul>
</blockquote>

</article>
















<div class="row">
  <div class="col-xs-1">
    <h3 class="text-left">
      
      <a href="../03-dates-as-data/index.html"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">previous episode</span></a>
      
    </h3>
  </div>
  <div class="col-xs-10">
    
  </div>
  <div class="col-xs-1">
    <h3 class="text-right">
      
      <a href="../05-exporting-data/index.html"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">next episode</span></a>
      
    </h3>
  </div>
</div>


      
      






<footer>
  <div class="row">
    <div class="col-md-6 copyright" align="left">
	
	Licensed under <a href="">CC-BY 4.0</a> 2018–2019
	by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
        Licensed under <a href="">CC-BY 4.0</a> 2016–2018
	by <a href="http://datacarpentry.org">Data Carpentry</a>
	
    </div>
    <div class="col-md-6 help-links" align="right">
	
	<a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/edit/gh-pages/_episodes/04-quality-control.md">Edit on GitHub</a>
	
	/
	<a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/blob/gh-pages/CONTRIBUTING.md">Contributing</a>
	/
	<a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/">Source</a>
	/
	<a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/blob/gh-pages/CITATION">Cite</a>
	/
	<a href="mailto:team@carpentries.org">Contact</a>
    </div>
  </div>
  <div class="row">
    <div class="col-md-12" align="center">
      Using <a href="https://github.com/carpentries/styles/">The Carpentries style</a>
      version <a href="https://github.com/carpentries/styles/releases/tag/v9.5.3">9.5.3</a>.
    </div>
  </div>
</footer>

      
    </div>
    
<script src="../assets/js/jquery.min.js"></script>
<script src="../assets/js/bootstrap.min.js"></script>
<script src="../assets/js/lesson.js"></script>
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');
  ga('create', 'UA-37305346-2', 'auto');
  ga('send', 'pageview');
</script>

  </body>
</html>
