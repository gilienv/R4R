<img src = /Images/R4R_header.png>

## Solutions to Exercise from Lesson : Dates As Data

---
### Exercise 1

#### Challenge: pulling month, day and year out of dates</p>

  * In the <code class="highlighter-rouge">dates</code> tab of your spreadsheet you have the data from 2014 plot 3. 
There’s a <code class="highlighter-rouge">Date collected</code> column.</li>
  * Let’s extract month, day and year from the dates to new columns. For this we  can use the built in Excel functions <code class="highlighter-rouge">YEAR()</code> <br><code class="highlighter-rouge">MONTH()</code>  <br />
<code class="highlighter-rouge">DAY()</code>
  * (Make sure the new column is formatted as a number and not as a date.)
  * You can see that even though you wanted the year to be 2014, your spreadsheet program automatically interpreted it as 2015, the year you entered the data.</p>
---
#### Solution
 <img src="/Images/solution_exercise_1_dates.png" alt="dates, exersize 1" />

---
### Exercise 2

#### Challenge: pulling hour, minute and second out of the current time</p>

Current time and date are best retrieved using the functions <code class="highlighter-rouge">NOW()</code>, which
returns the current date and time, and <code class="highlighter-rouge">TODAY()</code>, which returns the current
date. The results will be formatted according to your computer’s settings.</p>

1) Extract the year, month and day from the current date and time string returned by the <code class="highlighter-rouge">NOW()</code> function.
2) Calculate the current time using <code class="highlighter-rouge">NOW()-TODAY()</code>
3) Extract the hour, minute and second from the current time using functions <code class="highlighter-rouge">HOUR()</code>, <code class="highlighter-rouge">MINUTE()</code> and <code class="highlighter-rouge">SECOND()</code>.
4) Press <code class="highlighter-rouge">F9</code> to force the spreadsheet to recalculate the <code class="highlighter-rouge">NOW()</code> function, and check that it has been updated.
---
#### Solution
1) To get the year, type <code class="highlighter-rouge">=YEAR(NOW())</code> into any cell in your spreadsheet. To get the month, type <code class="highlighter-rouge">=MONTH(NOW())</code>. To get the day, type <code class="highlighter-rouge">=DAY(NOW())</code>.
2) Typing <code class="highlighter-rouge">=NOW()-TODAY()</code> will result in a decimal value that is not easily human parsable to a clock-based time. You will need to use the strategies in the third part of this challenge to convert this decimal value to readable time.
3) To extract the hour, type <code class="highlighter-rouge">=HOUR(NOW()-TODAY())</code> and similarly for minute and second
<h2 id="preferred-date-format">Preferred date format</h2>

* It is much safer to store dates with <a href="#day">YEAR, MONTH, DAY</a> in separate columns or as <a href="#doy">YEAR and DAY-OF-YEAR</a> in separate columns.</p>


<blockquote>
  <p>Note: Excel is unable to parse dates from before 1899-12-31, and will thus leave these untouched.  If you’re mixing historic data
from before and after this date, Excel will translate only the post-1900 dates into its internal format, thus resulting in mixed data.
If you’re working with historic data, be extremely careful with your dates!</p>
</blockquote>

---

### Exercise 3

* What happens to the dates in the “dates” tab of our workbook if we save this sheet in Excel (in <code class="highlighter-rouge">csv</code> format) and then open the file in a plain text editor (like TextEdit or Notepad)? 
* What happens to the dates if we then open the <code class="highlighter-rouge">csv</code> file in Excel?

---

#### Solution
- Click to the “dates” tab of the workbook and double-click on any of the values in the <code class="highlighter-rouge">Date collected</code> column. Notice that the dates display with the year 2015.
- Select <code class="highlighter-rouge">File -&gt; Save As</code> in Excel and in the drop down menu for file format select <code class="highlighter-rouge">CSV UTF-8 (Comma delimited) (.csv)</code>. Click <code class="highlighter-rouge">Save</code>
- You will see a pop-up that says “This workbook cannot be saved in the selected file format because it contains multiple sheets.” Choose <code class="highlighter-rouge">Save Active Sheet</code>.
- Navigate to the file in your finder application. Right click and select <code class="highlighter-rouge">Open With</code>. Choose a plain text editor application and view the file. Notice that the dates display as month/day without any year information.
- Now right click on the file again and open with Excel. Notice that the dates display with the current year, not 2015. <br />
- As you can see, exporting data from Excel and then importing it back into Excel fundamentally changed the data! 

<p><strong>Note</strong><br />
You will notice that when exporting into a text-based format (such as CSV), Excel will export its internal date integer instead of a useful value (that is, the dates will be represented as integer numbers). This can potentially lead to problems if you use other software to manipulate the file.</p>

<h3 id="advantages-of-alternative-date-formatting">Advantages of Alternative Date Formatting</h3>

<h3 id="-storing-dates-as-year-month-day"><a name="day"></a> Storing dates as YEAR, MONTH, DAY</h3>

<p>Storing dates in YEAR, MONTH, DAY format helps remove this ambiguity. Let’s look at this issue a bit closer.</p>

<p>For instance this is a spreadsheet representing insect counts that were taken every few days over the summer, and things went something like this:</p>

<p><img src="/Images/6_excel_dates_2.jpg" alt="So, so ambiguous, it's even confusing Excel" /></p>

<p>If Excel was to be believed, this person had been collecting bugs <strong>in the future</strong>. Now, we have no doubt this person is highly capable,
but I believe time travel was beyond even their grasp.</p>

<p>Entering dates in one cell is helpful but due to the fact that the spreadsheet programs may interpret and save the data in different ways
(doing that somewhat behind the scenes), there is a better practice.</p>

<p>In dealing with dates in spreadsheets, separate date data into separate fields (day, month, year), which will eliminate any chance of
ambiguity.</p>

<h3 id="-storing-dates-as-year-day-of-year"><a name="doy"></a> Storing dates as YEAR, DAY-OF-YEAR</h3>

<p>There is also another option. You can also store dates as year and day of year (DOY). Why? Because depending on your
question, this might be what’s useful to you, and there is practically no possibility for ambiguity creeping in.</p>

<p>Statistical models often incorporate year as a factor, or a categorical variable, rather than a numeric variable, to account for 
year-to-year variation, and DOY can be used to measure the passage of time within a year.</p>

<p>So, can you convert all your dates into DOY format? Well, in Excel, here’s a useful guide:</p>

<p><img src="/Images/7_excel_dates_3.jpg" alt="Kill that ambiguity before it bites you!" /></p>

<h3 id="-storing-dates-as-a-single-string"><a name="str"></a> Storing dates as a single string</h3>

<p>Another alternative could be to convert the date string
into a single string using the <code class="highlighter-rouge">YYYYMMDDhhmmss</code> format.
For example the date <code class="highlighter-rouge">March 24, 2015 17:25:35</code> would
become <code class="highlighter-rouge">20150324172535</code>, where:</p>

<p>YYYY:   the full year, i.e. 2015<br />
MM:     the month, i.e. 03<br />
DD:     the day of month, i.e. 24<br />
hh:     hour of day, i.e. 17<br />
mm:     minutes, i.e. 25<br />
ss:     seconds, i.e. 35</p>

<p>Such strings will be correctly sorted in ascending or descending order, and by
knowing the format they can then be correctly processed by the receiving
software.</p>


---

| <a href="/Documents/Day02_Problems.md"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Previous Lesson</span></a> | <a href="/Documents/Day03.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a> | <a href="/Documents/Day02_Sol2.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Solutions To Exercises</span></a> 
  | ---- | ----|---- | 
  
---
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
	