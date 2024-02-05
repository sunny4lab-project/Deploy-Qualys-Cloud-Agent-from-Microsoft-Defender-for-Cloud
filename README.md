# 👨‍🏫 Deploy Qualys Cloud Agent from Microsoft (Azure) Defender for Cloud

# <img width="931" alt="Installed Cloud Agent " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/ec31c0ae-959f-4027-b32b-c6f4338438c4">


This guide provides a comprehensive walkthrough on deploying Qualys Cloud Agent from Microsoft Defender for Cloud on Azure, applicable to both Windows and Linux virtual machines. By following these steps, you can strengthen your security infrastructure, extending vulnerability management capabilities to your cloud workloads. This deployment enables the assessment of vulnerability findings within both Microsoft Defender for Cloud and your Qualys subscription, ensuring a robust and integrated approach to securing your Azure environment.



# **Here's how it works**

Microsoft Defender for Cloud is like a control center for keeping your Azure infrastructure safe. It works with Qualys, a tool for checking vulnerabilities. Here's how it works: If some virtual machines don't have the right protection, Microsoft Defender for Cloud takes care of it. It puts small Qualys agents on these machines to collect info about potential issues and this process is automated. This info goes to the Qualys Cloud Platform, which then sends back details about vulnerabilities and health. It's like a teamwork system to keep everything secure and in check.
<details><summary>Click here for the steps</summary>

 # **Step 1:**
**Qualys Integrations and setting up of Activation key**

- ▶️ Log in to your Qualys account
 # <img width="961" alt="Qualys Login screen " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/86e4ba03-994b-45df-989a-def080f1d34b">

  - ▶️ Navigate to Panel on the left scroll down and select "cloud agent"
   # <img width="706" alt="select Cloud agent " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/a0496ac8-3f75-4075-b23a-5f0c9effd1f7">
    
  - ▶️ Click on the "agent management" button at the top panel
# <img width="703" alt="management agent" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/9be8d8b3-669c-42b7-9e54-dc0419207652">

  - ▶️ Create a New Key by clicking the Agent tab and clicking the "New Key" button 🔳 below. 
# <img width="695" alt="New Key" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/00cce5f3-e202-4908-a744-2fc9b39e82b6">

  - ▶️ Check the vulnerability management box and then click on the "Generate" button which should generate the activation key for the agent to be set up on Azure.
# <img width="538" alt="New Activation key" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/9cd15cc6-8989-48b4-9530-9dedb47c043f">

 - ▶️ the Azure agent is currently supported for Windows and Linux. Click the Install Instructions
button for Windows or Linux. 
# <img width="540" alt="Installation Requirement " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/567a923f-5164-4986-af84-a2b891a259e1">

 - ▶️ Click the "Deploying in Azure Cloud" button and then Copy the License Code and Public Key. In the process of deploying the cloud agent in Azure, both the License and Public keys will be needed.
   # <img width="538" alt="Deploying in Axure Cloud" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/b6fed228-8f9d-4c07-934e-e091653365c3">

   # Step: 2

   **Deploying Qualys Cloud Agents in Azure**

Using Qualys Cloud Agent (QCA) for Vulnerability Assessment (Bring Your Own License - BYOL) allows you to deploy QCA through Microsoft Defender for Cloud. It includes an Autodeploy feature that automatically installs agents on any virtual machines in your subscription that lack protection. This service is accessible with both the free and standard tiers of Microsoft Defender for Cloud.

- ➡️  Login into the Microsoft Azure portal and navigate to “Microsoft Defender for Cloud” and on the navigation panel to your left, click on "recommendations"
  # <img width="784" alt="Recommendation settings" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/87a73103-0d2b-442b-82bf-609529dc36be">

- ➡️ Click on Remediate Vulnerability and select "Machines should have a vulnerability assessment solution" 
# <img width="794" alt="Remediate Vulnerability" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/3fca25cd-db06-41a6-b2fb-6ef4398cf148">

- ➡️ On the description panel, scroll down and click on "unhealthy resources" Scroll down a bit select the VMs listed, and click on the "Fix" button. The Unhealthy resources column lists all the VM resources, without Qualys cloud agent.
   # <img width="587" alt="VM should be fixed Vulnerability" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/1e6b457d-2933-4f35-9e2c-bbde9dd8a890">

- ➡️ Choose a vulnerability assessment solution. Select Configure a new third-party vulnerability scanner(BYOL - requires a separate license). and then select Qualys extension to configure and click the "Proceed" button below.
- **🗒️Note:-** 

**Threat and vulnerability management by Microsoft Defender for Endpoint (included
with Microsoft Defender for servers):** This option will automatically get the threat and
vulnerability management findings without the need for additional agents. it is built-in
module for Microsoft Defender for Endpoint, threat, and vulnerability management.

**Deploy the integrated vulnerability scanner powered by Qualys (included with
Microsoft Defender for servers):** This option is intended for non-Qualys customers who
want to leverage the Qualys Vulnerability Assessment via Azure Defender included in the
Microsoft Defender for Cloud. You should not choose this option if they
want their assessment findings in their Qualys subscription. 

**Deploy your configured third-party vulnerability scanner (BYOL - requires a separate
license):** Choose this option if you already have an existing solution from Qualys. This
option will expose vulnerability assessment findings to your Qualys subscription.
Configure a new third-party vulnerability scanner (BYOL - requires a separate license):
Choose this option if you want to create a new solution.

# <img width="703" alt="Qualys Extension to configure" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/de2b7b0f-6acf-46b6-8289-b8d10c1a6f36">

-➡️ Fill in all the needed information from Microsoft Azure Installation Requirements on the Qualys Cloud deployment page. You will need to provide the subscription, Resource group, Location, License, and Public Key. License and Public keys should be on your Qualys cloud agent deployment page. Subscriptions, Resource groups, and Locations should be your Azure information from the initial creation of your Azure account.
# <img width="752" alt="Configure Qualys" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/754b18c3-f2d2-4e13-a9f1-f78af2dd0a7c">

</details>




 # **Prerequisites**

<details><summary>Click here for details</summary> 

  
  **Before proceeding with the deployment, ensure that you have the following:**

🔖 **Microsoft Subscriptions:** You have to have a Microsoft Azure account setup already
🔖 **Microsoft Defender for Cloud Subscription:** Activate and configure Microsoft Defender for Cloud for your environment (it comes with 30 days free trials).
🔖 **Qualys Subscription:** Obtain a Qualys subscription and ensure you have the necessary credentials to access the Qualys Cloud Platform.
