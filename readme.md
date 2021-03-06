# Application summary

This application allows the user to search through and analyze the data (a list of courses offered by the school) by various metrics. It heavily utilizes the LDA model when attempting to determine topics from descriptions.

This project excludes the french component in some areas, as we are more comfortable in English. Including French would likely require some guidance but minimal coding.

The application is written in R Shiny.

## features
A) General data filtering

1. Convert data to UTF-8.
2. Clean the timestamps for the durations.
3. Allow for filtering the data by metrics such as course type, duration, and so on.

B) Listing interdependencies

4. For each value in the translations sheet, create a list of all terms that it should also tag.

C) Data analyzing through the LDA model

5. Gather a list of all course names as the domain for the LDA model.
6. Create an algorithm implementing the LDA model on a character vector of the descriptions.
7. Run the LDA model on the character vector of the descriptions with translations appended.

D) Finding good course groupings for a curriculum

8. Find the terms that it should be tagged by.
9. Create a list of courses that covers all terms that have been tagged (from the filtered data).

E) Create a search function

10. Search existing courses by tags. (Searching for a tag will output courses with it)
11. Search existing courses by tags, including similar terms.

F) Download feature

12. Download the analysis.

Credits to https://towardsdatascience.com/beginners-guide-to-lda-topic-modelling-with-r-e57a5a8e7a25 for helping with writing out the LDA model.
