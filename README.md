## api-automation-assessment

### Prerequisites
..\Jenkins\workspace\RestApiBooks\htmlReports   (should be created) 


### HTML Publisher Plugin for Report in Jenkins Server 
* Manage Jenkins-> 
* Manage Nodes-> 
* Click settings(gear icon)-> 
* click Script console on left and type in the following command: 
* System.setProperty("hudson.model.DirectoryBrowserSupport.CSP", "")  

### Execute windows batch command on Jenkins
```
newman run https://raw.githubusercontent.com/kamuranakcay/api-automation-assessment/master/RestApiBooks/RestApiBooksTest.postman_collection.json  
-e https://raw.githubusercontent.com/kamuranakcay/api-automation-assessment/master/RestApiBooks/RestApiBooksData.postman_environment.json  
-r html --reporter-html-export "htmlReports\%BUILD_TIMESTAMP% - Build %BUILD_ID%.html"    
--reporter-html-template "Template\templateMetro.hbs" 
```
