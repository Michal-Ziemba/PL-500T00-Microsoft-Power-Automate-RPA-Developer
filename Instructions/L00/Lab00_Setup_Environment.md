---
lab:
    title: 'Lab 0 - Setup and environment preparation'
    module: 'Module 0 - Setup'
---

# Setup the lab environment

**⏱️ The estimated time to complete this lab is 30 minutes.**

Attention to MCTs: Please make sure you are familiar with
the TrainerPrepGuide for this course, especially the teaching tips and
recommendations. 

## WWL Tenants - Terms of Use
If you are being provided with a tenant as a part of an instructor-led training delivery, please note that the tenant is made available for the purpose of supporting the hands-on labs in the instructor-led training.
Tenants should not be shared or used for purposes outside of hands-on labs. The tenant used in this course is a trial tenant and cannot be used or accessed after the class is over and are not eligible for extension.
Tenants must not be converted to a paid subscription. Tenants obtained as a part of this course remain the property of Microsoft Corporation and we reserve the right to obtain access and repossess at any time. 

## Introduction

Let's get started. In this first lab, you will ensure you have access to a Power Platform 
trial tenant and access the Power Platform admin center. In the admin 
center, you will create the environments for use during the course.

You will also see the Power Automate Desktop application and install .NET 
and Browser extension pre-requisities which are required for the remainder 
of the course. 


## Exercise 1 - Verify your Power Platform trial tenant

In this exercise, you will verify access to the Power Apps Maker portal in a Dev environment.

### Task 1 – Acquire your Power Platform trial tenant

1.  Verify that you have your **Microsoft 365 credentials** from the Authorized Lab Host available. 

2.  In a new browser tab, navigate to `https://make.powerapps.com`

3.  Enter the `email address` provided by the Authorized Lab Host. 

4.  Select **Sign in**. 

5.  Enter the `password` provided by the Authorized Lab Host. 

6.  Optionally, select **Yes** to stay signed in.

7.  If prompted, enter `0123456789` for **Phone number** and select **Submit**.

8.  **Refresh** the tab and verify the **Dev One** environment is selected under **Environment** in the top right. 

    > **Note:** For the rest of this course when it says Dev environment, it will be referring to this **Dev One** environment. This is where you will do most of the development steps for this course.


### Task 2 - Intialize OneDrive for Business

1.  Select the **App launcher** menu from the top left and under **Apps**, select **OneDrive**. A new tab will load.

2.  **Wait** while Microsoft initializes your OneDrive. Select **Your OneDrive is ready**. **Close** the tab.


## Exercise 2 - Create a Test environment

In this exercise, you will create a Test environment for deploying your work to later on.

### Task 1 – Create a Test environment

1.  In a new browser tab, navigate to `https://aka.ms/ppac`

2.  Select **Get Started** and select **Environments** from the left navigation.

3.  Select **+ New**.

4.  In the **New environment** pane, enter `Test Two` for **Name**.

5.  Change the **Type** drop-down to **Developer**.

6.  Select **Next** and select **Save**.

    > Note: It may take a couple of minutes for the new environment to be provisioned and become available in the list of the environments.

7.  Refresh the **Environments** list.

8.  When your environment shows as 'Ready', select the **Test** environment by selecting the ellipsis (...) menu and selecting **Settings**. 

9.  Explore the different areas available in **Settings** but do not make any changes yet. 


## Exercise 3 - Power Automate Software 

In this excercise, you will be configuring Power Automate Desktop and accompanying applications.

### Task 1 - Configure Power Automate Desktop 

Power Automate Desktop is installed by default on Windows 11, but you will need to sign in and configure the environment. 

1.  Search the **Start** menu for `Power Automate` and open the **Power Automate** app. 

2.  When Power Automate Desktop opens, sign in using your Office 365 Tenant credentials. Select **Next** and **Get started**. 

    > Optional: Select **Start tour** and go through the welcome prompts to get a feel for the application. 

3.  From the **Environments** list, select the **Dev One** environment. 


### Task 2 - Configure the Power Automate Machine-Runtime App 

To run attended and unattended flows across cloud and desktop environments, the **machine-runtime app** needs to be configured. 

1.  In Power Automate Desktop, select **⚙️ Settings**. Under Machine settings, select **Open machine settings**. 

2.  On the **Machine settings** screen, select the **Dev One** environment. The machine-runtime app will register the machine in the Dev environment's Dataverse database. You should see a success notification "Your machine XXXXYYX has been registered". 

    > **Note:** If you get an error stating a premium license is required; in the notification, select the **💎 Go premium** button and select **Start trial** then dismiss the notification.

3.  Once it has connected, you can close the **Power Automate machine runtime** window. 



## Exercise 4 – Copy Lab Resources 

1.  Create a folder **Labs** on the **C:** drive, if you don't already have that folder.

2.  Copy the lab resources folder to **C:\Labs**, if it doesn't already exist.

3.  Browse to **C:\Labs\Resources\Funding manager app** and double-click on the **Woodgrove Bank Funding Manager.exe** executable.

4.  Select **Yes** on the download .NET popup.

    <img src="../L00/media/image5.png" alt="Screenshot showing the download .NET dialog" />

5.  Select open file on the downloaded .exe file in the browser downloaded file list. 

6.  Select **Install** and wait for the installation to complete.

    <img src="../L00/media/image7.png" alt="Screenshot showing the .NET Windows desktop runtime installation wizard" />

7.  Select **Close** after the installation completed and **close** the browser tab.

8.  Browse to **C:\Labs\Resources\Funding manager app** and double-click
    on the **Woodgrove Bank Funding Manager.exe** executable file again. 

    <img src="../L00/media/image8.png" alt="Screenshot showing the Woodgrove Bank Funding Manager.exe file" />

9.  The app should launch. **Close** the application.

