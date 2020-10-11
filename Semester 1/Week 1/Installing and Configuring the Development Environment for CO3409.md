# Installing and Configuring the Development Environment for CO3409

This will guide you through configuring the development environment we will be using for the module. This guide is designed for you to install the development enviroment on either your own machine (assuming it is running Microsoft Windows) or a virtual machine. 

**Please Note: ** 

- Take care to read the instructions carefully and pay particular attention to versions of the required software.
- If you are using the Azure lab virtual machine. The JDK, Netbeans and Payara are already installed and located at the root of the C drive. If this is the case **You may proceed directly to step 4.** 



## Step 1 - 	Install Java Software Development Kit

Currently, NetBeans and Payara only run on Java JDK 8. Install the SDK (Software Development Kit), not the JRE (run-time environment).

Download and install either the Oracle version (https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) or the Zulu version (https://www.azul.com/downloads/zulu/ )

Next we need to ensure that your ` Java Home` environment variable is set correctly. To do this follow the steps below.

1.  In Windows Explorer, right click on **This PC** and select **Properties** > **Advanced System Settings**..

2. On the Advanced tab, select Environment Variables, and then edit **JAVA_HOME** to point to where the JDK software is located, for example, C:\Program Files\Java\jdk1.8.0_51.

   

## Step 2 - Install Netbeans

Development of NetBeans has been taken over by Apache. This module requires you to use NetBeans 11.0. It can be downloaded from [Here](https://archive.apache.org/dist/incubator/netbeans/incubating-netbeans/incubating-11.0/incubating-netbeans-11.0-bin.zip) .

1. Run the installer. Once it has finished launch Netbeand and in the menu bar click **Tools > Java Platform** and ensure the JDK 8 is chosen.



## Step 3 - Download and Install Payara Server

1. Download Payara Server from https://www.payara.fish/software/downloads/. Unzip the Payara Server into a folder with no spaces in its name (e.g. C:\Users\<yourname>\Documents\payara)

2. Download Payara Server Micro from https://www.payara.fish/software/downloads/. Save the jar in a folder.

   

## Step 4 - Install Payara Plugins and Payara Server into Netbeans

To Install the Payara server into NetBeans see https://blog.payara.fish/adding-payara-server-to-netbeans for a detailed step by step guide. Alternatively follow the instructions below.

1. Run NetBeans and Click **Tools** > **Plugins**
2. Search for 'Payara' in the **Available Plugins** tab. Check all the available checkboxes, which includes the main plugin and common libraries for working with Payara Server.
3. Click **Finish** and restart NetBeans
4. Next, Click **Tools**>**Servers** and click **Add Server**.
5. Select Payara Server, and name the server, Payara. 
6. Select the location of directory to which you extracted the Payara Server. Read and accept the license agreement. Click **Next**.
7. Select the default local domain, **domain1**. Enter 'admin' as the username and leave the password field blank.
8. Then close the window