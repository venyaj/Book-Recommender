# Assumptions
- Every book must have a unique author (one-to-many)
- Publisher to Book is one-to-many (every book only has one publisher)
- The user can submit up to one review per book (a user/book pair uniquely identifies a review). A user may review more than one book, and a book may have reviews from multiple distinct users.
- Users to Books is called Reviews and is many-to-many
- Usernames are unique
- Ratings must be between 0 and 10 inclusive (will use an assertion for this)
- The order in a Friends relationship matters (A wants recommendations from B) and is many-to-many

# Relational Schema

User(Username STRING PK, DisplayName String, PasswordHash String, Age Int)

Author(Name String PK, Popularity INT)

Book(ISBN String PK, Title String, YearReleased Int, Author String, PublisherId FK references Publisher.PublisherId)

Review(Username String FK references User.Username, ISBN String FK references Book.ISBN, Rating INT, Description String, PK = (Username, ISBN))

Publisher(PublisherName String, PublisherId Int PK)

Friends(WantsRecs String FK references User.Username, GivesRecs String FK references User.Username);

**Important Note:** Since we don't have popularity information for every author in the Books database, we chose to not enforce Books.Author as a foreign key rather than creating a new record in Authors with a NULL popularity when we don't have this information.
