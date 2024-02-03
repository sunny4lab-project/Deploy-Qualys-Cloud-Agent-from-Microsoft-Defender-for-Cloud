# 👨‍🏫 Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud

This guide provides a comprehensive walkthrough on deploying Qualys Cloud Agent from Microsoft Defender for Cloud on Azure, applicable to both Windows and Linux virtual machines. By following these steps, you can strengthen your security infrastructure, extending vulnerability management capabilities to your cloud workloads. This deployment enables the assessment of vulnerability findings within both Microsoft Defender for Cloud and your Qualys subscription, ensuring a robust and integrated approach to securing your Azure environment.

# **Here's how it works**

Microsoft Defender for Cloud is like a control center for keeping your Azure infrastructure safe. It works with Qualys, a tool for checking vulnerabilities. Here's how it works: If some virtual machines don't have the right protection, Microsoft Defender for Cloud takes care of it. It puts small Qualys agents on these machines to collect info about potential issues and this process is automated. This info goes to the Qualys Cloud Platform, which then sends back details about vulnerabilities and health. It's like a teamwork system to keep everything secure and in check.
<details><summary>Click her for the steps</summary>

 # **Step 1:**
**Qualys Integrations and setting up of Activation key**

- ▶️ Log in to your Qualys account
  <img width="961" alt="Qualys Login screen " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/86e4ba03-994b-45df-989a-def080f1d34b">

  - ▶️ Navigate to Panel on the left scroll down and select "cloud agent"
    <img width="706" alt="select Cloud agent " src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/a0496ac8-3f75-4075-b23a-5f0c9effd1f7">
    
  - ▶️ Click on the "agent management" button at the top panel
<img width="703" alt="management agent" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/9be8d8b3-669c-42b7-9e54-dc0419207652">

  - ▶️ Create a New Key by clicking on the "New Key" button 🔳 below. 
<img width="695" alt="New Key" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/00cce5f3-e202-4908-a744-2fc9b39e82b6">

  - ▶️ Check the vulnerability management box and then click on the "Generate" button which should generate the activation key for the agent to be set up on Azure.
<img width="538" alt="New Activation key" src="https://github.com/sunny4lab-project/Deploy-Qualys-Cloud-Agent-from-Microsoft-Defender-for-Cloud/assets/139194279/9cd15cc6-8989-48b4-9530-9dedb47c043f">

 - ▶️ the Azure agent is currently supported for Windows and Linux. 


</details>




 # **Prerequisites**

<details><summary>Click here for details</summary> 

  
  **Before proceeding with the deployment, ensure that you have the following:**

🔖 **Microsoft Subscriptions:** You have to have a Microsoft Azure account setup already
🔖 **Microsoft Defender for Cloud Subscription:** Activate and configure Microsoft Defender for Cloud for your environment (it comes with 30 days free trials).
🔖 **Qualys Subscription:** Obtain a Qualys subscription and ensure you have the necessary credentials to access the Qualys Cloud Platform.
