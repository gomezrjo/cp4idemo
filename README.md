# App Connect assets for CP4I Demonstration

This Repo contains multiple App Connect assets (a.k.a. BAR files) to be used as part of an end-to-end CP4I demonstration.

* **jgr-cp4i-mqapi-prem** is an Integration that exposes an MQ Queue as a REST API. The contract can be found [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/jgr-cp4i-mqapi-prem.json). And this is how the flow looks like:

![ACE Integrations Image 0](images/jgr-cp4i-mqapi-prem.png)

* **jgr-cp4i-fwdmq** is an Integration that gets the MQ message produced by the previous flow and forwards it to another queue doing message transformation and protocol conversion to kafka. The json schema used in the input messabe can be found [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/contact.json), and the COBOL copy book with the format for the back end system is located [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/contact.cpy). And this is how the flow looks like:

![ACE Integrations Image 1](images/jgr-cp4i-fwdmq.png)

* **jgr-cp4i-mock-backend** is an Integration that simulate the Back End system that process the request message. This is how the flow looks like:

![ACE Integrations Image 2](images/jgr-cp4i-mock-backend.png)

* **SFLeads** is an Integration developed using the Designer Authoring Tool showcasing the SalesForce Smart Connector. This is how the flow looks like:

![ACE Integrations Image 3](images/SFLeads-Flow.png)
