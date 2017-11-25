# Stara API 

**General for all Vehicles**

- Type of car
- Search by name
- Search by year



**For an individual vehicle**

- Fuel
  - Time of refuel
  - Amount of fuel
  - Type of fuel
  - Current status of the kilometer meter??
  - Which station the refuel took place
- Wash
  - Time of last wash
  - What type of wash  (pre-wash & foam & brushless wash etc.)
- Location
  - We can fetch data for a vehicle for a given time period
  - From there get latitude and longitude points every 10 seconds for that time period
  - Possibly plot the route of the vehicle?



**What Stara is currently displaying (Excel)**

- Comparison of fuel consumption between vehicle types
- Overall consumption during the year (graph with plots two times a year and each line represents a car type)
- How often each car type refuels each year, how many liters on average each type refuels and the total amount for the year



**Things that the STARA partner talked about**

- *Depends if we get access to the data*
  - Check how much fuel is refuled for each station ( refueling the big tanks on the stations )
  - Compare that amount to the fuel that has been extracted from the tank
  - Try to detect if there's any difference ( maybe somebody stole some fuel? )
- Using three different datasets
  - SAP order data (information about fuel stations)
    - We will get that through excel sheets
  - Dataset about where cars are refueling
    - Postman
  - Dataset about what each car is consuming
    - Postman
- Check how much each car type is polluting
  - Do some research on Wikipedia for example about how each car pollutes per mile for example
  - Compare that to how much each car has driven
- Compare fuel consumption between drivers/car types on similar routes
- ​