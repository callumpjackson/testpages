---
title: Scalable and resilient cloud-native integration <br/>300-level live demo
layout: preparation
banner: images/scalable-resilient-integration-banner-PREP-5-25-23.jpg
---


<span id="place1"></span>

<span id="top"></span>

| **DEMO OVERVIEW** | | 
| :---         | :--- |
| **Scenario overview** | In this demo we will see how Focus Bank maintains, enhances and elastically scales its IBM MQ and IBM App Connect Enterprise cloud-native integration. |
| **Demo products** | Cloud Pak for Integration |
| **Demo capabilities** | Declarative product upgrade; IBM streaming queues; Pipeline deployment; Horizontal scalability and continuous availability |
| **Demo intro slides** | Download the Introduction and Overview slides <a href="https://ibm.box.com/s/quzwd2gvn7zbo9oo19xi1o05gtdlvmwj" target="_blank" rel="noreferrer">here</a>. This is a short deck of customer-facing slides that sets the context for the demo. |
| **Demo script** | A complete demo script is on the second tab above. You can download a printer-ready PDF of the demo script <a href="https://ibm.box.com/s/jsz9v4mva1jdz7gg1fls3xk4rhgiezvh" target="_blank" rel="noreferrer">here</a>.<br/><br/> This demo script has multiple tasks that each have multiple steps. In each step, you have the details about what you need to do (**Actions**), what you can say while delivering this demo step (**Narration**), and what diagrams and screenshots you will see.<br/><br/>This demo script is a suggestion, and you are welcome to customize based in your sales opportunity. Most importantly, practice this demo in advance. If the demo seems easy for you to execute, the customer will focus on the content. If it seems difficult for you to execute, the customer will focus on your delivery. |
| **Required versions** | Cloud Pak for Integration 2022.4.1 |
| **How to get support** | • Open a support case at <a href="https://techzone.ibm.com/help" target="_blank" rel="noreferrer">IBM Technology Zone Help</a> regarding issues with reserving and provisioning Tech Zone environments.<br/>• Contact <a href="https://ibm-cloud.slack.com/archives/C0216F39ACU" target="_blank" rel="noreferrer">#platinumdemos-automation-support</a> regarding issues with setting up and running this demo. |

### **DEMO INSTALLATION AND SETUP**

<details markdown="1">

<summary>1 - Provision a Cloud Pak for Integration environment</summary>

To provision your Cloud Pak for Integration environment, follow these steps: <br/>

1. To reserve a preinstalled Cloud Pak for Integration (CP4I) cluster on Red Hat OpenShift, go <a href="https://techzone.ibm.com/my/reservations/create/6430260cd7e2100017627406" target="_blank" rel="noreferrer">here</a>. Select if you prefer to make a reservation now or schedule for later. 
<br/><img src="images/prep-image001.png" width="800" />
<br/>

2. If you do not have a sales opportunity, select the purpose **Practice / Self-Education** (1) for a 3-day reservation (which can be extended to 8 days) and fill in the **Purpose description** (2).
<br/><img src="images/prep-image002.png" width="800" />
<br/>

3. Select the **Preferred Geography**.
<br/><img src="images/prep-image003.png" width="800" />
<br/>

4. Several additional fields will appear, the defaults can remain. Scroll down and click **Submit**.
<br/><img src="images/prep-image004.png" width="800" />
<br/>

5. You will receive several emails as the provisioning process continues. You should expect the final email to be sent after 2-3 hours. The final email should look similar to the following.
<br/><img src="images/prep-image005.png" width="800" />
<br/>

**[Go to top](#top)**

<br/><br/>

</details>

<span id="AccessOpenShift"></span>

<details markdown="1">

<summary>2 - Access your OpenShift cluster and install the command line</summary>


In this section, you access your OpenShift cluster and install the OpenShift command line tool. 

1. Open the **PakInstaller Portal** link that was included in the final email.
<br/><img src="images/prep-image101.png" width="800" />
<br/>

2. Navigate to the **OpenShift Console** tab.
<br/><img src="images/prep-image102.png" width="800" />
<br/>

3. Scroll down and open the **OpenShift Web Console** link (1) using **kubeadmin** as the username and **password** (2) shown.
<br/><img src="images/prep-image103.png" width="800" />
<br/>

4. On the web console page, click **?** (1), and select **Command line tools** (2).
<br/><img src="images/prep-image104.png" width="800" />
<br/>

5. Follow the links to install the OpenShift Command Line Interface (CLI) for your Operating System.
<br/><img src="images/prep-image105.png" width="800" />
<br/>

6. To configure the command line on your machine, copy and run the **OC Login command**.
<br/><img src="images/prep-image106-1.png" width="800" />
<br/><img src="images/prep-image106-2.png" width="800" />

You have successfully configured the Openshift command line on your machine.

<br/>

**[Go to top](#top)**

<br/><br/>

</details>

<span id="cloneGitHub"></span>

<details markdown="1">

<summary>3 - Clone the demo assets from a GitHub repository</summary>

To copy the repository you will need to have the Git CLI on your machine. If you don’t have it, follow the installation steps described in this page, based on your operating system.


1. To download the scripts to run the demo, create a directory, and from there run the following command:

   ```git clone https://github.com/IBM/platinum-demo-code-cloud-native-integration.git```

   <br/>

2. Change to the new cloud-native-integration directory:
   
   ```cd cloud-native-integration```

   <br/>

**[Go to top](#top)**

<br/><br/>

</details>

<span id="installDemo"></span>

<details markdown="1">

<summary>4 - Install the demo and access the Web UI</summary>

1. To deploy the demo run:

   ```./deploy.sh```

   If you didn’t use CP4I as the project name, you can append your custom project name to the deploy command. For example:

   ```deploy.sh custom-cp4i```

   <br/>

2. The deployment will take approximately 10 minutes to install. To wait for the deployment to complete and receive the web console URL run the command:

   ```./getURL.sh```

   If you didn’t use CP4I as the project name, you can append your custom project name to the getURL command. For example:

   ```getURL.sh custom-cp4i```

<br/>

Your have completed the demo setup.

<br/>

**[Go to top](#top)**

<br/><br/>

</details>
<hr/>
Click [here](demo-script) to go to the **Demo script** on the next tab.