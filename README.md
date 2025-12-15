Objective

Configure and test basic firewall rules to allow or block network traffic using Windows Firewall, and understand how firewalls filter network traffic.

Step 1: Open Windows Firewall

Press Windows + R

Type wf.msc

Press Enter

Windows Defender Firewall with Advanced Security opens

Step 2: View Current Firewall Rules

Click Inbound Rules (left panel)

Existing firewall rules will be displayed

Step 3: Block Inbound Traffic on Port 23 (Telnet)

Click Inbound Rules

Click New Rule… (right panel)

Select Port → Click Next

Select TCP

Select Specific local ports → Enter 23

Click Next

Select Block the connection

Click Next

Select Domain, Private, Public

Click Next

Rule Name: Block Telnet Port 23

Click Finish

✅ Port 23 is now blocked

Step 4: Test the Rule

Open Command Prompt

Run:

telnet localhost 23


Connection fails → rule is working

Step 5: Allow SSH (Port 22)

Click Inbound Rules

Click New Rule…

Select Port

Select TCP

Enter 22

Click Next

Select Allow the connection

Click Next

Select Domain, Private, Public

Rule Name: Allow SSH Port 22

Click Finish

Step 6: Remove Test Block Rule (Restore State)

Go to Inbound Rules

Find Block Telnet Port 23

Right-click → Delete

Click Yes
