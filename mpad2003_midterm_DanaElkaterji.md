**October 19 2024**<br>
**MPAD2003 Introductory Data Storytelling**<br>
**Dana El-katerji**<br>
**Presented to Jean-Sébastien Marier**<br>

# Midterm Project: Exploratory Data Analysis (EDA)

Use one hashtag symbol (`#`) to create a level 1 heading like this one.

## Foreword

For this assignment, you must extract data from a dataset provided by the instructor. You must then clean and analyze the data, create exploratory charts/visualizations, and find a potential story idea. Your assignment must clearly detail your process. You are expected to write about 1500-2000 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub Classroom.

I have been assigning different versions of this project to my digital journalism and data storytelling students for a few years now. Its structure was inspired by the main sections/chapters of [*The Data Journalism Handbook*](https://datajournalism.com/read/handbook/one/). This version was further inspired by the [Key Capabilities in Data Science](https://extendedlearning.ubc.ca/programs/key-capabilities-data-science) program offered by the University of British Columbia (UBC).

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Introduction

In this assignment, I will analyze a dataset from the City of Ottawa concerning Garbage and Recycling issues. This data has been collected through various channels, including counters, data submissions, dispatches, emails, voice calls, walk-ins, and web submissions. It contains essential information such as the type of complaint, reasons for filing, and the opening and closing dates of each case, along with the addresses where the issues were reported. By examining this dataset, we can gain valuable insights into the community's concerns regarding water and environmental matters. Scott Berinato’s framework for data storytelling will guide this analysis, focusing on the date and type of complaints to identify potential resolutions (“Telling Stories with Data in 3 Steps (Quick Study)”). The original dataset can be accessed on Open Ottawa, and the CSV version is available on my GitHub portal. The main sections of this assignment will include data acquisition, data cleaning, and analysis.


[Original Dataset on the City of Ottawa's website](https://open.ottawa.ca/documents/65fe42e2502d442b8a774fd3d954cac5/about)

[Link to RAW data on GitHub] //fix it 
[Link to Google Sheets Dataset](https://docs.google.com/spreadsheets/d/1DqOkj_1srIewF3xUey7auqMXSc99X9v5726dv3Mzogo/edit?gid=533431493)


## 2. Getting Data

Use two hashtag symbols (`##`) to create a level 2 heading like this one.

## Steps on how to import data into Google Sheets:
   <b> 1. Download the dataset:</b> Visit the City of Ottawa's open data portal and download the dataset in CSV format onto your computer.

   <b>2. Open Google Sheets: </b> Go to Google Sheet and click on "Blank Spreadsheet" to create a new spreadsheet.

   <b>3. Import the dataset:</b>
   <ul>
   <ol> + Click on  <b>File > Import.</b> </ol>
   <ol> + Then click on <b> Browse</b> and select the City of Ottawa CSV file that you downloaded earlier. </ol>
   <ol> + Choose the <b>“Comma” </b>as your separate type. </ol>
</ul>

To include a screen capture, use the sample code below. Your images should be saved in the same folder as your `.md` file.

![](import-screen-capture.png)<br>
*Figure 1: The "Import file" prompt on Google Sheets.*

![](midtermPicOfTheData.png) 
*Figure 2: The Screenshot of the data" from Dana's computer.*


A public link to your Google Sheets spreadsheet:

[Link to Google Sheets Dataset](https://docs.google.com/spreadsheets/d/1DqOkj_1srIewF3xUey7auqMXSc99X9v5726dv3Mzogo/edit?usp=sharing)


<b>General Observations Regarding the Dataset</b><br>

In this dataset, there are <b> 11 columns and 261,200 rows. </b> Upon initial inspection, I noticed several instances of <b>/N, </b>suggesting potential missing information in some cells. However, overall, the data appears to be <b>clean.</b> The columns are properly labeled, and the majority of the cells contain relevant information corresponding to their respective columns.

I observed that<b> "Garbage and Recycling" </b>is the most frequently repeated service type, while <b>"Licenses and Permits"</b> has the least occurrences.

<b>Specific Observations Regarding the Dataset</b><br>

The dataset includes various types of information:
<ul>
<ol><b>Column C:</b> Service Type This column contains categories such as <b>Water and Environment,</b> which are <b>nominal variables (“Statistics: Power from Data!”). </b>These values are qualitative, representing distinct service types that cannot be ordered or ranked.
  </ol>
<ol><b>Column B:</b> Status of the Request This column indicates whether the request is <b>open, closed, or in progress,</b> also classified as <b>nominal variables (“Statistics: Power from Data!”).</b> These are qualitative values representing the current state of each request without any ranking.</ol>

<ol><b>Column E & F:</b> Opening and Closing Dates These columns show when the request was submitted and when it was closed, representing <b>interval-level</b> variables (“Statistics: Power from Data!”). Dates can be ordered chronologically, and they are arbunary points, which makes them interval data. <br>
</ol>
  </ul>


<b>Something missing in the dataset</b><br>

In<b> Column F, Row 7,</b> the Closed Date is missing (represented as '/N') for a Garbage and Recycling request that was opened on <b>2024-07-05.</b> This is surprising because most of the garbage and recycling requests in the dataset have been resolved within a few days or weeks. <br>

<b>A question or hypothesis that comes in mind when looking at the raw data</b>

When looking at the raw data, there are many instances of '/N,' My question is: Why do most resolved cases not have a closing date? 





**Here are examples of functions and lines of code put in grey boxes:**

1. If you name a function, put it between "angled" quotation marks like this: `IMPORTHTML`.
1. If you want to include the entire line of code, do the same thing, albeit with your entire code: `=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)`.
1. Alternatively, you can put your code in an independent box using the template below:

``` r
=IMPORTHTML("https://en.wikipedia.org/wiki/China"; "table", 5)
```
This also shows how to create an ordered list. Simply put `1.` before each item.

## 3. Understanding Data

### 3.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

Insert text here.

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As Cairo (2016) argues, a data visualization should be truthful...

### 3.2. Cleaning Data

Insert text here.

### 3.3. Exploratory Data Analysis (EDA)

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 4. Potential Story

Insert text here.

## 5. Conclusion

Insert text here.

## 6. References

Include a list of your references here. Please follow [APA guidelines for references](https://apastyle.apa.org/style-grammar-guidelines/references). Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
