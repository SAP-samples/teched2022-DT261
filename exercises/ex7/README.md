# Configure the Data Replication Framework - Replication Model
In this step we will configure the entities to replicated to Industry Cloud. Depending on the application in scope different entities are required (order sourcing requires different entities than promotion planning). A replication model groups together outbound implementations for the individual entities (product, plant, sales organization etc.). We plan to automate this configuration. In the exercise we will configure it manually. <br>
Starting point is again the DRF configuration, transaction code DRFIMG (IMG path: Data Replication -> Define Custom Settings for Data Replication -> Define Technical Settings -> Define Replication Models).


## Maintain a Replication Model
You require the business system configured in exercise 6.
1. Go to Define Custom Settings for Data Replication -> Define Technical Settings -> Define Replication Models <br>![](/exercises/ex7/images/EX7_1.jpg)
2. Select 'New Entries'
3. Create replication model DT261-<group number> with a short text <br>![](/exercises/ex7/images/EX7_2.jpg)
4. Select the replication model and click on Assign Outbound Implementation <br>![](/exercises/ex7/images/EX7_3.jpg)
5. For the example of the supplier this looks like this <br>![](/exercises/ex7/images/EX7_4.jpg)
6. Select the Outbound Implementations and click on "Assign Target Systems for Repl. Model/Outb. Impl" and assign the Business System defined in exercise 6 to the Outbound Implementation <br>![](/exercises/ex7/images/EX7_5.jpg)
7. Add other Outbound Implementations to the Replication Model <br> <todo add a table of all outbound implementations available in HE4>
8. Save your changes.
9. Return to the Replication Model overview, select your Replication Model and press "Activate". ![](/exercises/ex7/images/EX7_6.jpg) 
