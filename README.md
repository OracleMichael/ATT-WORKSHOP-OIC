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
2. **Click** the hamburger menu Ξ (looks like three stacked horizontal lines) and select **Autonomous Transaction Processing**.
![](images/1.1.2.png)
3. On the left, change the **compartment** to "att_workshop". Then, click on the ATP instance called "ATP_WORKSHOP". _Make sure your region is "US East (Ashburn)" or you will not see the instance._
![](images/1.1.3.png)
4. Click the button called **DB Connection**. This will give you a pop-up wizard to download the wallet. Keep the wallet type as "Instance Wallet" and add a password for the wallet.
![](images/1.1.4.1.png)
![](images/1.1.4.2.png)
