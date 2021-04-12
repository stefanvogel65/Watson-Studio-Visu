# Visulization in Watson Studio, Tutorial

This is a simple intro into Watson Studio on IBM Cloud and a guide to get started with visulizing data with no code using Cognos Dashboard embedded.

## Step 1: Login and create Watson Studio Service

When ready, start Watson Studio:

<img src="https://user-images.githubusercontent.com/35991100/114362811-0d82f880-9b78-11eb-9f64-3f84e3924bbc.png" alt="drawing" width="75%"/>

## Step 2: Getting started in Watson Studio

Start Watson Studio and create a new project.

<img src="https://user-images.githubusercontent.com/35991100/114353808-be37ca80-9b6d-11eb-88e0-ffc655ff7de9.png" alt="drawing" width="75%"/>

Select Create an empty project and give it a name.

Under Settings, add a Dashboard as a new service.

<img src="https://user-images.githubusercontent.com/35991100/114363214-78ccca80-9b78-11eb-8c20-b47c94c28bfe.png" alt="drawing" width="75%"/>

If you did not yet created a Cognos Dashboard Embedded service, create one now. If it exists, associate it with your project.

## Step 3: Upload data set

Use the following link to download the Customer Churn data from Kaggle to your local system:

[customer-churn-kaggle.csv](https://s3.us.cloud-object-storage.appdomain.cloud/developer/default/tutorials/watson-studio-data-visualization-preparation-transformation/static/customer-churn-kaggle.csv)

Upload the data set as a new asset:

<img src="https://user-images.githubusercontent.com/35991100/114364392-a2d2bc80-9b79-11eb-98c3-5f2c29aa6785.png" alt="drawing" width="75%"/>

## Step 4: Basic visualization in Watson Studio

To view the data set, locate the data asset and then click the name of the data set to open it.

Watson Studio shows you a preview of the data in the Preview tab.

<img src="https://user-images.githubusercontent.com/35991100/114369679-ebd93f80-9b7e-11eb-9047-102398f1e097.png" alt="drawing" width="75%"/>

Alternatively, the Profile tab gives you profiling information that shows the distribution of the values. For numerical features, it also shows the maximum, minimum, mean, and standard deviation for the feature.

Create a profile for the first time:

<img src="https://user-images.githubusercontent.com/35991100/114369856-19be8400-9b7f-11eb-9fe4-71fc8d91c758.png" alt="drawing" width="75%"/>

After a while, the profile is displayed:

<img src="https://user-images.githubusercontent.com/35991100/114426140-0b418e00-9bba-11eb-876c-bf6e01b4a449.png" alt="drawing" width="75%"/>

Notice that although the numerical columns are identified to be of type varchar, the profiler is smart enough to recognize these to be numerical columns, convert them implicitly, and compute the mean and the standard deviation.

Notice that the churn parameter does not provide a balanced distribution of churn and no-churn observations. This might mean that you should adopt cross-validation strategies during the model building and evaluation phase.

## Step 5: More visualizations using the Cognos Dashboard service

You can look further into the data set by creating a dashboard with associated visualizations. This basically requires three steps: creating an empty dashboard, adding a data source to be used for visualizations, and adding appropriate visualizations to the dashboard.

To create the dashboard:

Click Add to project + and then select Dashboard to create a new dashboard.

<img src="https://user-images.githubusercontent.com/35991100/114371432-c51c0880-9b80-11eb-867a-b0a8299e56fc.png" alt="drawing" width="75%"/>

Click OK to create an empty freeform dashboard with a single Tab.

<img src="https://user-images.githubusercontent.com/35991100/114372125-7f137480-9b81-11eb-80c1-190a5eeaaa57.png" alt="drawing" width="75%"/>

Add the churn data as a data source. You can preview the data at the bottom of the tab panel:

<img src="https://user-images.githubusercontent.com/35991100/114374498-fc3fe900-9b83-11eb-9589-e5a693053dd6.png" alt="drawing" width="75%"/>

Notice that you can view and change the properties of the columns. Simply click the 3 dots to the right of the column name, then select Properties in the pop-up menu. This displays a window as shown above, and allows you to alter the default setting for Usage (Identifier, Attribute, and Measure) and Aggregate Function (Count, Count Distinct, Maximum, and Minimum). For now, you should be fine with the default settings.

To create a visualization that shows the distribution of churns and no-churns as a pie chart, select the Visualizations icon in the toolbar to the left.

<img src="https://user-images.githubusercontent.com/35991100/114375145-acaded00-9b84-11eb-80e7-72727d1e7956.png" alt="drawing" width="75%"/>

Select a Pie chart and drop it on the canvas. The Fields view opens to the right.

Select the Sources icon in the toolbar to the left (located above the Visualizations icon). Drag the churn column onto the Segments property of the pie chart. Drag the churn column onto the Size property of the pie chart.

<img src="https://user-images.githubusercontent.com/35991100/114375823-5a210080-9b85-11eb-9a3f-ac55eb14f8be.png" alt="drawing" width="75%"/>

Click the Expand button on the pie chart to maximaize it.

<img src="https://user-images.githubusercontent.com/35991100/114377021-7cffe480-9b86-11eb-9edb-650cfd979df4.png" alt="drawing" width="75%"/>

Open the Properties view and select to display a titel under the General tab. Enter a meaningful title.

<img src="https://user-images.githubusercontent.com/35991100/114377375-e1bb3f00-9b86-11eb-928b-39def51cce10.png" alt="drawing" width="75%"/>


Follow similar steps and create two more visualizations:

* A Stacked column chart showing State (visualization field Bars) and Churn (visualization fields Length and Color) on the X and Y axis, respectively
* A Pie chart showing the distribution of the International Plan (visualization fields Segments and Size)

This should result in a dashboard similar to the following image. Notice that you can move visualizations on the dashboard using the Move widget command located on the top of each visualization.

<img src="https://user-images.githubusercontent.com/35991100/114378815-5e9ae880-9b88-11eb-9f65-4388d7364ccb.png" alt="drawing" width="75%"/>

The dashboards are dynamic by nature and support exploration of the data using filters. In the visualization that shows International Plan, click the slice associated with the value "yes". This creates a filter that will apply to all other (connected) visualizations on the current dashboard.

<img src="https://user-images.githubusercontent.com/35991100/114426566-7e4b0480-9bba-11eb-9e75-b45a4d70f1f1.png" alt="drawing" width="75%"/>

[//]: # (Use this to insert images: <img src="" alt="drawing" width="75%"/>)




