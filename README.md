# 3 Part Mini Project: Building a sample database that will be used to track pets at a pet store and manipulating it to solve business questions.
## Part 1: Creating a table with the list of pets and their characteristics
### CREATE TABLE Statement Explanation:
The column names I have chosen for my pet_store table are pet_ID, pet_type, gender, and behavior. For the petID column, I chose INT because it’s the primary key for my table and my values
are integers. For the pet_type column I chose a VARCHAR data type with the character length of 7 because the longest pet type name available at my store is hamster, which is 7 characters. 
For the gender column, I used CHAR with a length of 1 character because the only genders available would be f for female and m for male. There wouldn’t be a change in the data type length.
As for the behavior column, the data type is VARCHAR with a character length of 50 because I wanted an ample amount of room to note additional behaviors I might notice in the pets.
### INSERT TABLE Statement Explanation:
The data fields are pet_type, gender, and behavior, so customers can get a good idea of the main characteristics of the pets that they’re looking to buy. The petID field is to help the store
owner keep track of each pet’s identity in relation to its characteristics and for the table to have a primary key.
### WHERE Clause Explanation:
My query answers the question of a potential customer looking for an energetic dog or cat as a pet. The data to be returned will show the information of each of the pet. The query addresses
the question by pulling only the matching rows of cats or dogs that display energetic behavior.
## Part 2: Creating a new table to track the cost and inventory of each pet. In this table, the primary ID for the table created in Pt 1 will be a foreign key in the Pt 2 table.
### CREATE TABLE Statement Explanation:
The column names for my pet_pricing table are uniqueID, salePrice, isStillForSale, createTimeStamp, createdBy, updateTimeStamp, updatedBy, and pet_name. The data type for uniqueID is set to INT
because it is the primary key in my pet_pricing table and it needs to have the same data type as the pet_store.petID in order to be a foreign key for the pet_store table. The data type for
salePrice is SMALLMONEY because the pets won’t be priced high enough to be needing the MONEY data type. isStillForSale data type is CHAR(1) because the values input for the column are only 
going to be ‘t’ for true, ‘f’ for false. The createTimeStamp and updateTimeStamp columns are both DATETIME data types so I could include the exact time and day values for the table. The createdBy, 
updatedBy, and pet_name columns are defined by the VARCHAR(25)  data type because the values input in these columns are names, and the character length is enough to fit the names of the workers 
and the pets.
### INSERT TABLE Statement Explanation:
The uniqueID column was created in order to link the week 6 pet_pricing table to the pet_store table from week 5. The salePrice, createTimeStamp, createdBy, updateTimeStamp, updatedBy, and 
pet_name columns were created to record/track more detailed information of when the price of the pets changes and which worker was responsible for changing each pet’s price.
### SELECT Statement w/ Inner Join and CREATE VIEW Statement Explanation:
I am joining on the petID and uniqueID because those are the columns that will allow the pet_store and pet_pricing tables to merge. As for the pet_name, isStillForSale, and salePrice columns, I am
joining on those columns in order to see the prices for pets that are available or unavailable.  Based on the data fields, the data expected to be shown is all of the pets in the store that have 
either been sold/still on the market, and for how much they were sold for/what they’re selling for. My query addresses the business question “Which pets were sold for what price? And which pets
are still waiting to be sold for what price?” because it includes each pets’ sold/selling status and price. Creating the view makes it easier and faster for me to lookup the pet inventory and 
price information I want to quickly check. Creating the view also helps me focus on looking at only the relevant columns I want.  My Part 1 SELECT Statement was focused on finding specific 
behaviors in certain pet types to help customers narrow down the characteristics they would be looking for in their pet, whereas my Part 2 SELECT Statement was focused on viewing the inventory
and pricing information of the pets that have been sold or waiting to be sold in the pet store.
## Part 3: Creating a Stored Procedure to record the sale of a pet
### Stored Procedure Explanation:
The Stored Procedure accurately checks to make sure the pet is in stock before updating it with the buyer's information.
### Sample Stored Procedure Execution Explanation:
In this example query, I am selling Bailey, the cat, as indicated by her petID number being 10 to a customer named Johnny Appleseed and recording his phone number.
