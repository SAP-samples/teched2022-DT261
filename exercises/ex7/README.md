# Configure the Data Replication Framework - Replication Model
In this step we will configure the entities to replicated to Industry Cloud. Depending on the application in scope different entities are required (order sourcing requires different entities than promotion planning). A replication model groups together outbound implementations for the individual entities (product, plant, sales organization etc.). We plan to automate this configuration. In the exercise we will configure it manually. <br>
Starting point is again the DRF configuration, transaction code DRFIMG (IMG path: Data Replication -> Define Custom Settings for Data Replication -> Define Technical Settings -> Define Replication Models).


## Maintain a Replication Model
You require the business system configured in exercise 6.
1. Go to Define Custom Settings for Data Replication -> Define Technical Settings -> Define Replication Models <br>![](/exercises/ex7/images/EX7_1.jpg)
2. Select 'New Entries'
3. Create replication model DT261_<group number> with a short text <br>![](/exercises/ex7/images/EX7_2.jpg)<br>replication model *DT261_00* can be used as template. 
4. Select the replication model and click on Assign Outbound Implementation <br>![](/exercises/ex7/images/EX7_3.jpg)
5. For the example of the supplier this looks like this <br>![](/exercises/ex7/images/EX7_4.jpg)
6. Select the Outbound Implementations and click on 'Assign Target Systems for Repl. Model/Outb. Impl' and assign the Business System defined in exercise 6 to the Outbound Implementation <br>![](/exercises/ex7/images/EX7_5.jpg)
7. Add other Outbound Implementations to the Replication Model <br> 
| Outbound Implementation |
| ----------------------- |
| CIC_COSD                |
| CIC_COUNTR              |
| CIC_CUST                |
| CIC_SUPLR               |
| CIC_FCAL                |
| CIC_FCALD               |
| CIC_HOLIDY              |
| CIC_CURC                |
| CIC_DCHAIN              |
| CIC_DIST                |
| CIC_LANG                |
| CIC_PLANT               |
| CIC_MCH                 |
| CIC_PROD                |
| CIC_SLSORG              |
| CIC_TRANS               |
| CIC_UOM                 |
| CIC_SOS                 |
| CIC_LOADGP              |
| CIC_TEMPB               |
| CIC_PRDPLT              |
| CIC_PURORG              |
| CIC_CUSTOD              |
| CIC_DIV                 |
| CIC_CHTC                |


8. Save your changes.
9.  Return to the Replication Model overview, select your Replication Model and press 'Activate'. <br> ![](/exercises/ex7/images/EX7_6.jpg) 


<br> 

### Go back to: [**Configure the Data Replication Framework - Business System**](../ex6/README.md) or Continue to: [**Run Replication for configured entities**](../ex8/README.md)