# AWS Basics

Free level, we can get an EC2, VPC, type t2.micro server, with 1vCPU, 1GB of ram and up to 30GB of storage, totally free for the promotional period.

# Step 1

Access the login page:

https://aws.amazon.com/pt/console/

Now click the login (or login again) button.
Next time use your login email.
Now enter your password. 
</br> 
</br> 
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver01.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver02.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver03.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver04.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
 

# step 2

Console homepage. click the menu icon:

Services or “Services”
In the first option of the menu, choose:

Computing
In the second option, choose

EC2 (virtual cloud servers)

</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver05.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver06.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
 

# step 3

You will now be on the EC2 Dashboard page. Click on the button:

run instance
It will enable a second option of:

run instance

</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver07.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver08.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver09.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
 

# step 4

By clicking on the button from the previous step, you will be forwarded to the page that allows the creation of a new instance. In this step you will be able to select all the options you want to configure your server on Amazon. A reminder, in the upper right corner you will probably see the name Virginia do Norte (or North Virginia), that means you are in the datacenter of Virginia do Norte. You can click there and switch to another region closer to you, envisioning a lower latency (ping), such as, for example, a datacenter in São Paulo.

</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver10.png" 
alt="Minha Figura">
</br>  

# step 5

On the instance creation page, the first step is to select your server name. In our example, we chose the VPC name, but feel free to choose whatever name works best for you.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver11.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 6

The next step is to select which operating system image you want installed on the server. In this example, we are going to select the Linux Operating System, on the Ubuntu distribution, which is eligible for the free tier.
The ubuntu version chosen was the last one available on the creation date of this tutorial, which was: Ubuntu Server 22.04 LTS (HVM), SSD Volume Type, in the 64-bit version (x86).
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver12.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 7

The next step is to choose the instance type (processing capacity and ram), we choose the t2.micro version, also enabled for the free tier. This version has 1vCPU and 1GB of ram.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver13.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 8

Now we need to define the key pair for remote connection to the server via SSH. Let's click on the option:

Create new key pair
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver14.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 9

So we need to first define the name for the key file. In this example we choose the name of:

KeyVPCaws
We use encryption:

RSA
And since we connected via the terminal with openSSH, we opted for the key format of the type:

.pem
Now to finish creating the keys, just click on the button:

Create key pair
The download should start and your keys should be saved to your computer's Downloads folder.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver15.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 10

In this step now we are going to configure the network settings. Let's leave the options selected:

<ul> 
<li> Create security group</li> 
<li> Allow SSH traffic from (Anywhere 0.0.0.0/0)</li> 
<li> Allow HTTPs traffic from the internet</li> 
<li> Allow HTTP traffic from the internet</li> 
</ul> 
</br>
</br>
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver16.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 11

We now have the option to select server storage (disk space). By default, this option starts with 8GB, which is the minimum size of the selected Ubuntu image. At the time of writing this tutorial, Amazon allows you to use up to 30GB of storage for the free tier. In this tutorial, we are going to select only 10GB of gp2 type of Root Volume.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver17.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 12

In this tutorial we are not going to select advanced options, or advanced details, we can skip directly to the last Summary step.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver18.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 13

Now we have the opportunity to review all the options before performing the server instance creation. Check again that all options are correct (Name, Ubuntu Image, 64bits, type t2.micro, 1 vol. 10gb). Remember to review whether these options are still within the free tier, as Amazon may change the criteria.

Amazon AWS - New EC2 Instance - Remember to Block Your Card!
An important tip before continuing. Remember to have a virtual card linked to your AWS account. Because at this stage now, you have the possibility to enter your bank's application and block your card, to ensure that no charges are made. This avoids 2 problems:

AWS wrongful charge (it happened that they tried to charge me, but it could be just to confirm my card again). But when in doubt, protect yourself.
You have mistakenly selected an option that is not in the free tier. This way you avoid billing and have the possibility to cancel the service, without having to ask for a chargeback.
After reviewing the items above, click the button:

run instance
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver19.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 14

You will be taken to a page informing you that you have successfully created your instance. Click the button to continue:

View all instances
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver20.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 15

In this step you will be on the instances overview page. In this case, we only have one instance created, named VPC. On this screen, it is important to write down your public IP, because with it we are going to make the connection via ssh to the server. Then select your instance, so that its data is visible.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver21.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 16

With the instance created and its public IP noted down, we can connect via SSH. On your computer, open the prompt.
Now you need to walk to the folder where you saved the server connection key. In this example, the key was downloaded to the Downloads folder, so:

cd Downloads
Now let's use the command below to connect to the server. In this example, we will use the IP 15.229.47.227. The key in this example is named KeyVPCaws.pem. Remember to change the command below, with the correct information of your key name and your server IP. By default, the username on this Ubuntu linux image is ubuntu.

ssh -i KeyVPCaws.pem ubuntu@15.229.47.227
If you have had any problems with insecure key permissions and you are using a mac os or linux operating system, just change the file permission (chmod 600 ChaveVPCaws.pem), if you are using windows, open the key file in notepad, copy the content. Create another file in notepad, paste the key content, and save this new file in the directory you intend to use the ssh connection.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver22.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver23.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 

# step 17

If you performed all the steps correctly, you are now connected to your server via an SSH connection.
 
</br>  
 <img src="https://github.com/sovanderlei/AWS_Basics/blob/main/imagens/awsserver24.png" style="width:800px;height:600px;" 
alt="Minha Figura">
</br> 
</br> 
</br> 
