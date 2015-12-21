###Student Programs File (I)
**File Name:** StudentPrograms  
**Description:** This file details student participation in various programs for the current school year. There should be one record per student per program for the current school year. For example, if a student enters, exits and re-enters a program, there should be two records to reflect these two separate enrollments into the program. If a student is participating in or received services from more than one program, there should be a record for each program. Information for the State Transitional Bilingual Instruction Program is not included in this file. It is reported separately in the Student Bilingual Programs [File J](\StudentBilingualPrograms.md). Information for the Special Education Program is not included in this file. It is reported separately in the Student Special Education Programs [File K](\StudentSpecialEducationPrograms.md).  

**Sample File Name:** 12345_0000_StudentPrograms_20070303.txt

####Element I01 - School Year
**Field Name:** SchoolYear  
**Data Type:** char  
**Size:** 4  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The ending year for the current school year for the district. The four digit year in which the current school year ends.  
**Business Rules:** For the 2008�2009 current school year, report 2009.  
**Example:** 2009  
**Valid Values:** 2009  
**Last Updated:** September 2007  

####Element I02 - Serving County District Code
**Field Name:** ServingCountyDistrictCode  
**Data Type:** char  
**Size:** 5  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The County-District Code for the district providing service to the student. This is the unique 5-digit number that combines the 2-digit county code and the 3-digit district code.  
**Business Rules:**Must be a valid value, County-District Code, from the County-District Codes in Appendix A. Numeric value. Use leading zeros as necessary. Report the code representing the district as assigned by OSPI in Appendix A.  
**Example:** 12345  
**Valid Values:** Refer to valid values table in Appendix A.  
**Last Updated:** September 2007  

####Element I03 - District Student ID
**Field Name:** DistrictStudentID  
**Data Type:** varchar  
**Size:** 50  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** This is the student identifier assigned by the district to the student. This data element is used in the matching of district data with records in CEDARS.  
**Business Rules:** The value is unique within the school district. The value can be any combination of alpha and/or numeric values up to fifty characters in length. This ID should follow the student throughout their enrollment within the district and should not be reassigned to another student.  
**Example:** 123456789012 or 124 or TG096  
**Last Updated:** September 2007  

####Element I04 - State Student ID (SSID)
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

####Element I05 - Location ID
**Field Name:** LocationId  
**Data Type:** varchar  
**Size:** 4  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The Location ID for the school as generated by the District�s Student Information System, SIS.  
**Business Rules:** This is an internal number generated by the District and is required.  
If you do not have an ID assigned to this field, report the OSPI School Code reported in [Element A5](\A-Location.md#element-a05---school-code), School Code.  
The ID reported in Element I05 must be included in the [Location File A](\A-Location.md).  
**Example:** 1234  
**Last Updated:** September 2007

####Element I06 - Program Code
**Field Name:** ProgramCode  
**Data Type:** Numeric    
**Size:** See Data Type Definitions.  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The State assigned Program Code in which the student is receiving services at any point during the current school year.    
**Business Rules:** See Valid Values below.
If the student received services or participated in a program listed in the valid values table below at any point in the current school year, then that participation should be reported here.  
If Element I06 is equal to Title III Native America Program, Code 14, the student must have [Element B11](\B-DistrictStudent.md#element-b11---ethnicity-code), Ethnicity Code equal to 1 (American Indian/Alaskan Native) OR the student must have [Element M05](\M-StudentRace.md#element-m05---race-code), Race Code (American Indian/Alaskan Native). In addition to one of the above, [Element B17](\B-DistrictStudent.md#element-b17---student-primary-language-code), Primary Language Code, must equal 639, English. The student must also take the WLPT placement test to enter the Title III Native American Program.  
If Element I06 is equal to Title III Immigrant, Code 15, [Element B10](\B-DistrictStudent.md#element-b10---birth-country), Birth Country is required.  
**Example:** 2  
**Valid Values:** 1 � 21st Century Community Learning Program  
2 � Early Education  
3 � Gifted  
4 � LAP Targeted Assistance Reading  
5 � LAP Targeted Assistance Language Arts  
6 � LAP Targeted Assistance Math  
8 � Title I Targeted Assistance Reading  
9 � Title I Targeted Assistance Language Arts  
10 � Title I Targeted Assistance Math  
12 � Title I Targeted Assistance Science  
13 � Title I Targeted Assistance Social Studies  
14 � Title III Native American  
15 � Title III Immigrant  
16 � 504  
17 � Migrant  
18 � NCLB Supplemental Services  
19 � Free Reduced Meals Participation  
20 � No longer used  
**Last Updated:** August 2009

####
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

####
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

####
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**

####
**Field Name:**
**Data Type:**
**Size:**
**Allow NULL?:**
**Description:**
**Business Rules:**
**Example:**
**Valid Values:**
**Last Updated:**