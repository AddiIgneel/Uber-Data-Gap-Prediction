# Uber-Data-Gap-Prediction
Model predicts gap prediction for data collected for Uber
As less than 10% of worlds citizens own automobiles, the frequency at which citizens commute on taxis, buses, trains, and planes is very high. Uber and other ride sharing service, roughly processes over 11 million trips, plans over 9 billion routes and collects over 50TB of data per day. To meet needs of riders, these services must continually innovate to improve cloud computing and big data technologies and algorithms in order to process this massive amount of data and uphold service reliability. Supply-demand forecasting is critical to enabling these services to maximize utilization of drivers and ensure that riders can always get a car whenever and wherever they may need a ride. Supply-demand forecasting helps to predict the volume of drivers and riders at a certain time period in a specific geographic area. For instance, demand tends to surge in residential areas in the mornings and in business districts in the evenings. Supply-demand forecasting allows these services to predict demand surges and guide drivers to those areas. The end result is higher earnings for drivers and no surge pricing for riders!

The data was collected by my Teacher. The data is uncleaned and not sorted properly. There are following files in training data folder.

  1. The Order Info Table shows the basic information of an order, including the passenger and the driver (if driver id
     =NULL, it means the order was not answered by any driver), place of origin, destination, price and time. The fields  
     order id, driver id, passenger id, start hash, and dest hash are made not sensitive.
     
  2. The District Info Table shows the information about the districts to be evaluated in the contest. You need to do the
     prediction given the districts from the District Definition Table. In the submission of the results, you need to map the
     district hash value to district mapped ID.
     
  3. The POI Info Table shows the attributes of a district, such as the number of different facilities. For example, 2#1:22
     means in this district, there are 22 facilities of the facility class 2#1. 2#1 means the first level class is 2 and the
     second level is 1, such as entertainment#theater, shopping#home appliance, sports#others. Each class and its number
     is separated by 
     
  4. The Traffic Jam Info Table shows the overall traffic status on the road in a district, including the number of roads at
     different traffic jam levels in different time periods and different districts. Higher values mean heavier traffic.
    
  5. The Weather Info Table shows the weather info every 10 minutes each city. The weather field gives the weather conditions
     such as sunny, rainy, and snowy etc; all sensitive information has been removed. The unit of temperature is Celsius degree,
     and PM2.5 is the level of air pollutions.

The test data is described as following:
     All the tables in test data are same except the order table it has the following fields :
     Field Type Meaning Example
     order id string order ID 70fc7c2bd2caf386bb50f8fd5dfef0cf
     passenger id string user ID 238de35f44bbe8a67bdea86a5b0f4719
     start district hash string departure d4ec2125aff74eded207d2d915ef682f
     dest district hash string destination 929ec6c160e6f52c20a4217c7978f681
     Time string Timestamp of the order 2016-01-15 00:35:11
