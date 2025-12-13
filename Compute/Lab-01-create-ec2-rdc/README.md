<h1>Create a windows EC2 Instance and Connect it using Remote Desktop Connnection (RDC)</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)


<h2>Description</h2>
In this lab, a windows EC2 instance was launched  using Amazon Machine Images (AMI), AWS provided preconfigured instance templates. Specically, we created this instance from microsoft windows server. And the goal was to connect to this instance using Remote Desktop Connection (RDC).
This lab demonstrates how to launch a Windows EC2 instance and connect to it using Remote Desktop Connection (RDC).  
The objective is to understand the core components required to deploy and access a Windows virtual machine in AWS, including AMIs, instance types, key pairs, VPC networking, and security group configuration.
<br /><br />

<h2>Services Used</h2>

- <b>Amazon EC2</b>  
- <b>VPC</b>  
- <b>Security Groups</b>  
- <b>AMI</b>
- <b>RDC app</b>
<br />

<h2>Architectural Diagram</h2>


<h2>Environments</h2>

- <b>AWS Management Console</b>  
- <b>Windows Remote Desktop Client</b> (RDC)
<br />

<h2>Lab Walk-through</h2>

<p align="center">
Launch a Windows EC2 Instance: <br/>
<img src="INSERT-IMAGE-LINK-HERE" height="80%" width="80%" alt="Launch EC2 Instance"/>
<br /><br />
  
<p align="center">
Select/Create a Key Pair: <br/>
<img src="INSERT-IMAGE-LINK-HERE" height="80%" width="80%" alt="EC2 Key Pair"/>
<br /><br />

<p align="center">
Configure Security Group (Allow RDP - Port 3389): <br/>
<img src="INSERT-IMAGE-LINK-HERE" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />

<p align="center">
Connect Using Remote Desktop Connection: <br/>
<img src="INSERT-IMAGE-LINK-HERE" height="80%" width="80%" alt="Remote Desktop Connection"/>
<br /><br />

<p align="center">
Successfully Logged Into the EC2 Windows Environment: <br/>
<img src="INSERT-IMAGE-LINK-HERE" height="80%" width="80%" alt="EC2 Remote Desktop Session"/>
<br /><br />
</p>

<h2>Skills Learned</h2>

- Deploying EC2 Windows Instances  
- Creating and using key pairs  
- Configuring security groups  
- Connecting via Remote Desktop Protocol (RDP)  
- Understanding basic EC2 networking concepts  


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
