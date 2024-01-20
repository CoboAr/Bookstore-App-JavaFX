# Bookstore-app-JavaFX
A simple implementation of a bookstore app, graphical user interface (GUI) based.

## Requirements
NetBeans IDE 8.2     
JavaFX

## What is bookstore app?

The app is a single-window GUI, that is, ONLY one window is available to the user of the app (analogous to a web browser). This implies that if a user of the app clicks a button
to obtain a new screen, the last screen of the app should be replaced by the new screen, in the SAME
window (i.e. multiple windows MUST NOT get opened while using the app).

Whenever a user of the app clicks the [x] button (i.e. the exit button) at the top-right of the app win-
dow, all the relevant data currently present in the app should be written in two relevant files books.txt and customers.txt.


Every time the app is started, the data from the two files
books.txt and customers.txt is loaded in the data structure(s) of the app.
There are two kinds of users of this application: Owner and Customer. There is
only one Owner and zero or more Customers who uses the application.

## How does it work?
The app starts with a login-screen. The login-screen has three GUI items: a username field, a password
field, and the button [login]. The owner’s username is admin and password is admin.

![login screen](https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/86127112-2238-412d-9e94-84d6c7bf135e)


<ul>
  <li>How the owner will use the BookStore app:</li>
  <ul>
  <li>When the owner enters her username and password, and clicks button [login], a new screen replaces
the login-screen. We call this new screen owner-start-screen. The owner-start-screen has three buttons:
[Books], [Customers], [Logout].
A sample owner-start-screen is:

[owner start screen demo.webm](https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/234cdab4-8b2e-491d-9fa9-c1179b74a8ca)

![owner-start-screen](https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/352541d5-c4c6-4ac1-ad99-b1bbe226a590)
</li>
<li>
  When the owner clicks the button [Books], he sees a screen having three parts, a top part, a
middle part, and a bottom part. This is the owner-books-screen. The top part
of owner-books-screen contains a table. The table has two columns with heading Book Name
and Book Price, from left to right. A row in the table contains the name of a book in the Book
Name column, and its price in the Book Price column. It is assumed that the owner has only
one copy of a book, and hence the information about a book in a row implies just one copy of
that book.   
  
  The middle part of owner-books-screen contains three GUI items: two textfields
Name and Price; one button [Add]. When the owner enters a book’s name and its price in the
Name and the Price fields respectively, and then clicks the [Add] button, a new row containing
the book’s information gets entered in the table.   

The bottom part of the owner-books-screen
contains a [Delete] button and a [Back] button. When the owner selects a row in the table, and
then clicks the [Delete] button, the selected row should get deleted from the table and conse-
quently the book information corresponding to the deleted row gets removed from the bookstore. If the owner clicks the [Back] button, she should be taken back to the owner-start-
screen.

[owner books demo.webm](https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/3b13351a-2835-4d2a-93ae-290edbe58fc2)
</li>
<li>
  When the owner clicks the button [Customers], he sees a screen having three parts, a top part,
a middle part, and a bottom part. This is the owner-customers-screen. The
top part of owner-customers-screen contains a table. The table has three columns with heading Username, Password, Points, from left to right. They refer to a customer’s username, pass-
word, and the points the customer has earned by buying books.   
  
  The middle part of owner-
customers-screen contains three GUI items: two textfields Username and Password; one button[Add]. The owner can register a customer to the bookstore as follows: When the owner enters a
customer’s username and password in the Username and the Password fields respectively, and
then clicks the [Add] button, a new row containing the customer’s information gets entered in
the table. The Points for this newly added row can be 0, or any number.   

The bottom part of the owner-customers-screen contains a [Delete] button and a [Back] button. When the owner selects a row in the table, and then clicks the [Delete] button, the se-
lected row should get deleted from the table and consequently the customer information corresponding to the deleted row gets removed from the bookstore. If the owner clicks the [Back] button, he should be taken back to the owner-start-screen.   

https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/6bf5c46a-38ce-406b-b2ab-ed15c794dd23


</li>
</ul>

  <li>How a registered customer will use the BookStore app:</li>
  
  When a customer, say Jane (previously added by the owner) enters her username and password, and
clicks button [login], a new screen replaces the login-screen. We call this new screen customer-start-
screen. The customer-start-screen has three parts, a top part, middle part, and a bottom part.

<ul>
  <li>The top part shows the message “Welcome Jane. You have P points. Your status is S”. Here, P
is the number of points Jane currently has. S is one of the two status, either Gold or Silver, that
Jane has. A customer who has points less than 1000 has status silver. A customer who has
points 1000 or above has status gold.</li>

  <li>The middle part of customer-start-screen contains a table. The table has three columns. From
left to right, the first column has heading Book Name, the second column has heading Book
Price, the third column has the heading Select. A row in the table contains the name of a book
in the Book Name column, its price in the Book Price column, and a checkbox in the Select
column. The checkbox can be either checked or unchecked.</li>

<li>The bottom part of the customer-start-screen contains three buttons, [Buy], [Redeem points
and Buy], [Logout]. If the customer clicks the [Logout] button, she should be taken back to the
login-screen.</li>      


[customer start screen.webm](https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/44c30f26-640f-4389-9ad8-b5b18a5615e1)

</ul>
When the customer clicks either the button [Buy], or [Redeem points and Buy], a new screen replaces
the customer-start-screen. We call this new screen customer-cost-screen. This screen has three GUI
items from top to bottom.

<ul>
  <li>The top item is the message Total Cost: TC. Here TC is the total transaction cost. It is as-
sumed that the total cost of books is just the sum of the cost of individual books. There is no tax to be paid by the customer.</li>

  <li>The middle item is the message Points: P, Status: S. P is the current number of points of the
customer. S is the current status of the customer.</li>

<li>The bottom item is a [Logout] button. If the customer clicks the [Logout] button, he should be
taken back to the login-screen.</li>

</ul>

For the case [Redeem points and Buy], the TC should be the transaction cost after the relevant
amount of existing points of the customer has been redeemed. Here it is assumed that when possible,
all the accumulated points must be redeemed. Further assumption: Number of points can be 0 or positive. It is assumed that for every 1 CAD spent by the customer, she earns 10 points. It is also as-
sumed that for every 100 points redeemed by a customer, only 1 CAD is deducted from her transaction cost. The transaction cost must not be less than 0.      


**An example to explain accumulation and redemption of points, and update of customer’s status is
as follows:**       

If  there are four books in the store whose prices are 50, 100, 200, 500. Let's assume
that one customer has been added previously in the store by the owner.
<ul>
  <li>When the customer logs in for the first time, the points P should be zero, and the status S
should be Silver. If the customer clicks button [Buy] for buying two books whose prices are
200, and 500 then TC should be 700, and customer’s points P should become 7000 and status S
should become Gold.</li>
  
  <li>In the next login session, if the same customer clicks [Redeem points and Buy] for buying the
book with price 50, then TC should be 0, and customer’s points P should become 2000. Cus-
tomer’s status S stays at Gold.</li>

<li>In the next login session, if the same customer again clicks [Redeem points and Buy] to buy
the book with price 100, then TC should be 80, and customer’s points P should become 800.
The customer’s status should change to Silver.</li>
</ul>

https://github.com/CoboAr/Bookstore-app-JavaFX/assets/144629565/17617078-fbf8-48d4-a523-dd1f9ca339de

<li>State design pattern:</li>
The State design pattern was used in the “Client”, “State”, “Silver”,
and “Gold” classes. This design pattern was perfect for handling classes where a change of internal state can change the behavior of an object. In this
case, the change in the number of points a client has determines whether their state is set to
Silver or Gold. The State design pattern is implemented in a way such that if the points reach
or eclipse “1000” then it will set the status to “Gold” otherwise, the status will remain on “Silver”. The pattern  allows the programmer to add more states in the future just by declaring new subclasses and without altering the original code.

</ul>

Enjoy! And please do let me know if you have any comments, constructive criticism, and/or bug reports.
## Author
## Arnold Cobo
