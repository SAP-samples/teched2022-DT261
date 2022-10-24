# Enable Data Ingestion for Industry Cloud Solutions.

In this exercise, you will enable Data Ingestion for Industry Cloud solutions (DI). It is used as integration point to SAP S/4HANA.

## Assign entitlements for Data Ingestion for Industry Cloud Solutions.

In order to enable DI you need to have entitlements assigned to your subaccount.

1. Add entitlement for DI to your Subaccount:

   - In your Subaccount, navigate to  ***Entitlements*** in the Navigation Menu and then click on ***Configure Entitlements***.
            
      ![](/exercises/ex1/images/19.png)

   - Click on ***Add Service Plans***, search for ***`Data Ingestion`*** in the ***Search*** field. Select the entitlement from the list and check ***`application (Application)`*** and ***`default`*** plans from the ***Available Plans*** list. Click ***Add 2 Service Plans***.
      
      ![](/exercises/ex1/images/20.png)
      ![](/exercises/ex1/images/21.png)

   - Click ***Save*** on the Entitlements view.
      > **Note:** Do not forget or skip this step as the entilements will not be saved and you cannot continue with next exercises. 
      
      ![](/exercises/ex1/images/22.png)

## Subscribe for Data Ingestion (DI) for Industry Cloud Solutions application.
In order to use the DI application you need to subscribe for it and assign required roles to your user.

1. Subscribe for DI application.

   - From the Navigation Menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](/exercises/ex1/images/23.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`Data Ingestion for Industry Cloud Solutions`*** for *Service*,
     - ***`application`*** for *Plan*,
     - Click on ***Create***.

        ![](/exercises/ex1/images/24.png)

    You should now have successfully ***Subscribed*** for Data Ingestion for Industry Cloud Solutions application.

      ![](/exercises/ex1/images/25.png)

2. Create Role Collection, add Roles to it, and asign it to your user.
   - From Navigation Menu, navigate to ***Security*** > ***Role Collections***. Click on ***`+`*** button in the top-right corner of the screen.

      ![](/exercises/ex1/images/26.png)
  
   - Set Name for the Role Collection (f.e. ***`dt261-di`***) and click ***Create***.

      ![](/exercises/ex1/images/27.png)
   
   - Click on the created Role Collection and click ***Edit*** from the detailed view.

      ![](/exercises/ex1/images/28.png)

   - Click on the popup button in the ***Role Name*** field.

      ![](/exercises/ex1/images/29.png)

   - In ***Select: Rome*** view:
     - Select ***`di4cic!b9957`*** for ***Application Identifier***, 
     - Check the checkboxes for ***`integration-settingsREAD`***, ***`integration-settingsWRITE`***, ***`UsersandRolePermissionREAD`***, and ***`UsersandRolePermissionWRITE`*** Roles,
     - Click ***Add*** button.

      ![](/exercises/ex1/images/30.png)
   
   - Now add your user to the Role Collection by entiring your user id in the ***ID*** field as shown on the screenshot. Click on your user from the value help. Then, click ***Save** button.

      > **Note:** You have to use the pre-created user for the on-site TechEd hands-on workshop. Please ask your instructors for more details.  

      ![](/exercises/ex1/images/31.png)

## Enable access to Data Ingestion (DI) for Industry Cloud Solutions APIs.
In order to enable integration to SAP S/4HANA you need to create credentials for the DI APIs.

1. Create service instance of DI.

   - From the Navigation Menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](/exercises/ex1/images/32.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`Data Ingestion for Industry Cloud Solutions`*** for *Service*,
     - ***`default`*** for *Plan*,
     - ***`Other`*** for *Runtime Environment*,
     - Set name for the *Instance Name* - f.e. ***`di`***,
     - Click on ***Create***.

        ![](/exercises/ex1/images/33.png)

2. Create service binding for created service instance.

   - In the ***Instance adn Subscriptions*** view, find the DI instance created in the previous step, click on ***...*** (*Actions*) button and select ***Create Service Bindings***.

      ![](/exercises/ex1/images/34.png)

   - In the *New Binging* pop-up:
       - set name for *Binding Name* - f.e. ***`di`***, 
       - click ***Create***.
         
         ![](/exercises/ex1/images/35.png)

3. Download Credentials for the DI APIs:
   
   - In the ***Instance adn Subscriptions*** view, find the DI instance created and click on  ***1 service binding*** link in *Credentials* column.
      
      ![](/exercises/ex1/images/36.png)
   
   - In the ***Credentials*** view, click on  ***Download*** and save the file locally.
      
      ![](/exercises/ex1/images/37.png)
   
   > **Note:** These credentials will be needed in the next exercise in order to configure the integration from SAP S/4HANA to DI.

<!-->
## Configure conent of DI .
TO DO
-->

<br>After completing these steps you will have enabled Data Ingestion for Industry Cloud Solutions and have access to its application and APIs.

## Summary

Now that you have enabled ata Ingestion for Industry Cloud Solutions, you need to integrate it to SAP S/4HANA.
<br>
### Go back to: [Enable SAP Intelligent Returns Management solution](../ex0/README.md) or Continue to: [Intgerate Data Ingestion for Industry Cloud with S/4HANA on-prem system](exercises/ex2/README.md)