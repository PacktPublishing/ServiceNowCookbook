# Understand web services 

Out of box, service-now provide many channels to communicate with outside world.  Service-Now is capable enough to communicate over HTTP based web services. It�s is advisable to use MID (Management, Instrumentation, and Discovery) server as it facilitates communication between service-now platform and external applications. 

## Getting ready 
To step through this recipe, you should have active instance and valid credentials with admin/web services role.  
How to do it...
1.	Open any standard web browser & type instance address. 
2.	Login in service-now instance with valid credentials.
3.	Let's understand some basics first as follows. 
    1.	Consumer (Outbound): The consumer service of web services allowed to interact with published web services and perform create, read, update and delete operations based on WSDL (short for web service description language) and ACL. To send SOAP and Rest message to external system following method can be used. 
		*  Outbound Rest
		*  Outbound SOAP
    2.  Publisher (Inbound): By inbound web service of service-now, 3rd party system can make a request to get information from service-now tables or in better words I shall say by this type of web services, you can access and modify service-now table�s data through any client application. 
		*  Direct web services 
		*  ODBC Driver
		*  Import Set
		*  Scripted web services 
4.	Now on left hand side, in the search box type web services and service-now will search out System Web Services Application as follows.
	*  Web services 
5.	System Web services application have many modules but we will take a look at key ones only.
6.	Now, to create a new inbound web service, click on Create New Module under Inbound as follows.
    *  Inbound web services
	1.	After clicking, you will able to see web service configuration page where you need to enter following fields. 
		*  Label: Incident  Inbound Web Service
		*  Name: u_incident__inbound_web_service
		*  Copy field from target table : True
		*  Create transform map : true
		*  Target table : Incident
	*  Inbound web service configuration part 1
	2.	Click on Create button to create Incident Inbound Web Service. 
	3.	After clicking on Create button. A new web service Incident Inbound Web Service will be added in System Web Services application as given below. 
	*  New web service Incident Inbound Web Service 
	4.	Now, click on Incident Inbound Web Service and after clicking it you will able to see screen as shown below now create necessary transform map for web service for determining the relationship between two systems .It is important to note that if you don�t� want to run any business run then uncheck button and click on Auto Map Matching Field button.
	*  Table transform map
	5.	After clicking on Auto Map Matching Field button, you will able to see all fields on incident table in Field Maps section. Now, mark number field as Coalesce as follows and click on Update button.
	*  Field Maps
	6. 	Now, click on Incident Inbound Web Service again to view the WSDL of web service.
	*  WSDL
	7.	If you click on https://dev17372.service-now.com/u_incident__inbound_web_service.do?WSDL then you will able to see XML format of web service. 
	8.	Now create appropriate ACL and add role (REST) to web service user for Incident Inbound Web Service, web service for external system so that external system can insert data in service-now instance without any issues.
	9.	Now you can share this WSDL with external system or users to perform necessary actions. 
	10.	 It is important to note, you can view all the data which is coming to the web service by clicking on Input Row button for troubleshooting purpose.
	*  Import Rows 

See also
To read about the outbound soap web services click below link http://wiki.servicenow.com/index.php?title=Outbound_SOAP_Web_Service#gsc.tab=0