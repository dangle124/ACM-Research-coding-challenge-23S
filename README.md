# ACM Research Coding Challenge (Spring 2023)

## I. Data Preperation
### 1. Data Cleaning
Because data is massive, we cannot guarantee that there are no missing data. Therefore, we need to make sure all data has no "defection" by removing any rows that contains blank data.
### 2. Datatype Consistency
Although all numeric data appears to be float, some of their actual data type may be object. Therefore, we need to convert all data in object type to float type. After checking the output, they are in correct type, as shown in the figure below

<img width="314" alt="image" src="https://user-images.githubusercontent.com/104542629/212501727-025e03dc-0ebe-4efa-8654-22f8a5191d13.png">

## II. Data Summary 
We will get the basic descriptitive statistics of data, such as number of rows, average of each column (mean), standard deviation, minimum, maximum, 25, 50, 75 percentitiles, in case we need them later.

<img width="350" alt="image" src="https://user-images.githubusercontent.com/104542629/212502255-e6add5a9-ae98-47c5-a89d-12a945e360a4.png"> <img width="200" alt="image" src="https://user-images.githubusercontent.com/104542629/212502270-6e7e56b9-deda-4e57-a05c-c2f10e5e67e3.png">

### 1. Common Star Type 
To find the common star type, I will find the frequency of each type. The common type will have the highest frequency

### 1. Relationship between spectral class and temperature
#### a) Convert spectral class into numeric
First, to find the relationship between temperature and color, we need to convert color value into numeric; otherwise, we will not be able to compute anything. According to the article "What are the different types of stars in the universe?," posted on StarLust website, the classes of stars are O, B, A, F, G, K, and M. These classes also corresponds to a color, such as blue, blue-white, white, yellow-white, yellow, orange, and red, respectively [1]. We will use integer (0-6) to replace the classes (color) as the following: O-6, B-5, A-4, F-3, G-2, K-1, and M-0. 
#### b) Correlation between spetral class and temperature


