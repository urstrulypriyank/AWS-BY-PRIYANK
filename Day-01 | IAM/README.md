# Identity and Access Management (IAM)
IAM stands for identity and access management as the name suggest we can manage users and authorization for every aws services.
- manage user and authentication, authorization and restriction of services (like read, modification access )
- It is always recommended to not to use AWS root user instead create a custom user and give administrationPrivileges to give equivalent priviliges as root
- one liner -> Who can access what 

# Lab 01 - IAM
Lab for configuring permissions in IAM, according to AWS best practices.

### 1. User Creation

In this part, we will create a user with administrator permissions through the AWS Console.

   1.1. Access the AWS Dashboard for IAM (https://console.aws.amazon.com/iam/home)
   1.2. Click on **Users**
   1.3. Click on **Create User**

![Image 01](https://drive.google.com/u/1/uc?id=1f5_Pw0ewqwiSuPdCBc6LUMbFyD-H3hPO&export=download)


   1.4. Define the user name, choosing the access type.
   using permissions options, we can attach policies directly like *AWS Management Console Access*, to allow login and access through the AWS console. Click **Next: Permissions**.
Three step user process for user creation.
![Image 02](https://drive.google.com/u/1/uc?id=1FX-eiZbK_jFdgSQEewIE50waACdKvO&export=download)

   1.5. The groups part would be where we include this user in a group, but we will cover the groups part in another part of this tutorial.

   1.6. Select the "Attach existing policies directly" tab and choose the permission this user needs. In this tutorial, we will choose **AdminstratorAccess** (in practice, be very careful when using this type of permission) as this give full access of the account to the user. Click **Next: Tags**.
  
   1.7. In this part, we can define tags to make management easier. tags are just key value pair for identification Click on **Next: Review** and finally on **Create User**.


### 2. Group Creation

2.1. To create a group, go to the AWS IAM dashboard, click **User Groups** on the left side of the screen, then click **Create Group**

2.2. Set the group name and click on **Next Step**.

2.3. Choose the permission that will be associated with this group. This means that any user added to this group will have these permissions. For this tutorial we will choose **AdministratorAccess** permission and click on **Next Step**.

![Image 04](https://drive.google.com/u/1/uc?id=1uZWfNAMZ-L7Us8URqyP7csjIVE6Sw2Ev&export=download)

2.4. To finish, click **Create Group**.
- To create groups go to User Groups in IAM 
- Go to create Group
- Provide name and select the users that you want to be part of this group 
- select the access policy for the group 
- ![Image 04](https://d2yblsmsldwfto.cloudfront.net/lab01/lab-01-iam-04.png)
### 4. Add MFA to Root account

4.1. Access the main screen of the IAM Dashboard click on **Activate MFA on your root account** and then click on **Manage MFA**

![Image 05](https://d2yblsmsldwfto.cloudfront.net/lab01/lab-01-iam-05.png)

4.2. Click **Activate MFA**.

![Image 06](https://d2yblsmsldwfto.cloudfront.net/lab01/lab-01-iam-06.png)

4.3. Choose one of three options: the first is to add Virtual MFA, using an application like Google Authenticator or Authy, for example, the second for physical MFA and the third for another type of MFA. For this tutorial, we are going to use **Virtual MFA**.

![Image 07](https://d2yblsmsldwfto.cloudfront.net/lab01/lab-01-iam-07.png)

4.4. Use Google Authenticator or Microsoft Authenticator to scan the QR Code and get the code to configure.