# JEEVAN 

## Problem

It is projected that by the year 2025, 60% of the world’s land mass and billions of people will find themselves in the water-scarce situation. At a minimum world will face economic challenges from this water scarcity, and at the maximum the world will face a grave humanitarian crisis. Hundreds of millions of people will suddenly find themselves in places where there once was water but there is no longer.

According to a NitiAayog report on water management index last year, India is currently suffering from the worst water crisis in its history with the country ranked at 120 among 122 countries in the quality of water. By 2020, it said, as many as 21 major cities of India including Delhi, Bangalore, Chennai, and Hyderabad will run out of water.

India is among the world’s most water-stressed countries. Yet,India remains one of the largest water users per unit of GDP.This suggests that the way in which India manages its scarce water resources accounts for much of its water woes. Government capacities are lacking as far as improving water management is concerned, while policies and incentives often favor inefficient and unproductive use of water. It’s high time we all have to be conscious for our most valuable resource of Earth.

![alt text](https://github.com/jeevanlife2020/Jeevan/blob/master/pic.png?raw=true)

## Solutions:

JEEVAN is a single platform for water management system, where we can measure, monitor and predict the usage of water at a per capita basis of the gross domestic product (GDP). There are many organizations which are already doing a bits and pieces of work for the water crisis awareness and water management, but there is no single platform where everyone can reach out and get the information regarding the water usage at a per capita basis and can also get the information of the water usage of an area and can also get the information regarding the prediction of the water usage in the upcoming 5 years. JEEVAN is an open-source AI enabled platform that serves as a one-stop for the water usage measure, monitor, prediction and can also check the water wastage at a very granular level.

For Users, JEEVAN is an extremely easy-to-use, user-friendly platform where the user can measure the water usage of the family and can also check the flowrate of the water. The user can also get aware of the leakage, if any by using this platform and can control the water wastage.

•	JEEVAN is computable – JEEVAN measures the usage of water for individual family and also monitors the flowrate of each family and the total usage of water in an area. By using JEEVAN we can keep a track on the water consumption of each family and as a result we can control the unnecessary wastage of water.

•	JEEVAN is intelligent – JEEVAN keeps a track of the continuous flow rate of each family and can also monitor if there is any water leakage occurred in any pipeline and send an email to the registered user where the leakage is detected. By using JEEVAN we can easily track if any leakage occurs and can take actions on that leakage without wasting a lot of water.

•	JEEVAN is AI enabled – JEEVAN platform is AI- enabled, it is trained over 10 years of water consumption data over different postal areas. It can predict the water usage of all the postal areas for the upcoming 5 years. By using JEEVAN we can get a clear scenario of the water scarcity that may occur in the upcoming years and as a result we can get aware of the scenario and control the unnecessary wastage of water.


Scopes and the potential use-cases of JEEVAN is endless – We usually measure the usage of the electricity internet telephone and pay the bills, but we forget to measure the usage of the water and as a result we do unnecessary wastage in the areas where we get water easily and on the other side the areas those who face water scarcity has to fight even for drinking water. By using JEEVAN we can get a clear scenario of the areas that will face the water stress in the near future. We can restrict the unnecessary wastage of water and can transmit the conserved water to the nearby area where the water scarcity hits. By doing so we can atleast give some water to those who starve for the drinking water. By using the JEEVAN platform the Governments and the organizations that works for the water crisis awareness program and the water management program can get the easy access to the detailed information’s of the water usage and the prediction of the scarcity of water and as a result they can take the proper precautions steps to control the scenario’s.



# Getting Started with Python on IBM Cloud

To get started, we'll take you through a sample Python Flask app, help you set up a development environment, deploy to IBM Cloud and add a Cloudant database.

The following instructions are for deploying the application as a Cloud Foundry application. To deploy as a container to **IBM Cloud Kubernetes Service** instead, [see README-kubernetes.md](README-kubernetes.md)

## Prerequisites

You'll need the following:
* [IBM Cloud account](https://console.ng.bluemix.net/registration/)
* [Cloud Foundry CLI](https://github.com/cloudfoundry/cli#downloads)
* [Git](https://git-scm.com/downloads)
* [Python](https://www.python.org/downloads/)

## 1. Clone the sample app

Now you're ready to start working with the app. Clone the repo and change to the directory where the sample app is located.
  ```
git clone https://github.com/Project-JEEVAN/Jeevan-Dashboard.git
cd Jeevan-Dashboard
  ```

  Peruse the files in the *Jeevan-Dashboard* directory to familiarize yourself with the contents.

## 2. Run the app locally

Install the dependencies listed in the [requirements.txt](https://pip.readthedocs.io/en/stable/user_guide/#requirements-files) file to be able to run the app locally.

You can optionally use a [virtual environment](https://packaging.python.org/installing/#creating-and-using-virtual-environments) to avoid having these dependencies clash with those of other Python projects or your operating system.
  ```
pip install -r requirements.txt
  ```

Run the app.
  ```
python server.py
  ```

 View your app at: http://localhost:8000

## 3. Prepare the app for deployment

To deploy to IBM Cloud, it can be helpful to set up a manifest.yml file. One is provided for you with the sample. Take a moment to look at it.

The manifest.yml includes basic information about your app, such as the name, how much memory to allocate for each instance and the route. In this manifest.yml **random-route: true** generates a random route for your app to prevent your route from colliding with others.  You can replace **random-route: true** with **host: myChosenHostName**, supplying a host name of your choice. [Learn more...](https://console.bluemix.net/docs/manageapps/depapps.html#appmanifest)
 ```
 applications:
 - name: GetStartedPython
   random-route: true
   memory: 128M
 ```

## 4. Deploy the app

You can use the Cloud Foundry CLI to deploy apps.

Choose your API endpoint
   ```
cf api <API-endpoint>
   ```

Replace the *API-endpoint* in the command with an API endpoint from the following list.

|URL                             |Region          |
|:-------------------------------|:---------------|
| https://api.ng.bluemix.net     | US South       |
| https://api.eu-de.bluemix.net  | Germany        |
| https://api.eu-gb.bluemix.net  | United Kingdom |
| https://api.au-syd.bluemix.net | Sydney         |

Login to your IBM Cloud account

  ```
cf login
  ```

From within the *Jeevan-Dashboard* directory push your app to IBM Cloud
  ```
cf push
  ```

This can take a minute. If there is an error in the deployment process you can use the command `cf logs <Your-App-Name> --recent` to troubleshoot.

When deployment completes you should see a message indicating that your app is running.  View your app at the URL listed in the output of the push command.  You can also issue the
  ```
cf apps
  ```
  command to view your apps status and see the URL.

## 5. Add a database

Next, we'll add a NoSQL database to this application and set up the application so that it can run locally and on IBM Cloud.

1. Log in to IBM Cloud in your Browser. Browse to the `Dashboard`. Select your application by clicking on its name in the `Name` column.
2. Click on `Connections` then `Connect new`.
2. In the `Data & Analytics` section, select `Cloudant NoSQL DB` and `Create` the service.
3. Select `Restage` when prompted. IBM Cloud will restart your application and provide the database credentials to your application using the `VCAP_SERVICES` environment variable. This environment variable is only available to the application when it is running on IBM Cloud.

Environment variables enable you to separate deployment settings from your source code. For example, instead of hardcoding a database password, you can store this in an environment variable which you reference in your source code. [Learn more...](/docs/manageapps/depapps.html#app_env)

## 6. Use the database

We're now going to update your local code to point to this database. We'll create a json file that will store the credentials for the services the application will use. This file will get used ONLY when the application is running locally. When running in IBM Cloud, the credentials will be read from the VCAP_SERVICES environment variable.

1. Create a file called `vcap-local.json` in the `Jeevan-Dashboard` directory with the following content:
  ```
  {
    "services": {
      "cloudantNoSQLDB": [
        {
          "credentials": {
            "username":"CLOUDANT_DATABASE_USERNAME",
            "password":"CLOUDANT_DATABASE_PASSWORD",
            "host":"CLOUDANT_DATABASE_HOST"
          },
          "label": "cloudantNoSQLDB"
        }
      ]
    }
  }
  ```

2. Back in the IBM Cloud UI, select your App -> Connections -> Cloudant -> View Credentials

3. Copy and paste the `username`, `password`, and `host` from the credentials to the same fields of the `vcap-local.json` file replacing **CLOUDANT_DATABASE_USERNAME**, **CLOUDANT_DATABASE_PASSWORD**, and **CLOUDANT_DATABASE_URL**.

4. Run your application locally.
  ```
python server.py
  ```

  View your app at: http://localhost:8000. Any names you enter into the app will now get added to the database.

5. Make any changes you want and re-deploy to IBM Cloud!
  ```
cf push
  ```

  View your app at the URL listed in the output of the push command, for example, *myUrl.mybluemix.net*.
  
 ## 7. User guide
 To use the Jeevan application to monitor water usage, new device installation, [see README-user-guide.md](README-user-guide.md)
