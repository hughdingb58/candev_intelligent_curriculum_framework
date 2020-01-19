# Application summary

This application allows the user to search through and analyze the data (a list of courses offered by the school) by various metrics. It heavily utilizes the LDA model when attempting to determine topics from descriptions.

The application is written in R Shiny.

## todo / features
A) General data filtering - Done 
1. Convert data to UTF-8.
2. Clean the timestamps for the durations.
3. Allow for filtering the data by metrics such as course type, duration, and so on.

B) Listing interdependencies
4. For each value in the translations sheet, create a list of all terms that it should also tag.

C) Data analyzing through the LDA model
5. Gather a list of all course names as the domain for the LDA model.
6. Create an algorithm implementing the LDA model on a character vector of the descriptions.
7. Run the LDA model on the character vector of the descriptions, with all translations appended with a lower weighting.
8. Search for course names that have a high value in the LDA model for *other* courses.

D) Finding good course groupings for a curriculum
9. Find the terms that it should be tagged by.
10. Create the minimum list of courses that covers all terms that have been tagged (from the filtered data). (First use the course that covers the most tags, then the course that covers the most remaining tags, and so on.)
11. Check for prerequisites. 

E) Create a search function
12. Search existing courses by tags. (Searching for a tag will output courses with it)
13. Search existing courses by tags, including similar terms.

F) Download feature
14. Download the analysis.