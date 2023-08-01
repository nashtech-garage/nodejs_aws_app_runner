# AWS App Runner

Deploy containerized web applications and APIs at scale.

AWS App Runner is a fully managed container application service that allows build and run secure web applications at scale without prior container or infrastructure experience.

![Diagram outlines the steps for creating an App Runner service](images/step_outline.png)

Step by step to create App Runner Service

## Go to App Runner Console

![Create App Runner Service](images/Create_App_Runner_Service.png)

## Step 1: Source and Deployment
![Step 1: Add Github Repo](images/Step1_Add_GitHub_Repo.png)

At the repository type, we can choose "Container registry" or "Source code repository". In this example, we will choose "Source code repository".

Click "Add new" button to create connection to Github

![Step 1: Github create new connection](images/Step1_GitHub_Connector_Create_New_Connection.png)

![Step 1: Github create new connection install new app](images/Step1_GitHub_Connector_Create_New_Connection_Install_New_App.png)

After click "Install Another" button, it will require permission to connect Github app

![Allow AWS Connect to GitHub](images/Step1_GitHub_Connector.png)

![Approve GitHub connect to AWS](images/Step1_GitHub_Connector_Create_New_Connection_Install_New_App_Install_For_GitHub.png)

![Approve GitHub connect to AWS](images/Step1_GitHub_Connector_Create_New_Connection_Install_New_App_Install_For_GitHub_Choose_Repo.png)

![Repo display in Dropdown](images/Step1_GitHub_Connector_Create_New_Connection_Repo_In_DropDown.png)

## Step 2: Configure build

![Open Configure Build](images/Step2_Configure_Build.png)

![Update value of configuration](images/Step2_Configure_Build_Configuration.png)

At step 2 we can configure manual or create "apprunner.yaml" at code folder

![Apprunner Yaml File](images/apprunner-yaml.png)

## Step 3: Configure service

![Configure service for app runner](images/Step3_Configure_Service.png)

At this step, we can choose configuration for service.

## Step 4: Review and create

![Review and Create](images/Step4_Review_And_Create.png)

## Finally

After finish step 4, we can see the dashboard of StartAppRunner Service

![Dashboard of StartAppRunner](images/Step_Done.png)

Wait some minutes (5min), we will see the result

![Deploy Success](images/Deploy_Success.png)

If our code have problem, service will automatic roll back.
![Roll back when we got problem](images/Build_Wrong.png)

Because we choose manual, so if we want to deploy again, click "Deploy" button.
