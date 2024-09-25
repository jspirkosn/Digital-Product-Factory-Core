![image](https://github.com/user-attachments/assets/2892501b-610b-4ac4-89e8-7cbbfd07c5f0)# Digital-Product-Factory-Core
The Digital Product Factory fast-tracks digital transformation by automating the builds of secure, compliant, and user-friendly digital products and services that run on the ServiceNow platform.
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
    - Branch: master
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
<summary>Government Factory Templates</summary>
	This is the start of templates
</details>

# Creating New Factory Templates
In this section, we call out how to build and add a new template to the Digital Product Factory.
1. Open App Engine Studio and Go to Templates
   ![image](https://github.com/user-attachments/assets/a6853d7d-c21d-4496-a8fa-3fb2d1fc3d73)
1. hover over any of the existing factory templates and choose "use template"
1. When the app creator comes up, choose a name that represents your new template
1. In the example below, I'm creating a template for licensing and permitting, so I named it "Pub Sub" to represent a Public Sector Sub-App and "licenses and permits" to represent the type of app
   ![image](https://github.com/user-attachments/assets/7c0d66bb-cea3-42bb-af85-0d8efbc3614e)
1.   




