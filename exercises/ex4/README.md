# Create an OAuth Client Profile 
In this exercise, you will create an OAuth Client Profile later used in the connectivity to the APIs of gateway. 
The RFC destination of the next exercise will use the Oauth client for authentication. 

You will need the file from the service binding of [Exercise 1](../ex1/README.md#enable-access-to-data-ingestion-di-for-industry-cloud-solutions-apis).

> **Warning**
> The content of this exercise is up-to-date as of TechEd 2022. Please go to the official [SAP Data Ingestion for Industry Cloud documentation](https://help.sap.com/docs/DI_ICS/925366f331c54ee88e2b61ddae0be9fc/88da41cc955e49f1b7080e882bae36d4.html?locale=en-US) for the most recent version.

## Log On to S/4HANA System

- Open SAP GUI

    ![](images/EX4_8.jpg)

- Log on to your S/4HANA system using your username and password.

   ![](images/EX4_9.jpg)

   ![](images/EX4_10.jpg)

   > **Note**
   > During your TechEd hands-on, you will be provided with a predefined username (`DT261-<your participant number>`) and password.

## Create an OAuth Client Profile

1. Create a new OAuth Client:

   - Call transaction `OA2C_CONFIG` prefixed with `/n`. A browser window will open. Log on with the credentials from the previous step. 

      ![](images/EX4_11.jpg)
      
   > **Note**
   > In case *Internet Explorer* is opened, copy the URL and open it in a different browser (e.g. Chrome).

   > **Note**
   > In case of an error like below, copy the url and enter it in a browser.
      ![](images/teched_error1.jpg)

   - Press the ***Create*** button.

      ![](images/EX4_2.jpg)

   - In the *Create* dialog:
      - Select ***`CIC_OAUTH_PROFILE`*** as ***OAuth 2.0 Client Profile***,
      - Enter a name in ***Configuration Name*** (e.g. ***`DT261_<your participant number>`***),

        ![](images/EX4_5.jpg)

      - Enter the `clientID` from the service binding file in ***OAuth 2.0 Client ID***,

         ![](images/EX4_3.jpg) 

      - Click the ***OK*** button.

2. Set OAuth Client Profile details:

   - Scroll down and select the ***Administration*** tab in the ***Details*** section.

   - Enter the ***`clientSecret`*** from the service binding file in the ***Client Secret*** field.

   - Enter the ***`url`*** from the service binding file in the ***Authorization Endpoint*** field, remove the leading `https://` and append `/oauth/token?grant_type=client_credentials&response_type=token` to it.

   - Enter the ***`url`*** from the service binding file in the ***Token Endpoint*** field, remove the leading `https://` and append `/oauth/token?grant_type=client_credentials&response_type=token` to it.

     ![](images/teched6.jpg)

   - Select ***Client Credentials*** from the *Selected Grant Type* selector.

    ![](images/EX4_7.jpg)
   
   - Click the ***Save*** button at the top of the screen.

## Next Steps

In the next exercise you will use this OAuth Client and create an RFC connection with it.

### Go back to: [**Configure Data Ingestion for Industry Cloud Solutions**](../ex2/README.md) or Continue to: [**Configure the RFC Connection**](../ex5/README.md)
