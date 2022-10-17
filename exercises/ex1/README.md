# Enable SAP Intelligent Returns Management solution

In this exercise, we will enable and configure usage of SAP Intelligent Returns Management Industry Cloud Solution.

## Subscribe for SAP Intelligent Returns Management

1. Login to SAP BTP cockpit:
* Open [https://cockpit.us21.hana.ondemand.com/cockpit/#](https://cockpit.us21.hana.ondemand.com/cockpit/#).
* Provide your user and password.

2. Select desired Global Account (if you have multiple ones).


<br>![](/exercises/ex1/images/01_01_0010.png)

2.	Insert this line of code.
```abap
response->set_text( |Hello World! | ). 
```



## Exercise 1.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)


## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

