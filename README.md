# MoMA Art Explorer

## The Situation
You work as a Research Intern at the Museum of Modern Art (MoMA) in New York City, one of the most popular and visited art museums in the world.

## The Assignment
The Museum's Curator has given you access to the database of artwork on display, and needs your help in exploring each artist's progression interactively.
Your task is to create a tool that allows the Curator to select a nationality, artist, and minimum year of creation and display their earliest work.

## The Objectives
1. Clean & prepare the data
2. Extract artist information
3. Display their work

## The Data Set

#### The Museum of Modern Art (MoMA) Collection
This research dataset contains 157,630 records, representing all of the works that have been accessioned into MoMA’s collection and cataloged in their database. It includes basic metadata for each work, including title, artist, date made, medium, dimensions, and date acquired by the Museum. Some of these records have incomplete information and are noted as “not Curator Approved.”

#### Recommended Analysis
1. How modern are the artworks at the Museum?
2. Which artists are featured the most?
3. Are there any trends in the dates of acquisition?
4. What types of artwork are most common?

#### Objective 1: Clean & prepare the data
Your first objective is to clean the artwork data by looking up the artist(s) for each piece and extracting its date of creation.

* Open the MoMA_OnView.xslx file and review the data in each tab.
* Look up the Artist for each artwork by using the ConstituentID field.

    - Use XLOOKUP to retrieve the artist from the "Artists" worksheet.
    - Modify the lookup_value in the function by splitting the ConstituentID by each comma.
    - Join the results so that you have all the artists for each artwork in a single cell.

* Create a CleanDate column that extract the first 4 numeric characters from each Date.
* Clean the OnView column by removing the “MoMA” prefix and quotation marks.

#### Objective 2: Extract artist information
Your second objective is to create dependent dropdown lists for nationality and artist, and display their number of artworks and their earliest & latest work on display.

* In a new sheet, create a dropdown list with artists’ Nationality in alphabetical order.
* Create a second, dependent dropdown list with the Artists for the selected nationality.
* Calculate the number of Artworks on display for the selected artist.
* Return the CleanDate for the earliest and latest artwork on display for the selected artist.

#### Objective 3: Display their work
Your final objective is to return additional information on the selected artist's earliest work after a certain date, along with the image of the artwork itself.

* Return the Title, CleanDate, Medium, Dimensions, Classification, Department, DateAcquired, ImageURL, and OnView for each of the selected artist’s artworks.
* Create a new data validation rule where the user can type in the Min Year to filter the selected artist’s work by.
* Incorporate the Min Year into the filter criteria for the artwork returned.
* Filter and transpose the list so that you only show the details for their earliest artwork.
* Use the ImageURL to display the artwork inside of a cell.

#### [Project Link]()