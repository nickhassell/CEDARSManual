###District Student File (B)
**File Name:** DistrictStudent  
**Description:** This file consists of a record(s) for each student served in the district during the current school year along with the basic demographic data associated with the student. A student should have a record for each enrollment. Multiple enrollment records within one district will be necessary if the student enters, exits, and reenters a district. Entry and exit dates may not overlap for individual students.  

**Sample File Name:** 12345_0000_DistrictStudent_20070303.txt  

####Element B01 - School Year
**Field Name:** SchoolYear  
**Data Type:** char  
**Size:** 4  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The ending year for the current school year for the district. The four digit year in which the current school year ends.  
**Business Rules:** For the 2008–2009 current school year, report 2009.  
**Example:** 2009  
**Valid Values:** 2009  
**Last Updated:** September 2007  

####Element B02 - Serving County District Code
**Field Name:** ServingCountyDistrictCode  
**Data Type:** char  
**Size:** 5  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The County-District Code for the district providing service to the student. This is the unique 5-digit number that combines the 2-digit county code and the 3-digit district code.  
**Business Rules:**Must be a valid value, County-District Code, from the County-District Codes in Appendix A. Numeric value. Use leading zeros as necessary. Report the code representing the district as assigned by OSPI in Appendix A.  
**Example:** 12345  
**Valid Values:** Refer to valid values table in Appendix A.  
**Last Updated:** September 2007  

####Element B03 - Resident County District Code
**Field Name:** ResidentCountyDistrictCode  
**Data Type:** char  
**Size:** 5  
**Allow NULL?:** No. May not be left blank. Data is required.
**Description:** The County-District Code where the student physically resides. This is the unique 5-digit number that combines the 2-digit county code and the 3-digit district code.  
**Business Rules:** Must be a valid value, County-District Code, from the County-District Codes in Appendix A. This will appear as a numeric value and should include leading zeros even though this is submitted as a character data type. Report the code representing the district where the student physically resides as assigned by OSPI in Appendix A.  
**Example:** 02345  
**Valid Values:** Refer to valid values table in Appendix A.  
**Last Updated:** January 2009  

####Element B04 - District Student ID
**Field Name:** DistrictStudentID  
**Data Type:** varchar  
**Size:** 50  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** This is the student identifier assigned by the district to the student. This data element is used in the matching of district data with records in CEDARS.  
**Business Rules:** The value is unique within the school district. The value can be any combination of alpha and/or numeric values up to fifty characters in length. This ID should follow the student throughout their enrollment within the district and should not be reassigned to another student.  
**Example:** 123456789012 or 124 or TG096  
**Last Updated:** September 2007  

####Element B05 - State Student ID (SSID)
**Field Name:** SSID  
**Data Type:** char  
**Size:** 10  
**Allow NULL?:** Yes. Conditional. If the district does not provide data, OSPI will issue the SSID number.  
**Description:** Randomly generated number that functions as a unique student identifier for each Washington public school student. This number is assigned by OSPI. The SSID is not based on the name of the student.  
**Business Rules:** SSID values must be exactly 10 digits in length and only contain numeric values.  
Uploading two or more student records from the same district with identical SSIDs, but with different District Student IDs, will trigger an exception error.  
SSID numbers must not begin with a zero. A Null value indicates a new student with no previously issued SSID and will trigger the SSID assignment/matching process. Students who are home schooled and receive services through the school district (Running Start, special education, etc.) shall be issued an SSID number and reported in CEDARS.  
**Example:** 1234567890  
**Last Updated:** September 2007  

####Element B06 - Legal Last Name
**Field Name:** LastName  
**Data Type:** varchar  
**Size:** 60  
**Allow NULL?:** No. may not be left blank. Data is required.  
**Description:** The legal last name of the student.  
**Business Rules:** Every effort should be made to obtain the student’s legal last name. When this is not possible, the name provided by the parent should be submitted in this data element. Possible proof of name documents are Social Security Card, Passport, F-1 Visa, and Birth Certificate.  
**Example:** Smith  
**Last Updated:** September 2007  

####Element B07 - Legal First Name
**Field Name:** FirstName  
**Data Type:** varchar  
**Size:** 60  
**Allow NULL?:** Conditional. May be left blank when student has no first name.  
**Description:** The legal first name of the student.  
**Business Rules:** Every effort should be made to obtain the student’s legal first name. When this is not possible, the name provided by the parent should be submitted in this data element. Possible proof of name documents are Social Security Card, Passport, F-1 Visa, and Birth Certificate.  
**Example:** John  
**Last Updated:** January 2009  

####Element B08 - Legal Middle Name(s)
**Field Name:** MiddleName  
**Data Type:** varchar  
**Size:** 60  
**Allow NULL?:** Conditional. May be left blank only when student has no middle name.  
**Description:** The legal middle name(s) of the student.  
**Business Rules:** Conditional. May be left blank only when student has no middle name.  
Every effort should be made to obtain the student’s legal middle name. When this is not possible, the name provided by the parent should be submitted in this data element. Possible proof of name documents are Social Security Card, Passport, F-1 Visa, and Birth Certificate.  
**Example:** Ray  
**Last Updated:** September 2007  

####Element B09 - Birth Date
**Field Name:** BirthDate  
**Data Type:** datetime MM/DD/YYYY Format.  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The student’s month, day and year of birth in the MM/DD/YYYY format.  
**Business Rules:** The student must be under the age of 21 on September 1st for the current school year as defined in WAC 392-121-031. The birth date must be prior to the current date.  
**Example:** 1/2/2003 or 01/02/2003  
**Last Updated:** September 2007  

####Element B10 - Birth Country
**Field Name:** BirthCountry  
**Data Type:** char  
**Size:** 3  
**Allow NULL?:** Yes. Conditional.  
**Description:** The country where the student was born.  
**Business Rules:** Required for students participating or receiving services from the Title III Immigrant Program.  
If Element I06, Program Code, is equal to 15, Title III Immigrant, a valid Birth Country must be reported.  
Must be a valid National Origin Country Code from the National Origin Country Codes found in Appendix C.  
**Example:** MEX  
**Valid Values:** Refer to the valid values table in Appendix C.  
**Last Updated:** May 2009  

####Element B11 - Ethnicity Code (CSRS Transitional)
**Field Name:** CSRSEthnicityCode  
**Data Type:** Numeric  
**Size:** See Data Type Definitions.  
**Allow NULL?:** No. May not be left blank. Data is required for 2009-2010 school year if you do not provide data in new Element L05 (ethnicity code) and M05 (race code).  
**Description:** The student’s ethnicity code.  
**Business Rules:** Only valid Ethnicity Codes from the 08-09 CSRS Data Manual Element 15 may be submitted. Standards for the Classification of Federal Data on Race and Ethnicity can be found at: http://edocket.access.gpo.gov/2007/pdf/E7-20613.pdf  
**Example:** 2  
**Valid Values:** This is a CSRS Transitional Element. It will be eliminated in Sept 2010 and replaced by the data elements in Table L (ethnicity code) and Table M (race code). If data is provided in Element L05 and M05, the data provided in this element (B11) will be ignored and reporting will be pulled from Element L05 and M05. If data is not provided for both L05 and M05, data from B11 will be used.  
**Last Updated:** May 2009  

####Element B12 - Gender
**Field Name:** Gender  
**Data Type:** char  
**Size:** 1  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The student’s gender.  
**Business Rules:** See Valid Values below. All students must have a gender of male or female assigned.  
**Example:** M or F  
**Valid Values:** F-Female  
M-Male  
**Last Updated:** September 2007  

####Element B13 - Grade Level
**Field Name:** GradeLevel  
**Data Type:** varchar  
**Size:** 2  
**Allow NULL?:** No. May not be left blank.  Data is required.  
**Description:** The grade level in which the student is enrolled.  
**Business Rules:** All students must have a grade level assigned based on district policy and consistent with the Grade Level Codes defined in Appendix E.  
**Example:** 1 or 01  
**Valid Values:** Refer to the valid values table in Appendix E. A suggested list of Grade Level Assignments by Age is listed in Appendix G.  
**Last Updated:** September 2007  

####Element B14 - Date Enrolled in District
**Field Name:** DistrictEnrollmentDate  
**Data Type:** datetime	MM/DD/YYYY Format.  
**Size:** See Data Type Definitions.  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The date on which the student began attending class.  
**Business Rules:** This date must be the same as, or earlier than, the date contained in 	Element C06, Date Student Enrolled in School.  
Continuously enrolled status for the district will be calculated for AYP purposes based on this element and Element B15, Date Exited from District. If the student has been enrolled in the district for many years, but the district’s Student Information System is not able to track historical data because it re-enrolls students each year, you may use the date in Element C06, Date Student Enrolled in School, which is the date enrolled for the current school year.  
If, during the current school year, the student exits the district and then returns, the date the student returned to the district and resumed participation in class becomes the district enrollment date. The district enrollment date shall be reported in the current school year in which the enrollment occurred.  
If the student exits and returns one or more times within an current school year, all of the entry/exit dates shall be reported (requires multiple records for the student).  
If a student has multiple records the Date Enrolled in District may not overlap with another record for the student.  
If the student enrolls during the summer when school is not in session, use the date the student will begin classes (the first day of the current school year) as the district enrollment date.  
The enrollment date must be on or after [Element B09, Birth Date](#Element-B09---Birth-Date), and less than six months from the future enrollment.  
**Example:** 1/1/2000 or 01/01/2000  
**Last Updated:** April 2008  

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

[Element ](#)
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**
