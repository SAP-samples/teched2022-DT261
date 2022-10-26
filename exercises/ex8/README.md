# Run Replication for configured entities
After the configuration of the Replication Model you will now start replication of data. This is typically performed through a periodic job. For this exercise we will manually trigger replication.
You will use the Replication Model configured in exercise 7. 

## Run Replication 
1. Call transaction DRFOUT.
2. Enter the Replication Model you maintained in exercise 7.
3. Select "Outbound Implementation" CIC_SUPLR 
4. Select "Manual" in section Replication Mode. Avoid running DRFOUT in initial mode setting to avoid longer wait times <br>[](/exercises/ex8/images/EX8_1.jpg)
5. Click on "Manual Replication Filter Criteria" <br>[][def]
6. Enter Supplier to <todo add sample data>
7. Press "Save".
8. Execute DRFOUT (press F8).

[def]: /exercises/ex8/images/EX8_2.jpg

