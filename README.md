
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket. This builds upon what was done in the previous project, "osTicket: Prerequisites and Installation". <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine)
- Windows 10 (21H2)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Configuration Steps</h2>

<p>
First things first, there are two important links. The first one is this link:</br>


http://localhost/osTicket/scp/login.php 

This is the Admin/Analyst login page, and is where your Employees and Admins will use to manage the Ticketing System. It looks like this.
</p>
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a2c4e270-487a-450a-b9e8-faa9a734e7ce" />
</p>
<p>
And this one is for End Users. This is where Users can create and submit tickets.

http://localhost/osTicket 

It looks like this.
</p>
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b31ee7bd-2b1f-44cd-8317-1f4007753065" />
</p>

<p>
First, we're going to log in as an Admin and configure some roles. To do this, use the first link, and log in.
Once you're logged in, it should look like this.
</p>
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/8026dc14-4000-4cb3-a848-e3dbbbbe91cc" />
</p>
<p>
I'd also like to point out this "Admin Panel" Button.

<br />
<img width="330" height="36" alt="image" src="https://github.com/user-attachments/assets/b1b6acf7-44c8-4ee7-a61e-07a32432ec8f" />

When you first log in, you'll be logged in on the "Agent" panel, which shows you what the page looks like if you were essentially logged in as a Help Desk worker. You can click the Admin panel to switch to the sysAdmin side of things and configure stuff on the backend, which is what we're going to do, so go ahead and click it.
</p>

<p>
When you first switch to the Admin panel, it should look like this.
</p>
<p>
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/8c4ab563-db8c-4e7d-bb3b-5cf6eb079410" />
</p>
<p>
The first thing we're going to do is create a new Role, "Supreme Admin". So first, hover over agents, and in the dropdown menu, click roles.
</p>
<p>
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/fd511031-55cd-40b4-b1f0-11a02c3021f2" />
</p>
<p>
Then click "Add New Role".
</p>
<p>
<img width="979" height="118" alt="image" src="https://github.com/user-attachments/assets/8c9119dc-cf86-477f-86b2-0462be940595" />
</p>
<p>
Name: Supreme Admin
</p>
<p>
<img width="1071" height="573" alt="image" src="https://github.com/user-attachments/assets/dafa504c-18c3-4123-95c9-1a906b0a968b" />
</p>
<p>
Now, click permissions, and check everything under Tickets, Tasks, and Knowledgebase.
</p>
<p>
<img width="1919" height="1080" alt="image" src="https://github.com/user-attachments/assets/8d011434-6dde-4012-a392-7ecb1044d7e6" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/427a6e94-67b2-40df-9ebc-ee30d864c537" />
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/acc5ec7e-9030-4886-9274-74f21ef83f55" />
</p>
<p>
Once that's done, click "Add Role".
</p>
<p>
<img width="1917" height="1080" alt="image" src="https://github.com/user-attachments/assets/906c299e-2f51-478f-b0c2-a3c532a44428" />
</p>
With the "Supreme Admin" role created, we can move to configuring Departments for Ticket visibility between Help Desk vs SysAdmins and Networking.
To do that, first click "Departments".
<p>
<img width="1289" height="232" alt="image" src="https://github.com/user-attachments/assets/582b5217-627d-4d9c-be76-6c04a3bb64b5" />
</p>
<p>
Then click "Add New Department".
</p>
<p>
<img width="960" height="43" alt="image" src="https://github.com/user-attachments/assets/949529a4-5d8c-4b05-bb89-84af0df1fe99" />
</p>
<p>
For this, we're going to create a Top Level Department named "SysAdmins". The rest of the settings we can leave alone for now.
</p>
<p>
<img width="964" height="793" alt="image" src="https://github.com/user-attachments/assets/c496023f-32fa-4230-8b05-4e55d7bffef9" />
</p>
<p>
Once that's filled out, go ahead and hit "Create Dept" at the bottom of the screen.
</p>
<p>
Now, we're going to create an Online Banking Team. To do this, click on "Teams" on the dashboard, then click "Add New Team".
</p>
<p>
<img width="1179" height="394" alt="image" src="https://github.com/user-attachments/assets/e9acb4f6-8e71-494b-b6b9-758ed6cca906" />
<img width="1004" height="116" alt="image" src="https://github.com/user-attachments/assets/d1e5f42c-0e71-4404-aa4f-7286c40958a1" />
</p>
<p>
Name: Online Banking
</p>
<p>
<img width="1149" height="637" alt="image" src="https://github.com/user-attachments/assets/50427074-68da-493d-a6a3-96ad6f71020e" />
</p>
<p>
Go ahead and click "Create" to finish.
</p>
<p>
<img width="1052" height="86" alt="image" src="https://github.com/user-attachments/assets/4eb0c443-4e84-45db-a6e5-012f64eccd64" />
</p>
<p>
Now that the "Online Banking" team is created. We're going to configure Ticket Settings to allow anyone to create and submit tickets. To do this, hover your mouse over "Settings", then click "User".
</p>
<p>
<img width="1072" height="393" alt="image" src="https://github.com/user-attachments/assets/7a67a8a6-7838-4cdc-aa9a-54e920ebe3aa" />
</p>
<p>
Make sure the "Require registration and login to create tickets" is UNCHECKED.
</p>
<p>
<img width="1191" height="799" alt="image" src="https://github.com/user-attachments/assets/ae67b973-48e1-4b57-ab9c-d50ecd437165" />
</p>
<p>
Once we're finished verifying that's unchecked, we're going to go to the "Agents" panel and create some Employees. Once you get to the panel, click "Add New".
</p>
<p>
<img width="1011" height="205" alt="image" src="https://github.com/user-attachments/assets/7a6baf99-c21e-4e37-8f92-3cfef98fdc6d" />
<img width="857" height="46" alt="image" src="https://github.com/user-attachments/assets/d3d75420-1240-4b37-9403-fb653e1f16a4" />
</p>
<p>
We're going to create 2 Agents here. A SysAdmin named "Jane Doe", and a Support Agent named "John Doe".
</p>
<p>
<img width="1056" height="720" alt="image" src="https://github.com/user-attachments/assets/9b048d28-52ef-418b-b888-32f8eddfd9c6" />
<img width="943" height="349" alt="image" src="https://github.com/user-attachments/assets/058648f0-4aa7-48aa-8a6f-e3c97e4abb88" />
<img width="945" height="673" alt="image" src="https://github.com/user-attachments/assets/5fda32f8-1db9-48d4-96a7-3c9cc7282bea" />
<img width="982" height="398" alt="image" src="https://github.com/user-attachments/assets/355d48a5-d4b6-4e02-928f-46894cdaa883" />
<img width="1057" height="299" alt="image" src="https://github.com/user-attachments/assets/b8e6c33d-f1f0-4e01-aa1b-5e10056b3a15" />
</p>
<p>
Now that we have our Agents created, we're going to configure our users (customers). You can do this much in the same way, but first we have to switch from the Admin panel to the Agent Panel. You can do this by pressing the Agent Panel button in the upper right of the page.
</p>
<p>
<img width="458" height="58" alt="image" src="https://github.com/user-attachments/assets/24bebe8d-af21-4142-8106-abad301f4338" />
</p>
<p>
Then, hover your mouse over Users and click User Directory.
</p>
<p>
<img width="1166" height="357" alt="image" src="https://github.com/user-attachments/assets/66a74ce2-eabe-44d9-ad11-4adddecb56c1" />
</p>
<p>
Then, click "Add New". We're going to create two users (customers), Karen and Ken.
</p>
<p>
<img width="978" height="293" alt="image" src="https://github.com/user-attachments/assets/4e45d0c9-7098-459d-9e9b-accf5540f205" />
<img width="629" height="388" alt="image" src="https://github.com/user-attachments/assets/ec938810-dca1-4b30-a1eb-8b8631f996f4" />
<img width="975" height="307" alt="image" src="https://github.com/user-attachments/assets/1147aee2-868b-435c-9475-30bc07069efc" />
<img width="950" height="281" alt="image" src="https://github.com/user-attachments/assets/2ad36df8-ee56-4a4d-a12b-00a5b75789f5" />
<img width="1049" height="322" alt="image" src="https://github.com/user-attachments/assets/fc7053e9-1578-44ba-9078-ad5890a24523" />
</p>
<p>
Now that we've got our users, we can configure our SLAs (Service Level Agreements). To do this, go back to the Admin Panel, then hover over Manage and click SLA.
</p>
<p>
<img width="1002" height="493" alt="image" src="https://github.com/user-attachments/assets/3f58f7fd-611a-4015-8bce-b5e7eb115438" />
</p>
<p>
We're going to create 3 different types of SLAs. 
Sev-A (Grace Period: 1 hour, Schedule: 24/7)
Sev-B (Grace Period: 4 hours, Schedule: 24/7)
Sev-C (Grace Period: 8 hours, Business Hours)

Now that we know what we're creating, go ahead and click "Add New SLA Plan" and create them.
</p>
<p>
<img width="841" height="31" alt="image" src="https://github.com/user-attachments/assets/7b915734-bc12-44ef-afbf-b44bd79a4d6b" />
<img width="1014" height="708" alt="image" src="https://github.com/user-attachments/assets/aeb13b65-cdbf-4e7a-93b2-54db25ec9dbc" />
<img width="1224" height="761" alt="image" src="https://github.com/user-attachments/assets/3dc53e34-767b-4037-afeb-2e77e3c94ca8" />
<img width="1046" height="735" alt="image" src="https://github.com/user-attachments/assets/c4c9b64e-51fc-450c-8e50-0c38fe575c09" />
<img width="984" height="288" alt="image" src="https://github.com/user-attachments/assets/9727a08b-8adf-47d8-a325-1a4234932628" />
</p>
<p>
Next, we're going to create different Help Topics for users to choose from when creating a ticket. To do this, go to the Admin Panel, then hover over Manage and click Help Topics.

We'll be creating the following Help Topics:
Business Critical Outage
Personal Computer Issues
Equipment Request
Password Reset
Other

When you're ready, click "Add New Help Topic" to create one.
</p>
<p>
<img width="993" height="459" alt="image" src="https://github.com/user-attachments/assets/7f0a1f09-8181-45b6-8a95-cc3eb10677d1" />
<img width="1024" height="392" alt="image" src="https://github.com/user-attachments/assets/b70ed22e-3e3a-4bc3-809d-331d5aa36465" />
<img width="999" height="532" alt="image" src="https://github.com/user-attachments/assets/8b1e74c2-e6ee-4e3b-b64a-c651791edacd" />
<img width="1080" height="630" alt="image" src="https://github.com/user-attachments/assets/0565ceff-7bce-4aa3-af45-f779196d1b99" />
<img width="1154" height="606" alt="image" src="https://github.com/user-attachments/assets/3a7f32da-2509-49ac-8932-d663f9df6ed7" />
<img width="1271" height="841" alt="image" src="https://github.com/user-attachments/assets/4ff9329d-0146-43e3-b24e-166deaa0abd6" />
<img width="1069" height="694" alt="image" src="https://github.com/user-attachments/assets/83e2781b-11ab-4085-8814-44da7ff683fb" />
<img width="987" height="526" alt="image" src="https://github.com/user-attachments/assets/05a2c12b-f3cb-4278-bdf8-152a98ba15a7" />
</p>
<br />

<h2 align="center" /h>
With that done, we now have a configuration that allows us to start handling customer support tickets!
