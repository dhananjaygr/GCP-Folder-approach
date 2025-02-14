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

6. Then, under the template permissions, provide the following details:

   Platform Friendly Name: **Google Cloud Platform (1)**
   Permission Type: **Custom Role (2)**
   Profile Type: **Attendee (3)**
   Scope: **GCP Folder (4)**
   Custom Role URL: **abc.json**

   ![](/img/05.png)

6. 

   >**Note:** For now, to access the folder, we need to provide folder-level permissions through a custom role. In the future, a separate built-in role for folder     access will be available. 

   Below is a sample that includes permissions for Folder management, Project management, IAM roles, Compute Engine, Networking, Storage, and more.
   **Link:** [Basic Custom Role](https://cloudlabs-gcp.s3.us-east-1.amazonaws.com/gcpcustomrole.json)

7. 
