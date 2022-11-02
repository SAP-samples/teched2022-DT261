# Create an OAuth client 
In this exercise, you will create an OAuth client later used in the connectivity to the APIs of gateway. 
The RFC destination of the next exercise will use the Oauth client for authentication. 

You will need the file from the service binding of [Exercise 1](../ex1/README.md#enable-access-to-data-ingestion-di-for-industry-cloud-solutions-apis).

## Create an OAuth client

1. Log on to your S/4HANA system using your username and password.

      > **Note:** During your TechEd hands-on, you will be provided with a predefined username and password.

2. Call transaction `OA2C_CONFIG`. A browser window will open. Log on with the credentials from the previous step. In case of an error like below, copy the url and enter it in a browser.

   ![](images/teched_error1.jpg)

3. Press the ***Create*** button.

   ![](images/EX4_2.jpg)

[//]: # (TODO: Something needs to be replaces)
4. Enter OAuth 2.0 client OPPS_OAUTH2_PROFILE <todo, needs to be replaced>. Enter a name with your participant ID. Enter OAuth 2.0 client ID from exercise 1. <todo add more detail> The client ID is part of the service binding of the data ingestion app.

   ![](images/EX4_3.jpg) 

   The created screen looks like this

   ![](images/EX4_5.jpg)

5. Press OK.

6. For the OAuth 2.0 configuration enter the 'Client Secret' in section General Settings. You find the client secret in the file in step 4 (element 'clientsecret').   

7. In section Authorization Server Settings find the fields Authorization Endpoint and Toke Endpoint.
   - 'Authorization Endpoint': Concatenate the value for element 'url' and /oauth/token?grant_type=client_credentials&response_type=token
   - 'Token Endpoint': Concatenate the value for element 'url' and /oauth/token?grant_type=client_credentials&response_type=token
   
     ![](images/teched6.jpg)

8. In Section Access Settings select 'Client Credentials'

9. Save.

## Next Steps

[//]: # (TODO: Add a description of what happens next)

### Go back to: [**Configure Data Ingestion for Industry Cloud Solutions**](../ex2/README.md) or Continue to: [**Configure the RFC Connection**](../ex5/README.md)
