# ACM Research Coding Challenge (Spring 2023) - Draft

## I. Data Preperation
### 1. Data Cleaning
Because data is massive, we cannot guarantee that there are no missing data. Therefore, we need to make sure all data has no "defection" by removing any rows that contains blank data.
### 2. Datatype Consistency
Although all numeric data appears to be float, some of their actual data type may be object. Therefore, we need to convert all data in object type to float type. After checking the output, they are in correct type, as shown in the figure below

<img width="314" alt="image" src="https://user-images.githubusercontent.com/104542629/212501727-025e03dc-0ebe-4efa-8654-22f8a5191d13.png">

## II. Data Analysis 
We will get the basic descriptitive statistics of data, such as number of rows, average of each column (mean), standard deviation, minimum, maximum, 25, 50, 75 percentitiles, in case we need them later.

<img width="350" alt="image" src="https://user-images.githubusercontent.com/104542629/212502255-e6add5a9-ae98-47c5-a89d-12a945e360a4.png"> <img width="200" alt="image" src="https://user-images.githubusercontent.com/104542629/212502270-6e7e56b9-deda-4e57-a05c-c2f10e5e67e3.png">

### 1. Common Star Type 
To find the common star type, I will find the frequency of each type. The common type will have the highest frequency

### 1. Relationship between spectral class and temperature
Let's make a hypothesis that there is a linear relationship between spectral class and temperature.
#### a) Convert spectral class into numeric
First, to find the relationship between temperature and color, we need to convert color value into numeric; otherwise, we will not be able to compute anything. According to the article "What are the different types of stars in the universe?," posted on StarLust website, the classes of stars are O, B, A, F, G, K, and M. These classes also corresponds to a color, such as blue, blue-white, white, yellow-white, yellow, orange, and red, respectively [1]. We will use integer (0-6) to replace the classes (color) as the following: O-6, B-5, A-4, F-3, G-2, K-1, and M-0. 
#### b) Regression table
The regression table below shows all the statistic values needed to prove the hypothesis mentioned earlier. 
<img width="463" alt="image" src="https://user-images.githubusercontent.com/104542629/212528039-a602d703-1ace-45dd-b915-75ffb491a9ee.png">

We will use hypothesis testing to prove the coefficient of the linear regression, generated by spectral class as independent variable and temperature as dependent variable. If the coefficients of the linear regression equation equals to 0, there is no relationship as being stated in the hypothesis.

Consider coefficient of temperature:

    H0: coefficient of temperature = 0
    HA: coefficient of temperature ≠ 0
    
    H0: intercept = 0
    HA: intercept ≠ 0   
From the regression table, we obtain both of the P value (P>|t|) of the coefficient of temperature and intercept, and they are all 0. It means that almost no chance that we falsely reject the H0. In the other words, we can state that there exists a linear relationship between spectral class and temperature and accept the hypothesis that we stated earlier. 
#### b) Linear Regression Graph



