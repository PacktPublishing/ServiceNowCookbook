# ServiceNow Cookbook
This is the code repository for [ServiceNow Cookbook](https://www.packtpub.com/networking-and-servers/servicenow-cookbook?utm_source=github&utm_medium=repository&utm_content=9781785880520), published by Packt. It contains all the supporting
project files necessary to work through the book from start to finish.

## About the Book
This book will help you build data-driven apps and it will also explore development best practices. You will learn to set up email notifications for users and work with the database view for reporting. Next, the book will guide you through creating various tasks from the workflow and show you how to make the most of the workflow utilities available in ServiceNow. Finally, the book will drive you through the auditing and diagnosing aspects of ServiceNow.

## Instructions and Navigation
All of the code is organized into folders. The commands and instructions will look like the following:

```javascript
    function onSubmit() 
    {
     // get contract end date
     var con_end = g_form.getValue('u_contract_end_date');
 
     // get contract start date
     var sat_date = g_form.getValue('u_contract_start_date');	
	
     // check if contract end date is earlier than start date

     if(sat_date > con_end)
	  
	   {
		  // alert for user 
		  alert("Please select valid contract end date. Contract end     date cannot be in past");
		 
		  // highlight necessary field on form
		  
      g_form.flash("u_contract_end_date", "#FF0000", 10);
		  
		  // don't allow submission of form
		  return false;
	   }
     }
```

## Related products:
* [Mastering ServiceNow - Second Edition](https://www.packtpub.com/virtualization-and-cloud/mastering-servicenow-second-edition?utm_source=github&utm_medium=repository&utm_content=9781786465955)
* [Learning ServiceNow](https://www.packtpub.com/networking-and-servers/learning-servicenow?utm_source=github&utm_medium=repository&utm_content=9781785883323)
* [Mastering ServiceNow](https://www.packtpub.com/networking-and-servers/mastering-servicenow?utm_source=github&utm_medium=repository&utm_content=9781782174219)

### Suggestions and Feedback
[Click here](https://docs.google.com/forms/d/e/1FAIpQLSe5qwunkGf6PUvzPirPDtuy1Du5Rlzew23UBp2S-P3wB-GcwQ/viewform) if you have any feedback or suggestions. 
