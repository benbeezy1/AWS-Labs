<h1>Creating an Application Load Balancer and Auto Scaling Group</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)


<h2>Description</h2>
In this lab, I created and configured an amazon EC2 auto scaling and ELB. The configuration responds to a simulated stress on the web server thereby spunning more instance to accomodate the demand. 
<br /><br />

<h2>Services Used</h2>

- <b>ELB</b>  
- <b>Security Groups</b>  
- <b>AMI</b>
- <b>Auto Scaling</b>
- <b>Target groups</b>
<br />

<h2>Architectural Diagram</h2>

<h2>Environments</h2>

- <b>AWS Management Console</b>  
<br />

<h2>Lab Walk-through</h2>

<p align="center">
<b>Created two security groups (SG):</b>
<br /><br />

(1) Security group for the load balancer with HTTP inbound rule;  
<p align="center">
<br /> 
<img src="https://i.imgur.com/ilWCBbL.png" height="80%" width="80%" alt="Load balancer SG"/>
<br /><br />

(2) SG for the launch template with two inbound rules (SSH) and (HTTP) from load balancer SG.
<p align="center"><br />
<img src="https://i.imgur.com/2jtkftL.png" height="80%" width="80%" alt="Launch EC2 Instance"/>
<br /><br />
</p>
  
<p align="center">
<b>Created a Key Pair to allow for open SSH connection: </b>

<img src="https://i.imgur.com/Xqk8h1X.png" height="80%" width="80%" alt="EC2 Key Pair"/>
<br /><br />

<p align="center">
Then a Launch template was created: this template allows the creation of a saved instance configuration that can be reused, or in our case launched at a later time by the auto scaling, when the demand is high. The launch template SG was selected <br/>
<img src="https://i.imgur.com/oZ2BTQL.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<br/>
<img src="https://i.imgur.com/8mHuF7D.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<br/>
<img src="https://i.imgur.com/Xqd3D7K.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />

<p align="center">
Next: The target group and load balancer was then created. The load balancer routes requests to the target group and performs health checks on the targets. The target typr was instance (in our case EC2). <br/>
<br/>
<img src="https://i.imgur.com/laiAEFa.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<br/>
<img src="https://i.imgur.com/7QeDcjF.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<br/>
<img src="https://i.imgur.com/gpSyE8H.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />

<p align="center">
Next thing was to create the load balancer which would help distribute incoming HTTP and HTTPS traffic across the targets that we previously created. When the load balancer receives a connection request, it evaluates the listener rules in priority order to determine which rule to apply, and if applicable, it selects a target from the target group for the rule action. <br/>
<img src="https://i.imgur.com/c9yTwXR.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<br/>
<img src="https://i.imgur.com/RiL44Ft.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />

<p align="center">
Finally, the auto scaling group was created. Information such as the subnets (two was selected) for the instances and the number of instances the group must maintain at all times was included.  Min = 1 and Max = 2. The scaling group was integrated with the load balancer. Health checks was configured and set to happen every 60 secs. <br/>
<img src="https://i.imgur.com/EDMqFEs.png" height="80%" width="80%" alt="EC2 Remote Desktop Session"/>
<br /><br />
  <br/>
<img src="https://i.imgur.com/cG6BZEr.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
    <br/>
<img src="https://i.imgur.com/RnwjOsM.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<img src="https://i.imgur.com/tsDge5o.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />
<img src="https://i.imgur.com/0i9wW7M.png" height="80%" width="80%" alt="Security Group Configuration"/>
<br /><br />

<p align="center">
<b>The web server was live and recieved traffic from the ELB</b><br/>
<img src="https://i.imgur.com/k0cvFPB.png" height="80%" width="80%" alt="EC2 Remote Desktop Session"/>
<br /><br /> 
  
<h2>Skills Learned</h2>

- Deploying an Auto scaling group using launch template
- Integrated the scaling group with ALB  
- Configuring security groups  
- Understanding how an application scales up and down based on demand.  


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
