---
title: Using Event Automation to detect time-sensitive revenue opportunities <br/>300-level live demo
layout: demoscript
banner: images/temp-banner.jpg
---

<span id="top"></span>

<details markdown="1">

<summary>Introduction</summary>

Today we will see how Focus Corp, an online retailer, uses real-time transaction data to capitalize on time-sensitive revenue opportunities. 


Focus Corp has a goal of driving more revenue from its first-time customers. The marketing team want to send a high-value promotion to first-time customers immediately after a large initial order.


Focus Corp use IBM MQ to coordinate transactions between its order management system and its payments gateway. We’ll see how these transactions can be harvested to generate a Apache Kafka event stream and exposed to other teams for reuse. The marketing team will use this event stream to precisely identify which customers to send the promotional offer to.


Let’s get started!

(Demo intro slides <a href="https://ibm.box.com/s/quzwd2gvn7zbo9oo19xi1o05gtdlvmwj" target="_blank" rel="noreferrer">here</a>)

(Printer-ready PDF of demo script <a href="https://ibm.box.com/s/jsz9v4mva1jdz7gg1fls3xk4rhgiezvh" target="_blank" rel="noreferrer">here</a>)

<br/><br/>

</details>

<p/>

<details markdown="1">

<summary>1 - Creating an event stream from a message queue</summary>

Focus Corp’s integration team exposes the enterprise’s data using event streams. This allows application teams to subscribe to the data without impacting the backend system, decoupling development, and lowering risks. The integration team have received a request to access customer orders. The order management system and its payment gateway exchange customer orders over IBM MQ. The integration team will tap into this communication, clone each of the orders and publish into an event stream.

<br/>

| **1.1** | **Configure a new queue in IBM MQ for the cloned order messages** |
| :--- | :--- |
| **Narration** | Focus Corp’s integration team log into the IBM MQ console. They create a new queue called TO.KAFKA to store the cloned order messages before they are published to Apache Kafka. |
| **Action** &nbsp; 1.1.1 | Click ...<br/> <img src="images/1-1-something.png" width="800" /> |

| **1.2** | **Configure IBM MQ to clone the orders** |
| :--- | :--- |
| **Narration** | Next the integration team identify the queue being used between the order management system and its payment gateway. They update the configuration to specify TO.KAFKA as the streaming queue. This causes IBM MQ to clone all new messages put to the queue. Once saved the new configuration is live, and the integration team can see cloned order messages stacking up in the TO.KAFKA queue. |
| **Action** &nbsp; 1.2.1 | Click ...<br/> <img src="images/1-2-something.png" width="800" /> |

| **1.3** | **Define the orders event stream** |
| :--- | :--- |
| **Narration** | Next the integration team open the IBM Event Streams console to create the orders stream where the messages will be published. They have options to customize the replication and retention settings that control the redundancy and volume of data held.  |
| **Action** &nbsp; 1.3.1 | Click ...<br/> <img src="images/1-3-something.png" width="800" /> |

| **1.4** | **Configure the IBM MQ to IBM Event Streams bridge** |
| :--- | :--- |
| **Narration** | Next the integration team open the Red Hat OpenShift console to configure the MQ to IBM Event Stream bridge. The bridge is supplied and supported by IBM and built on the Apache Kafka connector framework. The configuration includes the connectivity details for both IBM MQ and IBM Event Streams. Once created, the connector reads messages from the TO.KAFKA queue and publishes to the order stream. |
| **Action** &nbsp; 1.4.1 | Click ...<br/> <img src="images/1-3-something.png" width="800" /> |

| **1.5** | **View the orders in the stream** |
| :--- | :--- |
| **Narration** | The integration team return to the IBM Event Streams console to view the order stream. They see the events since they configured the streaming queue in IBM MQ. |
| **Action** &nbsp; 1.5.1 | Click ...<br/> <img src="images/1-3-something.png" width="800" /> |

| **1.6** | **Publishing the orders stream** |
| :--- | :--- |
| **Narration** | Next the integration team open the IBM Event Endpoint Management console. The console supports two usages, one for teams publishing event streams, and a second for those consuming. The integration team publish the order stream by discovering the topic on IBM Event Streams. They include a description, example message and publish the topic for subscribers.  |
| **Action** &nbsp; 1.5.1 | Click ...<br/> <img src="images/1-3-something.png" width="800" /> |

<br/>

**[Go to top](#place1)**

<br/><br/>

</details>

<p/>

<details markdown="1">

<summary>2 - Browsing the self-service event stream catalog</summary>

Focus Corp’s marketing team wants to use the two streams to offer a high-value promotion to specific first-time customers immediately after those customers place their initial order. The team browses the self-service catalog to find the event streams they need.  
<br/>

| **2.1** | **Title** |
| :--- | :--- |
| **Narration** | TEXT |
| **Action** &nbsp; 2.1.1 | Click ...<br/> <img src="images/3-1-1-click-scale.png" width="800" /> |


<br/>

**[Go to top](#place1)**

<br/><br/>

</details>

<p/>

<details markdown="1">

<summary>3 - Using the no-code editor to configure the solution </summary>

The marketing team’s business requirement is to correlate newly created customer accounts with orders of over 100 dollars within a 24-hour window. 

<br/>

| **3.1** | **Title** |
| :--- | :--- |
| **Narration** | TEXT |
| **Action** &nbsp; 3.1.1 | Click ...<br/> <img src="images/3-1-1-click-scale.png" width="800" /> |

  
<br/>

**[Go to top](#place1)**

<br/><br/>

</details>

<p/>

<details markdown="1">

<summary>4 - Sending the output to the marketing application </summary>

<br/>

| **3.1** | **Title** |
| :--- | :--- |
| **Narration** | TEXT |
| **Action** &nbsp; 3.1.1 | Click ...<br/> <img src="images/3-1-1-click-scale.png" width="800" /> |

  
<br/>

**[Go to top](#place1)**

<br/><br/>

</details>

<p/>

<details markdown="1">

<summary>Summary</summary>

<br/>

In this demo we showed how ...


Thank you for attending today’s presentation.


**[Go to top](#place1)**

<br/><br/>

</details>