# ACM Research Coding Challenge (Spring 2023) - Draft

## I. Problem description
Among seven properties (columns), a relationship between any two properties may exist. By understanding such relationships, we may predict, estimate, or examine one property by evaluating the other without wasting time collecting data. I will examine the relationship between spectral class and temperature. My goal is to find whether the temperate of a star has any effect on the appearent color. 

## II. Summary
My hypothesis is that temperature and color of a star has a positive linear relationship. Before analyzing data, I cleanned up the given data to remove any rows that contain missing data and converted colors to numeric values. After preparing data, I used two methods to examine the relationship. In the first method, I used correlation value. The second one, I computed the regression table and used hypothesis test to examine the coefficient of the linear regression. The result from both methods showed that between temperature and color existed a positive linear relationship. 

## III. Data Preperation
### 1. Data Cleaning
Because data is massive, we cannot guarantee that there are no missing data. Therefore, we need to make sure all data has no "defection" by removing any rows that contain blank data.

Another issue had arisen that the color values in the data table were inconsistent; for one color, there were multiple ways to write that color. For example, 'blue white' was written as 'Blue white', 'Blue White', 'Blue-white', etc. Therefore, I had to modify all colors so that they are written in lower case, with no leading and trailing whitespace and no hyphen. Also, 'yellowish' and 'whitish' were written as 'yellow' and 'white'. 
### 2. Convert color (string) into numeric value
Because color can be classified into warm and cool colors, I ordered the color data as the following: red, orange red, orange, pale yellow orange, yellow, yellow white, white, blue white, and blue. Next, I assigned numbers from 1 to 9 respective to that order.

| Color | Numeric Value |
| --- | --- |
| red | 1 |
| orange red | 2 |
| orange | 3 |
| pale yellow orange | 4 |
| yellow | 5 |
| yellow white | 6 |
| white | 7 |
| blue white | 8 |
| blue | 9 |

## IV. Data Analysis 
### 1. Hypothesis
There is a positive linear relationship between the color and temperature of a star.

### 2. Compute regression values
#### a) Correlation 
I computed the correlation between temperature and color by using a predefined method in Python, and the result is nearly 0.79. 

<img width="359" alt="image" src="https://user-images.githubusercontent.com/104542629/212599002-0ff698c9-2bd9-429c-96b3-518ee28000a8.png">

The correlation is greater than 0 and smaller than 1. This means that there exists a relationship between the two and maybe closely linear. However, this may not be sufficient enough to prove my hypothesis because the value is not very close to 1, so I need further examination. 

#### b) Regression table
I set temperature as the independent variable (x) and color as the dependent value (y). The regression table below shows all the statistic values needed to prove the hypothesis mentioned earlier.

<img width="464" alt="image" src="https://user-images.githubusercontent.com/104542629/212596855-0ea30766-04a7-4621-817d-252c588cc2fa.png">

Based on the values shown in the regression table, the linear regression equation is y = 0.0003x + 1.5512. We will use hypothesis testing to prove the coefficient of linear regression.

Consider coefficient of temperature:

    H0: coefficient of temperature = 0
    HA: coefficient of temperature ≠ 0
    
    H0: intercept = 0
    HA: intercept ≠ 0 

From the regression table, we obtain both of the P values (P>|t|) of the coefficient of both temperature and intercept as 0. The typical threshold for P is 0.05. Therefore, it means that almost no chance that we falsely reject the H0. In the other words, we can state that there exists a positive linear relationship between the temperature and color of a star. We can accept the hypothesis that we stated earlier. 

### 3. Linear Regression Graph
<img width="297" alt="image" src="https://user-images.githubusercontent.com/104542629/212601253-faf83263-b182-4cd7-8603-2bac583159f5.png">

### V. Conclusion
Based on the the correlation and hypothesis testing that I computed, my hypothesis is proven that the higher the numeric color value, the higher the temperature of a star. In the other word, the cooler the color, the hotter the star. However, it is important to note that we cannot use this linear regression equation to estimate the color of a star from its temperature because the R-square value (0.629), which represents how fit the data to the linear regression, is not good enough.  
