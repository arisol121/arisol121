<h1>Hi, - I'm Arolinda! </h1>

 <h2>Cybersecurity Project</h2>
Project 
<h2>Description</h2>
Hands on Siem home lab used for threat detection and security monitoring. 

<h2>Tools Used</h2>
Virtualbox 

<h2>Links</h2>
 Elastic Cloud free trial at https://cloud.elastic.co/registration
<h2>Siem Home lab setup step by step:</h2>

**Step 1.** -<b>Sign up for free trial without credit card</b>

<img width="724" alt="Screenshot 2024-03-10 121220" src="https://github.com/arisol121/arisol121/assets/79430449/260221a4-4046-4455-869d-5f551c4ef83e">
<h2></h2>

**Step 2.** -<b>Create Deployment and choose a region</b> 

<img width="737" alt="deployment " src="https://github.com/arisol121/arisol121/assets/79430449/465c99a0-3a79-41cc-b79d-9a496440ba2b">
<h2></h2>

**Step 3.**  -<b>Download Kali Linux VM https://www.kali.org/get-kali/#kali-virtual-machines</b>
<br />
Create a new VM with Kali 

<img width="703" alt="vm" src="https://github.com/arisol121/arisol121/assets/79430449/6faf0c8a-42a7-4d2e-b292-25e70a2da5fe">

Next select the hamburger menu icon at the top left corner and at the bottom select add integrations:

<img width="239" alt="integration 2" src="https://github.com/arisol121/arisol121/assets/79430449/74987f47-b0c8-49bf-892b-37fa4320235b">

**Step 4.** -<b>Search for Elastic Defend</b>

<img width="811" alt="Screenshot 2024-03-04 072412" src="https://github.com/arisol121/arisol121/assets/79430449/a91ce903-1e07-411e-b5b8-3b9c11ae5f7d">
<h2></h2>

**Step 5.** -<b>Install Elastic Agent</b>

<img width="722" alt="install elastic " src="https://github.com/arisol121/arisol121/assets/79430449/77d17e46-e8ee-48ca-81c6-c36502273d88">
<h2></h2>

**Step 6.** -<b>Select copy to clipboard and paste the command on the kali linux terminal must have root priveleges to run the command</b>

<img width="699" alt="Linux 1" src="https://github.com/arisol121/arisol121/assets/79430449/051401a6-7cfb-4f04-baf9-939f80702701">


<img width="334" alt="root alic" src="https://github.com/arisol121/arisol121/assets/79430449/29e19c56-02f3-45bf-9d34-de33884ee8ac">
<img width="410" alt="Screenshot 2024-085513" src="https://github.com/arisol121/arisol121/assets/79430449/9e94b88b-565f-461d-9952-345fdd9899e4">

After the agent has been installed successfully now I will verify the agent has been installed by running the command- sudo (systemctl status elastic-agent.service)
<h2></h2>

**Step 7.** -<b>Now to verify the agent is working I will run the nmap command running this command will establish connections to any application listening</b> 


<img width="375" alt="Screenshot 2024-03-06 085741" src="https://github.com/arisol121/arisol121/assets/79430449/cbbe967b-7dbc-4faf-9052-02a7b801ca23">

<br />
<h2></h2>

**Step 8.** -<b>Now to start querying and analyzing the logs in the siem go to the homepage and on the top left corner select the hamburger menu icon and scroll to the observability section and select Logs</b>


<img width="366" alt="logs" src="https://github.com/arisol121/arisol121/assets/79430449/501c4910-d09c-4261-956d-7e9d7855531d">

Filtered the logs by searching in the search bar process.args 
<h2></h2>

**Step 9.** -<b>Created a Dashboad to visualize the events
On the top right side select create a dashboard </b>


<img width="662" alt="dashboard" src="https://github.com/arisol121/arisol121/assets/79430449/d61ecf50-ad7e-4b85-b778-e47be59d9593">


**Then select create visualization to add visualization** 

<img width="565" alt="create visualization" src="https://github.com/arisol121/arisol121/assets/79430449/83fdbeef-dcb7-464c-b198-25c7f1249e93">

- <b>Select Bar horizontal stacked as visualization type
- under bar visualization select metrics</b>
- <b>Horizontalaxi section select @timestamp</b>
- <b> Vertical axis select count</b>

<img width="677" alt="visualization" src="https://github.com/arisol121/arisol121/assets/79430449/cbd2a91d-53a0-48b2-8281-128986e52f94">

- <b>Then select hamburger menu icon and under Security section select alerts </b>
- <b>Select manage rules</b>
<img width="181" alt="alerts" src="https://github.com/arisol121/arisol121/assets/79430449/8201079a-7ed4-403b-a420-eb07b7a5faf1">

<img width="664" alt="manage rules" src="https://github.com/arisol121/arisol121/assets/79430449/64281ddb-ff15-4a29-8798-b27bf4386e1e">

Click create new rule 

<img width="401" alt="create new rule" src="https://github.com/arisol121/arisol121/assets/79430449/69be97e5-6d10-4f94-8ea0-72c3343bd6f1">

Create custom query
- <b>In the custom query sectin seach for event.action</b>
- <b>Under the about rule section type nmap scan</b>
- <b>The rule actions section select the connector type </b>
- <b>Select email </b>
<img width="380" alt="action connector" src="https://github.com/arisol121/arisol121/assets/79430449/232f1182-7dc8-4737-a6d8-caa7ab50342b">


- <b>then create & enable rule</b>
<img width="360" alt="create enable" src="https://github.com/arisol121/arisol121/assets/79430449/2fd7f5d2-1117-433c-8d5f-2d516f4c1619">



