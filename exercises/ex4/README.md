# Create an OAuth client 
In this exercise we will create an OAuth client later used in the connectivity to the APIs of gateway. The RFC destination will use the Oauth client for authentication. You need the credentials file from the service binding from section 3 of exercise 1 (In the Credentials view, click on Download and save the file locally).

## Create an OAuth client

1. Log on to S/4HANA system HE4 using your user and password.
2. Call transaction OA2C_CONFIG. A browser window will open. Log on with the same credentials from step 1. In case of an error like below, copy the url and enter it in a browser.<br>![][def]
3. Press Create.<br>![][def2]
4. Enter OAuth 2.0 client OPPS_OAUTH2_PROFILE <todo, needs to be replaced>. Enter a name with your participant ID. Enter OAuth 2.0 client ID from exercise 1. <todo add more detail> The client ID is part of the service binding of the data ingestion app. <br>![][def3] <br>The created screen looks like this <br>![][def4]
5. Press OK.
6. For the OAuth 2.0 configuration enter the 'Client Secret' in section General Settings. You find the client secret in the file in step 4 (element 'clientsecret').   
7. In section Authorization Server Settings find the fields Authorization Endpoint and Toke Endpoint.
   - 'Authorization Endpoint': Concatenate the value for element 'url' and /oauth/token?grant_type=client_credentials&response_type=token
   - 'Token Endpoint': Concatenate the value for element 'url' and /oauth/token?grant_type=client_credentials&response_type=token <br>![](images/teched6.jpg)
8. In Section Access Settings select 'Client Credentials'
9. Save.

### Go back to: [**Configure Data Ingestion for Industry Cloud Solutions**](../ex2/README.md) or Continue to: [**Configure the RFC Connection**](../ex5/README.md)

[def]: images/teched_error1.jpg
[def2]: images/EX4_2.jpg
[def3]: images/EX4_3.jpg
[def4]: images/EX4_5.jpg