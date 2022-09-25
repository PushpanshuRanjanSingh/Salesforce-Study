## <u>SALESFORCE ROADMAP</u>

1. **Salesforce Admin:** 
    1. Objects 
    2. Fields and Relationships 
    3. Validation Rules 
    4. Page and Layouts

2. **Process Builder:** It is a point-and-click tool that lets you easily automate if/then business processes and see a graphical representation of your process as you build.
    1. Create/Update Records
    2. Send Emails
    3. Call other Process Builder
    4. etc

3. **Apex Class:** It is a strongly typed, object-oriented programming language for building SaaS and CRM.
    > Similar Syntax as Java
    
    ```apex
    //eg.
    public class ApexClass{
        public static void main(){
            // code here
        }
    }
    ```
    
    **Features of APEX Class:**
    1. Case Insensitive Language
    2. Perform DML Operations like Insert, Update, and Delete on Salesforce Object records.
    3. Query sObject records using SOQL(Salesforce Object Query Language), SOSL(Salesforce Object Search Language)
    4. Salesforce Object can be used as a Datatype. 
    
    ```apex
    //eg.
    Contact contact = new Contact()
    ```
    
4. **SOQL:**
    1. It is used to search your organisation's salesforce data for specific information.
    2. It is similar to SELECT Statement in the widely used SQL but designed specifically for Salesforce data.
    
    ```apex
    //eg.
    SELECT Id, Name from Account WHERE NAME="Salesforce"
    ```  

5. **SOSL:**
    1. Use it to construct Text-Based Search Queries against the search index.
    2. Use it when you don't know where the data resides.
    
    ```apex
    //eg.
    FIND {Salesforce} IN Name RETURNING Account
    ```  

6. **APEX Trigger:**
    It provides an option to perform Action before and after the EVENTS to record in Salesforce, such as Insertion, Deletion and Updation.
    
    ```apex
    //syntax
    trigger TriggerName on ObjectName(trigger_events){
        
        //code block
    }
    ```
    
    <u>**Types of Events**</u>
    1. Before Insert
    2. After Insert
    3. Before Delete
    4. After Delete
    5. Before Update
    6. After Update

7. **Lightweight Web Component[LWC]:**
   > **AURA** component is also used for frontend but LWC is Enough
   1. It is a framework for the front end, developed on modern web standards.
   2. It is built using native HTML and javascript.
   3. Here we have HTML, js, config and CSS 
       
      ``` 
        lwc
        |____lwc_Component
        |____|____lwc_Component.html
        |____|____lwc_Component.js
        |____|____lwc_Component.js-meta.xml
        |____|____lwc_Component.css
      ```
    
    4. LWC File Code example

    HTML
    
    ```html
    <template>
        <lightning-card title={myTitle}>
        <p>
            This is my First Lightning Component
        </p>
        </lightning-card>
    </template>
    ```

    Javascript
    
    ```js
    import { LightningElement } from 'lwc';

    export default class MyFirstLwc extends LightningElement {
        myTitle = "Salesforce_Noob"
    }
    ```

    Meta Config
    
    ```xml
    <?xml version="1.0" encoding="UTF-8"?>
    <LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata">
    <apiVersion>55.0</apiVersion>
    <isExposed>true</isExposed>
    <targets>
        <target>lightning__RecordPage</target>
    </targets>
    </LightningComponentBundle>
    ```

    CSS
    
    ```css
    input {color: blue;}
    ```

    

Create Project : SFDX: Create Project with Manifest
Project--->force_app--->main--->default--->lwc

Create Web Component : SFDX: Create Lightning Web Components in the LWC folder
Will get 1 Js File, 1 HTML file with the same name and 1 XML file with the same name

Authorize an Org : SFDX: Authorize an Org

Deploy the source to org : SFDX: Deploy this source to ORD
