---
lab:
    title: 'Lab 6 - Monitor and Debug Flows'
    module: 'Module 6 - Troubleshooting'
---

# Troubleshooting

## Scenario

In this lab, you will learn how to monitor and debug desktop flows.

## High-level lab objectives

-   Monitor desktop flows

-   Debug desktop flows

-   Add retry to desktop flow

# Exercise \#1: Monitor flows

In this exercise, you will monitor desktop flows.

## Task \#1: Monitor desktop flows

1.  Navigate to <https://make.powerautomate.com/> and make sure you are
    in your dev environment.

2.  Click on **More** and select **Discover all**.

> <img src="../L06/media/image1.png" style="width:4.03825in;height:2.19688in"
> alt="Select more and discover all" />

3.  Under **Monitor** select **Desktop flow runs**.

> <img src="../L06/media/image35.png" style="width:4.03825in;height:2.19688in"
> alt="Select more and discover all" />

4.  If you don’t see anything, make sure you are in your Dev
    environment.

5.  Turn on **Auto refresh**.

> <img src="../L06/media/image2.png" style="width:3.09336in;height:1.12486in"
> alt="enable auto-refresh" />

6.  Click on the ellipses of one the **Woodgrove
    Funding Manager Draw** run and select **See parent flow run**.

> <img src="../L06/media/image3.png" style="width:5.65652in;height:1.84381in"
> alt="select and complete as described" />

7.  You should see the parent cloud flow run (CF Manage Woodgrove
    Funding Process).

> <img src="../L06/media/image4.png" style="width:5.55648in;height:2.80377in"
> alt="review the screen" />

8.  Click on the browser back button.

9.  Click to open the **Woodgrove Funding Manager Draw** run.

> <img src="../L06/media/image5.png" style="width:5.55876in;height:1.56667in"
> alt="select as described" />

10.  You should see all the actions in the flow run.

> <img src="../L06/media/image6.png" style="width:6in"
> alt="review the screen" />

11. Click on the start timestamp to open the **Set variable** action.

> <img src="../L06/media/image7.png" style="width:5.40955in;height:1.59108in"
> alt="select as described" />

12. Go to the **Action Details** pane and click **See output details**.

> <img src="../L06/media/image8.png" style="width:5.90681in;height:2.16141in"
> alt="select as described" />

13. You should see details of the variable.

> <img src="../L06/media/image9.png" style="width:5.44663in;height:1.52401in"
> alt="review the details" />

14. Close the **Outputs** pane.

15. You may wish to review the other actions.

## Task \#2: Flow monitor

1.  Launch **Power Automate for desktop**, make sure your dev
    environment is selected.

2.  Click **Settings**.

> <img src="../L06/media/image10.png" style="width:5.54165in;height:0.91236in"
> alt="select as described" />

3.  Click on the **Monitoring/Notifications** dropdown, select **Flow
    monitoring window**, and click **Save**.

> <img src="../L06/media/image11.png" style="width:3.01474in;height:3.66762in"
> alt="select as described" />

4.  Close the **Settings** pane.

5.  Run the **Perform Site Inspection**.

> <img src="../L06/media/image12.png" style="width:4.50233in;height:1.19677in"
> alt="select as described" />

6.  Click **OK**.

> <img src="../L06/media/image13.png" style="width:4.55088in;height:2.62674in"
> alt="select as described" />

7.  Notice the monitor. Click **Pause**.

> <img src="../L06/media/image14.png" style="width:2.9443in;height:1.75614in"
> alt="select as described" />

8.  The flow should pause. Click **Resume**.

> <img src="../L06/media/image15.png" style="width:2.83949in;height:1.63204in"
> alt="select as described" />

9.  Click **Stop**. The flow should stop, and the monitor should
    disappear.

# Exercise \#2: Debug flows

## Task \#1: Debug flow

1.  Go to Power Automate desktop flow and run the **Perform Site
    Inspection** flow again.

2.  Enter **456 Main Street** for Address and click **OK**.

> <img src="../L06/media/image16.png" style="width:4.02111in;height:2.30399in"
> alt="select and complete as described" />

3.  Wait for the flow to finish running.

4.  The flow should fail, and you should see an error in the
    notification.

> <img src="../L06/media/image17.png" style="width:3.51521in;height:2.05119in"
> alt="review the details" />

5.  Click **Edit** flow.

> <img src="../L06/media/image18.png" style="width:5.3426in;height:1.59764in"
> alt="select and complete as described" />

6.  Add a breakpoint on the first press button action. Clicking to the
    left of the line number will add a breakpoint.

> <img src="../L06/media/image19.png" style="width:6.34411in"
> alt="add the breakpoint" />

7.  Edit the property address variable and change the default value to **456 Main Street**.

8.  Click **Run**.

9.  The flow will pause when the breakpoint is hit. Click **Run next
    action**.

> <img src="../L06/media/image20.png" style="width:5.09983in;height:3.1231in"
> alt="select run next action" />

10. The flow should advance to the next action and pause again. Click
    **Run next action** again.

11. Click **Run next action** until the flow fails.

> <img src="../L06/media/image21.png" style="width:5.61447in;height:2.00525in"
> alt="select and complete as described" />

## Task \#2: Add retry

1.  Click **Subflows** and select + New subflow.

> <img src="../L06/media/image22.png" style="width:3.49932in;height:1.84952in"
> alt="select and complete as described" />

2.  Enter **WaitFlow** for name and click **Save**.

3.  Go to the **Actions** pane, search for **wait** and double click on
    the **Wait** action.

> <img src="../L06/media/image23.png" style="width:3.16957in;height:1.75135in"
> alt="select and complete as described" />

4.  Enter **60** and click **Save**.

> <img src="../L06/media/image24.png" style="width:5.13309in;height:2.13168in"
> alt="select and complete as described" />

5.  The subflow should now have one wait action. Select the **Main**
    tab.

> <img src="../L06/media/image25.png" style="width:5..5in;height:1.8in"
> alt="select and complete as described" />

6.  Go to the **Actions** pane, search for **error**, drag **On block
    error** action, and place it after the **Get details of element on
    web page** for the **JobNumber** action.

> <img src="../L06/media/image26.png" 
> alt="select and complete as described" />

7.  Enter **RetryOnError** for Name, click **+ New rule**, and select
    **Run subflow**.

> <img src="../L06/media/image27.png" style="width:3.69774in;height:1.88284in"
> alt="select and complete as described" />

8.  Select the **WaitFlow** you created and click **Continue flow run**.

> <img src="../L06/media/image28.png" style="width:3.47332in;height:1.87211in"
> alt="select and complete as described" />

9.  Select **Go to beginning of block** for Exception handling mode and
    click **Save**.

> <img src="../L06/media/image29.png" style="width:3.34968in;height:2.27785in"
> alt="select and complete as described" />

10. Click to select the action below the error block.

> <img src="../L06/media/image30.png" style="width:3.75594in;height:1.43617in"
> alt="select and complete as described" />

11. Hold the **\[SHIFT\]** and click to select the **End** loop action.

> <img src="../L06/media/image31.png" style="width:4.53475in;height:3.09245in"
> alt="select and complete as described" />

12. Drag all the selected actions and drop them inside the error block.

13. The **On block error** action should now look like the image below.

> <img src="../L06/media/image32.png" style="width:4.80585in;height:3.85032in"
> alt="review the screen" />

14. Click **Save** and wait for the flow to be saved.

## Task \#3: Test 

1.  Remove the breakpoint and Click **Run**.

2.  The flow will switch to the subflow if error occurs.

> <img src="../L06/media/image33.png" style="width:5.24168in;height:1.1525in"
> alt="watch the flow run" />

3.  The flow will go back to the main flow after **60** seconds.

4.  The process should complete successfully.

> <img src="../L06/media/image34.png" style="width:61in"
> alt="review completed flow run" />
