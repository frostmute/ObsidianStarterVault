---
category:
  - "[[../00 - CATEGORIES/Clippings]]"
feature: "![[../03 - MEDIA & FILES/a1ebfe9c4494585b8517ff35cd219dc5_MD5.png]]"
---

# Cloudant Setup

## Creating an Instance

In these instructions, create IBM Cloudant Instance for trial.

1. Hit the "Create Resource" button.  
    [![step 1](../03%20-%20MEDIA%20&%20FILES/a1ebfe9c4494585b8517ff35cd219dc5_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_1.png)
    
2. In IBM Cloud Catalog, search "Cloudant".  
    [![step 2](../03%20-%20MEDIA%20&%20FILES/6da486227ee2ad511806379796dabbb6_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_2.png)
    
3. You can choose "Lite plan" for free.  
    [![step 3](../03%20-%20MEDIA%20&%20FILES/8537e889538d0d8b2757ec7c014365c6_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_3.png)
    
4. Select Multitenant(it's the default) and the region as you like.  
    [![step 4](../03%20-%20MEDIA%20&%20FILES/96955688428cb67059923c2c2935a25b_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_4.png)
    
5. Be sure to select "IAM and Legacy credentials" for "Authentication Method".  
    [![step 5](../03%20-%20MEDIA%20&%20FILES/c3d37ba8186b2ef3dfd14287f1893424_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_5.png)
    
6. Select Lite and be sure to check the capacity.  
    [![step 6](../03%20-%20MEDIA%20&%20FILES/68ac3f817439b315a9fa5f424e9d641f_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_6.png)
    
7. And hit "Create" on the right panel.  
    [![step 7](../03%20-%20MEDIA%20&%20FILES/67e582d31881417517b96eff6a2a2df2_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_7.png)
    
8. When all of the above steps have been done, open "Resource list" on the left pane. you can see the Cloudant instance in the "Service and software". Click it.  
    [![step 8](../03%20-%20MEDIA%20&%20FILES/9acb9ab50a5455e18768f193a2a85c10_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_8.png)
    
9. In resource details, there's information to connect from Self-hosted LiveSync.  
    Copy the "External Endpoint(preferred)" address. (*1). We use this address later, with the database name.  
    [![step 9](../03%20-%20MEDIA%20&%20FILES/9d7f0da9738cfa0509e33aaeda091d84_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/cloudant_9.png)
    

## Database setup

[[https://github.com/vrtmrz/obsidian-livesync/blob/main/docs/setup_cloudant.md#database-setup]]

1. Hit the "Launch Dashboard" button, Cloudant dashboard will be shown.  
    Yes, it's almost CouchDB's fauxton.  
    [![step 1](../03%20-%20MEDIA%20&%20FILES/8b1bee172cec77881c27236800fafee6_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/couchdb_1.png)
    
2. First, you have to enable the CORS option.  
    Hit the Account menu and open the "CORS" tab.  
    Initially, "Origin Domains" is set to "Restrict to specific domains"., so set to "All domains(*)"  
    _NOTE: of course We want to set "app://obsidian.md" but it's not acceptable on Cloudant._ [![step 2](../03%20-%20MEDIA%20&%20FILES/d247b9b1888b0a44d127b8b366a18561_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/couchdb_2.png)
    
3. Next, Open the "Databases" tab and hit the "Create Database" button.  
    Enter the name as you like (*2) and Hit the "Create" button below.  
    [![step 3](../03%20-%20MEDIA%20&%20FILES/c0da7dd4734c136914c55a06a9841a28_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/couchdb_3.png)
    
4. If the database was shown with joyful messages, the setup is almost done.  
    And, once you have confirmed that you can create a database, usually there is no need to open this screen.  
    You can create a database from Self-hosted LiveSync. [![step 4](../03%20-%20MEDIA%20&%20FILES/d14730b534bf2970016ccd11bd64f150_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/couchdb_4.png)
    

### Credentials Setup

[[https://github.com/vrtmrz/obsidian-livesync/blob/main/docs/setup_cloudant.md#credentials-setup]]

1. Back into IBM Cloud, Open the "Service credentials". You'll get an empty list, hit the "New credential" button.  
    [![step 1](../03%20-%20MEDIA%20&%20FILES/fe123628631432023196aaca4fb4d417_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/credentials_1.png)
    
2. The dialog to create a credential will be shown.  
    type any name or leave it default, hit the "Add" button.  
    [![step 2](../03%20-%20MEDIA%20&%20FILES/c2918fffbe23fbdfad6e1da157bd2d1f_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/credentials_2.png)  
    _NOTE: This "name" is not related to your username that uses in Self-hosted LiveSync._
    
3. Back to "Service credentials", the new credential should be created.  
    open details.  
    [![step 3](../03%20-%20MEDIA%20&%20FILES/d592b8ddfb1ec0f831c329c54beed34b_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/instruction_images/credentials_3.png)  
    The username and password pair is inside this JSON.  
    "username" and "password" are so.  
    follow the figure, it's  
    "apikey-v2-2unu15184f7o8emr90xlqgkm2ncwhbltml6tgnjl9sd5"(*3) and "c2c11651d75497fa3d3c486e4c8bdf27"(*4)
    

## Self-hosted LiveSync settings

[[https://github.com/vrtmrz/obsidian-livesync/blob/main/docs/setup_cloudant.md#self-hosted-livesync-settings]]

[![Setting](../03%20-%20MEDIA%20&%20FILES/d53c95aa35f5b47d4e863788ded5c1db_MD5.png)](https://github.com/vrtmrz/obsidian-livesync/blob/main/images/remote_db_setting.png)

The Setting should be as below:

|Items|Value|example|
|---|---|---|
|URI|(*1)|[https://xxxxxxxxxxxxxxxxx-bluemix.cloudantnosqldb.appdomain.cloud](https://xxxxxxxxxxxxxxxxx-bluemix.cloudantnosqldb.appdomain.cloud/)|
|Username|(*3)|apikey-v2-2unu15184f7o8emr90xlqgkm2ncwhbltml6tgnjl9sd5|
|Password|(*4)|c2c11651d75497fa3d3c486e4c8bdf27|
|Database name|(*2)|sync-test|