## UK Food Standards Agency Data Evaluation
### Overview
The UK Food Standards Agency evaluates various establishments across the United Kingdom and assigns them a food hygiene rating. You have been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data. This analysis will help their journalists and food critics decide where to focus future articles.

Part 1: Database and Jupyter Notebook Setup
Use NoSQL_setup_starter.ipynb for this section of the challenge.

###Import Data:

Import the data provided in the establishments.json file from your Terminal.
Name the database uk_food and the collection establishments.
Copy the text you used to import your data from your Terminal to a markdown cell in your notebook.
Set Up Notebook:

Import the necessary libraries: PyMongo and Pretty Print (pprint).
Create an instance of the Mongo Client.
Confirm Data Load:

List the databases you have in MongoDB and confirm that uk_food is listed.
List the collection(s) in the database to ensure that establishments is there.
Find and display one document in the establishments collection using find_one and display it with pprint.
Assign the establishments collection to a variable for further use.
Part 2: Update the Database
Use NoSQL_setup_starter.ipynb for this section of the challenge.

### Add New Restaurant:

An exciting new halal restaurant just opened in Greenwich but hasn't been rated yet. The magazine has asked you to include it in your analysis. Add the following information to the database:
json
Copy code
{
    "BusinessName": "Penang Flavours",
    "BusinessType": "Restaurant/Cafe/Canteen",
    "BusinessTypeID": "",
    "AddressLine1": "Penang Flavours",
    "AddressLine2": "146A Plumstead Rd",
    "AddressLine3": "London",
    "AddressLine4": "",
    "PostCode": "SE18 7DY",
    "Phone": "",
    "LocalAuthorityCode": "511",
    "LocalAuthorityName": "Greenwich",
    "LocalAuthorityWebSite": "http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress": "health@royalgreenwich.gov.uk",
    "scores": {
        "Hygiene": "",
        "Structural": "",
        "ConfidenceInManagement": ""
    },
    "SchemeType": "FHRS",
    "geocode": {
        "longitude": "0.08384000",
        "latitude": "51.49014200"
    },
    "RightToReply": "",
    "Distance": 4623.9723280747176,
    "NewRatingPending": True
}
### Update Restaurant Information:

Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the BusinessTypeID and BusinessType fields.
Update the new restaurant with the BusinessTypeID you found.
Remove Dover Establishments:

Check how many documents contain the Dover Local Authority.
Remove any establishments within the Dover Local Authority from the database.
Check the number of documents to ensure they were deleted.
Convert Data Types:

Some of the number values are stored as strings. Convert these using update_many:
Convert latitude and longitude to decimal numbers.
Convert RatingValue to integer numbers.
Part 3: Exploratory Analysis
Use NoSQL_analysis_starter.ipynb for this section of the challenge.
