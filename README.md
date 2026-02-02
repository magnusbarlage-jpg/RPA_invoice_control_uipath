# UiPath RPA Invoice Control Automation

## Overview
This repository contains a demo version of a UiPath based automation for invoice control in a Windows ERP environment.
The solution automates the preparation, extraction, validation, and processing of invoice data and supports invoice release based on defined business rules.
All data used in this repository is fully anonymized and provided for demonstration purposes only.

The original implementation was developed in a professional working student context and is represented here as a portfolio safe demo project.

## Business Context
Invoice control processes often require manual interaction across multiple systems and documents.
Typical challenges include repetitive data entry, inconsistent validation, and limited transparency during invoice approval.
This automation demonstrates how a structured RPA solution can standardize checks, reduce manual effort, and increase process reliability.

## Business Goal
The goal of this automation is to reduce manual invoice checking effort, improve data quality, and support faster and more consistent invoice release decisions by applying rule based validation logic.

## Process Overview
The automation follows a structured multi step process:

1. Refresh invoice related export data from the ERP system
2. Read and filter incoming invoice PDF documents
3. Extract relevant invoice fields using Document Understanding
4. Prepare and clean structured datasets for processing
5. Enter validated invoice data into the ERP system
6. Compare end amounts and support invoice release

## Implemented Workflows
The solution is split into clearly separated workflows, each representing one logical process step.

### P0_refresh Data export from ERP
Automates the update of invoice related export data in the ERP Windows client to ensure up to date reference information for processing.

### P1_Extract Data from PDF Invoices
Processes invoice PDF documents using UiPath Document Understanding.
Includes document digitization with OCR, keyword based classification, and structured data extraction.
Creates separate datasets for invoice and service related information.

### P2_Invoice Data to ERP
Automates structured data entry into the ERP Windows client.
Includes robust UI automation logic and guarded segments to ensure stability during interaction with the application.

## Technical Highlights
This project demonstrates several key RPA competencies relevant for professional environments:

* End to end automation covering document handling, data processing, validation, and ERP interaction
* Document Understanding implementation with taxonomy loading, OCR digitization, and extraction scopes
* Desktop UI automation in a real Windows ERP client
* Data driven processing using DataTables for scalable iteration
* Structured workflow design with clear separation of responsibilities
* Robust handling of repetitive ERP interactions using guarded logic
* Use of UiPath Modern Design principles

## Tech Stack
* UiPath Studio using Modern Design
* UiPath Document Understanding
* OmniPage OCR
* Keyword Based Classifier
* Windows UI Automation
* DataTable based processing
* Excel based structured outputs

## Repository Structure
The repository is organized as follows:

* workflows  
  Contains all UiPath XAML workflows

* data  
  Contains anonymized demo input files and reference data

* docs  
  Contains documentation assets such as the value stream map

* project.json  
  UiPath project configuration file

* README.md  
  Project documentation

## How to Run the Demo
1. Open the project in UiPath Studio
2. Ensure demo files are available in the data folder
3. Adjust local paths if required
4. Execute the workflows in the following order:
   P0 then P2 then P4 then P3 then P5

## Data Privacy and Disclaimer
This repository contains only anonymized demo data.
No confidential company information, system credentials, or internal identifiers are included.
All system names, file paths, and values are generalized to ensure safe public sharing.

## Suggested Improvements
Potential future enhancements for this solution include:

* Centralized configuration management
* Extended logging and execution reporting
* Clear separation of extraction rules and ERP entry rules
* Automated test datasets for extraction validation

## Portfolio Note
This project is intended to demonstrate practical RPA implementation skills, process understanding, and structured automation design.
It reflects experience gained in a real business environment and is not a tutorial or learning example.

