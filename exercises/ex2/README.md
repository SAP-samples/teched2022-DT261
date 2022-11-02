# Configure the Data Ingestion Application - Systems and Entities

In this exercise, you will configure the source systems (S/4HANA Business System) as well as the entities to be replicated.

## Maintain Business System and Entities

To start you will launch the Data Ingestion for Industry Cloud Solutions from your Subaccount. 

![](images/EX2_1.jpg)

1. Maintain a new Business System:

   - Go to the ***System Information*** tab.

      ![](images/EX2_3.jpg)

   - Click the ***Add*** button.

       ![](images/EX2_2.jpg)

[//]: # (TODO: Replace screenshot with DT261)
   - Set the *System Name* (e.g. ***`DT260_<your group number>`***) and click the ***Add*** button.

       ![](images/EX2_4.jpg)

       > **Note:** The Business System will be important in [Exercise 6](../ex6/README.md).

2. Assign the Business System to the Business Partner Data Object:

   - Go to ***Data Ingestion*** tab. 

       ![](images/EX2_5.jpg)

   - Select the ***Edit*** (*Pencil*) button of the Business Partner Data Object. 

       ![](images/EX2_6.jpg)

   - In the *Edit* dialog, select the Business System from before as ***Source System ID***. 
   - In the ***Edit*** dialog:
     - Select the Business System from before as ***Source System ID***,
     - Click the ***Save*** button.

      ![](images/EX2_7.jpg)

   - The line with Business Partner should look like this: 

       ![](images/EX2_8.jpg)

3. Assign the Business System to other Data Objects:

    - Repeat step 2 and assign the Business System to the other data objects listed below:
      - Country Codes
      - Currency Codes
      - Customer Order
      - Distribution Channel Codes
      - Language Codes
      - MerchandiseCategoryHierarchyNode
      - Plant
      - Product
      - Sales Organization
      - UnitOfMeasureCodes

4. Activate all Data Objects:

    - In the ***Data Objects*** tab:
      - Check the checkbox to select all Data Objects,
      - Click the ***Activate*** button,
	
      ![](images/EX2_9.jpg)
       
      - Confirm the activation by clicking the ***Activate*** button.
      
      ![](images/EX2_10.jpg)

## Next Steps

Now that you have configured Data Ingestion for Industry Cloud Solutions, you need to integrate it to SAP S/4HANA.

### Go back to: [**Enable Data Ingestion for Industry Cloud Solutions**](../ex1/README.md) or Continue to: [**Create an OAuth client**](../ex4/README.md)