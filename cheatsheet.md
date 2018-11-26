# Creating CRUD Application with MongoDB, IBM Cloud and Node JS

The below markdown file consists of commands, links and code snippets that will help you complete and understand the lab - Creating CRUD Application with MongoDB, IBM Cloud and Node JS. 

## Running the app locally

• Clone the application from the repository 
• cd into the project folder and if required by any modules, run

```
	npm install
```		
• Start the application by typing
```
	node app.js
```		
• When the application executes, the first line will say:
```
	http://localhost:<port_number>
```		
Paste this URL in the browser to open the application.

## Running the app on Cloud

• Download and install Cloud Foundry CLI to be used on the terminal
• Open the command prompt where the application exists
• On the Terminal, Connect to IBM Cloud using the CF CLI and follow the prompts to log in. 
• Once you're in the same space as the app,

```
  cf api https://api.eu-gb.bluemix.net
  cf login
```

• Create the manifest.yml file and change the <unique_name> parameter to something unique.

```
  applications:
    - path: .
    name: <Unique_Name>
    host: <Unique_Name>
    framework: node
    memory:256M
    instances: 1
    services:
    - <service-name>
```  

## Troubleshooting

To troubleshoot your IBM Cloud app the main useful source of information are the logs, to see them, run:

  ```
  $ cf logs <application-name> --recent
  ```