# nosql-challenge
# Instructions

## Part 1: Database and Jupyter Notebook Set Up

1. **Use NoSQL_setup_starter.ipynb for this section of the challenge.**

2. **Import Data:**
   - Import the data provided in the `establishments.json` file from your Terminal.
   - Name the database `uk_food` and the collection `establishments`.
   - Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.

3. **Import Libraries:**
   - Within your notebook, import the libraries you need: PyMongo and Pretty Print (`pprint`).

4. **Create Mongo Client:**
   - Create an instance of the Mongo Client.

5. **Confirm Database and Collection:**
   - List the databases you have in MongoDB. Confirm that `uk_food` is listed.
   - List the collection(s) in the database to ensure that `establishments` is there.
   - Find and display one document in the `establishments` collection using `find_one` and display with `pprint`.
   - Assign the `establishments` collection to a variable to prepare the collection for use.

## Part 2: Update the Database

1. **Use NoSQL_setup_starter.ipynb for this section of the challenge.**

2. **Add New Restaurant:**
   - An exciting new halal restaurant just opened in Greenwich but hasn't been rated yet. Add the provided information to the database.

3. **Find BusinessTypeID:**
   - Find the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.

4. **Update New Restaurant:**
   - Update the new restaurant with the `BusinessTypeID` you found.

5. **Remove Establishments in Dover:**
   - The magazine is not interested in any establishments in Dover. Check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database and check the number of documents to ensure they were deleted.

6. **Convert String Values to Numbers:**
   - Use `update_many` to convert latitude and longitude to decimal numbers.
   - Use `update_many` to convert `RatingValue` to integer numbers.

## Part 3: Exploratory Analysis

- **Use NoSQL_analysis_starter.ipynb for this section of the challenge.**

- **Notes:**
  - `RatingValue` ranges from 1-5, with higher values indicating better ratings.
  - Some fields, like 'Pass', represent non-numeric values and will be coerced to nulls during the database setup.

- **Explore the Database:**
   - For each question, use `count_documents` to display the number of documents, `pprint` to show the first document, and convert the result to a Pandas DataFrame, printing the number of rows and displaying the first 10 rows.

   1. Establishments with a hygiene score equal to 20.
   2. Establishments in London with a `RatingValue` greater than or equal to 4.
   3. Top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant "Penang Flavours".
   4. Number of establishments in each Local Authority area with a hygiene score of 0, sorted from highest to lowest. Display the top ten local authority areas.
