# AWS-SECURITY-GROUP
Managing security groups in AWS EC2 instances

Log in to your AWS account and navigate to the EC2 Dashboard

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d9eb1cf2-4041-4edb-a2f7-535d727ac817" />

Find the "Security Groups" option in the sidebar under "Network & Security

Notice that there are two security groups listed here: the default group and launch-wizard-1 (created earlier for your 'My First EC2' instance)

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3802b406-eb3d-48c2-adaf-b83ce52947d5" />

We can review launch-wizard-1 by right-clicking it and exposing its details and inbound outbound rules

<img width="1622" height="380" alt="image" src="https://github.com/user-attachments/assets/7b174584-7bd5-4484-8f74-2eee946740ce" />

The security group ID is located in the details section, similar to an EC2 instance ID

<img width="1801" height="873" alt="image" src="https://github.com/user-attachments/assets/86637a65-cc10-4549-837a-0f0763199c65" />

Next, we can take a look at the Inbound rules by selecting the tab to the right of Details

<img width="1920" height="929" alt="image" src="https://github.com/user-attachments/assets/3866b80d-646b-4b55-ae4e-258ff2c3c7a0" />

An inbound rule (or ingress rule) for an AWS security group defines what incoming traffic is allowed to reach the resources (such as EC2 instances) associated with that security group

The security group launch-wizard-1 currently has two inbound rules: 

The first type is HTTP, which allows unencrypted web traffic from anywhere on the public internet to reach port 80 on your instance. This is standard if you are hosting a public-facing website

The second type is SSH, which allows secure shell command-line access from anywhere on the public internet (0.0.0.0/0) to your instance

<img width="1521" height="229" alt="image" src="https://github.com/user-attachments/assets/ebc1dcf8-2179-4787-a6c0-845b3c852cc5" />

Inbound traffic over port 80 permits public access to the web server. If this rule were deleted from the security group, incoming connections to the site would be denied

Current state:

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/6f8aff3c-81f9-46e4-89e9-21a100b9d3e2" />

Removing the port 80 rule:

Right-click Edit inbound rules

<img width="1024" height="314" alt="image" src="https://github.com/user-attachments/assets/d0e519d2-efe9-4e33-a602-2d48665f8b9f" />

Remove the HTTP rule by clicking Delete, circled in red below, then hit Save rules

<img width="1024" height="286" alt="image" src="https://github.com/user-attachments/assets/f2da8fd4-feb3-4cbc-974a-a653cafa8912" />

<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/69281f49-befe-4e20-9860-6d23779e5f93" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f338ddd6-c77a-4a99-ba80-861b17780ae9" />

Now, if you refresh the page 
