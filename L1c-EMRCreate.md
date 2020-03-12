# Launch an EMR Cluster

## Create a Cloud9 Development Environment

### Navigate to the EMR Console

* In the AWS Console, use the Services menu and navigate to the EMR console.  One way to do so, is to expand the Services top menu and type "EMR" in the service search field.

Hint: use a different browser tab than you are using for your Cloud9 Development Environment, as we will be returning to Cloud9 multiple times.

![screenshot](images/EMR1.png)

### Create an EMR Cluster

* Click "Create cluster"

![screenshot](images/EMR2.png)

* Click on "Go to advanced options"

![screenshot](images/EMR3.png)

* Ensure that these components are checked: Hadoop, Hive, Spark, Tez, Pig

![screenshot](images/EMR4.png)

* Leave the rest of the page at their defaults and click Next

![screenshot](images/EMR5.png)

* Leave the Hardware Configuration page at their defaults and click Next

![screenshot](images/EMR6.png)

* Leave the General Options page at their defaults and click Next

![screenshot](images/EMR7.png)

* On the Security Options page, choose the EMRKeyPair in the EC2 key pair drop-down.

![screenshot](images/EMR8.png)

* Then click "Create cluster"

![screenshot](images/EMR9.png)

* Your cluster will start creating:

![screenshot](images/EMR10.png)

### Update the Security Group for the Master Node

* Click on the link for the Security groups for Master to launch the EC2 Security Groups console page in a new browser tab

![screenshot](images/EMR11.png)

* On the Security Group page, click the checkbox in front of the master (ElasticMapReduce-master)

![screenshot](images/EMR12.png)

* In the bottom pane, click "Inboud rules" tab.  Then click the "Edit inbound rules" button

![screenshot](images/EMR13.png)

* Scroll to the bottom of the page and click the "Add rule" button

![screenshot](images/EMR14.png)

* For the new rule, pick SSH from the first drop down.  Leave the second drop-down as Custom.  In the Source field to the right, start typing "sg".  This will pop-up a list of your Security Groups.  Pick the one that begins AWS-Cloud0-EMR-day.

![screenshot](images/EMR15.png)

* Then click "Save rules"

![screenshot](images/EMR16.png)

### Connect to your EMR Cluster

* Return to your EMR Console tab in your browser.  Your cluster should likely now say "Waiting Cluster ready".  You may also need to click the refresh icon on the right hand side of the page to refresh the details.  If it does not yet say Waiting, then wait a bit longer (or ask your instructor)

![screenshot](images/EMR17.png)

* Click on the SSH link next to your Master public DNS field

![screenshot](images/EMR18.png)

* Select the Mac/Linux tab.  Then highlight the ssh command and copy it to your clipboard

![screenshot](images/EMR19.png)

* Now return to your Cloud9 browser tab and paste the command into your Terminal tab inside the Cloud9 environment

![screenshot](images/EMR20.png)

* Hit enter to run the ssh command.  Type in yes when prompted.


![screenshot](images/EMR21.png)


## Congratulations - you have created an EMR Cluster and connected to it via SSH
Please continue to the [next section](L2a-S3.md).
