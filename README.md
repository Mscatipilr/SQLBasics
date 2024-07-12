# SQLBasics

## Objective:
The purpose of this assignment is to provide you with hands-on practice with SQL basics. You'll be setting up your database, creating tables, and inserting and querying data.

## Instructions:
For this assignment, you will work with SQLite, a simple file-based database system that's great for learning SQL. Follow the steps below to complete the assignment:

Download and Install SQLite: Follow the instructions here Links to an external site.to download and install SQLite on your system. (You are also welcome to use the online version Links to an external site., but you won't be able to do the database commands)

Create a New SQLite Database: Create a new SQLite database called 'Bookstore'. ( where you want your DB create text file then name it BookStore.db it will create a DB for you to use.)

Create a Table: In the 'Bookstore' database, create a table called 'Books'. The 'Books' table should have the following columns: 'BookID' (integer), 'Title' (string), 'Author' (string), 'PublicationYear' (integer), 'Price' (float).

Insert Data into the Table: Insert at least five different books into the 'Books' table.

Query the Table: Write and execute the following SQL queries on your 'Books' table:

Retrieve all books in the 'Books' table.
Retrieve all books published after 2000.
Retrieve all books written by a certain author (choose an author from the books you inserted).
Update the price of a certain book (choose a book from the books you inserted).
Delete a certain book from the 'Books' table (choose a book from the books you inserted).
 
## Submission:
Please submit the SQL queries you wrote for each of the steps above. Additionally, write a brief reflection (about 1 paragraph) on what you learned from this assignment and any challenges you faced. Feel free to also put this in a repo with a readme for the reflection.

# My Work
--- Copy from Windows Command Prompt ---

C:\Program Files (x86)\SQL lite>sqlite3

SQLite version 3.46.0 2024-05-23 13:25:27 (UTF-16 console I/O)
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.

sqlite> sqlite3 BookStore.db

sqlite> CREATE TABLE IF NOT EXISTS Books (<br />
(x1...>     BookID INTEGER PRIMARY KEY,<br />
(x1...>     Title TEXT,<br />
(x1...>     Author TEXT,<br />
(x1...>     PublicationYear INTEGER,<br />
(x1...>     Price REAL<br />
(x1...> );<br />
sqlite><br />
sqlite> INSERT INTO Books (BookID, Title, Author, PublicationYear, Price) VALUES (1, 'To Kill a Mockingbird', 'Harper Lee', 1960, 10.99);<br />
sqlite> INSERT INTO Books (BookID, Title, Author, PublicationYear, Price) VALUES (2, '1984', 'George Orwell', 1949, 9.99);<br />
sqlite> INSERT INTO Books (BookID, Title, Author, PublicationYear, Price) VALUES (3, 'The Great Gatsby', 'F. Scott Fitzgerald', 1925, 8.99);<br />
sqlite> INSERT INTO Books (BookID, Title, Author, PublicationYear, Price) VALUES (4, 'Moby Dick', 'Herman Melville', 1851, 11.99);<br />
sqlite> INSERT INTO Books (BookID, Title, Author, PublicationYear, Price) VALUES (5, 'War and Peace', 'Leo Tolstoy', 1869, 12.99);<br />

sqlite> SELECT * FROM Books;<br />
1|To Kill a Mockingbird|Harper Lee|1960|10.99<br />
2|1984|George Orwell|1949|9.99<br />
3|The Great Gatsby|F. Scott Fitzgerald|1925|8.99<br />
4|Moby Dick|Herman Melville|1851|11.99<br />
5|War and Peace|Leo Tolstoy|1869|12.99

sqlite> SELECT * FROM Books WHERE PublicationYear > 1900;<br />
1|To Kill a Mockingbird|Harper Lee|1960|10.99<br />
2|1984|George Orwell|1949|9.99<br />
3|The Great Gatsby|F. Scott Fitzgerald|1925|8.99

sqlite> SELECT * FROM Books WHERE Author = 'George Orwell';<br />
2|1984|George Orwell|1949|9.99

sqlite> UPDATE Books SET Price = 12.99 WHERE Title = '1984';<br />
sqlite> DELETE FROM Books WHERE Title = 'Moby Dick';<br />
sqlite> SELECT * FROM Books;<br />
1|To Kill a Mockingbird|Harper Lee|1960|10.99<br />
2|1984|George Orwell|1949|12.99<br />
3|The Great Gatsby|F. Scott Fitzgerald|1925|8.99<br />
5|War and Peace|Leo Tolstoy|1869|12.99

## Reflection

I've learned that there is quite a bit that goes into creating a database. SQL has a lot of features, many of which I don't know about or how to use. I've learned you can create and manipulate databases in several ways, such as: using commands in the command promt; using point and click in a GUI like the SQLite 3 GUI; and using commands in an SQL editor. I've learned some about the actual commands to create and manipulate databases as shown above. I had some challenges understanding how the editing process works, from accessing the created database to creating/accessing a table and where exactly to use the query commands. With help from co-workers, the internet, and trial and error, I was able to figure it out.
