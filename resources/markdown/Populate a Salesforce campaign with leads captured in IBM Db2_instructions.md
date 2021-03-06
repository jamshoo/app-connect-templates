To refer to these instructions while editing the flow, open [the github page](https://github.com/ot4i/app-connect-templates/blob/master/resources/markdown/Populate%20a%20Salesforce%20campaign%20with%20leads%20captured%20in%20IBM%20Db2_instructions.md) (opens in a new window).

## Prerequisites

This template references entities that you can create as follows:

- In your Salesforce instance, create a custom field for the Campaign object to uniquely identify the event for which you are creating a campaign. Name the custom field **Conference** with a data type of **Text**.
- In your IBM Db2 instance, create a database table named **LEADS** in the **DB2INST1** schema.  Sample DDL:
  `CREATE TABLE LEADS (LEADID SMALLINT NOT NULL GENERATED ALWAYS AS IDENTITY (START WITH 1 INCREMENT BY 1), FIRSTNAME VARCHAR(25), LASTNAME VARCHAR(25), FULLNAME VARCHAR(60), ADDRESS1 VARCHAR(255), ADDRESS2 VARCHAR(255), ADDRESS3 VARCHAR(255), ADDRESS4 VARCHAR(255), CITY VARCHAR(25), REGION VARCHAR(25), POSTALCD VARCHAR(25), COUNTRY VARCHAR(25), PHONE VARCHAR(25), COMPANY VARCHAR(255), LEADTXT VARCHAR(255), CONFERENCE VARCHAR(255), EMAIL VARCHAR(60))`

  Insert some sample data into the LEADS table.


## Using the template

1. Click **Create flow** to start using the template.
1. Click each node to review its configuration. If necessary:
   - Connect to your [Salesforce account](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/use-ibm-app-connect-salesforce/).
   - Connect to your [IBM Db2 account](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/use-ibm-app-connect-ibm-db2/).
1. In the IBM Db2 node, check that the **Where** condition matches the CONFERENCE column in the Db2 table to the **Conference** custom field in your Salesforce campaign.
1. To start the flow, in the banner open the options menu [&#8942;] and then click **Start flow**.
