# Enable SAP Intelligent Returns Management solution

In this exercise, we will enable and configure usage of SAP Intelligent Returns Management Industry Cloud Solution.

## Setup your SAP Business Technology Platform (BTP) accounts

1. Login to SAP BTP cockpit:
   * Open [https://cockpit.**us21**.hana.ondemand.com/cockpit/](https://cockpit.us21.hana.ondemand.com/cockpit/#)

      > **Note:** You can exchange the **us21** from the URL with another region in case you are not based in USA

   * Provide your username and password and press **Log On**
      > **Note:** During your TechEd hands-on, you will be provided wit predefined user and password

        <br>![](/exercises/ex0/images/1.png)

2. Select desired Global Account (if you have multiple ones) and click on **Continue**

      <br>![](/exercises/ex0/images/2.png)

## Level 2 Heading

After completing these steps you will have....

1.	Click here.
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
