# Programming-Assignment-4

Author: Arabelle Y. Villarin

Section: 2ECE-D

Date Submitted: September 19, 2024

------------------------------------------------------------------------------------------------------------------------------

#### Description

This Jupyter Notebook focuses on Experiment 4, which deals with the essential processes of data wrangling and data visualization. The notebook includes examples related to real-world data manipulation and visualization tasks, specifically involving problems related to the ECE board exam.

##### Contents

Data Wrangling: Includes importing and manipulating datasets using the pandas library.

Data Visualization: It demonstrates how to create visual representations of data using common Python libraries.

ECE Board Exam Problem: The notebook contains a specific problem set related to the ECE board exams.

To run this notebook, the following Python libraries are required:

- pandas

- matplotlib

Before anything else, I used
````
import pandas as pd
````
to load the pandas functions.

#### Problem 1 (A)

I extracted the excel file to be used by inputting the code:
````
board = pd.read_excel('board2.xlsx')
board
````
To specifically show the results, I used .loc to show only the required information from the students which includes Name, GEAS, and Electronics where track is constant as Instrumentation and hometown Luzon.

![Screen Shot 2024-09-19 at 9 32 29 PM](https://github.com/user-attachments/assets/0650176e-ecc3-4b19-88dc-7296f82cd380)

#### Problem 1 (B)
This problem is similar to A. but it focuses on getting the average of the students. I used the function .mean() to get the average of Math, Electronics, GEAS, and Communication for each student:
````
average = ['Math', 'Electronics', 'GEAS', 'Communication']

board['average'] = board[average].mean(axis=1)
board
````

To specifically show the results, I used .loc to show only the required information from the students which includes Name, Track, Electronics, Average where hometown is constant as Mindanao and gender Female.

![Screen Shot 2024-09-19 at 9 37 22 PM](https://github.com/user-attachments/assets/72e1197c-be56-4171-975d-5d905c99a030)

#### Problem 2

This section aims to visualize the hometown, gender, track, and average board exam scores of the students through a bar chart.

I used plt.figure to input the plot size of the bar graph

````
fig1 = plt.figure(figsize=(20, 4))
````

The plot.bar, on the other hand, indicates which label goes in the Y- and X-axis
````
plt.bar(board['Name'], board['average'], color = colors)
````

Lastly, the plot.title indicates the title of the bar graph itself.

-------------------------------------------------------------------------------------------------------------------------------

## Conclusion

In this activity, we practiced data wrangling and visualization to analyze student performance in the ECE board exams. By organizing the data and creating visual representations, we were able to understand more about the topic and have meaningful insights. This exercise demonstrated the importance of using data to better understand and interpret real-world information.















