## Understand how to read and write a CSV File in Python with pandas! 
 
##What is a CSV file? 
A CSV file(Comma Separated Values File) is a type of plain text file that uses specific structuring to organize your data. 

They can typically look like this: 

column 1, column 2, column 3
R1 data, R1 data, R1 data
R2 data, R2 data, R2 data 

You can see how each data point is being sperated by a ",". 

#How can we use python and pandas to read these files? 
 Well we can use a nice tool call pandas that makes opening, reading, and analyzing a csv file easy with just three lines of code. 

```
import pandas
df =pandas.read_csv('fileName.csv')
print(df)
```
Yep using pandas can really make it that easy! 

# Now lets see how to Write CSv files with pandas

You may think writing a DataFrame to a CSV file would be much harder, but it turns out it is just as easy as reading one! 

Below lets just wirte a quick one that shows how we could write to a new CSV file with new column names for a simple student file. 

```
import pandas
df = pandas.read_csv('student.csv',
    index_col='Student',
    parse_dates=['Grade Level'],
    header =0,
    names = ["Student', "Grade Level', 'Major'])
df.to_csv('student_modified.csv')
```
Hopefully looking at both examples you can see how we are using pandas and DataFrames to make reading and writing CSV files easy! To learn more about pandas and DataFrame [vist](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)

#Conclusion 
If you can take this short dicription of what reading and writing CSV files can look like with python using pandas and run with it by expandin on the topic with outside articles and challenges than you will never be caught on the backfoot when it comes to the need of dealing with importing data. 
