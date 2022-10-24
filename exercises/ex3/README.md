# Enable the SAP Order and Delivery Scheduling solution

In this exercise, you will enable and configure the usage of SAP Order and Delivery Scheduling Industry Cloud solution.

## Assign entitlements for the SAP Order and Delivery Scheduling (ODS) Industry Cloud solution

In order to enable ODS you need to have entitlements assigned to your subaccount.

1. Add entitlement for ODS to your Subaccount:

   - In your Subaccount, navigate to  ***Entitlements*** in the navigation menu and then click on ***Configure Entitlements***.
            
      ![](/exercises/ex3/images/38.png)

   - Click on ***Add Service Plans***, search for ***`SAP Order and Delivery Scheduling`*** in the ***Search*** field. Select the entitlement from the list and check ***`default`*** and ***`application (Application)`*** plans from the ***Available Plans*** list. 
      
      ![](/exercises/ex3/images/39.png)
      ![](/exercises/ex3/images/40.png)
   
   - Now, search for ***`Launchpad Service`*** in the ***Search*** field. Select the entitlement from the list and check ***`standard (Application)`*** plan from the ***Available Plans*** list. Click ***Add 3 Service Plans***. 
      
      ![](/exercises/ex3/images/40-1.png) 

   - Click ***Save*** on the Entitlements view.
      > **Note:** Do not forget or skip this step as the entitlements will not be saved, and you cannot continue with next exercises. 
      
      ![](/exercises/ex3/images/41.png)

## Enable SAP Order and Delivery Scheduling and configure access to it

In order to be able to use the ODS capabilities, you need to enable the ODS application and APIs.

1. Subscribe to the ODS application.

   - From the navigation menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](/exercises/ex3/images/42.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`SAP Order and Delivery Scheduling`*** for *Service*,
     - ***`application`*** for *Plan*,
     - Click on ***Create***.

        ![](/exercises/ex3/images/43.png)

    > You should now have successfully ***Subscribed*** to SAP Order and Delivery Scheduling application.

      ![](/exercises/ex3/images/44.png)

2. In the ***Instances and Subscriptions*** page, click on ***Create***.

      ![](/exercises/ex3/images/45.png)

   - - In the ***New Instance or Subscription*** pop-up, select:
     - ***`SAP Order and Delivery Scheduling`*** for *Service*,
     - ***`default`*** for *Plan*,
     - ***`Other`*** for *Runtime Environment*,
     - Set name for the *Instance Name* - e.g. ***`ods`***,
     - Click on ***Create***.

        ![](/exercises/ex3/images/46.png)

3. Create service binding for created service instance.

   - In the ***Instance and Subscriptions*** view, find the ***ods*** instance created in the previous step, click on ***...*** (*Actions*) button and select ***Create Service Bindings***.

      ![](/exercises/ex3/images/47.png)

   - In the *New Binding* pop-up:
       - Set name for *Binding Name* - e.g. ***`ods`***, 
       - Click ***Create***.
         
         ![](/exercises/ex3/images/48.png)

4. Download Credentials for the ODS APIs:
   
   - In the ***Instance adn Subscriptions*** view, find the ***ods*** instance created and click on the ***1 service binding*** link in *Credentials* column.
      
      ![](/exercises/ex3/images/49.png)
   
   - In the ***Credentials*** view, click on ***Download*** and save the file locally.
      
      ![](/exercises/ex3/images/50.png)
   
   > **Note:** These credentials will be needed in the next steps in order to configure the integration in Launchpad Service.

5. Create Role Collection, add Roles to it, and assign it to your user.
   - From the navigation menu, navigate to ***Security*** > ***Role Collections***. Click on ***`+`*** button in the top-right corner of the screen.

      ![](/exercises/ex3/images/67.png)
  
   - Set Name for the Role Collection (e.g. ***`dt261-ods`***) and click ***Create***.

      ![](/exercises/ex3/images/68.png)
   
   - Click on the created Role Collection and click ***Edit*** from the detailed view.

      ![](/exercises/ex3/images/69.png)

   - Click on the popup button in the ***Role Name*** field.

      ![](/exercises/ex3/images/70.png)

   - In ***Select: Role*** view:
     - Select ***`order-delivery-scheduling!b7728`*** for ***Application Identifier***, 
     - For this exercise, check the checkbox in front of the *Role Name* header to select all ODS Roles, 
     - Click ***Add*** button.

      ![](/exercises/ex3/images/71.png)
   
   - Now add your user to the Role Collection by entering your user id in the ***ID*** field as shown on the screenshot. Click on your user from the value help. Then, click the ***Save*** button.

      > **Note:** You have to use the pre-created user for the on-site TechEd hands-on workshop. Please ask your instructors for more details.  

      ![](/exercises/ex3/images/72.png)

## Enable SAP BTP Launchpad Service and configure the ODS application in it

In order to be able to use the ODS capabilities, you need to configure it in the Launchpad Service.

1. Subscribe to the Launchpad Service application.

   - If not already there, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](/exercises/ex3/images/51.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`Launchpad Service`*** for *Service*,
     - ***`standard`*** for *Plan*,
     - Click on ***Create***.

        ![](/exercises/ex3/images/52.png)

    > You should now have successfully ***Subscribed*** to the Launchpad Service application.

      ![](/exercises/ex3/images/53.png)

2. Assign the ***Launchpad_Admin*** Role Collection to your user.

   - From the navigation menu, navigate to ***Security*** > ***Role Collections***. Select the predefined ***Launchpad_Admin*** Role Collection and click on the ***Edit*** button in the top-right corner of the screen.

      ![](/exercises/ex3/images/54.png)
   
   - Add your user to the Role Collection by entering your user id in the ***ID*** field as shown on the screenshot. Click on your user from the value help. Then, click the ***Save*** button.

      > **Note:** You have to use the pre-created user for the on-site TechEd hands-on workshop. Please ask your instructors for more details.  

      ![](/exercises/ex3/images/55.png)

3. Create a destination for the Launchpad Service.

   - From the navigation menu, navigate to ***Connectivity*** > ***Destinations*** and click on ***New Destination***.

      ![](/exercises/ex3/images/56.png)

   - In the ***Destination Configuration*** view, set:
     - ***`flp-content-provider-destination`*** for *Name*,
     - ***`HTTP`*** for *Type*,
     - ***`https://app.orderdeliveryscheduling.cloud.sap/api/flpContent`*** for *URL*,
     - ***`OAuthClientCredentials`*** for *Authentication*,
[//]: # (Is this intended to be cliend?)
     - ***`<cliend id value from the credentials created for ODS service instance>`*** for *Client ID*. You have downloaded the ODS service instance credentials in **Step 4.** from  **Enable SAP Order and Delivery Scheduling and configure access to it** above,
     - ***`<cliend secret value from the credentials created for ODS service instance>`*** for *Client Secret*. You have downloaded the ODS service instance credentials in **Step 4.** from  **Enable SAP Order and Delivery Scheduling and configure access to it** above,
     - ***`Dedicated`*** for *Token Service URL Type*,
     - ***`url value from the credentials created for ODS service instance>`*** for *Token Service URL*. You have downloaded the ODS service instance credentials in **Step 4.** from  **Enable SAP Order and Delivery Scheduling and configure access to it** above,
     - Click on ***Save***.

        ![](/exercises/ex3/images/57.png)

4. Configure Content Provider in Launchpad Service.
   
   - Open Launchpad Service by navigating to ***Services*** > ***Instances and Subscriptions*** and clicking on ***Launchpad Service*** hyperlink.
      
        ![](/exercises/ex3/images/58.png)

   -  In the newly opened Launchpad Service browser window, navigate to ***Channel Manager*** and click ***+ New*** button.

        ![](/exercises/ex3/images/59.png)

   - In the ***New Content Provider*** pop-up, set:
     - ***`ODS Apps`*** for *Tittle*,
     - ***`ODS_Apps`*** is automatically filled for *ID*,
     - ***`flp-content-provider-destination`*** for *Design-Time Destination*,
     - ***`flp-content-provider-destination`*** for *Runtime Destination*,
     - ***`Use default runtime destination`*** for *Runtime Destination for Dynamic Data*,
     - click ***Save***.

        ![](/exercises/ex3/images/60.png)

      >**Note:** Make sure that you get successful status ***Created***.
      
        ![](/exercises/ex3/images/61.png)

5. Create Site and assign relevant roles for the Launchpad.
   
   - Navigate to ***Site Directory*** and click on ***+ Create New Site***. Then set ***`ODS`*** for *Site Name* and click ***Create*.

      ![](/exercises/ex3/images/62.png)
      ![](/exercises/ex3/images/63.png)

   - In the Settings view of the site you just created, click on the **<** button on the top-left corner to get back to the *Site Directory*. 

      ![](/exercises/ex3/images/64.png)

   - Set the Site as default one by clicking on ***...***, then click ***Set as Default***, and then confirm by clicking ***OK***.
    
      ![](/exercises/ex3/images/65.png)
      ![](/exercises/ex3/images/66.png)

<!-- To complete the steps for role assignments for the site>


<br>After completing these steps you will have enabled SAP Intelligent Returns Management solution and have access to its application.

## Summary

Now that you have enabled SAP Intelligent Returns Management, you need to enable data integration to SAP S/4HANA via Data Ingestion for Industry Cloud.

<br>

### Go back to: [**Overview**](../../README.md) or Continue to: [**Enable data integration via Data Ingestion for Industry Cloud**](../ex1/README.md)
--> 