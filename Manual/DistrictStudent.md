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
Continuously enrolled status for the district will be calculated for AYP purposes based on this element and [Element B15, Date Exited from District](#element-b15---date-exited-from-district). If the student has been enrolled in the district for many years, but the district’s Student Information System is not able to track historical data because it re-enrolls students each year, you may use the date in Element C06, Date Student Enrolled in School, which is the date enrolled for the current school year.  
If, during the current school year, the student exits the district and then returns, the date the student returned to the district and resumed participation in class becomes the district enrollment date. The district enrollment date shall be reported in the current school year in which the enrollment occurred.  
If the student exits and returns one or more times within an current school year, all of the entry/exit dates shall be reported (requires multiple records for the student).  
If a student has multiple records the Date Enrolled in District may not overlap with another record for the student.  
If the student enrolls during the summer when school is not in session, use the date the student will begin classes (the first day of the current school year) as the district enrollment date.  
The enrollment date must be on or after [Element B09, Birth Date](#element-b09---birth-date), and less than six months from the future enrollment.  
**Example:** 1/1/2000 or 01/01/2000  
**Last Updated:** April 2008  

####Element B15 - Date Exited from District
**Field Name:** DistrictExitDate  
**Data Type:** datetime	MM/DD/YYYY Format.  
**Size:** See Data Type Definitions.  
**Allow NULL?:** Yes. Conditional. See Business Rules.  
**Description:** The date on which the student withdraws from the school district. The last day the student attended or received services from the district. This date will change each time a student leaves the district.  
**Business Rules:** If a date is entered, then Element C08, Date Student Exited from School, should have a matching exit date for the school within the district that was last attended by the student.  
If the student enters and exits on the same date, the same date is used in Elements B14, B15, C06 and C08.  
If the student exits and returns within a current school year all of the entry/exit dates shall be reported (requires multiple records for the student).    
If the student leaves the district during the summer, use the actual date the student left the district as the district exit date.  
Continuously enrolled status for the district will be calculated for WASL purposes based on this element and [Element B14](#element-b14---date-enrolled-in-district).  
**Example:** 1/1/2000 or 01/01/2000  
**Last Updated:** May 2009  

####Element B16 - Disability Code
**Field Name:** DisabilityCode  
**Data Type:** Numeric  
**Size:** See Data Type Definitions  
**Allow NULL?:** No. May not be left blank. Data is required  
**Description:** Indicates the student’s disabling condition.  
**Business Rules:** See Valid Values below.  
If a student has a disability, regardless of whether or not they are receiving special education program services, the disability should be reported here.  
If the value in this data element, B16, is (1), then the student must be under the age of 9 as of 8/30 of the current school year. The value must be changed from (1) to another valid value prior to the student’s ninth birthday. For example if the student turns 9 on 8/30/2008 the status must be changed from (1) before 8/30/2008, the student’s birth date.  
If the student has an active record in the Student Special Education Programs File K, the student must have a value of 1–14 in this element. Students who have 0, no disability reported, should not have a record in the Special Education Table (Table K). Additionally, having a disability does not automatically imply that the student is being served by Special Education.  
**Example:** 1 or 01  
**Valid Values:** 0 – No Disability Reported  
1 – Developmental Delays (used only for students 0-8 years old)  
2 – Emotional/Behavioral Disability  
3 – Orthopedic Impairment  
4 – Health Impairment  
5 – Specific Learning Disability  
6 – Mental Retardation  
7 – Multiple Disabilities  
8 – Deafness  
9 – Hearing Impairment  
10 – Visual Impairment  
11 – Deaf-Blindness  
12 – Communication Disorders  
13 – Autism  
14 – Traumatic Brain Injury  
Refer to the valid value table in Appendix I.  
**Last Updated:** August 2009

####Element B17 - Student Primary Language Code
**Field Name:** PrimaryLanguageCode  
**Data Type:** Numeric  
**Size:** See Data Type Definitions  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** The first learned language spoken by the student.  
**Business Rules:** This language will always be the student's native or first language spoken. Must be a valid value from the Language Codes listed in Appendix K. If the student is reported as receiving State Transitional Bilingual Instruction services, this value should not equal 639 (English). Upon exiting the State Transitional Bilingual Instruction Program, this Element, B17, Student Primary Language Code, should remain the student’s native or first language spoken.  
**Example:** 015 or 15  
**Valid Values:** Refer to valid values table in Appendix K.  
**Last Updated:** August 2009

####Element B18 - Student Language Spoken at Home
**Field Name:** LanguageSpokenAtHome  
**Data Type:** Numeric  
**Size:** See Data Type Definitions  
**Allow NULL?:** Yes. This is an optional field.  
**Description:** The primary language the student speaks at home.  
**Business Rules:** This language may change over time. Must be a valid value from the Language Codes listed in Appendix K. If a student speaks multiple languages, indicate the language the student uses to communicate at home.  
**Example:** 015 or 15  
**Valid Values:** Refer to valid values table in Appendix K.  
**Last Updated:** August 2009

####Element B19 - Social Security Number
**Field Name:** SSN  
**Data Type:** char  
**Size:** 9  
**Allow NULL?:** Yes. This is an optional field.  
**Description:** The student's Social Security number.  
**Business Rules:** Must be a 9 digit numeric value only. Do not include hyphens. Social Security numbers may begin with a zero and if they do, the leading zero must be included.  
**Example:** 123456789  
**Last Updated:** January 2007

####Element B20 - Residential Zip Code + 4
**Field Name:** ZipCode  
**Data Type:** varchar  
**Size:** 9  
**Allow NULL?:** Yes. This is an optional field.  
**Description:** The zip code of the student's residential address.  
**Business Rules:** This should be the five digit postal code, and the four digit extension (no hyphen), if available. Valid value must be five or nine numeric digits.  
**Example:** 985040001 or 98504  
**Last Updated:** January 2007  

####Element B21 - Is Student Homeless
**Field Name:** IsHomeless  
**Data Type:** char  
**Size:** 1  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** Indicates whether or not the student was homeless at the time of extract during the current school year as defined in McKinney-Vento Act, Section 725(2).  
**Business Rules:** See Valid Values below.  
Section 725 of the McKinney-Vento Act defines the following terms:  
* Homeless children and youth mean individuals who lack a fixed, regular, and adequate nighttime residence. The term includes--
	1. Children and youth who are sharing the housing of other persons due to loss of housing, economic hardship, or a similar reason; are living in motels, hotels, trailer parks, or camping grounds due to the lack of alternative adequate accommodations; are living in emergency or transitional shelters; are abandoned in hospitals; or are awaiting foster care placement;
	2. Children and youth who have a primary nighttime residence that is a public or private place not designed for or ordinarily used as a regular sleeping accommodation for human beings;
	3. Children and youth who are living in cars, parks, public spaces, abandoned buildings, substandard housing, bus or train stations, or similar settings; and
	4. Migratory children (as defined in section 1309 of the Elementary and Secondary Education Act of 1965, as amended) who qualify as homeless because they are living in circumstances described in this definition.
* Enroll and enrollment include attending classes and participating fully in school activities.
* Unaccompanied youth includes a youth not in the physical custody of a parent or guardian.  
**Example:** Y  
**Valid Values:** Y - Yes  
	N - No  
**Last Updated:** July 2008  

####Element B22 - Is Student an Approved Private School Student Attending Class Part Time
**Field Name:** IsApprovedPrivateSchoolStudentAttendingPartTime  
**Data Type:** char  
**Size:** 1  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** Indicates whether or not the student is enrolled in an approved private school and is attending class(es) part time.  
**Business Rules:** See Valid Values below.  
A student is defined as Approved Private School Attending Class Part Time when they are also enrolled in a public school for the purpose of taking any course or receiving any ancillary service, or any combination of courses and ancillary services.  

**Example:** Y  
**Valid Values:** Y – Yes  
	N – No  
**Last Updated:** July 2008

####Element B23 - Is Student a Home-Schooled Student Attending Class Part time
**Field Name:** IsHomeBasedStudentAttendingPartTime   
**Data Type:** char  
**Size:** 1  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** Indicates whether or not the student is a home-schooled student attending class(es) part time.  
**Business Rules:** See Valid Values below.  
A student is defined as Home-Schooled Attending Class Part Time when they are participating in home-based instruction and also are enrolled in a public school for the purpose of taking any course or receiving any ancillary service.  
**Example:** N  
**Valid Values:** Y – Yes  
	N – No  
**Last Updated:** January 2009

####Element B24 - Is Student from a Foreign Country with an F-1 Visa
**Field Name:** IsF1VisaForeignExchangeStudent  
**Data Type:** char  
**Size:** 1  
**Allow NULL?:** No. May not be left blank. Data is required.  
**Description:** Indicate whether or not the student is a foreigner with an F-1 Visa. Only F-1 Visa students are to be marked ‘Y’ in this field. Foreign exchange students are to be marked ‘N’ in this field.  
**Business Rules:** See Valid Values below.  
This data element pertains to students on an F-1 Visa. Students on F-1 Visas do not generate apportionment because someone is paying tuition to the district to enable their enrollment.  
In contrast, foreign exchange students (e.g., J-1 Visa) are in a program that ‘exchanges’ a student from our country with a student from another country. As a result, foreign exchange students are regarded as ‘regular’ students in the district and generate apportionment for the district like any other resident student.  
**Example:** Y or N  
**Valid Values:** N – No  
	Y – Yes  
**Last Updated:** September 2007

####Element B25 - Is Student in Foster Care
**Field Name:** IsStudentInFosterCare  
**Data Type:**  char  
**Size:** 1  
**Allow NULL?:** Yes. This is an optional field.  
**Description:** Indicates if student is currently in the State’s foster care system.  
Attorneys and other advocates who work in the child welfare field are most likely aware that regulations of the U.S. Department of Health and Human Services (USHHS) define the term foster care very broadly. USHHS regulations define “foster care” as follows:  
*“24-hour substitute care for children placed away from their parents or guardians and for whom the State agency has placement and care responsibility. This includes, but is not limited to, placements in foster family homes, foster homes of relatives, group homes, emergency shelters, residential facilities, child care institutions, and preadoptive homes.” 45 C.F.R. §1355.20.*  
**Business Rules:** See Valid Values below.  
**Example:** Y or N  
**Valid Values:** N – No  
	Y – Yes  
**Last Updated:** January 2009

####Element B26 - Graduation Requirements Year
**Field Name:** GradRequirementsYear  
**Data Type:** char  
**Size:** 4  
**Allow NULL?:** Yes. Conditional. See Business Rules. Data is required if the student is in grades 9–12.  
**Description:** The graduation year for which the student is held accountable for meeting the requirements of graduation.  
**Business Rules:** This year will generally be four years after the year the student enters 9th grade.  This year is not to be changed due to IEP or State Transitional Bilingual Instruction plans. If an IEP or State Transitional Bilingual Instruction plan indicates the student may have additional years to meet the requirements of graduation, then the Expected Year of Graduation, [Element B27](#element-b27---student-expected-year-of-graduation), is to be adjusted. In these cases, the student is still held to the graduation requirements that are defined for the year recorded within this Element B27. This must be within a reasonable range between 12 and 25 years of the student’s birth date.  
**Example:** For the school year 2008–2009, enter 2012.  
If a student entered the 9th grade in September of 2003, then this data element should reflect a year of 2007. If that same student has an IEP that indicates that the student’s Expected Year of Graduation, [Element B27](#element-b27---student-expected-year-of-graduation) should be extended to 2008; this data element will remain 2007. This indicates that the student is held to the graduation requirements of the class of 2007, but the student has until 2008 to meet those requirements.  
**Last Updated:** May 2009

####Element B27 - Student Expected Year of Graduation
**Field Name:** ExpectedGradYear  
**Data Type:** char  
**Size:** 4  
**Allow NULL?:** Conditional. Data is required if the student is in grades 9–12.  
**Description:** The year in which the student is expected to graduate.  
**Business Rules:** If the student is in grades 9–12, this data is required. Students shall be assigned an expected graduation year that is four school years greater than the year they begin 9th grade, or for transfer students (out-of-district or out-of-state), based on a transcript evaluation.  
* Special Education students may be assigned an expected graduation year beyond the standard four-year period, and their expected year of graduation can be changed during or prior to the school year in which the student turns 16, if determined by their IEP team. If a student is determined eligible for services after the student turns 16, the IEP team reviews the information and assigns an expected graduation date at the IEP meeting following the eligibility requirement. 
* Students in transitional bilingual education programs may be assigned an expected graduation year beyond the standard four-year period. 
* Migrant students may be assigned an expected graduation year beyond the standard four-year period.

**Student Graduation Requirements:**

* Students must meet the minimum graduation requirements in place for their assigned graduation year. Students entering 9th grade in the 2008–09 school year are assigned a graduation year of 2012 (four years).
* If special education, transitional bilingual, or migrant students have an adjusted expected graduation year, they must meet the requirements of their unadjusted graduation year (9th grade entry plus 4 years).
* Students who take more time or less time to graduate still must meet the graduation requirements for their assigned graduation year, not the year of actual graduation.
* The requirements for the graduation year stay with the students throughout their high school experience regardless of the length of time it takes to graduate.  

If an assignment mistake was made in the original determination of the Please update in your next CEDARS submission. You will receive a ‘critical soft exception’ for each updated expected graduation year.  
**Example:** 2010  
**Last Updated:** May 2009

####Element B28 - Cumulative Grade Point Average
**Field Name:** GPA  
**Data Type:** numeric  
**Size:** 4,3 (Five characters including the decimal point)  
**Allow NULL?:** Yes.  Conditional. Data is required if the student has earned a GPA.  
**Description:** This is the student's cumulative grade point average (GPA) as reported on the state standardized transcript, reported using a numerical range from 0.000 to 4.000.  The GPA must be a “positive” number.  
For GPAs stored in other formats, make the appropriate transformation (WAC 180-57-050, WAC 180-57-055).  
**Business Rules:** See Valid Values below.  
This data element is reported for students in grades 9–12.  
If a student has a zero grade point average because of failure in all classes, the GPA would be reported as 0.000.  
Pass/Fail courses (passed or failed) do not generate a GPA. If only Pass/Fail courses are taken, the data element should be left blank since no numerical GPA has been earned.  
Incoming freshmen might not have GPAs until the end of the first semester/grading period.  
If GPA is not assigned, the GPA may be left blank.  
**Example:** 3.256  
**Valid Values:** 0.000 to 4.000  
**Last Updated:** September 2007  

####Element B29 - Credits Attempted
**Field Name:** CreditsAttempted  
**Data Type:** numeric  
**Size:** 6,2 (Seven characters including the decimal point)  
**Allow NULL?:** Yes. Conditional. See Business Rules.  
**Description:** The total cumulative number of credits the student has attempted for courses earning high school credit.  
**Business Rules:** See Valid Values below.  
This data element is reported for all credits attempted by the student for courses earning high school credit.  
**Example:** 12345.56  
**Valid Values:** 0.00 to 9999.99  
**Last Updated:** May 2009  

####Element B30 - Credits Earned
**Field Name:**  CreditsEarned  
**Data Type:** numeric  
**Size:** 6,2 (Seven characters including the decimal point)  
**Allow NULL?:** Yes. Conditional. See Business Rules.  
**Description:** The total cumulative number of credits the student has earned for high school credit courses.  
**Business Rules:** See Valid Values below.  
This data element is reported for all credits earned by the student for courses earning high school credit.  
If a student has zero credits earned because of failure in all classes, the credits earned would be reported as 0.00.  
Incoming freshmen may have high school credits for courses taken in an earlier grade level.  
**Example:** 1234.56  
**Valid Values:** 0.00 to 9999.99  
**Last Updated:** May 2009  