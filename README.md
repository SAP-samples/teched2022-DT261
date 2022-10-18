# DT261 - Simplify Data Integration Between SAP S/4HANA and SAP’s Industry Cloud

## Description

This repository contains the material for the SAP TechEd 2022 session called DT261 - Simplify Data Integration Between SAP S/4HANA and SAP’s Industry Cloud.  

## Overview

The Consumer Industries Cloud offers a modular cloud suite. Data Ingestion for Industry Cloud (DI) provides the integration into the modular suite. DI promotes the sharing of data between applications and ensures a seemless integration with SAP S/4HANA. In our session we will configure this integration for master data from S/4HANA to the industry cloud.

We will use the examples of SAP Order and Delivery Schedule (ODS) and SAP Intelligent Returns Management (IRM), two offerings of the modular suite. ODS is in charge of defining possible delivery windows for suppliers based on configuration and SAP S/4HANA master data. IRM streemlines the returns process for a retailer by guiding consumers through the handling of an item and an AI based disposition engine in the warehouse to handle the goods.   

Data will flow from SAP S/4HANA to Data Ingestion and be distributed to the applications.

## Requirements

To complete exercises bellow, you need access (licenses) for the following SAP solutions:
- SAP S/4HANA on-prem, version ???<!--to be added by Christian--> and above OR SAP ECC, version ???<!--to be added by Christian--> or above
- SAP Intelligent Returns Management
- SAP Order and Delivery Scheduling
- Data Ingestion for Industry Cloud Solutions
- SAP Integration Suite
- SAP Fiory Launchpad

> **Note:**
> For the on-site TechEd workshop you will be provided with enviroment having above requirements available.

## Exercises

Excercises must be executed in the order below:

<!-- to be validated with Christian and Fabian -->

- [Enable SAP Intelligent Returns Management solution](exercises/ex0/README.md) <!--Stani-->
- [Enable data integration via Data Ingestion for Industry Cloud](exercises/ex1/README.md)<!--Stani-->
    - [Enable Data Ingestion for Industry Cloud](exercises/ex1/README.md#exercise-11-sub-exercise-1-description)<!--Stani-->
    - [Intgerate Data Ingestion for Industry Cloud with S/4HANA on-prem system](exercises/ex1/README.md#exercise-12-sub-exercise-2-description)
        - [Integrate Data Ingestion with SAP Integration Suite](exercises/ex1/README.md#exercise-12-sub-exercise-2-description)<!--Stani-->
        - [Integrate S/4HANA on-prem with SAP Integration Suite](exercises/ex1/README.md#exercise-12-sub-exercise-2-description)<!--Christian-->
- [Enable SAP Order and Delivery Scheduling](exercises/ex2/README.md) <!--Stani-->
- [Run the biz scenario with IRM and ODS](exercises/ex3/README.md) <!--Christian-->
  
<!-- 
**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

-->

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
