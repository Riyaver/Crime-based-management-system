# Crime-based-management-system
The project undertaken is a ‘Crime reporting management system’.

The following are the tables (entities) created along with their assumption for their attribute.
1)Crime_reporting table: This table is for the person who will be filing the report. it includes the report_id which is a primary key , name character datatype default as ‘anonymous’, gender char whose default value is null, phone number default null and address, default null, of the person who is reporting the crime as well as includes the date and time when the case was reported.

2)Admin_table: Admin table is used to check the team and team leader assigned, the police station in which report was filed and includes the court which will oversee the case. Here, the team leader and their team cannot be null. And uses admin_id which references the repot_id of crime_reporting table. 

3)Crime_information: this table includes all the information related to the crime such as the evidence, the time and place where the crime occurred, the place cannot be null, it contains a   crime_info_report_id which references report_id from crime_reporting and a primary key crime_info_id.

4) Crime_type: This table has the information regarding the type of crime which has occurred, it includes crime_type_id which references crime_reporting table, crime_id which is a primary key and the id of the type of crime, and name of the crime with its description. The name of the crime cannot be null.
   
5)Criminal_information: this table includes the information about the criminal for example type of crime committed, to which case (report_id) he/she is linked to, and basic details such as name, age, gender, address and it also includes appearance and  photograph of criminal which uses check constraint for range 0 and 1, if the data is 1 then photograph is criminal is available otherwise not.

6)  Victim_information: this contains the information of victim such as name, age, gender, address, the condition of victim, etc. it also includes the relation of victim to the person who is filing the report, it cannot be null.

7)Location: it tells us about the location of crime such as house number, street, sector, pincode, etc

8)Status_of_case: this is the final table (entity) which tells us about the current status of the case filed. Whether all the evidence is collected or not, whether the criminal is arrested or the case is still pending. For these attributes, data type int is given and range of 0 to 1 is set using check constraint because of that, the only allowed values are 0 or 1, where 0 if for false and 1 is for true 


DESIGN OF THE PROJECT
<img width="939" height="678" alt="image" src="https://github.com/user-attachments/assets/af295599-0545-40e9-8660-abd5624658b6" />



