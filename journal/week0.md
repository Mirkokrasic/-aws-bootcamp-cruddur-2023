# Week 0 — Billing and Architecture

#I've Installed gitpod and install aws client.

```sh
tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
```

#Install of AWS CLI with preload configuration in Gitpod

![image](https://user-images.githubusercontent.com/32469871/221148330-0f880d73-4df1-4ff1-824a-eb4b0aa949fc.png)

#Create new user and put it in admin group

![image](https://user-images.githubusercontent.com/32469871/221147910-d8dd1e88-31df-4f21-9108-bc703c12e592.png)

#I puted Env Vars

I set up these credentials for the current bash terminal and configure gitpod to preload it everytime I run it.
```
export AWS_ACCESS_KEY_ID=""
export AWS_SECRET_ACCESS_KEY=""
export AWS_DEFAULT_REGION=us-east-1
```

```
gp env AWS_ACCESS_KEY_ID=""
gp env AWS_SECRET_ACCESS_KEY=""
gp env AWS_DEFAULT_REGION=us-east-1
```

#Created MFA authentication and access key

![image](https://user-images.githubusercontent.com/32469871/221148644-a864a50d-df95-4632-829a-d6d441bf4fcf.png)

#Created Cloudwatch alarm when the daily will go to 1$

![image](https://user-images.githubusercontent.com/32469871/221149514-04e58b47-360e-4aa4-9d7e-c6e96e723b7a.png)

#Created budget with 1$ 

![image](https://user-images.githubusercontent.com/32469871/221150030-80531802-bff7-4fed-8266-b76a21716de2.png)

#Created an SNS notification service to be notified if my billing alarm is triggered

![image](https://user-images.githubusercontent.com/32469871/221164216-981c0bd2-18f1-43ef-ab9b-eebee5cf951a.png)


#Created logical architecture and I added some security features using LucidChart in order to user MFA in our Crudder app

![image](https://user-images.githubusercontent.com/32469871/221162464-f1803c57-cb40-4804-bb6a-b1f61c1f3d28.png)

Link to my LucidChart :

https://lucid.app/lucidchart/0091155b-032b-46be-a9e1-dd04428d8b1a/edit?viewport_loc=-916%2C2%2C3012%2C1479%2C0_0&invitationId=inv_d76eedcd-7380-470b-9a0c-c7e559baa09a

