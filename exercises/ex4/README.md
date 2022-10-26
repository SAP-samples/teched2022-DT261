# Create an OAuth client 
In this exercise we will create an OAuth client later used in the connectivity to the APIs of gateway. The RFC destination will use the Oauth client for authentication. You need the credentials file from the service binding in step nn <todo link file>

## Create an OAuth client

1. Log on to S/4HANA system HE4 using your user and password.
2. Call transaction OA2C_CONFIG. A browser window will open. Log on with the same credentials from step 1. In case of an error like below, copy the url and enter it in a browser.<br>![](/exercises/ex4/images/teched_error1.jpg)
3. Press Create.<br>![](/exercises/ex4/images/EX4_2.jpg)
4. Enter OAuth 2.0 client OPPS_OAUTH2_PROFILE <todo, needs to be replaced>. Enter a name with your participant ID. Enter OAuth 2.0 client ID from exercise 1. <todo add more detail> The client ID is part of the service binding of the data ingestion app.
<br>![](/exercises/ex4/images/EX4_3.jpg)
<br>The create screen looks like this 
<br>![](/exercises/ex4/images/EX4_5.jpg)
5. Press OK
6. For the OAuth 2.0 configuration enter the "Client Secret" in section General Settings. You find the client secret in the file in step 4 (element "clientsecret").   
7. In section Authorization Server Settings find the fields Authorization Endpoint and Toke Endpoint.
   1. "Authorization Endpoint": Concatenate the value for element "url" and /oauth/token?grant_type=client_credentials&response_type=token
   2. "Token Endpoint": Concatenate the value for element "url" and /oauth/token?grant_type=client_credentials&response_type=token ![](/exercises/ex4/images/EX4_4.jpg)
8. In Section Access Settings select "Client Credentials"
9.  Save.