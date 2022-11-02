# Configure the Data Ingestion Application - Systems and Entities
In this step you will configure the source systems (S/4HANA Business System) as well as the entities to be replicated.
To start you will launch the Data Ingestion for Industry Cloud Solutions from your subaccount. <br>![](images/EX2_1.jpg)


## Maintain Business System and Entities

1. Go to Tab 'System Information'. <br>![](images/EX2_3.jpg)
2. Click 'Add'. <br>![](images/EX2_2.jpg)
3. Create a Business System DT260_<your group number>. The Business System will be important in exercise 6. <br>![](images/EX2_4.jpg)
4. Go to tab 'Data Ingestion'. <br>![](images/EX2_5.jpg)
5. In the list activate the data ingestion by Data Object starting with Business Partner. <br>![](images/EX2_6.jpg)
6. Assign the Business System from step 3 to the Business Partner. <br>![](images/EX2_7.jpg)
7. The line with Business Partner should look like this: <br>![](images/EX2_8.jpg)
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
9. Select all Data Objects and click 'Activate'  <br>![](images/EX2_9.jpg)
10. Confirm the activation <br>![](images/EX2_10.jpg)

## Next Steps:
Now that you have configured Data Ingestion for Industry Cloud Solutions, you need to integrate it to SAP S/4HANA.
<br> 
### Go back to: [**Enable Data Ingestion for Industry Cloud Solutions**](../ex1/README.md) or Continue to: [**Create an OAuth client**](../ex4/README.md)