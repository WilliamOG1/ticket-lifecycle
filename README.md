<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Ticket Lifecycle: Intake to Resolution</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Ticket Lifecycle Stages</h2>

- Intake (How tickets enter the system)
- Assignment and Communication (Setting properties and ownership)
- Working the Issue (Troubleshooting and updates)
- Resolution (Solving and closing tickets)

---

## Part 1: Creating Tickets as End Users  

### Scenario 1: Business Critical Outage  

1. Navigate to the **End User Portal**: [http://localhost/osTicket](http://localhost/osTicket)  
2. Sign in as user **Karen**  
3. Click **"Open a New Ticket"**  
4. Select **Help Topic**: "Business Critical Outage"  
5. Enter **Subject**: `"Entire mobile/online banking system is down"`  
6. Provide a **detailed description**:  
   > "All customers are reporting they cannot access their accounts through the mobile app or website. This is affecting all banking services."  
7. Click **"Create Ticket"**  

### Scenario 2: Software Issue  

1. Return to the **End User Portal**  
2. Sign in as user **Karen**  
3. Click **"Open a New Ticket"**  
4. Select **Help Topic**: "Personal Computer Issues"  
5. Enter **Subject**: `"Accounting department needs Adobe upgrade, broken"`  
6. Provide a **detailed description**:  
   > "The accounting department reports that Adobe Acrobat is crashing when they try to edit financial documents. The entire team is affected."  
7. Click **"Create Ticket"**  

### Scenario 3: Hardware Failure  

1. Return to the **End User Portal**  
2. Sign in as user **Ken**  
3. Click **"Open a New Ticket"**  
4. Select **Help Topic**: "Equipment Request"  
5. Enter **Subject**: `"CFO's laptop will no longer turn on"`  
6. Provide a **detailed description**:  
   > "The CFO's laptop isn't powering on. They need immediate assistance as they have an important presentation today."  
7. Click **"Create Ticket"**  

## Part 2: Managing Tickets as Help Desk Professionals  

### Scenario 1: Critical System Outage  

#### **Initial Assessment (as John)**  

1. Log in to the **Agent Panel** as **"John"**  
2. Locate the ticket **"Entire mobile/online banking system is down"**  
3. Observe the default ticket properties:  
   - **Priority**: (Default)  
   - **Department**: (Default)  
   - **SLA**: (Default)  
   - **Assigned To**: (Unassigned)  

#### **Setting Ticket Properties (as John)**  

1. Update ticket properties:  
   - **Priority**: `"Emergency"`  
   - **Department**: `"Online Banking"`  
   - **SLA Plan**: `"Sev-A (1 hour, 24/7)"`  
   - **Assigned To**: `"Jane"` (SysAdmins department)  
2. Add an internal note:  
   > "Escalating to SysAdmins due to system-wide outage"  
3. Save changes  

#### **Access Verification (as John)**  

- Attempt to view the ticket again  
- Notice that after reassignment to another department, you **no longer have access**  

#### **Working the Ticket (as Jane)**  

1. Log in to the **Agent Panel** as **"Jane"**  
2. Locate the ticket **"Entire mobile/online banking system is down"**  
3. Review ticket details and priority  
4. Add a reply to the customer:  
   > "We are investigating the banking system outage. Our technical team is working to restore service as quickly as possible."  
5. Change ticket status to **"In Progress"**  
6. Add an internal note:  
   > "Located issue with database connectivity. Working on resolution."  
7. After resolution, add another reply:  
   > "We have identified and fixed the issue. The mobile and online banking systems should now be operational. Please confirm you can access your account."  
8. Change ticket status to **"Resolved"**  

---

### Scenario 2: Software Issue  

#### **Initial Assessment (as John)**  

1. Log in to the **Agent Panel** as **"John"**  
2. Locate the ticket **"Accounting department needs Adobe upgrade, broken"**  

#### **Setting Ticket Properties (as John)**  

1. Update ticket properties:  
   - **Priority**: `"High"`  
   - **Department**: `"Support"`  
   - **SLA Plan**: `"Sev-B (4 hours, 24/7)"`  
   - **Assigned To**: `"John"` (self-assignment)  
2. Save changes  

#### **Working the Ticket (as John)**  

1. Add a reply to the customer:  
   > "I'll be assisting with the Adobe issues in the accounting department. Can you provide me with the version currently installed and the specific error message?"  
2. Change ticket status to **"In Progress"**  
3. After customer response, add an internal note:  
   > "Confirmed outdated Adobe version. Will need to deploy updates to accounting department."  
4. Reply to customer:  
   > "We will be upgrading Adobe for the accounting department. Please allow 2 hours for this process."  
5. After resolution, add another reply:  
   > "The Adobe upgrade has been deployed to all accounting department computers. Please try opening your documents again and confirm the issue is resolved."  
6. Change ticket status to **"Resolved"** after confirmation  

---

### Scenario 3: Hardware Issue  

#### **Initial Assessment (as John)**  

1. Log in to the **Agent Panel** as **"John"**  
2. Locate the ticket **"CFO's laptop will no longer turn on"**  

#### **Setting Ticket Properties (as John)**  

1. Update ticket properties:  
   - **Priority**: `"High"`  
   - **Department**: `"Support"`  
   - **SLA Plan**: `"Sev-B (4 hours, 24/7)"`  
   - **Assigned To**: `"John"` (self-assignment)  
2. Save changes  

#### **Working the Ticket (as John)**  

1. Add a reply:  
   > "I'll be handling this issue with the CFO's laptop. I'll come to their office immediately to assess the problem."  
2. Change ticket status to **"In Progress"**  
3. Add an internal note:  
   > "Initial assessment shows power supply failure. Need replacement hardware."  
4. Reply to customer:  
   > "The laptop's power supply has failed. We have a replacement laptop ready - I'll configure it with the CFO's settings and deliver it within the hour."  
5. After resolution, add another reply:  
   > "I've set up the replacement laptop with all necessary software and transferred data from the backup. Please confirm everything is working as expected."  
6. Change ticket status to **"Resolved"** after confirmation  
