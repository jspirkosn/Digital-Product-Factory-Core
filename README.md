# Digital-Product-Factory-Core
The Digital Product Factory fast-tracks digital transformation by automating the builds of secure, compliant, and user-friendly digital products and services that run on the ServiceNow platform.
# Using the Digital Product Factory
There are two ways to use the Digital Product Factory: either install it on your own instance following the installation instructions below or use the current version on our shared instance. <li><a href="mailto:john.spirko@servicenow.com?subject=Request to access the Digital Services Forum shared ServiceNow instance &amp;body= Please grant me admin access to the dswrkgrpdemo instance." target="_self">Get a Link to our shared instance (Request in email)</a></li> 
- Once logged in to an instance with the factory installed, go to the Employee Center (https://[your_instance].service-now.com/esc) and click on the "Digital Factory Services" menu
  ![image](https://github.com/user-attachments/assets/a87cd96f-a043-4da6-aab7-1f5c2df38040)
- Select one of the available factories and fill out the form

  Note: If the developer is not a user, the factory will create the user and assign them development privledges to this app only
- Submit the form
- Within five minutes an email will be sent to the developer and the submitter with instructions on how to proceed. See the example below:
  ![image](https://github.com/user-attachments/assets/391324c2-010d-4660-af36-18f018f0244b)

# Factory Installation Instructions
1. Install the following pre-requisite plugins onto the target instance (instance that will contain the factory application)
    - Workflow Studio
    - ServiceNow IntegrationHub Action Step - JSON Builder
    - App Engine Studio
3. GitHub Access - use an existing account or [GitHub Create Account](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
1. Log into your GitHub Account
1. In the browser where you logged in to GitHub, paste this URL: [https://github.com/jspirkosn/Digital-Product-Factory-Core]
1. In the upper right-hand corner of the page, you should see a button to fork the repo. Click to create your fork
1. Create a ServiceNow Credential - if you have a GitHub credential for ServiceNow, skip this step
    - Go to https://github.com/settings/tokens, and under Tokens (classic), click on "Generate new token"
    - Copy the token you generated; you'll need it in the next step
    - In the ServiceNow Navigator, go to "Connections & Credentials" -> "Credentials"
    - Click on "New" to create a new credential
    - Chose "Basic Auth Credential"
    - Give it a name and enter your **GitHub** User Name and Enter the token from above as your password (Note your GitHub password won't work)
1. In the ServiceNow Navigator, go to "System Applications" -> "Studio"
1. A dialog appears - click on "Import from Source Control"
    - URL: https://github.com/[your github user]/Digital-Product-Factory-Core (this is a reference to the forked repo you created)
    - Branch: main
    - Credential: chose credential from step 7   
1. Access the Employee Service Center - [your instance]/esc
	- Click on the "Digital Factory Services" topic
	- Select the "Digital Product Factory for Government Agencies" catalog item
1. Post Installation Instructions
	- On the target instance, set the permission for these four tables as shown below (You must be an admin to do this)
	![image](https://github.com/user-attachments/assets/2ab5006b-ba10-433e-a75e-7929b7b0c907)
	These are direct links to the permission pages:
		- **Sys_user_group:** https://[your_instance].service-now.com/now/nav/ui/classic/params/target/sys_db_object.do%3Fsys_id%3Dsys_user_group%26sysparm_refkey%3Dname
		- **Sc_category:** https://[your_instance].service-now.com/now/nav/ui/classic/params/target/sys_db_object.do%3Fsys_id%3Dsc_category%26sysparm_refkey%3Dname
		- **Sc_cat_item:** https://[your_instance].service-now.com/now/nav/ui/classic/params/target/sys_db_object.do%3Fsys_id%3Dsc_cat_item%26sysparm_refkey%3Dname
		- **Sc_cat_item_category:** https://[your_instance].service-now.com/now/nav/ui/classic/params/target/sys_db_object.do%3Fsys_id%3Dsc_cat_item_category%26sysparm_refkey%3Dname
	- Setup the connection credential so that 
1. See the "Installing Factory Templates" section for your Industry

Note: The factory will need to have the appropriate templates before it can build a product

The core install is now complete!

# Installing Factory Templates
The factory runs purpose-built factory templates.  This section will walk you through how to install the available templates. 
<details>
<summary>Public Sector Factory Templates</summary>
All Public Sector template repositories are pre-fixed with PST; for example, "PST- HHS Program Support Desk." The Digital Product Factory for Public Sector is part of the Digital Product Factory Core, but you will need to install the templates below or create  templates for the factory to function.

The list below contains a series of templates. Follow these instructions for each template. The illustration below the templates shows a list of dependent plugins.
1. Log into your GitHub Account (see the factory installation section above for more details) 
1. In the browser where you logged in to GitHub, paste the template URL you want to install from the List of Available Public Sector Factory Templates below  
1. In the upper right-hand corner of the page, you should see a button to fork the repo. Click to create your fork
1. Note the URL of your new repository that was created. It should be similar to the name of the repo you forked in the last step 
1. You should already have a GitHub credential in your ServiceNow instance, if you don't (see the factory installation section above for more details on how to get one)
1. In the ServiceNow Navigator, go to "System Applications" -> "Studio"
1. A dialog appears - click on "Import from Source Control"
    - URL: https://github.com/[your github user]/[template repository] (this is a reference to the forked repo you created above)
    - Branch: main
    - Credential: chose GitHub credential   
	
**List of Available Public Sector Factory Templates:**
1. **PST - HHS Program Support Desk** https://github.com/jspirkosn/PST---HHS-Program-Support-Desk
   ![image](https://github.com/user-attachments/assets/ec4a6e39-cc0a-439c-ba74-b5775a64b724)
1. **PST - Licensing and Permitting** https://github.com/jspirkosn/PST---Licensing-and-Permitting
    ![image](https://github.com/user-attachments/assets/cae07e6b-9bfd-4cca-8f15-5430c3df2945)
</details>
<details>
<summary>Financial Services Factory Templates</summary>
All Financial Services template repositories are pre-fixed with FST; for example, "FST - Power of Attorney." The Digital Product Factory for Financial Services is part of the Digital Product Factory Core but you will need to install the templates below or create your own templates for the factory to function.
	
**List of Available Financial Service Factory Templates:**
1. **Coming Soon** 
1. **Coming Soon** 
</details>

# Creating New Factory Templates
This section provides the details needed to build and add a new template to the Digital Product Factory.
1. Open App Engine Studio and Go to Templates
   ![image](https://github.com/user-attachments/assets/a6853d7d-c21d-4496-a8fa-3fb2d1fc3d73)
1. hover over any of the existing factory templates and choose "use template"
1. When the app creator comes up, choose a name that represents your new template but don't name it the same as your template
1. In the example below, I'm creating a template for licensing and permitting, so I named it "Pub Sub" to represent a Public Sector Sub-App and "licenses and permits" to represent the type of services the app will provide
   ![image](https://github.com/user-attachments/assets/7c0d66bb-cea3-42bb-af85-0d8efbc3614e)
1. You now have an app that your template will be based on, as shown below
   ![image](https://github.com/user-attachments/assets/74884486-f00c-4a24-8b91-9821388580d2)
1. Configure the app that will be the basis for the template
	- Configure Tables
		- Use the {program name} tag in your table labels (A factory workflow will replace that tag with the Product Name)
 		- In the next step, you will create at least one record producer for each of these tables (these tables should extend the industry model tables and comply with the industry reference architecture) 
	- Configure the record producers
		- There are two types of record producers: one used on the Service Delivery Side and the other on the Service Support side. The difference between the two is in the objects associated with them by the factory. The support side records producers are classified according to the CSDM, and the delivery side uses the industry data models provided by the ServiceNow industry teams. 
		- For the support type, the factory populates the business service and provides a list selector for the offering (Note: you can only submit tasks against the services contained in this product)
 		- For the support type, use the {program name support} tag in the label; this is how the factory knows to pre-populate the business service, and the service offering selector is dependent on it
		- For the support type, you must leave the Business Service ID and the Service Offering questions on the record producer for the factory to populate them; see example below
		  ![image](https://github.com/user-attachments/assets/8c43f56c-c46a-452c-bcfb-f03b1f94b77b)
 
 	 	
		- For the delivery type, the factory populates the product model, service (CSM Service, not CSDM service), and assignment group 
		- For the delivery type, use the {program name deliver} tag in the label; this is how the factory knows to pre-populate the product model, assignment group, and case type
		- For the delivery type, you must leave the Product, Service, and Assignment Group questions on the record producer for the factory to populate them; see example below
		  ![image](https://github.com/user-attachments/assets/85b98ae6-fe9a-44c9-9448-dd2cbf8b0a5b)
	- Configure the playbook and flows
		- Do not alter the {program name} Initialize flow; the factory calls this flow to configure the application 
		- Use the {program name} tag in your table labels (A factory workflow will replace that tag with the Product Name)
  		  ![image](https://github.com/user-attachments/assets/947e14ce-0e11-4a41-9336-6f9da2c0b006)

1. In App Engine Studio, Go to Templates
1. Click "Create new template" in the upper right and select "Existing app"
1. Open Workflow Studio and open the "Build a New Digital Product" flow
1. Copy one of the sections shown in steps 13 through 17 below
   ![image](https://github.com/user-attachments/assets/764b6309-e7a4-4f63-8e78-01e52a25d66a)
1. In the navigator, type "sys_app_template.list" to open the App Template table
1. Find your template and open the template record
1. Open the hamburger menu and copy the sys_id as shown below
   ![image](https://github.com/user-attachments/assets/89d67855-6955-4111-8b66-18fdf9f24f5b)
1. Go back to the Workflow "Build a New Digital Product" workflow and past your sys_id in the "Invoke Product Templates" Action Step as shown below
   ![image](https://github.com/user-attachments/assets/dd269303-0c6f-4f2a-af22-dc1ce733e09e)
1. After the "Invoke Product Templates" call the "Initialize Product" action as shown below (this is a call back to the newly build app to configure names)
   ![image](https://github.com/user-attachments/assets/df4272a4-e0ca-4fd7-8763-46921f6431ce)
1. After the "Initialize Product" set flow variables as shown below
   ![image](https://github.com/user-attachments/assets/a154e477-49fa-4549-80b1-a005a3818118)
1. After the flow variables configure the developer notification email as shown below
   ![image](https://github.com/user-attachments/assets/121ec302-e04f-4f0c-8e94-0434fcbe4e89)
   ![image](https://github.com/user-attachments/assets/1d9a70f0-6fc7-44bf-84ea-267af52d3c6b)


   
 

   


          
		
   




