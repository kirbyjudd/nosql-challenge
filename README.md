# nosql-challenge
nosql-challenge Module 12 Challenge

## Background

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## Part 1: Database and Jupyter Notebook Set Up
The first step was to import the establishments.json file from the terminal using this import text:
- mongoimport --type json -d uk_food -c establishments --drop --jsonArray establishments.json

After importing pymongo and pprint, an instance was created using the Mongo Client. I then confimred that the database was created and the data was loaded properly.

## Part 2: Update the Database
Next I had to update the database by adding a new restaurant called "Penang Flavours" into the stablihsments collection. I then was tasked with updating the restaraunt's BusinessTypeID.

The magazine was not interested in any establishments in Dover so I removed any establishments within the Dover Local Authority from the database and ensured that they were deleted properly.

I lastly update the latitude and longitudes values to make sure they were decimal numbers (Double) and the RatingValue value to make sure it was an intger number.

## Part 3: Exploratory Analysis
The last part of the assignment had me analyze the information from the database to answer these four questions:
- Which establishments have a hygiene score equal to 20?
- Which establishments in London have a RatingValue greater than or equal to 4?
- What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
- How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

I converted all of the question results to Pandas DataFrames.
