claims
======

Exploring JSON representation for claims data.

A sample BlueButton Test file (medicare/medicare_bbp.txt) from MyMedicare.gov has been used to create a medicare_bbp.xml and medicare_bbp.json format.
This has been based on the claims.xml file that was initially created by Ryan Panchadsaram. 

Latest change is to change field names to headlessCamelCase. ie. "Medicare Part B Effective Date" becomes "medicarePartBEffectiveDate".


Objective 
---------

The objective of this work is to:

1. Create structured file formats in XML and JSON that can be used for the CMS BlueButton Plus data-as-a-service project.
2. Create claims summary and claim detail sections that will also satisfy the needs of the payer community for BlueButton 
claims output for beneficiaries of Medicare, Medicaid and private insurance plans.

Design Principles
-----------------

The following design principles have been adopted in creating these file formats:

1. Keep it simple
2. Develop a single file format with the necessary sections incorporated within the file 
in order to avoid the challenges that can come with packaging multiple sets of files.


# Files in medicare folder:

## medicare_bbp.txt

This is a medicare bluebutton test file in simple ASCII format

## medicare_bbp.xml

This is an xml version based on the fields in the medicare_bbp.txt file 

## medicare_bbp.json

This is a json format file that has been generated from the medicare_bbp.xml using an xml to JSON converter at
http://www.freeformatter.com/xml-to-json-converter.html


TODO-ekivemark
--------------

1. Create a generic BlueButtonPlus.xml and BlueButtonPlus.json that covers medicare and non-medicare payers.
2. Confirm approach in using <source></source>field within data segments to identify source of data.
 
Current Source field Values:

+ patient
+ mymedicare.gov

