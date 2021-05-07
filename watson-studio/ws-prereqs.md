## Checking and setting pre-requsites for Watson Studio

Watson Studio requires a Cloud Object Storage (COS) service where it stores its projects, assets, and other artefacts. 
When you work on IBM Cloud Accounts with more complex structures Watson Studio might not be able to create or
link to an Cloud Object Storage service with proper priviledges. To assure Watson Studio can initialize successfully follow these steps:

### Assure COS service

In the resource list, check whether a COS service exists and is accessable for you. 

*  If none exists, create one.
   *  You might need to create a COS service in standard plan in case a lite service already exists in your account and in not accessible for you. 
   *  Assure the COS service is either global on in the region where you want to use your Watson Studion service.
   *  If you cannot create a COS service, check your privileges with your IBM Cloud account owner.
 * If a COS service exists, assure you have proper privileges to use it:
   *  Confirm that you can create a new test bucket on the COS service.
   *  In case you cannot, create a new COS service for you.

