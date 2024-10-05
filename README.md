#This is a guide for running ERPNext to Dokploy
You can follow the docker-compose.yml file for installation.

#Steps
1. Create a project in Dokploy
2. Create a compose service inside the project
3. Inside compose select the provider as Raw
4. Paste the docker-compose.yml code to Raw and save
5. Go to the Domains tab and click on Add domain
6. Select the service as frontend Host as your domain
7. Use port 8080
8. Active SSL with Letsencript
9. Deploy the code from the general tab and wait for 5-10 min after deployment is completed
10. Open your given domain it should run perfectly.

#If you are stuck on the setup page follow the steps below (Resolved in ERPNext:v15.38.0)
1. Open the terminal and select frontend container
2. run bench --site frontend install-app erpnext
3. Open the url in incognito mode and continue with setup.

For more frappe apps follow commands.txt commands
