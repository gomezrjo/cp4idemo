# App Connect assets for CP4I Demonstration

This Repo contains multiple App Connect assets (a.k.a. BAR files) to be used as part of an end-to-end CP4I demonstration.

* **SFLeads** is an Integration developed using the Designer Authoring Tool showcasing the SalesForce Smart Connector. The flow can be found [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/SFLeads.yaml) if you want to import it in your own Designer instance. This is how the flow looks like:

![ACE Integrations Image 1](images/SFLeads-Flow.png)

* **jgr-cp4i-mqapi-prem** is an Integration that exposes an MQ Queue as a REST API. Integration *jgr-cp4i-mqapi-dflt* is the same but using a different Output Queue. The contract can be found [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/jgr-cp4i-mqapi-prem.json). And this is how the flow looks like:

![ACE Integrations Image 2](images/jgr-cp4i-mqapi-prem.png)

* **jgr-cp4i-fwdmq-event** is an Integration that gets the MQ message produced by the previous flow and forwards it to another queue doing message transformation and protocol conversion to kafka. The json schema used in the input messabe can be found [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/contact.json), and the COBOL copy book with the format for the back end system is located [here](https://github.com/gomezrjo/cp4idemo/blob/main/artifacts/contact.cpy). And this is how the flow looks like:

![ACE Integrations Image 3](images/jgr-cp4i-fwdmq-event.png)

* **jgr-cp4i-kafka2mail** is an Integration that is subscribed to a Kafka Topic and using that information to send an email with an attachment. The integration uses an UDP to get the information to be used by the Email Output node. This is how the flow looks like:

![ACE Integrations Image 4](images/jgr-cp4i-kafka2mail.png)

* **jgr-cp4i-mock-backend** is an Integration that simulate the Back End system that process the request message. This is how the flow looks like:

![ACE Integrations Image 5](images/jgr-cp4i-mock-backend.png)

* **jgr-cp4i-esapi-scram** is an Integration that exposes a Kafka Topic as a REST API. It uses the same contract as the *jgr-cp4i-mqapi* integrations. This is how the flow looks like:

![ACE Integrations Image 6](images/jgr-cp4i-esapi-scram.png)

* **jgr-cp4i-mqivt** is a simple flow to demonstrate the basic ACE functionality with MQ that most "traditional" ACE users want to see. This is how the flow looks like:

![ACE Integrations Image 7](images/jgr-cp4i-mqivt.png)
