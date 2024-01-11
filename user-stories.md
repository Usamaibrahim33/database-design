<!-- - As a customer, so I can receive my tickets, I want to provide my contact information.
- As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
- As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies. -->
- USER STORY
1. "As a customer, so I can receive my tickets, I want to provide my contact information."
2. "As a customer, so I can decide which movie I want to watch, I want to see a list of movies."
3. "As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies."
4. "As a customer, so I can book tickets, I want to see the schedule of movies for a specific screen."
5. "As a customer, so I can choose a convenient time, I want to view the available showtimes for a particular movie on a specific day."
6. "As a customer, so I can have a personalized experience, I want to receive recommendations based on my movie preferences."
7. "As an admin, so I can track ticket sales, I want to view a report of tickets sold for each movie."
8. "As an admin, so I can manage screen information, I want to add or remove screens."
9. "As a customer, so I can enjoy loyalty benefits, I want to join a membership program."
10. "As a member, so I can enjoy discounts, I want to receive special offers on ticket prices."
11. "As a customer, so I can view upcoming releases, I want to see a list of movies coming soon to the cinema."


                                                ERD FOR THE USER STORY
 CUSTOMER ENTITY 
    * id(PK)                                                                                                                    one to one entity
    * name(string NOT NULL)
    * Email(string NOT NULL)
    * contactDetails(STRING NOT NULL)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * address(string NOT NULL)
    * membershipStatus(string NOT NULL)



MOVIE ENTITY
    * id(PK)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * title(string NOT NULL)
    * description(string NOT NULL)
    * genre()
    * schedule(NOT NULL)
    * duration(INT NOT NULL)
    * Price (INT NOT NULL)



TICKET ENTITY 
    * id(PK)
    * customer_id(FK)                                                                                       
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)


ADMIN ENTITY 
    * id(PK)
    * name(string NOT NULL)                                                                                
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * Email(string NOT NULL)




SCREEN ENTITY 
    * id(PK)
    * capacity(INT NOT NULL)                                                                             
    * number(INT NOT NULL)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * movieTime()


SHOWTIME ENTITY 
    * id(PK)
    * showDateTime(DATETIME)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * movieId(FK)
    * screen_id(FK)


TICKETSALES ENTITY 
    * id(PK)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * PurchaseDateTime(DATE INT)
    * ticket_id(FK)
    * numberOfSales(INT NOT NULL)




MEMBERSHIP ENTITY 
    * id(PK)
    * CreatedAt(DATE NOT NULL)
    * updatedAT(DATE)
    * MembershipStartDate(DATE)
    * MembershipEndDate(DATE)
    * customer_id(FK)


