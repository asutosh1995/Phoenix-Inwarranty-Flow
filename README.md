# Postman API Automation Integration with Github Action #


This repository is a demonstration for POC for integrating postman test with github action. The tests are written on postamn and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Action will trigger the project execution on every push to main branch.You can also execute the project manually using workflow_dispatch. The project runs ona aschedule time with the help of cron job.


The html reports is archived and kept in the artifact section for the team to download, alongwith that they can view the report directly from the github page: https://asutosh1995.github.io/Phoenix-Inwarranty-Flow/ .

The latest report is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi, myself Asutosh Acharya . I have 7 years of experience in Automation testing. My skill set includes Selenium Webdriver and API  testing using Postman and Rest Assured.You can connet with me at :(https://www.linkedin.com/in/asutosh-acharya-qa/) 

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing
3. Edge Case testing
4. Token Testing
5. Data driven testing with csv
6. Schema Validation
7. Secrets Management with Github Secrets




## Tech Stack ##
1. Postman
2. Node js v22
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. CSV for Data Driver Testing
8. AWS-EC2 instance for Self hosted github runner

## Github Pages ##
You can directly view the latest test report of the Postman test at the Github Page : https://asutosh1995.github.io/Phoenix-Inwarranty-Flow/


## HTML Report ##
The report will be created in the newman folder
![Postman Report](https://github.com/asutosh1995/Phoenix-Inwarranty-Flow/blob/static-content/newman.png)

![Postman Report](https://raw.githubusercontent.com/asutosh1995/Phoenix-Inwarranty-Flow/static-content/newman.png)

## Project Structure ##
```
Phoenix-Inwarranty-Flow
├─ Inwarranty-flow Collection Copy-with external csv.postman_collection.json  # Collection File
├─ QA.postman_environment.json # environment file
└─ testdata.csv # test data file

```


## How to run the project ##
You can run the project on your local system for that :
1. Clone the project on local system: https://github.com/asutosh1995/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from : https://nodejs.org/en/download
3. Install Newman using the command : ```npm install -g newman ```.  For mac users please use sudo before it.
4. Install Newman-reporter-htmlextra using the command :``` npm install -g newman-reporter-htmlextra```
5. Run the newman command :

   ```
              newman run 'Inwarranty-flow Collection Copy-with external csv.postman_collection.json' \ 
              -e QA.postman_environment.json \
              -r cli,htmlextra \
              --reporter-htmlextra-export ./newman/index.html
   ```


