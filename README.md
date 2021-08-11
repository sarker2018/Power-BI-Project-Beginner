# Power-BI-Project
Beginner Level Project

## First Experince & data loading

* There are three views in the Power BI
  * Report View
  * Data View
  * Model View

* To get the data from storage, click on the get Data button & select your type of data
![grafik](https://user-images.githubusercontent.com/61450446/129101428-8a14d9be-82bf-42f1-9c43-cc0c02428078.png)
<br> <br>
* In the pop-up window we select either load or we can transform if needed. 
![grafik](https://user-images.githubusercontent.com/61450446/129101664-a738baed-9864-4545-beae-a96351fcc636.png)

<br> <br>
* Loading time depends on the type of data we are loading
* After loading the we data, we see a list of all the available column on the right side of the window
![grafik](https://user-images.githubusercontent.com/61450446/129102322-3f5b7e35-e519-4272-ba7d-3e5eab6166e0.png)
<br> <br>
* After clikcing the table logo on the left side of the window, we can see the data and thier columns. But the columns are not descriptive, although the original data had columns name or description
![grafik](https://user-images.githubusercontent.com/61450446/129102706-aa2af904-ec57-44d5-8293-16b2c4bdf52f.png)

## Fixing the column name problem
* Source of the dataset is UCI- University of California, Irvine Machine Learning Repository. The dataset is about Credit Cards defaults in Taiwan in the year 2005
* The right-most column is populated with US states names so that we can later use them to categorised by the states/or geolocations
![grafik](https://user-images.githubusercontent.com/61450446/129103452-7f9db918-c394-4920-bc83-1021f8722fdd.png)
* Now we go to Home --> Transform; Here we see the descriptive names of the columns in the raw dataset.
![grafik](https://user-images.githubusercontent.com/61450446/129104568-fd8c586d-6001-46c5-950b-2eb09939b5ed.png)
* Here, we click on Remove Rows --> Remove Top Row; there will be a pop-up window to specify the numbers of rows to be removed. In our case, we specify only one row and click ok button
![grafik](https://user-images.githubusercontent.com/61450446/129104957-28cf4906-b5a6-473f-a6ab-624de1151179.png)
* Again we go to Home --> Use first row as Hearders. Now we see that the first is shown as column name.
![grafik](https://user-images.githubusercontent.com/61450446/129105266-e5174316-1320-4030-9960-6dcf171de971.png)
* We can double click on any column name and can rename them as we want.
* To execute the changes, we need to press Home --> Close & Apply button on the left corner of the window
* If we look at the SEX column, we see that the sex are given in 1 & 2. We can transform them in Male, Female; If there are value other than 1 & 2 we assume that they are unknown. * We can transform them by clicking on the `Home --> Transform --> Data Type Whole Number --> Text` ; We are doing this step because by default Power BI assumes that the column values are integers, but we need to change them to text so that we can perform our changes. 
* Now we Click on the `Change values` button and specify 1 = Male and 2 = Female. 
![grafik](https://user-images.githubusercontent.com/61450446/129107136-29d8f702-c965-4b7c-9d18-6ee1174b5390.png)
* If we did any mistake in any step, we can go the last correct step by looking at the `Applied Steps` window on the right side of the P-BI interface. We can also delete some steps if we want.
![grafik](https://user-images.githubusercontent.com/61450446/129107748-ae233f10-2ae9-45ff-beff-226b76e45def.png)

* We also need to change the EDUCATION column values to some maning full and descriptive labels. Here, the EDUCATION are are give in 1,2,3 as we before in the SEX column.
* We can do a trick, we can create a new column called Education and perform logical operation such as `If, else, value`. This is helpful because we are now performing multiple operation with a single execution. 

* Here we set
```
   1 = Graduate
   2 = Under Graduate
   3 = High School Diploma
   else = Unknown/ or as described in the original description in the source data.
```
![grafik](https://user-images.githubusercontent.com/61450446/129109418-1413121c-31c6-49ed-b813-94146b12fcf4.png)
* We can see that the column's values are in descriptive names instead of 1,2 3,
![grafik](https://user-images.githubusercontent.com/61450446/129109555-93557558-f5e9-41eb-85e1-ee8d9491c0aa.png)

* Now we can remove the original EDUCATION column by right click --> remove if we want to do.
* We perform the same operation on the MARRIAGE column, 

```
   1 = Married
   2 = Un Married
   else = Unknown
```
![grafik](https://user-images.githubusercontent.com/61450446/129110125-7e0fa85d-ff66-4c1b-888e-e77098b6a2fd.png)


## Visualisation & Report
* Click on the report view on the top-left of the three view options
![grafik](https://user-images.githubusercontent.com/61450446/129111633-2f7df2fa-8f89-484a-9c57-8839a5b21065.png)

* Now we want to see how the distribution of `DEFAUL` column look like respect to the age group
```
We just simply select the DEFAULT column
Then Drag the AGE colum to the Axis button (in the next-left)
```
![grafik](https://user-images.githubusercontent.com/61450446/129114390-71d04ed4-a3f4-4195-acd2-b0be85026da6.png)

* If you want to zoom a specific plot, just click on the focus mode
![grafik](https://user-images.githubusercontent.com/61450446/129114803-54e1e7d0-203f-4b0d-a5b9-71adef9d16ab.png)
* We can create different types of plots by clicking on the visualisation icons on the right side of the interface. Again, choice of plot depends on the specific problem and target report, and the domain knowledge as well.
![grafik](https://user-images.githubusercontent.com/61450446/129115098-a7d05767-74a9-499b-82f5-5c0f0d0ac8fe.png)
## DEFAULT by SEX; Adding a Legend to the plot; 
* Just drag the `SEX` column to the legend tab to set AGE as legend
![grafik](https://user-images.githubusercontent.com/61450446/129115475-85a248b2-a1fe-48a9-8ae7-ed920c231328.png)
* We can remove, export usw from the three dot `...` plot menu
![grafik](https://user-images.githubusercontent.com/61450446/129115631-a4cb5882-1c47-42e8-bce6-004ed8b24799.png)

## DEFAULT by EDUCATION_, SEX as legend
```
Select the DEFAULT check box like before
Drag the EDUCATION_ to the axis tab
Drag the SEX to the legend tab
```
### DEFAULT by AGE, SEX
![grafik](https://user-images.githubusercontent.com/61450446/129117029-aece827c-5c42-4ace-b0a8-b284d5215443.png)
```
Select the DEFAULT check box like before
Drag the AGE to the axis tab
Drag the SEX to the legend tab
```
### DEFAULT vs SEX with custom color
~~~
Select DEFAULT to create a new plot
Drag the SEX column on to the Axis tab

Roller button --> Data Colors --> Show All --> Push Off to On --> Select the color from the list
~~~
![grafik](https://user-images.githubusercontent.com/61450446/129117941-facb7e7c-9590-48b1-a556-3dbef1cb05c0.png)
