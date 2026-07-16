# Amazon EC2 Compute Lab

## Project Description
In this lab, I gained hands-on experience launching, configuring, and managing an Amazon Elastic Compute Cloud (EC2) instance. The project involved setting up a virtual server, bootstrapping an Apache web server, modifying network security groups to allow public web traffic, resizing the instance type, and safely terminating the resources. 

## Step-by-Step Project Guidelines

### Step 1: Launching and Configuring the EC2 Instance
* **Action:** I initiated the launch of a new EC2 instance, selecting the appropriate Amazon Machine Image (AMI) and instance type. I configured the network settings to place the instance inside the designated Lab VPC and added a bash script in the "User data" section to automatically install and start an Apache web server upon boot.
* **Proof:** ![Instance Configuration](Screenshots/1%20EC2%20Configuration.png)

### Step 2: Monitoring the Instance Status
* **Action:** After launching, I navigated to the EC2 Instances dashboard to monitor the initialization process. I verified that the instance state transitioned to `Running` and that it successfully passed both the system and instance status checks.
* **Proof:** ![Running Instance](Screenshots/2%20Running%20Instance.png)

### Step 3: Updating Security Groups & Accessing the Web Server
* **Action:** By default, the web server was not accessible from the internet. I modified the attached Security Group's inbound rules to allow HTTP traffic (Port 80) from anywhere (`0.0.0.0/0`). I then copied the instance's Public IPv4 address and successfully accessed the test webpage in my browser.
* **Proof:** ![Web Server Access](Screenshots/3%20WebSeverAccess.png)

### Step 4: Resizing the Instance
* **Action:** To demonstrate vertical scaling, I stopped the running instance, changed its instance type (e.g., to a `t3.small`), and increased its Elastic Block Store (EBS) volume size. Once modified, I restarted the instance to apply the hardware changes.

### Step 5: Clean Up and Termination
* **Action:** To adhere to cloud cost-optimization best practices, I disabled the instance's termination protection and successfully terminated the web server to ensure no further charges would be incurred.
* **Proof:** ![Instance Terminated](Screenshots/4%20Instance%20Terminated.png)
