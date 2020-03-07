# Pymaceuticals Project

## Background

In this study, 250 mice identified with SCC tumor growth were treated through a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. 

### Purposes of this project
Compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens 

### Methods

Used functions in pandas dataframe to generate summary statistics report
Functions:-
merge
    combined_df = pd.merge(df1,df2, on='index')

creat new dataframe
    new_df = df[['column1','column2']]

groupby using mean, max
    df = df.groupby(["column_name"]).mean()

rename columns
    df.rename(columns={"A": "a", "B": "c"})

show dataframe
    df.head()

show dataframe index
    df.columns

show number of rows in dataframe
    df.count()

Used Pandas to plot bar chart and pie chart

 Bar Chart
     df.plot(kind='bar',facecolor='blue')
   
  Pie Chart
     df.plot(kind='pie',autopct='%1.1f%%')

Used Matplotlib to plot bar chart and pie chart

  Bar Chart
    x = df['x axis column'].value_counts()
    x_axis = np.arange(1,len(x)+1,1)
    y_axis = x
    plt.bar(x_axis,y_axis, color='b',align='center')
    x_header = combined_data['Drug Regimen']
    x_axis_header = x_header.unique()
    tick_locations = [value for value in x_axis]
    plt.xticks(tick_locations, x_axis_header, rotation = "vertical")

  Pie Chart
     plt.pie(mouse_gender_df,labels=mouse_gender,autopct='%1.1f%%')
     
Used Matplotlib to show Quartiles, outliers and boxplots

  Box Chart
    data = df1,df2,df3,df4
    fig1, ax1 = plt.subplots()
    ax1.boxplot(data)
    plt.ylabel("Final Tumor Volume (mm3)")
    plt.xticks([1, 2, 3,4], ['df1','df2','df3','df4'])
    plt.show()

  Line Chart
    lines = df.plot(kind='line',x='x_axis',y='y_axis', color='b')
  
  Scatter Chart
    scatter = plt.scatter(x,y)

Used correlation function to find correlation coefficient and linear regression model

   correlation = st.pearsonr(df['x axis)'],df[y axis'])
    x_values = df['x axis']
    y_values = df['y axis']
    (slope, intercept, rvalue, pvalue, stderr) = linregress(x_values, y_values)
    regress_values = x_values * slope + intercept
    line_eq = "y = " + str(round(slope,2)) + "x + " + str(round(intercept,2))
    plt.scatter(x_values,y_values)
    plt.plot(x_values,regress_values,"r-")
    plt.annotate(line_eq,(6,10),fontsize=15,color="red")
    plt.xlabel('x axis')
    plt.ylabel('y axis')
    plt.show()


