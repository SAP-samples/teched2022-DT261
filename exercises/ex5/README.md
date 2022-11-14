# Configure the RFC Connection

In this exercise, you will configure the connection using the OAuth Client Profile from the previous exercise. 
The RFC connection will be used for the outbound calls to Data Ingestion.

You can use connection `DT261_00` as reference for this exercise.

> **Warning**
> The content of this exercise is up-to-date as of the SAP TechEd Hands-On Lab 2022. Please go to the official [SAP Data Ingestion for Industry Cloud documentation](https://help.sap.com/docs/DI_ICS/925366f331c54ee88e2b61ddae0be9fc/88da41cc955e49f1b7080e882bae36d4.html?locale=en-US) for the most recent version.

## Create an RFC Connection

* Call transaction `SM59`

* Press the ***Create*** button

   ![](images/EX5_5.png)

* In the *Create Destination* dialog:
   - Enter a destination name for ***Destination*** (e.g. ***`DT261_<your participant number>`***), 
   - Select ***`G HTTP connection to external server`*** for ***Connection Type***, 
   - Click the green checkmark button (*Continue*).

* In the ***Technical Settings*** tab of the new page:
   - Enter the ***`openapi_url`*** from the service binding file in the ***Host*** field. Remove `https://` from the value.<br>E.g.: For `"openapi_url":"https://api.us.di-ics.services.sap"` the 'Host' will be `api.us.di-ics.services.sap`

      ![](images/EX5_1.jpg)

* In the ***Logon & Security*** tab:
   - Push the ***OAuth Settings*** button, 

   - Select the *Profile*, `CIC_OAUTH_PROFILE`, and *Configuration* name from exercise 4. Press the ***Save*** button.

      ![](images/EX5_2.png)

   - Select the ***Active*** radio button for the ***SSL*** field in the *Status of Secure Protocol* section, 

      ![](images/EX5_3.png)

   - Press the ***Save*** button.

   - Run a connection test. `404 Not Found` is the expected response.

      ![](images/EX5_4.jpg)

      ![](images/EX5_6.png)

## Next Steps
In the next step we will configure the Data Replication Framework.

### Go back to: [**Create an OAuth client**](../ex4/README.md) or Continue to: [**Configure the Data Replication Framework - Business System**](../ex6/README.md)
