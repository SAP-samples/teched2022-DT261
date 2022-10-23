# Configure the RFC connection
In this step you will configure the connection using the OAuth profile from the previous step. The RFC connection will be used for the outbound calls to Data Ingestion.

## Create an OAuth client

1. Call transaction SM59
2. Press "Create"
3. enter "Destination" <todo find a name>
4. Selection connection type G - "HTTP connection to external server"
5. In the tab "Technical Settings" enter the value of "openapi_url" in field "Host". Remove https:// from the value.<br> For ```"openapi_url":"https://api.us.teched.sap"```<br> the "Host" will be ```api.us.teched.sap``` <br>
![](/exercises/ex5/images/EX5_1.jpg)
6. Go to tab "Logon & Security" and push button "OAuth Settings"
7. Select Profile and Configuration from exercise 4 <todo add name> <br>![](/exercises/ex5/images/EX5_2.jpg)
8. Press Save.
