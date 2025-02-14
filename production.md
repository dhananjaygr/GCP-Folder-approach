## GCP Folder Approach

### Feature Requirement
Set up the folder approach with four projects under each folder.

### Implementation
Each CloudLabs user deployment will be granted folder access, along with access to four projects and associated resources based on the permissions set.

### Steps for Testing the GCP Folder Approach:

1. Log in to the CL portal and navigate to the required tenant (WIZ). On the left-hand side of the page, you will see the Template section.

2. Navigate to the **Template (1)** section in the left menu and click on the **edit (2)** button.

   ![](/img/01.png)

3. Then, scroll down to the **Cloud Platform Configuration** section and click on the **Edit** button.

   ![](/img/02.png)

4. Under the **Cloud Platform Configuration section,** select the **Dedicated Tenant** option and then click the **Submit** button.

   ![](/img/03.png)

   ![](/img/04.png)

5. In the template, under the Cloud Template section, provide the necessary Cloud Template URL and Parameter URL if you want the resources to be ready for use when 
   the deployment happens.

   >**Note:** All Cloud Template deployments will be deployed under the first project only.

   ![](/img/template.png)

6. Then, under the **Edit Template Permissions,** provide the below-mentioned details: 

   Platform Friendly Name: **Google Cloud Platform (1)**

   Permission Type: **Custom Role (2)**

   Profile Type: **Attendee (3)**

   Scope: **GCP Folder (4)**

   Custom Role URL: **https://cloudlabs-gcp.s3.us-east-1.amazonaws.com/gcpcustomrole.json (5)**
   
   Then, Click on the **Submit (6)** button.

   ![](/img/05.png)

   >**Note:** For now, to access the folder, we need to provide folder-level permissions through a custom role. 
   >In the future, a separate built-in role for folder access will be available. 

   Below is a sample that includes permissions for Folder management, Project management, IAM roles, Compute Engine, Networking, Storage, and more.

   **Link:** [Basic Custom Role](https://cloudlabs-gcp.s3.us-east-1.amazonaws.com/gcpcustomrole.json)

7.  Now, provide the additional template permissions. Click on the **Add** button and provide the below-mentioned details:

    Platform Friendly Name: **Google Cloud Platform (1)**

    Permission Type: **Basic Role (2)**

    Profile Type: **Attendee (3)**

    Scope: **GCP Folder (4)**

    Permission: **Owner (5)**

    Then, Click on the **Submit (6)** button.

    ![](/img/06.png)

    ![](/img/07.png)

    >**Note:**  Giving Owner permissions at the folder level gives the user full control over the projects under it, allowing them to deploy, modify, and manage resources.

    >Projects will inherit permissions from the folder. Other resource or IAM-related permissions can be defined using custom roles and applied as needed.

8. Now, click the Submit button to submit the template.

9. Go to the **ODL (1)** section and click on the **Users (2)** section.

    ![](/img/08.png)

10. Now, deploy an ODL user from the **users** section.

11. Outputs Based on the Deployment:

    Below is the screenshot for the folder and the 4 projects that are accessible.

    ![](/img/09.png)

    Below is the screenshot for the Cloud Template deployment that occurred in the first project, as specified in the template.

    ![](/img/10.png)

    Below is the screenshot for the resources created in the other 3 projects.

    ![](/img/11.png)

    ![](/img/12.png)

    ![](/img/13.png)
    
