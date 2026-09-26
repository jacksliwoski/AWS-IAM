<h1>AWS IAM Group Policy Management</h1>


<h2>TLDR Description</h2>
Creating IAM users and groups in AWS, attaching policies to the groups, and verifying each user only has access to what its group allows.
<br />

<h2>Purpose</h2>
The purpose of this lab was to gain an introduction to the utilities offered by AWS through fiddling with IAM users and groups, and the policies applied to those groups. In a real world scenario an administrator would want to give access to some users on certain resources but deny access to other users who don’t have any business with those resources. Such a thing is done by applying the correct policies and permissions for specific users to ensure that resources are correctly protected.
<br />

<h2>Background Info</h2>
AWS IAM or Identity and Access Management is the service which controls and manages users and their permissions within the AWS service. IAM controls users, security credentials, and permissions.
<br />

<h2>Lab Summary</h2>
In this lab I gained a general understanding of the IAM User and Group creation and the application of policies on the created groups. I applied different policies to separate Groups and verified that the policies configured worked as intended by attempting to access unauthorized content on one of the Users and then verifying that they can access what the users are authorized for.
<br />

<h2>Lab Commands</h2>
As this lab was done through AWS there was no commands used, all of it was configured with their GUI.
<br />

<h2>Walk-Through:</h2>

<p align="center">
In this lab I will be configuring these users with their respective groups and permissions attached to their groups.<br/>
<img src="images/img1.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
From here I then went to the IAM Dashboard by clicking IAM under AWS Services.<br/>
<img src="images/img2.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Once I was on the IAM Dashboard I selected the Users tab on the left menu.<br/>
<img src="images/img3.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Adding user-1 into the S3-Support group<br/>
<img src="images/img4.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img5.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img6.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img7.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img8.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Adding user-2 into the EC2-Support group<br/>
<img src="images/img9.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img10.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img11.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Adding user-3 into the EC2-Admin group<br/>
<img src="images/img12.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img13.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img14.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
</p>

<h4>Verifying Configurations:</h4>
<p align="center">
user-1 can see s3 buckets since its configured to be a S3-Support.<br/>
<img src="images/img15.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img16.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Unauthorized to view ec2 instances so we are unable to view them with user-1<br/>
<img src="images/img17.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Unable to view S3 buckets as user-2 which is configured to be EC2-Support<br/>
<img src="images/img18.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img19.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
Able and authorized to be able to see EC2 instances as user-2<br/>
<img src="images/img20.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
With user-3 configured as a EC2-Admin, user-3 is able to view, create, start, and stop EC2 instances.<br/>
<img src="images/img21.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img22.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<img src="images/img23.png" height="80%" width="80%" alt="AWS IAM Group Policy Management"/>
<br />
<br />
</p>

<h2>Problems</h2>
The only issue I ran into was a quick fix but had me confused for a minute until I had a epitome, this issue was with the Region selected not being the correct one for my instance that I had created. Since I was set on the wrong region I wasn’t able to see the EC2 instance that I was working on, but once I realized this mistake it was an easy fix by just changing the region to the correct one.
<br/>
<br/>

<h2>Conclusion</h2>
Overall, through this lab I was able to learn the basic concepts of the AWS interfaces and the functions of its services focusing specifically on IAM with user creation and management with configuring their groups and permissions. After I configured groups and their respective permissions I added the users to their specific groups and verified my configurations worked, which they did.
<br />
