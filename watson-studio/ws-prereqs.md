## Checking and setting pre-requisites for Watson Studio

Watson Studio requires a Cloud Object Storage (COS) service where it stores its projects, assets, and other artefacts. 
When you work on IBM Cloud Accounts with more complex structures with regards to access groups and privileges,
Watson Studio might not be able to create or
link to an Cloud Object Storage service with proper privileges. To assure Watson Studio can initialize successfully take care of the following:

### Assure COS service with proper privileges

In the resource list, check whether a COS service exists and is accessable for you. 

*  If none exists, create one.
   *  You might need to create a COS service in standard plan in case a lite service already exists in your account and is not accessible for you (even though you might not be able to see the lite plan COS service in the resource list because of limited privileges). 
   *  Assure the COS service is either global or in the region where you want to use your Watson Studio service.
   *  If you cannot create a COS service, check your privileges with your IBM Cloud account owner.
 * If a COS service exists, assure you have proper privileges to use it:
   *  Confirm that you can create a new test bucket on the COS service.
   *  In case you cannot, create a new COS service.

### Settings when starting Watson Studio for the first time

When you start Watson Studio for the first time like instructed in Step 1 in the [tutorial](watson-visualization.md), 

1.  Make sure you associate it with the right account, and
2.  Under Services to provision, select Watson Knowledge Catalog and do *not* select Cloud Object Storage.
  
It should look similar to this screenshot:

<img src="https://user-images.githubusercontent.com/35991100/117416266-76f8eb80-af19-11eb-8c59-b5d15b71d2ad.png" alt="drawing" width="75%"/>

When Watson Studio now initializes, it selects your COS service that you assured above:

<img src="https://user-images.githubusercontent.com/35991100/117417192-5f6e3280-af1a-11eb-88a2-51155a48f32e.png" alt="drawing" width="75%"/>

