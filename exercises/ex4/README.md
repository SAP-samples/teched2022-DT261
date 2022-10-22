# Create an OAuth client and configure a new connection

In this exercise we will create an OAuth client later used in the connectivity to the APIs of gateway. The RFC destination will use the Oauth client for authentication. You need the credentials file from the service binding in step nn (todo link file)

## Create an OAuth client

1. Log on to S/4HANA system HE4 using your user and password.

2. Call transaction OA2C_CONFIG. A browser window will open. Log on with the same credentials from step one. In case of an error like below, copy the url and enter it in a browser.<br>![](/exercises/ex4/images/teched_error1.jpg)
3. Press Create<br>![](/exercises/ex4/images/teched2.jpg)
4. Enter OAuth 2.0 client OPPS_OAUTH2_PROFILE (to do, needs to be replaced). Enter a name with your participant ID. Enter OAuth 2.0 client ID from exercise 1. (todo add more detail). The client ID is part of the service binding of the data ingestion app.
![](/exercises/ex4/images/teched5.jpg)
5. Press OK
6. For the OAuth 2.0 configuration enter the "Client Secret" in section General Settings. You find the client secret in the file in step 4 (element "clientsecret").   
7. In section Authorization Server Settings find the fields Authorization Endpoint and Toke Endpoint.
   a. Authorization Endpoint: Concatenate the value for element "url" and /oauth/token?grant_type=client_credentials&response_type=token
   b. Token Endpoint: Concatenate the value for element "url" and /oauth/token?grant_type=client_credentials&response_type=token ![](/exercises/ex4/images/teched8.jpg)
8. In Section Access Settings select "Client Credentials"
9.  Save.



*****





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

        > **Note:** You need to choose a reagion where SAP IRM is available. For more information on where SAP IRM is available, 

### Go back to: [**Overview**](../../README.md) or Continue to: [**Enable data integration via Data Ingestion for Industry Cloud**](../ex1/README.md)