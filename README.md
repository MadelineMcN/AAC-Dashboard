# About

The purpose of this software application is to work with existing data from animal shelters to identify and categorize available dogs.

The source code for this application is comprised of:

· A python file that contains various module. These modules preform CRUD operations to the Austin Animal Center database as well as code to establish a connection to the database given certain credentials.

· A python file that takes information from the Animal Center Database and presents it in a python dashboard.

# Video Overview of Functionality

![](blob:https://stackedit.io/9ab45a30-5948-4c3e-851c-d6c60edbf712)

# Motivation

The motivation behind this application is to allow users at Grazioso Salvare to access easy-to-read data and analytics to select available rescue dogs for specific types of training programs. Part of this application can also be used to create, update, and delete entries of this database as well.

# Getting started

## Technologies Used:

For setup, you will need to following technologies:

· Python: This language was chosen due to its compatibility to Mongo and the MongoDB Query Language as well its ability to write executable code such as CRUD operations.

· Mongo: This database is open-source and document oriented.

· PyMongo: This will be helpful when setting up and troubleshooting the connection between python and the Mongo database.

· Jupyter Notebooks: Jupyter notebooks is used in the development of this application for easy testing and is a popular tool where data analytics is involved.

· Terminal: The terminal was used in this application to set up the database, create users, and set permissions.

· Dash: Python dash was used to populate data into a readable data table, pie chart, and map.

· Pandas: Used in this application to load data into a DataFrame. Dataframes are useful when different types of data are being displayed together. Additionally, pandas dataframe can be used with dash_table.

· Plotly: Used to generate and style dashboard charts

## Resources Used

·[https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)
· [https://plotly.com/python/pie-charts/](https://plotly.com/python/pie-charts/)
· [https://dash.plotly.com/dash-core-components](https://dash.plotly.com/dash-core-components)
· [https://www.mongodb.com/docs/](https://www.mongodb.com/docs/)
· [Make a README](https://www.makeareadme.com/), [Best README Template](https://github.com/othneildrew/Best-README-Template), [Best README Template](https://github.com/othneildrew/Best-README-Template), [A Beginners Guide to Writing a Kickass README](https://medium.com/@meakaakka/a-beginners-guide-to-writing-a-kickass-readme-7ac01da88ab3)

## Initial Setup

Import the database. The script used to import data into the AAC database is documented in this screenshot.

In order to gain access to this data, the admin will need to create a new user using this  Mongo script:

![](blob:https://stackedit.io/6e6fae34-8ced-4728-9f87-d7d1806f9479)

In your terminal, authenticate and access the Mongo AAC database by entering the following:

![](blob:https://stackedit.io/639772ff-1375-4bde-96af-9be5d0e3614c)

Enter your password when prompted

# Usage

This section of the documentation will briefly go over the source code as well as how the application looks and functions when it is run. (As it is hard to get the unique identifier in screenshots involving the charts, multiple unique identifiers were added).

## AnimalShelter. py

Modules:

· Create: Used to add data into the AAC database
· Read: Used to query and read data in the AAC database. Returns in cursor format
· Update: Can be used to modify entries in the database
· Delete: Deletes an entry using data as a parameter. Returns a cursor result of how many entries were deleted.


## Project2.ipynb

**Unique Identifier & Logo:**

Image provided by Grazioso Salvare.

Code used to create:

![](blob:https://stackedit.io/a35d942e-02b9-4a79-848e-cfc73c084986)



**Initial Data table view**

Before any dropdown options are selected, this is how the dashboard data table looks.

Code used to create:

![](blob:https://stackedit.io/656ae010-9703-419c-9db5-29d9dbf2217e)


**Initial Pie chart and Map**

When the pie chat is hovered over, type of breed displays as a pop out.

![](blob:https://stackedit.io/67de2032-ae9c-4c84-8195-db9f8603118c)


**Dropdown options**

Labels created for the purpose of displaying in the dropdown, value variable used to define actions when an option is selected.

Code used to create:

![](blob:https://stackedit.io/89ec9e02-744a-4191-bdeb-ad2bf1a4d27f)


**Option 1: Water Rescue**

Per the requirements, water rescue option from the dropdown needed to include- breeds: Labrador Retriever Mix, Chesapeake Bay Retriever, Newfoundland. Preferred Sex: Intact Female. Training Age: 26 weeks to 156 weeks

Code:

![](blob:https://stackedit.io/57fdfa81-8dfb-4967-9eae-ee7d107244dc)

**Option 2: Mountain or Wilderness**

Per the requirements, Mountain or Wilderness option from the dropdown needed to include- breeds: German Shepherd, Alaskan Malamute, Old English Sheepdog, Siberian Husky, Rottweiler. Preferred Sex: Intact Male. Training Age: 26 weeks to 156 weeks

Code:

![](blob:https://stackedit.io/ec11764c-74db-4af8-b960-6175a3fdd4d9)


**Option 3: Disaster or Individual Tracking**

Per the requirements, Disaster or Individual Tracking option from the dropdown needed to include- breeds: Doberman Pinscher, German Shepherd, Golden Retriever, Bloodhound, Rottweiler. Preferred Sex: Intact Male. Training Age: 20 weeks to 300 weeks

Code:

![](blob:https://stackedit.io/e3c25655-8763-47cb-a982-159a73c7e0b6)



**Reset:**

Resetting the dashboard returns it to its initial sate.



# Testing

Testing was executed after development of the python file "AnimalShelter. py". A brief example of what that looked like is documented below. For this, I wrote a simple program that adds a dog to the database and then pulls that entry from the database using the read module I created. New implementations include updating the newly created entry and then a clean-up/delete test at the end.

# Prompt Questions
-   How do you write programs that are maintainable, readable, and adaptable? Especially consider your work on the CRUD Python module from Project One, which you used to connect the dashboard widgets to the database in Project Two. What were the advantages of working in this way? How else could you use this CRUD Python module in the future?

	 - Code maintainability, readability and adaptability can be accomplished/attempted in multiple ways. One popular practice, as seen in the python file of this project, is modularization. By seperating each CRUD action into its own function, the code is more readable and the CRUD actions are easier to use in other files. 

-   How do you approach a problem as a computer scientist? Consider how you approached the database or dashboard requirements that Grazioso Salvare requested. How did your approach to this project differ from previous assignments in other courses? What techniques or strategies would you use in the future to create databases to meet other client requests?

	 - As a computer scientist, a problem must first be addressed by gather requirements. Grazioso Salvare had specific requirements of the application in order to to produce the correct results as displayed on the dashboard. The main difference of my approach to this project as opposed to other projects is that the requirements in this project were well-defined and from a ‘user’. In previous projects, I would typically be the one to decide what requirements would produce the results that matched the assignment criteria. 

-   What do computer scientists do, and why does it matter? How would your work on this type of project help a company, like Grazioso Salvare, to do their work better?
	 - This is an interesting question, as there is a large scope to what computer scientists do. In short, computer scientists use technology in attempt to answer questions, solve problems, and advance society. In this example, the work I did as a computer sciencist was used to help a non-profit place and train rescue dogs. 

# Contact

Madeline McNeeley

Last updated: October 21, 2022
