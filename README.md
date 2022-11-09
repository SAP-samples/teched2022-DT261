# DT261 - Simplify Data Integration Between SAP S/4HANA and SAP’s Industry Cloud

## Description

This repository contains the material for the SAP TechEd 2022 session called DT261 - Simplify Data Integration Between SAP S/4HANA and SAP’s Industry Cloud.  

## Overview

The Industry Cloud offers a modular cloud suite. Data Ingestion for Industry Cloud (DI) provides the integration into this modular suite. DI promotes the sharing of data between applications and ensures a seamless integration with SAP S/4HANA. In our session, we will configure this integration for master data from S/4HANA to the industry cloud.

We will use the examples of SAP Order and Delivery Schedule (ODS) and SAP Intelligent Returns Management (IRM), two offerings of the modular suite. ODS is in charge of defining possible delivery windows for suppliers based on configuration and SAP S/4HANA master data. IRM streamlines the returns process for a retailer by guiding consumers through the handling of an item and an AI based disposition engine in the warehouse to handle the returns.   

Data will flow from SAP S/4HANA to Data Ingestion and is distributed to the applications.

## Requirements

To complete the exercises below, you need access (licenses) to the following SAP solutions:
- SAP S/4HANA on-prem 2020 or later (SAP ECC on project base)
- SAP Intelligent Returns Management
- SAP Order and Delivery Scheduling
- Data Ingestion for Industry Cloud Solutions
- SAP Fiori Launchpad

> **Note**
> You will be provided with an environment having the above requirements available for the on-site SAP TechEd Hands-On Lab workshop.

## Exercises

The exercises must be executed in the order below:

- [Enable SAP Intelligent Returns Management solution](exercises/ex0/README.md)
- [Enable data integration to SAP S/4HANA via Data Ingestion for Industry Cloud](exercises/ex1/README.md)
    - [Enable Data Ingestion for Industry Cloud Solutions](exercises/ex1/README.md)
    - [Configure Data Ingestion for Industry Cloud Solutions](exercises/ex2/README.md)
    - [Integrate Data Ingestion for Industry Cloud with S/4HANA on-prem system](exercises/ex4/README.md)
        - [Create an OAuth client](exercises/ex4/README.md)
        - [Configure the RFC Connection](exercises/ex5/README.md)
        - [Configure the Data Replication Framework - Business System](exercises/ex6/README.md)
        - [Configure the Data Replication Framework - Replication Model](exercises/ex7/README.md)
        - [Run Replication for configured entities](exercises/ex8/README.md)
- [Enable SAP Order and Delivery Scheduling solution](exercises/ex3/README.md)
- [Run the biz scenario with IRM and ODS](exercises/ex9/README.md) 
  
## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
