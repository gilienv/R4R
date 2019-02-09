
<img src = /Images/R4R_header.png>
## Data Organization in Spreadsheets: Introduction
 
 
### Overview 
|----- | -----| 
| *Teaching: * | 15 min | 
 | *Exercises: * | 3 min |
|* Questions* | What are basic principles for using spreadsheets for good data organization? | 
| *Objectives* | Describe best practices for organizing data so computers can make the best use of data sets |
-----

<p>Authors:<strong>Gita Yadav</strong>, <strong>Ashley Sawle</strong><br /></p>

<p>Good data organization is the foundation of your research
project. Most researchers have data or do data entry in
spreadsheets. Spreadsheet programs are very useful graphical
interfaces for designing data tables and handling very basic data
quality control functions.</p>

<h3 id="spreadsheet-outline">Spreadsheet outline</h3>

<p>After this lesson, you will be able to:</p>
<ul>
  <li>Implement best practices in data table formatting</li>
  <li>Identify and address common formatting mistakes</li>
  <li>Understand approaches for handling dates in spreadsheets</li>
  <li>Utilize basic quality control features and data manipulation practices</li>
  <li>Effectively export data from spreadsheet programs</li>
</ul>

<p><em>Overall good data practices</em></p>

<p>Spreadsheets are good for data entry. Therefore we have a lot of data
in spreadsheets. 
Much of your time as a researcher will be spent in this ‘data wrangling’ stage.
It’s not the most fun, but it’s necessary. We’ll teach you how to think
about data organization and some practices for more effective data wrangling.</p>

<h3 id="what-this-lesson-will-not-teach-you">What this lesson will not teach you</h3>

<ul>
  <li>How to do <em>statistics</em> in a spreadsheet</li>
  <li>How to do <em>plotting</em> in a spreadsheet</li>
  <li>How to <em>write code</em> in spreadsheet programs</li>
</ul>

<p>If you’re looking to do this, a good reference is
<a href="https://www.amazon.com/Head-First-Excel-learners-spreadsheets/dp/0596807694/">Head First Excel</a>, published by O’Reilly</p>

<hr />

<h3 id="why-arent-we-teaching-data-analysis-in-spreadsheets">Why aren’t we teaching data analysis in spreadsheets</h3>

<ul>
  <li>
    <p>Data analysis in spreadsheets usually requires a lot of manual
work. If you want to change a parameter or run an analysis with a
new dataset, you usually have to redo everything by hand. (We do
know that you can create macros, but see the next point.)</p>
  </li>
  <li>
    <p>It is also difficult to track or reproduce statistical or plotting
analyses done in spreadsheet programs when you want to go back to
your work or someone asks for details of your analysis.</p>
  </li>
</ul>

<h3 id="spreadsheet-programs">Spreadsheet programs</h3>

<p>Many spreadsheet programs are available. Since most participants utilize Excel as their primary spreadsheet program, this lesson will make use of Excel examples.</p>

<p>A free spreadsheet program that can also be used is LibreOffice</p>

<p>Commands may differ a bit between programs, but the general idea
is the same.</p>

<blockquote class="callout">
  <h2 id="exercise">Exercise</h2>
  <ul>
    <li>How many people have used spreadsheets in their research?</li>
    <li>How many people have accidentally done something that made them
frustrated or sad?</li>
  </ul>
</blockquote>

<p>Spreadsheets encompass a lot of the things we need
to be able to do as researchers. We can use them for:</p>

<ul>
  <li>Data entry</li>
  <li>Organizing data</li>
  <li>Subsetting and sorting data</li>
  <li>Statistics</li>
  <li>Plotting</li>
</ul>

<p>We do a lot of different operations in spreadsheets. What kind of operations do you do in spreadsheets? Which ones do you think spreadsheets are good for?</p>

<h2 id="problems-with-spreadsheets">Problems with Spreadsheets</h2>

<p>Spreadsheets are good for data entry, but in reality we tend to
use spreadsheet programs for much more than data entry. We use them
to create data tables for publications, to generate summary
statistics, and make figures.</p>

<p>Generating tables for publications in a spreadsheet is not
optimal - often, when formatting a data table for publication, we’re
reporting key summary statistics in a way that is not really meant to
be read as data, and often involves special formatting
(merging cells, creating borders, making it pretty). We advise you to
do this sort of operation within your document editing software.</p>

<p>The latter two applications, generating statistics and figures, should 
be used with caution: because of the graphical, drag and drop nature of 
spreadsheet programs, it can be very difficult, if not impossible, to 
replicate your steps (much less retrace anyone else’s), particularly if your 
stats or figures require you to do more complex calculations. Furthermore, 
in doing calculations in a spreadsheet, it’s easy to accidentally apply a 
slightly different formula to multiple adjacent cells. When using a 
command-line based statistics program like R or SAS, it’s practically 
impossible to apply a calculation to one observation in your 
dataset but not another unless you’re doing it on purpose.</p>

<h3 id="using-spreadsheets-for-data-entry-and-cleaning">Using Spreadsheets for Data Entry and Cleaning</h3>

<p>However, there are circumstances where you might want to use a spreadsheet 
program to produce “quick and dirty” calculations or figures, and data 
cleaning will help you use some of these features. Data cleaning also
puts your data in a better format prior to importation into a 
statistical analysis program. We will show you how to use some features of 
spreadsheet programs to check your data quality along the way and produce 
preliminary summary statistics.</p>

<p>In this lesson, we will assume that you are most likely using Excel as
your primary spreadsheet program - there are others (gnumeric, Calc
from OpenOffice), and their functionality is similar, but Excel seems
to be the program most used by biologists and ecologists.</p>

<p>In this lesson we’re going to talk about:</p>

<ol>
  <li><a href="../01-format-data/">Formatting data tables in spreadsheets</a></li>
  <li><a href="../02-common-mistakes/">Formatting problems</a></li>
  <li><a href="../03-dates-as-data/">Dates as data</a></li>
  <li><a href="../04-quality-control/">Quality control</a></li>
  <li><a href="../05-exporting-data/">Exporting data</a></li>
</ol>



<blockquote class="keypoints">
  <h2>Key Points</h2>
  <ul>
    
    <li><p>Good data organization is the foundation of any research project.</p>
</li>
    
  </ul>
</blockquote>

</article>
















<div class="row">
  <div class="col-xs-1">
    <h3 class="text-left">
      
      <a href="../"><span class="glyphicon glyphicon-menu-up" aria-hidden="true"></span><span class="sr-only">lesson home</span></a>
      
    </h3>
  </div>
  <div class="col-xs-10">
    
  </div>
  <div class="col-xs-1">
    <h3 class="text-right">
      
      <a href="../01-format-data/index.html"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">next episode</span></a>
      
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
	
	<a href="https://github.com/datacarpentry/spreadsheet-ecology-lesson/edit/gh-pages/_episodes/00-intro.md">Edit on GitHub</a>
	
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
