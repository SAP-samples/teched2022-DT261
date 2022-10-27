# Configure the Data Ingestion Application - Systems and Entities
In this step you will configure the source systems (S/4HANA Business System) as well as the entities to be replicated.
To start you will launch the Data Ingestion for Industry Cloud Solutions from your subaccount. <br>![](/exercises/ex2/images/EX2_1.jpg)


## Maintain Business System and Entities

1. Go to Tab 'System Information'. <br>![](/exercises/ex2/images/EX2_3.jpg)
2. Click 'Add'. <br>![](/exercises/ex2/images/EX2_2.jpg)
3. Create a Business System DT260_<your group number>. The Business System will be important in exercise 6. <br>![](/exercises/ex2/images/EX2_4.jpg)
4. Go to tab 'Data Ingestion'. <br>![](/exercises/ex2/images/EX2_5.jpg)
5. In the list activate the data ingestion by Data Object starting with Business Partner. <br>![](/exercises/ex2/images/EX2_6.jpg)
6. Assign the Business System from step 3 to the Business Partner. <br>![](/exercises/ex2/images/EX2_7.jpg)
7. The line with Business Partner should look like this: <br>![](/exercises/ex2/images/EX2_8.jpg)
8. Follow the same step for the Data Objects
| Data Object | 
|-------------|
|Country Codes|
|Currency Codes|
|Customer Order|
|Distribution Channel Codes|
|Language Codes|
|MerchandiseCategoryHierarchyNode|
|Plant|
|Product|
|Sales Organization|
|UnitOfMeasureCodes|
9. Select all Data Objects and click 'Activate'  <br>![](/exercises/ex2/images/EX2_9.jpg)
10. Confirm the activation <br>![](/exercises/ex2/images/EX2_10.jpg)


<br> 
### Go back to: [Configure the Data Replication Framework - Business System)(../ex6/README.md) or Continue to: [Run Replication for configured entities](../ex8/README.md)