# Project : WHAT ARE MAIN FACTORS AFFECTING THE PRICE OF A USED CAR, DEALERS AND PRIVATE ARE NEEDED TO KNOW. 

# Reza Zamani 


# OVERVIEW
I explore a dataset from Kaggle, has 426K rows, to understand what factors affecting the price of a used car. Using different Machine Learning (ML) algorithms, I will say you what are the main drivers of the price of used cars. then you can pay attention to them as dealer or private to sell or buy. 

# Business Understanding
Using 18 factors, I will say which of them is important for price, how their proecess is affecting the price. Moreover, it is important to understand the strucrue of demand for used cars and in this project I will give you a clear suggestion to make decision about your portfolio of used cars.

If you are dealer or private and want to sell or buy used car, or if you are thinking which used car I can buy if I want to sell it again in the future it would be very easy for me. 
In this project I will give you a clear perspective to make decision. 

However all 18 factors do not have the same effect on price, and I will give you an advice to focus only main drivers of the price of a used car. I know you are familiar with some of them such as age, mileage, and model. I will give you more information to have better understanding from demand and supply sides fo the market of used cars. 

After applying the Machine Learning (ML) models, we will check the validity of the model to be sure that our model is wokring well and results are reliable. we will use different methods to be sure that our model has minimum error and maximum verification in mathcing with data and also in prediction of the price of used car and its drivers.

# Data Understanding
1- we have around 427000 data with 18 factors. 

2-  target variable is price 

3- factros (features) we have in our dataset : region, id, year, manufacturer (brand), model, condition,cylinders, state
                                               fuel, odometer, title_status, transmission, VIN, drive, size, type, paint_color  
                                               
4- Missing data: some features have missing data, we check their relative size and make decision about them to remover

5- Outliders: some data are outliers and they can affect negatively our results and analysis, using different plot and also some statistics approahces, we manage them

6- Price: 

6-1- range of price:  raw data shows that price fluctutes from 0 to more than 3 million dollars. 

6-2- outlier in pirce: it is clear that some prices are not reasonable, and we should make decision. we see them as outlier, and remover them from analysis. 

6-3- price between 5000 to 25000 covers most part of used cars, and used car with price more than 50000 dollars have very low demand. 

7- year: 

7-1- range of year: from 1900.

7-2- most demand for used cars comes back to cars with age <= 15 years. 

8- odomerter: 
8-1- range of odometer: odomter from 0 to around one million mile.

8-2- outliers: some data for odometers are outliers and we remove them.

8-3- cars have odometers between 50000 to 150000 have the highest demand. 

8- other features: we also check the distribution of other factors to be familiar with data and their behaviour. visualization of these factors are interesting and give us really important information. 

9- correlation:

9-1- correlation between price and year (age) : about  34 % (-34%,)

9-2- correlation between price and odometer (milage): around -45% 

9-3- correlation between year and odometer (milage): 28%

# Modeling
1- we use four models: linear regression, Lasso regression, Ridge regression,  SFS (Seaquential Feature Selection).

2- we apply polynomial also in these models. 

3- we use GridSearchCV for Ridge model.

4- we split dataset into two data sets: trainign and test datasets. 

4- at the begining of modeling we standardized all data to have reliable results, then scale of data is not important. 



# Evaluation
1- Criterias for evaluation: aftler applying each model, we extract MAE, MSE, RMSE, and R2 (or Score) for both traing and test datasets, then we have all following critreria for each model:

'Train_MAE', 'Train_MSE', 'Train_RMSE', and 'Train_Score'

'Test_MAE',  'Test_MSE', 'Test_RMSE' and 'Test_Score

2- Best model: after modeling we need to find the best model it is Ridge Regression 

3- Accuracy: model can predict price with traing data set with %86 accuract, and with test dat set with %77, overal it is around %80 and is a really good accuracy. 

4- with different features and their interaction with each other (polynomila), we study the main drivers of price of used cars, our main finding are as followings. 

# Deployment

# 1- First Part: List of factors affecting the price of used cars: 
Age, Odometer, Manufacturer, Transmissin, Condition, Cylinders, Fuel, Color, Type, and Drive. 

# 2- Second Part: How factor affecting used car price
1- Age: as age goes up, the price of used car goes down. age is an important factor as correlation between price and age is -30%

2- Odometer: as Odometer goes up, the price of used car goes down too. Odometer is also an important factor and its correlation with price is also  aorund -30%

3- Manufacturer:
3-1- Best companeis (used car for sale): Toyota, Honda, Tesla, and Ford
3-2- Worst companies (used carfor slae): Buick and Cheverolet.

4- Transmissin: manual transmission has negative effect on pirce, then it would be hard to be sold.

5- Condition: used cars with: good condition or like new condition have the highest level to be sold.

6- Cylinders: 4, 6, and 8 Cylinders cars have better chance to be sold.

7- Feul: fuel gas has negative effect on price, and cars with fuel gas are hard to sell.

8- Color: red and green cars are hard to sell and have negative effect on price.

9- Drive: drive_fwd is hard to sell, while drive_rwd has good condition for sell.

# Third Part: 11 clear suggestions (for buying and seeling used cars)

1- Price: focus on cars their prices is between 5000 to 25000 dollars , they have high demand.

2- Year (age): Focus on cars with age <= 15 years , they have high demand.

3- Odometer: cars have 500,000 <=odometer =< 150,000 have high demand. Not odometer >= 250,000 , as they have very low demand, get aside from them

4- Brand: focus on Toyota, Honda, Tesla, and Ford and get aside from uick or Cheverolet.

5- Condition: focus on car with these two conditions: good condition and like new conditions.

6- Cylinders: Foucs on 4, 6, and 8 cylinders , they have maximum demand.

7- Transmission: not manual transmission , as it has negative effect on pirce.

8- Color: not red or green cars , they have low demand, get aside from them.

9- Feul: not feul gas, as it has low demand, get aside from them.

10- Drive: not "drive_fwd" cars, as they have low demand.

11- Type: not "van" cars, do not enter them in your portfolio.

