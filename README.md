# Flight Management System

# Introduction

The flight management system is an application that assists passengers to easily book, modify, and cancel their flights. Travellers can complete mandatory web check-ins and obtain boarding passes from the comfort of their homes. The app sends notifications to passengers to remind them of their upcoming flights and the steps they need to finish before boarding. Along with all these features, this application has a feature called "Baggage Track" that aids traveller in tracking down their bags. With this tool, consumers may check real-time updates on their luggage and confirm that it is in fact traveling to its intended location. This delivery tracking app-like "baggage track" enables users to track their luggage with the help of a distinct bar code number that is assigned to each user's bag during airport check-in. This app primarily consists of data from one specific airline, for example emirates, and offers all the necessary flight information related to that particular airline. The application is free and designed to be mobile-friendly.

# Business Analysis

There are two users for this application. One is the customer, and the other is the administrator.
Customer: 
- With the help of their name, email, phone number, password, and nationality, users sign up for the app. Once logged in, the user can begin looking for flights by entering the appropriate departure and arrival cities, the date of travel, how many people will be traveling, and whether the trip is one-way or round-trip.
- In accordance with the search parameters, the app redirects to a page with relevant flights.
- After the user chooses the flight, they can make the payment by selecting the appropriate payment option.
- Users can access their reserved bookings in their profile, manage or cancel the flights. They can web check in and obtain their boarding passes up to 48 hours before take-off.
- The user can enable the ‘baggage track’ feature after checking in at the airport by inputting the special bar code number.

Administrator: 
- Admin can access the system with their login credentials.
- Administrators have the ability to add, update, and delete data regarding available flights and individual passenger’s luggage.


# Business Rules

The application primarily consists of two users: Customer/User and Administrator/Admin.
1.	CUSTOMER registers on the application with name, email, mobile number, and nationality. CUSTOMER can login to the app using USERNAME and PASSWORD.
2.	The CUSTOMER ACCOUNT will contain all the details regarding PROFILE, BOOKINGS, and PAYMENT METHODS.
3.	CUSTOMER can search for flights by entering appropriate FLIGHT DETAILS.
4.	The PAYMENT option is available for First class, Business class, and Economy ticket type.       
5.	The ADMIN will log in to the database system using the USERNAME and PASSWORD. ADMIN can add, update, and delete information regarding flight and customers.
6.	ADMIN will have unrestricted access to the payment.
7.	Only until the flight has taken off, both CUSTOMER and ADMIN will be able to access the BAGGAGE TRACK option. While the ADMIN can UPDATE the bag's location, the CUSTOMER can MONITOR the movement of their bag.

# Table Design and Analysis

<img src = "ER_Diagram.jpg">
There are six entities total in the flight management system, each with its own primary and secondary keys.
1.	User: This entity consists of one primary key – User_ID int(50). Other attributes are User_Name varchar(20), User_Email varchar(20), First_Name varchar(20), Last_Name varchar(20), User_Mobile varchar(20), User_Country varchar(20), Username varchar(20), Password varchar(20).
2.	Flight_Details: This entity consists of one primary key – Flight_ID int(50). Other attributes are Departure_City varchar(30), Arrival_City varchar(30), Date int(50), Trip_Type varchar(20), Passengers_Count int(50).
3.	Ticket_Type: This consists of one primary key which is also a foreign key – Flight_ID int(50). Other attributes are Ticket_Class varchar(20), Ticket_Price int(50).
4.	Payment: This consists of one primary key – Transaction_ID int(50) and two foreign keys – Flight_ID int(50), Booking_ID int(50). Other attributes are Trasaction_Date int(50), Trasaction_Time int(50).
5.	Bookings: This entity consists of one primary key – Booking_ID int(50) and two foreign keys – Flight_ID int(50), User_ID int(50). Other attributes are Booking_Date int(50), Booking_Time int(50).
6.	Baggage_Track: This entity consists of one primary key – Baggage_ID int(50). Three foreign keys – Flight_ID int(50), User_ID int(50), and Booking_ID int(50). And one other attribute Baggage_location varchar(20).

