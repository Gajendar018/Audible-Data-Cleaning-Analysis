
That's a great idea! Presenting your Audible data cleaning and analysis project on GitHub will clearly showcase your data skills.

Based on the case study presentation, here is a detailed description covering the project's introduction, objectives, process, and key cleaning steps, optimized for a GitHub README.

🎧 Audible Data Cleaning & Analysis Project
This project focuses on performing data cleaning and standardization on an Audible dataset using Microsoft Excel's Power Query Editor to prepare it for meaningful business analysis.

The goal was to transform raw, inconsistent data into a structured, clean, and accurate format, ensuring all fields are correctly typed and uniformly presented for reliable insights. 

🎯 Project Objectives
Prepare raw Audible dataset for insightful analysis using Excel tools. 

Standardize inconsistent data formats across multiple columns (Name, Author, Date, Time, Price, Stars). 

Convert text-based values (ratings, time) into appropriate numeric and duration formats. 

Split complex, multi-value fields (multiple authors, narrators) into separate columns for clarity. 

Create new, combined fields to enhance data readability and usability. 

🛠️ Tools Used

Microsoft Excel: Power Query, Pivot Tables, Formulas, Charts. 

⚙️ Data Cleaning & Transformation Steps
The data cleaning process involved several critical steps in Power Query to ensure data quality and consistency: | Column | Task | Power Query Steps | Result | | :--- | :--- | :--- | :--- | | name | Standardize titles. | Transform > Format > Capitalize Each Word.  | Consistent Title Case for all book names.  | | author | Separate multiple authors. | Split Column By Delimiter (using uppercase to lowercase transition or other delimiters).  | Each author separated into individual columns (author.1, author.2, etc.).  | | releasedate | Enforce consistent date format. | Change Type with Locale to Date with locale English (India) to enforce DD-MM-YYYY.  | All dates uniformly formatted (DD-MM-YYYY).  | | time | Convert text duration to a recognized Duration format. | 1. Replace Value to remove non-numeric text (hr, min, sec).  2. Add Custom Column for value rearrangement.  3. Split Custom Column and divide into 24-hour format.  4. Convert final column to Duration data type.  | Usable Duration format for analysis (e.g., average time).  | | price | Convert to numeric, handle errors. | 1. Change data type to Decimal Number.  2. Replace Errors with 0 (or another appropriate handling method).  3. Re-format column type to Currency and round to 2 Decimal Places.  | Consistent Currency format with two decimal places.  | | stars | Extract numeric rating from text. | 1. Split Column by Delimiter (Space) to isolate the numeric rating.  2. Remove extra text columns (e.g., "out of 5 stars").  3. Change column data type to Decimal Number.  | Clean numeric rating values (e.g., 4.5, 5).  | | narrated by | Separate multiple narrators. | Split Column By Delimiter (Comma) in Power Query.  | Each narrator separated into new columns (narrator.1, narrator.2, etc.).  |

✨ New Field Creation
A new field, Released Info, was created to combine the release date and language columns for easier data consumption. 


Formula Logic: Concatenated the formatted releasedate (DD-MM-YYYY) and the language column. 


Final Format Example: DD-MM-YYYY English (e.g., 04-08-2008 English). 

✅ Conclusion
The dataset is now structured, consistent, and ready for further business analysis, ensuring reliable insights and supporting data-driven decision-making. 
