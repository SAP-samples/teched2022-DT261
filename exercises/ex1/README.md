# Enable Data Ingestion for Industry Cloud Solutions.

In this exercise, you will enable Data Ingestion for Industry Cloud solutions (DI). It is used as integration point to SAP S/4HANA.

## Assign entitlements for Data Ingestion for Industry Cloud Solutions.

In order to enable DI you need to have entitlements assigned to your subaccount.

1. Add entitlement for DI to your Subaccount:

   - In your Subaccount, navigate to  ***Entitlements*** in the navigation menu and then click on ***Configure Entitlements***.
            
      ![](images/19.png)

   - Click on ***Add Service Plans***, search for ***`Data Ingestion`*** in the ***Search*** field. Select the entitlement from the list and check ***`application (Application)`*** and ***`default`*** plans from the ***Available Plans*** list. Click ***Add 2 Service Plans***.
      
      ![](images/20.png)
      ![](images/21.png)

   - Click ***Save*** on the Entitlements view.
      > **Note:** Do not forget or skip this step as the entitlements will not be saved, and you cannot continue with next exercises. 
      
      ![](images/22.png)

## Subscribe to Data Ingestion (DI) for Industry Cloud Solutions application.
In order to use the DI application you need to subscribe to it and assign required roles to your user.

1. Subscribe to DI application.

   - From the navigation menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](images/23.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`Data Ingestion for Industry Cloud Solutions`*** for *Service*,
     - ***`application`*** for *Plan*,
     - Click on ***Create***.

        ![](images/24.png)

    You should now have successfully ***Subscribed*** for Data Ingestion for Industry Cloud Solutions application.

      ![](images/25.png)

2. Create Role Collection, add Roles to it, and assign it to your user.
   - From the navigation menu, navigate to ***Security*** > ***Role Collections***. Click on ***`+`*** button in the top-right corner of the screen.

      ![](images/26.png)
  
   - Set Name for the Role Collection (e.g. ***`dt261-di`***) and click ***Create***.

      ![](images/27.png)
   
   - Click on the created Role Collection and click ***Edit*** from the detailed view.

      ![](images/28.png)

   - Click on the popup button in the ***Role Name*** field.

      ![](images/29.png)

   - In ***Select: Role*** view:
     - Select ***`All`*** for ***Role Name***
     - Select ***`di4cic!*****`*** for ***Application Identifier***, 
     - Check the checkboxes for ***`integration-settingsREAD`***, ***`integration-settingsWRITE`***, ***`UsersandRolePermissionREAD`***, and ***`UsersandRolePermissionWRITE`*** Roles,
     - Click ***Add*** button.

      ![](images/30.png)
   
   - Now add your user to the Role Collection by entering your user id in the ***ID*** field as shown on the screenshot. Click on your user from the value help. Then, click ***Save** button.

      > **Note:** You have to use the pre-created user for the on-site TechEd hands-on workshop. Please ask your instructors for more details.  

      ![](images/31.png)

## Enable access to Data Ingestion (DI) for Industry Cloud Solutions APIs.
In order to enable integration to SAP S/4HANA you need to create credentials for the DI APIs.

1. Create a service instance of DI.

   - From the navigation menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](images/32.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`Data Ingestion for Industry Cloud Solutions`*** for *Service*,
     - ***`default`*** for *Plan*,
     - ***`Other`*** for *Runtime Environment*,
     - Set name for the *Instance Name* - e.g. ***`di`***,
     - Click on ***Create***.

        ![](images/33.png)

2. Create service binding for created service instance.

   - In the ***Instance and Subscriptions*** view, find the DI instance created in the previous step, click on ***...*** (*Actions*) button and select ***Create Service Bindings***.

      ![](images/34.png)

   - In the *New Binging* pop-up:
       - set name for *Binding Name* - e.g. ***`di`***, 
       - click ***Create***.
         
         ![](images/35.png)

3. Download Credentials for the DI APIs:
   
   - In the ***Instance and Subscriptions*** view, find the DI instance created and click on  ***1 service binding*** link in *Credentials* column.
      
      ![](images/36.png)
   
   - In the ***Credentials*** view, click on ***Download*** and save the file locally.
      
      ![](images/37.png)
   
   > **Note:** These credentials will be needed in the next exercise in order to configure the integration from SAP S/4HANA to DI.

## Configure content of DI .
[//]: # (TO DO)

<br>After completing these steps you have enabled Data Ingestion for Industry Cloud Solutions and have access to its application and APIs.

## Next Steps

Now that you have enabled ata Ingestion for Industry Cloud Solutions, you need to configure it
<br>
### Go back to: [**Enable SAP Intelligent Returns Management solution**](../ex0/README.md) or Continue to: [**Configure Data Ingestion for Industry Cloud Solutions**](../ex2/README.md)