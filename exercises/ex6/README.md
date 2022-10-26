# Configure the Data Replication Framework - Business System
We use Data Replication Framework to read S/4HANA source data, transform it to the Industry Cloud format (One Domain Model) and send the data out to gateway.

We will use throughout the next exercises transaction DRFIMG to configure outbound implementations (IMG path: SAP Customizing Implementation Guide -> Logistics General -> Merchandise Lifecycle Optimization -> Outbound -> Data Replication Framework).

## Maintain a Business System for Replication
You configure the connection maintained in exercise 5 as business system for DRF.
1. Go to Define Custom Settings for Data Replication -> Define Technical Settings -> Define Technical Settings for Business Systems <br>![](/exercises/ex6/images/EX6_1.jpg)
2. Select 'New Entries'
3. Enter in column 'RFC Destination' the destination you created in exercise 5.
4. Enter in column 'Business System' the same destination <br>![](/exercises/ex6/images/EX6_2.jpg)
5. No other changes or entries are required.
6. Press enter, ignore the warning and save.

**Note:** The warning in step 6 will state that the business system selected in not part of the System Landscape Directory (SLO). For the purpose of this exercise the warning can be ignored.
