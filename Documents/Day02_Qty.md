<img src = /Images/R4R_header.png>

## Quality control
 
 | Overview | Description |
| --- | --- |
| Teaching | 20 minutes |
| Exercises | 0 minutes | 
| Question| How can we carry out basic quality control and quality assurance in spreadsheets? |
| Objective | Apply quality control techniques to identify errors in spreadsheets and limit incorrect data entry|
| Authors | [Gitanjali Yadav](http://www.nipgr.res.in/research/dr_gyadav.php) and [Ashley Sawle](https://www.cruk.cam.ac.uk/author/ashley-sawle) | 

###### Good data organization is the foundation of your research project. Most researchers have data or do data entry in spreadsheets. Spreadsheet programs are very useful graphical interfaces for designing data tables and handling very basic data quality control functions. 


###### When you have a well-structured data table, you can use several simple techniques within your spreadsheet to ensure the data you enter is free of errors. These approaches include techniques that are implemented prior to entering data (quality assurance) and techniques that are used after entering data to check for errors (quality control)

## Quality Assurance

###### Quality assurance stops bad data from ever being entered by checking to see if values are valid during data entry. For example, if research is being conducted at sites A, B, and C, then the value V (which is right next to B on the keyboard) should never be entered. Likewise if one of the kinds of data being collected is a count, only integers greater than or equal to zero should be allowed.</p>

###### To control the kind of data entered into a a spreadsheet we use Data Validation (Excel) or Validity (Libre Office Calc), to set the values that can be entered in each data column.</p>
1. Select the cells or column you want to validate
2. On the <code class="highlighter-rouge">Data</code> tab select <code class="highlighter-rouge">Data Validation</code></p>
<img src="/Images/data_validation.png" alt="Image of Data Validation button on Data tab" />
3. In the <code class="highlighter-rouge">Allow</code> box select the kind of data that should be in the
   column. Options include whole numbers, decimals, lists of items, dates, and
   other values.</p>
<img src="/Images/data_validation_window.png" alt="Image of Data Validation window" />
4. After selecting an item enter any additional details. For example, if you’ve
   chosen a list of values, enter a comma-delimited list of allowable
   values in the <code class="highlighter-rouge">Source</code> box.</p>


###### Let’s try this out by setting the plot column in our spreadsheet to only allow plot values that are integers between 1 and 24.</p>

<ol>
  <li>Select the <code class="highlighter-rouge">plot_id</code> column</li>
  <li>On the <code class="highlighter-rouge">Data</code> tab select <code class="highlighter-rouge">Data Validation</code></li>
  <li>In the <code class="highlighter-rouge">Allow</code> box select <code class="highlighter-rouge">Whole number</code></li>
  <li>Set the minimum and maximum values to 1 and 24.</li>
</ol>

<img src="/Images/plot_validation.png" alt="Image of Data Validation window for validating plot values" />

###### Now let’s try entering a new value in the plot column that isn’t a valid plot. The spreadsheet stops us from entering the wrong value and asks us if we would like to try again.

<p><img src="/Images/invalid_value.png" alt="Image of error when trying to enter invalid data" /></p>

###### You can also customize the resulting message to be more informative by entering your own message in the <code class="highlighter-rouge">Input Message</code> tab</p>
<img src="/Images/input_message.png" alt="Image of Input Message tab" /></p>

###### or allow invalid data to result in a warning rather than an error by modifying the <code class="highlighter rouge">Style</code> option on the <code class="highlighter-rouge">Error Alert</code> tab.</p>
<img src="/Images/error_alert.png" alt="Image of Error Alert tab" /></p>

###### Quality assurance can make data entry easier as well as more robust. For example, if you use a list of options to restrict data entry, the spreadsheet will provide you with a drop-downlist of the available items. So, instead of trying to remember how to spell <em>Dipodomys spectabilis</em>, you can select the right option from the list.</p>

<p><img src="/Images/drop_down_list.png" alt="Image of drop-down menu" /></p>

## Quality Control

###### Tip: *Before doing any quality control operations, save your original file with the formulas and a name indicating it is the original data. Create a separate file with appropriate naming and versioning, and ensure your data is stored as values and not as formulas. Because formulas refer to other cells, and you may be moving cells around, you may compromise the integrity of your data if you do not take this step!*

## readMe (README) files

###### As you start manipulating your data files, create a readMe document / text file to keep track of your files and document your manipulations so that they may be easily understood and replicated, either by your future self or by an independent researcher. Your readMe file should document all of the files in your data set (including documentation), describe their content and format, and lay out the organizing principles of folders and subfolders. For each of the separate files listed, it is a good idea to document the manipulations or analyses that were carried out on those data.<a href="https://data.research.cornell.edu/content/readme">Cornell University’s Research Data Management Service Group</a> provides detailed guidelines for how to write a good readMe file, along with an adaptable template.</p>

## Sorting

###### Bad values often sort to the bottom or top of the column. 
###### For example, if your data should be numeric, then alphabetical and null data will group at the ends of the sorted data. Sort your data by each field, one at a time. Scan through each column, but pay the most attention to the top and the bottom of a column. 
###### If your dataset is well-structured and does not contain formulas, sorting should never affect the integrity of your dataset

***Remember to expand your sort in order to prevent data corruption. Expanding your sort ensures that the all the data in one row move together instead of only sorting a single column in isolation. Sorting by only a single column will scramble your data - a single row will no longer represent an individual observation

## Exercise

###### We’ve combined all of the tables from the messy data into a single table in a single tab. Download this semi-cleaned data file to your computer: <a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/blob/gh-pages/data/survey_sorting_exercise.xlsx?raw=true">survey_sorting_exercise</a></p>

###### Once downloaded, sort the <code class="highlighter-rouge">Weight_grams</code> column in your spreadsheet program from <code class="highlighter-rouge">Largest to Smallest</code>.</p>
###### What do you notice?</p>

 ## Solution
 
###### Click the Sort button on the data tab in Excel. A pop-up will appear. Make sure you select <code class="highlighter-rouge">Expand the selection</code>.</p>

 <p class="output"><img src="/Images/sorting_button.png" alt="quality_control0, exercise1" /></p>

 ###### The following window will display, choose the column you want to sort as well as the sort order.</p>

<p class="output"><img src="/Images/sorting_example.png" alt="quality_control1, exercise1" /></p>

###### *Note how the odd values sort to the top and bottom of the tabular data. 
###### *The cells containing no data values sort to the bottom of the tabular data, while the cells where the letter “g” was included can be found towards the top. This is a powerful way to check your data for outliers and odd values.*

<p class="output"><img src="/Images/sorting_solution_1.png" alt="quality_control2, exercise1" /></p>

<p class="output"><img src="/Images/sorting_solution_2.png" alt="quality_control3, exercise1" /></p>

## Conditional formatting

###### Conditional formatting basically can do something like color code your values by some criteria or lowest to highest. This makes it easy to scan your data for outliers.

###### Conditional formatting should be used with caution, but it can be a great way to flag inconsistent values when entering data.</p>

## Exercise
  <ol>
    <li>In the main Excel menu bar, click <code class="highlighter-rouge">Home</code> &gt; <code class="highlighter-rouge">Conditional Formatting...</code> choose a formatting rule.</li>
    <li>Apply a <code class="highlighter-rouge">2-Color Scale</code> formatting rule with the lowest values set to orange and the highest values set to yellow.</li>
    <li>Now we can scan through and different colors will stand out. Do you notice any strange values?</li>
  </ol>

## Solution

###### Cells that contain non-numerical values are not colored. This includes both the cells where the letter “g” was included and the empty cells. 
<img src="/Images/conditional_formating.png" alt="quality_control4, exercise2" /></p>

###### It is nice to do be able to do these scans in spreadsheets, but we also can do these checks in a programming language like R, or in OpenRefine or SQL.


## Key Points
###### - Always copy your original spreadsheet file and work with a copy so you don’t affect the raw data
###### - Use data validation to prevent accidentally entering invalid data.</p>
###### - Use sorting to check for invalid data.</p>
###### - Use conditional formatting (cautiously) to check for invalid data.</p>

| <a href="../00-intro/index.html"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="../02-common-mistakes/index.html"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | 
  | ---- | ----|    
  
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
