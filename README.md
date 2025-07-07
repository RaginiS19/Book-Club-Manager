# Book-Club-Manager

Overview
Book Club Manager is a web-based Content Management System (CMS) built using ASP.NET Core MVC, MySQL, and Entity Framework (Code First). This platform allows users to create, manage, and organize book clubs, members, books, and meetings in an intuitive and structured interface. It is designed to help book enthusiasts streamline club activities, track reading progress, and manage member participation efficiently.

## Key Features
- 📖 Book Management – Add, edit, and browse books with genre and author details.
- 🏛️ Club Management – Create and manage book clubs with location and description.
- 👥 Member Directory – Maintain a list of members and their club memberships.
- 📅 Meeting Scheduler – Schedule meetings with assigned books and track attendees.
- 🔍 Search & Filter – Easily search for books, members, and filter meetings by club.


## Technologies Used
- ASP.NET Core MVC
- Entity Framework Core (Code First)
- MySQL Database
- Bootstrap / HTML / CSS
- LINQ & Razor Views

## Entities and Relationships
Entity	Key Fields	Relationships
- Book	Title, Author, Genre, Summary	One-to-many with Meeting
- Club	Name, Description, Location	One-to-many with Meeting, many-to-many with Member
- Member	Name, Email, Role	Many-to-many with Club, many-to-many with Meeting
- Meeting	Date, Location, BookId, ClubId	Belongs to Club, has one Book, many Members
- ClubMember (join table)	ClubId, MemberId	Links Members and Clubs
- MeetingMember (join table)	MeetingId, MemberId	Tracks who attended what

 ## MVP Features
- Book CRUD
* Add/edit/delete books
* View all books
* Club CRUD
* Add/edit/delete clubs
* Add members to a club

- Member CRUD
* Add/edit/delete members
* Assign to one or multiple clubs
* Meeting Scheduler
* Assign a book and club to each meeting
* Add members who attended

- Search & Filter
* Filter meetings by club
* Search books by genre or author


