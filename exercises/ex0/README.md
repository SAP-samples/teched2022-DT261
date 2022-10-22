# Enable SAP Intelligent Returns Management solution

In this exercise, you will enable and configure usage of SAP Intelligent Returns Management Industry Cloud solution.

## Login to SAP Business Technology Plafrom (BTP) Global Account

1. Login to SAP BTP cockpit:
   - Open [https://cockpit.**us21**.hana.ondemand.com/cockpit/](https://cockpit.us21.hana.ondemand.com/cockpit/#).

      > **Note:** You can exchange the ***us21*** from the URL with another region in case you are not based in USA.

   - Provide your username and password and press ***Log On***.
      
      > **Note:** During your TechEd hands-on, you will be provided wit predefined user and password.

      ![](/exercises/ex0/images/1.png)

2. Select desired Global Account (if you have multiple ones) and click on ***Continue***.

    ![](/exercises/ex0/images/2.png) <br>

## Create your Subaccount and assign entitlements for SAP Intelligent Returns Mananegement (IRM)

In order to enable SAP IRM you need to create a subaccount in one of the support regions and assigned IRM entitlements to it.

1. Create a Subaccount in the desired region:
    > **Note:** You will be provided with a pre-created Subaccount for the on-site TechEd hands-on workshop, so you do not have to execute this step. Please ask your instructors for more details.

    - Click on **_Create_** > ***Subaccount***.

      ![](/exercises/ex0/images/3.png)
   
    - Set values for:
      - *Display Name*. Example: ***`dt261`***,
      - *Subdomain*. Example: ***`dt261`***, 
      - *Region*. Example: ***`Microsoft Azure US East (VA) cf-us21`***, 

        > **Note:** You need to choose a reagion where SAP IRM is available. For more information on where SAP IRM is available, please visit the [official documentation](https://help.sap.com/docs/returns?locale=en-US).
     
      - and click ***Create***.

        ![](/exercises/ex0/images/4.png)


2. Add entitlement for SAP IRM to your Subaccount:

   - Click on the Subaccount you created from previous step and navigate to ***Entitlements*** in the Navigation Menu and then click on ***Configure Entitlements***.
      > **Note:** You have to select the pre-created Subaccount for the on-site TechEd hands-on workshop. Please ask your instructors for more details.
      
      ![](/exercises/ex0/images/5.png)
      ![](/exercises/ex0/images/6.png)
      ![](/exercises/ex0/images/7.png)

   - Click on ***Add Service Plans***, search for ***`SAP Intelligent Returns Management`*** in the ***Search*** field. Select the entitlement from the list and check ***`data-ingestion`*** and ***`application (Application)`*** plans from the ***Available Plans*** list. Click ***Add 2 Service Plans***.
      
      ![](/exercises/ex0/images/8.png)
      ![](/exercises/ex0/images/9.png)

   - Click ***Save*** on the Entitlements view.
      > **Note:** Do not forget or skip this step as the entilements will not be saved and you cannot continue with next exercises. 
      
      ![](/exercises/ex0/images/10.png)

## Subscribe for SAP Intelligent Returns Mananegement (IRM) and conficgure access to it

In order to be able to use the SAP IRM capabilities, you need to ebable the IRM application and configure the access to it.

1. Subscribe for SAP IRM application.

   - From the Navigation Menu, navigate to ***Services*** > ***Instances and Subscriptions***. Click on ***Create***.

      ![](/exercises/ex0/images/11.png)

   - In the ***New Instance or Subscription*** pop-up, select:
     - ***`SAP Intelligent Returns Management`*** for *Service*,
     - ***`application`*** for *Plan*,
     - Click on ***Create***.

        ![](/exercises/ex0/images/12.png)

2. Create Role Collection, add Roles to it, and asign it to your user.
   - From Navigation Menu, navigate to ***Security*** > ***Role Collections***. Click on ***`+`*** button in the top-right corner of the screen.

      ![](/exercises/ex0/images/13.png)
  
   - Set Name for the Role Collection (f.e. ***`dt261-irm`***) and click ***Create***.

      ![](/exercises/ex0/images/14.png)
   
   - Click on the created Role Collection and click ***Edit*** from the detailed view.

      ![](/exercises/ex0/images/15.png)

   - Click on the popup button in the ***Role Name*** field.

      ![](/exercises/ex0/images/16.png)

   - In ***Select: Rome*** view:
     - Select ***`irm!b1345`*** for ***Application Identifier***, 
     - Check the checkboxes for ***`ReturnObjectREAD`***, ***`ReturnObjectWRITE`***, and ***`SettingsREAD`*** Roles,
     - Click ***Add*** button.

      ![](/exercises/ex0/images/17.png)
   
   - Now add your user to the Role Collection by entiring your user id in the ***ID*** field as shown on the screenshot. Click on your user from the value help. Then, click ***Save** button.

      > **Note:** You have to use the pre-created user for the on-site TechEd hands-on workshop. Please ask your instructors for more details.  

      ![](/exercises/ex0/images/18.png)

<br>After completing these steps you will have enabled SAP Intelligent Returns Management solution and have access to its application.

## Summary

Now that you have enabled SAP Intelligent Returns Management, you need to enable data integration to SAP S/4HANA via Data Ingestion for Industry Cloud.

<br>

### Go back to: [**Overview**](../../README.md) or Continue to: [**Enable data integration via Data Ingestion for Industry Cloud**](../ex1/README.md)
