# iX-Class-Project
This is the class project for iX Data Science and AI course

Data Dictionary
ride_id: unique ID of a vehicle on a specific route on a specific day and time.
seat_number: seat assigned to ticket
payment_method: method used by customer to purchase ticket from Mobiticket (cash or Mpesa)
payment_receipt: unique id number for ticket purchased from Mobiticket
travel_date: date of ride departure. (MM/DD/YYYY)
travel_time: scheduled departure time of ride. Rides generally depart on time. (hh:mm)
travel_from: town from which ride originated
travel_to: destination of ride. All rides are to Nairobi.
car_type: vehicle type (shuttle or bus)
max_capacity: number of seats on the vehicle

Quality Assurance
The data set initially had 51645 entries however only 6249 unqiue entries (we grouped by the unique entries in order to get the total amount of tickets sold per day per route)
We made a new feature that aggregates the tickets bought per ride
There were no missing values
In comparison to the other data, cash payments comprised less than 1% of the payments but they were 
There were a number of object type features, which we converted into integers:
Split travel_date into year, month and day
Converted travel_date to weekday (starting from 0)
Converted car_type to 0 or 1 (Bus is 0 and shuttle is 1)
Converted travel_time to departure minutes from 00:00 and also obtained deaprture_hour
Encoded travel_from locations into integers (dictionary provided below):
        1. Awendo       
        2. Homa Bay     
        3. Kehancha     
        4. Kendu Bay   
        5. Keroka    
        6. Keumbu      
        7. Kijauri      
        8. Kisii        
        9. Mbita       
        10. Migori      
        11. Ndhiwa      
        12. Nyachenge    
        13. Oyugis      
        14. Rodi         
        15. Rongo        
        16. Sirare      
        17. Sori   
Cleaned up the data set

Individual Variable Distribution

Overall there are most tickets bought from Kisii with a massive spike, then Rongo
Most tickets from Kisii are bought for shuttle, other than that most are Buses
For average tickets per departure location, most are from Sirare, then Homa Bay, Mbita, and Migori are about the same
From the density curve we see that most common departure time are at around 7am
However, when we look at average tickets sold, surprisingly there is a massive spike for 7pm
Most tickets are bought for friday, however, and dip for saturday, other than that there is little variation
When we look at average tickets sold for weekdays there is far less variation
There are bus tickets sold than shuttle tickets

Relationships between Variables
- There is little meaningful correlation between variables in this data set
