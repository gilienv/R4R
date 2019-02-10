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


---

| <a href="/Documents/Day02_Dates.md"><span class="glyphicon glyphicon-menu-left" aria-hidden="true"></span><span class="sr-only">Back To Lesson</span></a> | <a href="/Documents/Day03.md"><span class="glyphicon glyphicon-menu-right" aria-hidden="true"></span><span class="sr-only">Go To Next Lesson</span></a>  
  | ---- | ----|
  
---
Licensed under <a href="">CC-BY 4.0</a> 2018–2019 by <a href="https://carpentries.org/">The Carpentries</a>
        <br>
Licensed under <a href="">CC-BY 4.0</a> 2016–2018 by <a href="http://datacarpentry.org">Data Carpentry</a>
	
