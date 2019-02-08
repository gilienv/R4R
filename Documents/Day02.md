
## General Information

<p>
  <a href="http://datacarpentry.org">Data Carpentry</a>
  workshops are for any researcher who has data they want to analyze, 
  and no prior computational experience is required. 
  This hands-on workshop teaches basic concepts, 
  skills and tools for working more effectively with data.
  We will cover Data organization in spreadsheets, 
  data cleaning with OpenRefine, 
  and learn how to use the statistical program R.
  If time allows we will also talk about Interacting with databases from R. 
  Participants will be encouraged to help one another
  and to apply what they have learned to their own research problems.
</p>
<p align="center">
  <em>
    For more information on what we teach and why,
    please see our paper
    "<a href="http://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.1001745">Best Practices for Scientific Computing</a>".
  </em>
</p>

<p id="who">
  <strong>Who:</strong>
  The course is aimed at graduate students and other researchers.
  <strong>
    You don't need to have any previous knowledge of the tools
    that will be presented at the workshop.
  </strong>
</p>

<p id="where">
  <strong>Where:</strong>
  E-Learning3, Level 2, School of Clinical Medicine, Cambridge Biomedical Campus, Cambridge CB2 0SP.
  Get directions with
  <a href="//www.openstreetmap.org/?mlat=52.186900&amp;mlon=0.137400&amp;zoom=16">OpenStreetMap</a>
  or
  <a href="//maps.google.com/maps?q=52.186900,0.137400">Google Maps</a>.
</p>

<p id="when">
  <strong>When:</strong>
  Jan 15-16, 2019.
  <a href="//calendar.google.com/calendar/render?action=TEMPLATE&amp;text=Data Carpentry Workshop&amp;dates=20190115/20190116&amp;trp=false&amp;sprop&amp;sprop=name:&amp;sf=true&amp;output=xml&amp;location=E-Learning3, Level 2, School of Clinical Medicine, Cambridge Biomedical Campus, Cambridge CB2 0SP&amp;details=Data Carpentry Workshop at School of Clinical Medicine">Add to your Google Calendar.</a>

</p>

<p id="requirements">
  <strong>Requirements:</strong> 
  We will be using pre-configured computers in the Schools E-Learning Suite.
 Participants can bring their own laptop with a
  Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) 
  that they have administrative privileges
  on. They should have a few specific software packages installed (listed
  <a href="#setup">below</a>) or by using Docker and relevant containers <a href="Installing_Dockerised_learning_environment.pdf">see here</a>.
This can also be done after the course to re-engage with the materials.
	
They are also required to abide by
  
  Data Carpentry's
  
  <a href="https://software-carpentry.org/conduct.html">Code of Conduct</a>.
</p>

<p id="accessibility">
  <strong>Accessibility:</strong> We are committed to making this workshop
  accessible to everybody. 
  Please get in touch (using contact details below) if you have any special 
  requirements.
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch and we will attempt to provide them.
</p>


<p id="contact">
  <strong>Contact</strong>:
  Please email
  
    
      
        
      
      <a href="mailto:mark.fernandes@cruk.cam.ac.uk">mark.fernandes@cruk.cam.ac.uk</a>
    
  
  for more information.
</p>

<hr />





<p><em>Surveys</em></p>

  <p><b>Please be sure to complete this survey after the workshop:</b> 
  <a href="https://www.surveymonkey.co.uk/r/DataCRJan19">Cambridge training survey</a></p>

  <p>We would also appreciate if you filled in these surveys for the Data Carpentry community:</p>
  <p><a href="https://www.surveymonkey.com/r/dcpreworkshopassessment?workshop_id=2019-01-15-CRUK-Cambridge-DCinR">Data carpentry pre-workshop Survey</a></p>
  <p><a href="https://www.surveymonkey.com/r/dcpostworkshopassessment?workshop_id=2019-01-15-CRUK-Cambridge-DCinR">Data carpentry post-workshop Survey</a></p>


<hr />



<p id="collaborative_notes">
  We will use this <a href="https://pad.carpentries.org/2019-01-15-CRUK-Cambridge">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>

<h2>Course Overview</h2>
<img src="assets/img/Data_carpentry_overview_fig.png" alt="overview" width="800" />

<h2 id="schedule">Schedule</h2>
<a href="https://bioinformatics-core-shared-training.github.io/2019-01-15-CRUK-Cambridge-DCinR//timetable">Timetable</a>.  
<h3>Day 1</h3>

<h4>Data organization in spreadsheets ( )</h4>

<p>
  <h2>Data files for the lesson are available 
	  <a href="https://ndownloader.figshare.com/files/2252083">here</a>.</h2>
</p>

<ol>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/00-intro/">Introduction</a> (18 mins)</li>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/01-format-data/">Formatting data</a> (35 mins)</li>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/02-common-mistakes/">Common formatting problems</a> (20 mins)</li>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/03-dates-as-data/">Dates as data</a> (13 mins)</li>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/04-quality-control/">Quality control</a> (20 mins)</li>
  <li><a href="http://www.datacarpentry.org/spreadsheet-ecology-lesson/05-exporting-data/">Exporting data</a> (10 mins)</li>
</ol>

<h4>Data cleaning with OpenRefine ( )</h4>

<p>
  <h2>Data files for the lesson are available 
	  <a href="https://ndownloader.figshare.com/files/7823341">here</a></h2>.
</p>

<ol>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/00-getting-started/">Introduction</a> (10 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/01-working-with-openrefine/">Basics of OpenRefine</a> (35 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/02-filter-exclude-sort/">Filtering and sorting</a> (20 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/03-numbers/">Examining numeric data</a> (20 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/04-scripts/">Generating scripts</a> (15 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/05-save-export/">Exporting data</a> (15 mins)</li>
  <li><a href="http://www.datacarpentry.org/OpenRefine-ecology-lesson/06-resources/">Other resources</a> (10 mins)</li>  
</ol>

<h4>Data analysis with R ( )</h4>

<ol>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/00-before-we-start.html">Overview of R and Rstudio</a> ( mins)</li>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/01-intro-to-r.html">Introduction to R</a> ( mins)</li>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/02-starting-with-data.html">Working with tabular data in R</a> ( mins)</li>
</ol>

<a href="https://rawgit.com/tavareshugo/2017-09-11-cambridge/gh-pages/materials_recap/day1_recap.html">Recap of R materials from Day 1 ( mins)</a>


<h3>Day 2</h3>


<h4>Data analysis with R</h4>

<ol>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/03-dplyr.html">Data manipulation using the R package dplyr</a> ( mins)</li>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/04-visualization-ggplot2.html">Data visualisation using the R package ggplot2</a> ( mins)</li>
  <li><a href="http://www.datacarpentry.org/R-ecology-lesson/05-r-and-databases.html">Interacting with databases from R</a> ( mins)</li>
</ol>

<p>
  <h2>CSV data files for the final part of Database lesson are available from  
	  <a href="https://github.com/datacarpentry/ecology-workshop/blob/master/data.md">here</a></h2>.
</p>

Learn more about SQL from the 
<a href="http://www.datacarpentry.org/sql-ecology-lesson/00-sql-introduction/">SQL data lessons</a>.

<p><b> Should you finish earlier than others and want some more challenges please have a go.  
 at this material from the R Software Carpentry course (They could also be done    
 post-course as a revision exercise):</b>   
<a href="http://swcarpentry.github.io/r-novice-gapminder/05-data-structures-part2/index.html">Gapmider R materials</a>

<p><u>Useful reference sheets</u>
<ol>
<li><a href="https://www.rstudio.com/wp-content/uploads/2016/05/base-r.pdf">Base R cheatsheet</a></li>
<li><a href="https://www.rstudio.com/wp-content/uploads/2015/02/data-wrangling-cheatsheet.pdf">Dplyr cheatsheet</a></li>
<li><a href="https://www.rstudio.com/wp-content/uploads/2015/03/ggplot2-cheatsheet.pdf">ggplot2 cheatsheet</a></li>
<li><a href="http://datacamp-community.s3.amazonaws.com/076cc4b0-6e77-4c75-b369-e60d1434817c">Tidyverse cheatsheet</a></li>
	<li><a href="https://github.com/gadenbuie/tidyexplain">Animations of joins, spread &amp; gather</a></li>
</ol>
</p>




<hr />



<h2 id="setup">Setup</h2>

<p>
  To participate in a
  
  Data Carpentry
  
  workshop,
  you will need access to the software described below.
  In addition, you will need an up-to-date web browser.
</p>
<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href="https://github.com/swcarpentry/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>


<div id="r"> 
  <h3>R</h3>

  <p>
    <a href="http://www.r-project.org">R</a> is a programming language
    that is especially powerful for data exploration, visualization, and
    statistical analysis. To interact with R, we use
    <a href="http://www.rstudio.com/">RStudio</a>.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="r-windows">Windows</h4>
      <a href="https://www.youtube.com/watch?v=q0PjTAylwoU">Video Tutorial</a>
      <p>
        Install R by downloading and running
        <a href="http://cran.r-project.org/bin/windows/base/release.htm">this .exe file</a>
        from <a href="http://cran.r-project.org/index.html">CRAN</a>.
        Also, please install the
        <a href="http://www.rstudio.com/ide/download/desktop">RStudio IDE</a>.
        Note that if you have separate user and admin accounts, you should run the 
        installers as administrator (right-click on .exe file and select "Run as 
        administrator" instead of double-clicking). Otherwise problems may occur later, 
        for example when installing R packages.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="r-macosx">macOS</h4>
      <a href="https://www.youtube.com/watch?v=5-ly3kyxwEg">Video Tutorial</a>
      <p>
        Install R by downloading and running
        <a href="http://cran.r-project.org/bin/macosx/R-latest.pkg">this .pkg file</a>
        from <a href="http://cran.r-project.org/index.html">CRAN</a>.
        Also, please install the
        <a href="http://www.rstudio.com/ide/download/desktop">RStudio IDE</a>.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="r-linux">Linux</h4>
      <p>
        You can download the binary files for your distribution
        from <a href="http://cran.r-project.org/index.html">CRAN</a>. Or
        you can use your package manager (e.g. for Debian/Ubuntu
        run <code>sudo apt-get install r-base</code> and for Fedora run
        <code>sudo dnf install R</code>).  Also, please install the
        <a href="http://www.rstudio.com/ide/download/desktop">RStudio IDE</a>.
      </p>
    </div>
  </div>
</div> 


<div id="openrefine"> 
  <h3>OpenRefine</h3>
  <p>
    For this lesson you will need <em>OpenRefine</em> and a
    web browser. <em>Note:</em> this is a Java program that runs on your machine (not in the cloud).
    It runs inside a web browser, but no web connection is needed.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="openrefine-windows">Windows</h4>
      <p>
        Check that you have either the Firefox or the Chrome browser installed and set as your default browser.
        <strong>OpenRefine runs in your default browser.</strong>
        It will not run correctly in Internet Explorer.
      </p>
      <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a></p>
      <p>Create a new directory called OpenRefine.</p>
      <p>Unzip the downloaded file into the OpenRefine directory by right-clicking and selecting "Extract ...". </p>
      <p>Go to your newly created OpenRefine directory.</p>
      <p>Launch OpenRefine by clicking <code>google-refine.exe</code> (this will launch a command prompt window, but you can ignore that - just wait for OpenRefine to open in the browser).</p>
      <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
    </div>
    <div class="col-md-4">
      <h4 id="openrefine-mac">Mac</h4>
      <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong> It may not run correctly in Safari.</p>
      <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
      <p>Create a new directory called OpenRefine.</p>
      <p>Unzip the downloaded file into the OpenRefine directory by double-clicking it.</p>
      <p>Go to your newly created OpenRefine directory.</p>
      <p>Launch OpenRefine by dragging the icon into the Applications folder.</p>
      <p>Use <code>Ctrl-click/Open ... </code> to launch it.</p>
      <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
    </div>
    <div class="col-md-4">
      <h4 id="openrefine-linux">Linux</h4>
      <p>Check that you have either the Firefox or the Chrome browser installed and set as your default browser. <strong>OpenRefine runs in your default browser.</strong></p>
      <p>Download software from <a href="http://openrefine.org/">http://openrefine.org/</a>.</p>
      <p>Make a directory called OpenRefine.</p>
      <p>Unzip the downloaded file into the OpenRefine directory.</p>
      <p>Go to your newly created OpenRefine directory.</p>
      <p>Launch OpenRefine by entering <code>./refine</code> into the terminal within the OpenRefine directory.</p>
      <p>If you are using a different browser, or if OpenRefine does not automatically open for you, point your browser at <a href="http://127.0.0.1:3333/">http://127.0.0.1:3333/</a> or <a href="http://localhost:3333">http://localhost:3333</a> to use the program.</p>
    </div>
  </div>
</div> 




<div id="sql"> 
  <h3>SQLite</h3>

  <p>
    SQL is a specialized programming language used with databases.  We
    use a simple database manager called
    <a href="http://www.sqlite.org/">SQLite</a> in our lessons.
  </p>

  <div class="row">
    <div class="col-md-4">
      <h4 id="sql-windows">Windows</h4>
      <p>
        The <a href="https://github.com/swcarpentry/windows-installer/releases/download/v0.3/SWCarpentryInstaller.exe">
          
          Data Carpentry
          
          Windows Installer
	</a>
        installs SQLite for Windows.
        If you used the installer to configure nano, you don't need to run it again.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="sql-macosx">macOS</h4>
      <p>
        SQLite comes pre-installed on macOS.
      </p>
    </div>
    <div class="col-md-4">
      <h4 id="sql-linux">Linux</h4>
      <p>
        SQLite comes pre-installed on Linux.
      </p>
    </div>
  </div>

  <p><strong>If you installed Anaconda, it also has a copy of SQLite
    <a href="https://github.com/ContinuumIO/anaconda-issues/issues/307">without support to <code>readline</code></a>.
    Instructors will provide a workaround for it if needed.</strong></p>
</div> 

</p></p>

      
<footer>
  <div class="row">
    <div class="col-md-6" align="left">
      <h4>
	Copyright &copy; 2016
	
	<a href="https://software-carpentry.org">Software Carpentry Foundation</a>
	
      </h4>
    </div>
    <div class="col-md-6" align="right">
      <h4>
	<a href="mailto:lessons@software-carpentry.org">Contact</a>
      </h4>
    </div>
  </div>
</footer>

    </div>
    
<script src="./assets/js/jquery.min.js"></script>
<script src="./assets/js/bootstrap.min.js"></script>
<script src="./assets/js/lesson.js"></script>
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
