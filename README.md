### "Data-driven Insights for UK Food Hygiene Ratings for Eat Safe, Love"


# Background

The UK Food Standards Agency conducts evaluations of establishments across the United Kingdom and assigns them food hygiene ratings. Eat Safe, Love, a food magazine, has contracted you to analyze the ratings data and provide insights to their journalists and food critics for future articles. By examining the ratings database, you will help identify establishments of interest and assist in decision-making for the magazine.

# Methods

### Part 1: Database and Jupyter Notebook Set Up

1. Import the establishments.json file into MongoDB using the Terminal, creating the uk_food database and establishments collection.
2. Import necessary libraries: PyMongo for MongoDB connectivity and Pretty Print (pprint) for formatted display.
3. Create a MongoDB client instance.
4. Confirm the successful creation of the database and data load:
   - List the databases to ensure "uk_food" is present.
   - List the collections in the database to confirm the "establishments" collection.
   - Use find_one and pprint to display one document from the establishments collection.
5. Assign the establishments collection to a variable for further use.

### Part 2: Update the Database

1. Add a new unrated halal restaurant, "Penang Flavours," located in Greenwich, to the establishments collection based on the provided information.
2. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return the BusinessTypeID and BusinessType fields.
3. Update the new restaurant document with the retrieved BusinessTypeID.
4. Check the number of documents containing the Dover Local Authority, remove them from the database, and verify the deletion.
5. Convert latitude and longitude values from strings to decimal numbers using update_many.

### Part 3: Exploratory Analysis

1. Address specific questions posed by Eat Safe, Love using the establishments database:
   - Determine the establishments with a hygiene score equal to 20.
   - Identify establishments in London with a RatingValue greater than or equal to 4.
   - Find the top 5 establishments with a RatingValue of '5,' sorted by the lowest hygiene score, nearest to "Penang Flavours."
   - Count the establishments in each Local Authority area with a hygiene score of 0, sort the results from highest to lowest, and print the top ten local authority areas.
2. Utilize count_documents, pprint, and Pandas DataFrame to present the results for each question.


## ANALYSIS & RESULTS

Establishments with  hygiene score equal to 20

![Alt text](DF%20Results/est_hygiene_score%20equal_to_20.png)

Establishments in London with a RatingValue greater than or equal to 4

![Alt text](DF%20Results/est_ratingValue%20greater%20than%20or%20equal%20to%204.png)

Top 5 establishments with a RatingValue rating value of '5', sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"

![Alt text](DF%20Results/est_top_five_nearest_Penang.png)

Establishments in each Local Authority area have a hygiene score of 0

![Alt text](DF%20Results/est_local_Autho_hygiene0.png)



Source:
https://courses.bootcampspot.com/courses/2799/assignments/42886?module_item_id=803399
