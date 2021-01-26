# ATT_WORKSHOP-OIC

This repository houses the materials for the hands-on portion of the workshop.

## Prerequisites

- Set up your workshop user. This generally consists of clicking the link in your email with subject "Please Reset Your Password for Your atttglobalnetworkservice Account"
- Make sure you are able to log in to Oracle Integration Cloud (OIC). Your workshop instructor will provide you the link to the **OIC home page**.
- Once you are able to log in to OIC, make sure you can create a connection and an integration.

With these steps you are good to go!

## Part 1: Connecting to ATP

This part handles the "non-optional" part of the lab. It is our objective to make sure every lab attendee is able to complete this integration.

### **Step 1: Create the ATP Connection**

First, you will need to retrieve the wallet file.
1. Log in to **cloud.oracle.com**.
![](images/1.1.1.png)
2. **Click** the hamburger menu Ξ (looks like three stacked horizontal lines) in the upper left corner and select **Autonomous Transaction Processing**.
![](images/1.1.2.png)
3. On the left, change the **compartment** to "att_workshop". Then, click on the ATP instance called "ATP_WORKSHOP". _Make sure your region is "US East (Ashburn)" or you will not see the instance._
![](images/1.1.3.png)
4. Click the button called **DB Connection**. This will give you a pop-up wizard to download the wallet. Keep the wallet type as "Instance Wallet" and add a password for the wallet. **Remember this password, you will use it to create the connection later in this step.**
![](images/1.1.4.1.png)
![](images/1.1.4.2.png)
Now that you have the wallet file, you can create the connection.
5. Navigate to the integration home page.
![](images/1.1.5.png)
6. **Click** the hamburger menu in the upper left corner and select **Integrations**, then **Connections**.
![](images/1.1.6.png)
7. **Create** a connection (upper right corner), then after the dialog box pops up, search for "ATP" and select the "Oracle ATP" adapter.
![](images/1.1.7.png)
8. In the wizard, give the connection a name, then click **Create**. We recommend that you add your name to the name to differentiate it from connections created by other workshop attendees. Then click **Create**.
![](images/1.1.8.png)
9. Perform the following:
  - **Click** the upload button (square button with up arrow) and upload the wallet file you downloaded. This should be the entire zip file.
  - For the **Wallet Password**, type the password you provided when you downloaded the wallet file.
  - For the **Database Service Username**, type "ADMIN".
  - For the **Database Service Password**, your workshop instructor will provide you with the admin password.
  - Finally, right above the security section, for the not-so-optional "Service Name (optional)" enter "atpworkshop_high". _Note: to locate a list of valid service names, unzip the wallet file, then open the tnsnames.ora file._
![](images/1.1.9.png)
10. Once you are done with the above, click "Test". The connection should give you a green banner notification, and the connection should show as 100% configured (100% in a blue oval). **Save** your connection.
![](images/1.1.10.png)

### **Step 2: Initialize the integration**

1. **Click** the hamburger menu in the upper left corner and select **Integrations**, then **Connections**.
![](images/1.2.1.png)
2. **Create** an integration (upper right corner), then after the dialog box pops up, select "Scheduled Orchestration".
![](images/1.2.2.png)
3. In the wizard, give the integration a name, then click **Create**. We recommend that you add your name to the name to differentiate it from integrations created by other workshop attendees. Then click **Create**. _The description is optional, but for your convenience: "This integration queries a table in ATP, then row-by-row modifies the data and updates the table in ATP."_
![](images/1.2.3.png)
_Note: for a better integration experience, we recommend you change the layout to "horizontal" and to click the reset button if your integration becomes too messy._
![](images/1.2.aux1.png)

### **Step 3: Invoke ATP to retrieve data**

1. 
