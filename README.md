# Postman API Automation Integration with Github Actions #
 This repository is a demonstration for POC for integrating postman test with github actions. The Test are written in Postman and they are executed on VM with the help of newman and newman-reporter-htmlextra.
 Github Actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch. The Projects runs on a scheduled time with the help of cron job.

 The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from github page : https://zeetkumar.github.io/Phoenix-Inwarranty-Flow/.
 The latest report is mailed to the team members using GMAIL SMTP.

 ## About Me ##
 Hi My Name is Jiten Ram. I have 5 years of experince in Automation testing and Devops.My SkillSet Includes UI Automation with Selenium Webdriver,Playwright and for API Testing I Use Rest Assured and Postman
 You can connect with me over:(https://www.linkedin.com/in/jitendratnitskm/)

 ## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Managements with Github Secrets 

 ## Tech Stack ##
 
 1. Postman
 2. Nodejs 22
 3. Newman
 4. Newman-Reporter-Htmlextra
 5. Github Actions
 6. Gmail SMPT
 7. Github Pages
 8. CSV for Data Driven Testing
 9. AWS-EC2 instance for Self hosted github runner.

 ## Github Pages ##
 You can directly view the latest test report of the Postman Test at the Github Page Link: https://zeetkumar.github.io/Phoenix-Inwarranty-Flow/

 # HTML Report ## 
The Report will be created in the newman folder
![Postman Report](https://github.com/zeetkumar/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ Inwarranty-flow Collection.postman_collection.json # Collection File
├─ QA.postman_environment.json #Environment File
└─ testdata.csv # TestData File

```

 # How to run the Project? ##
 You can run the project on your local system for that:
 1. Clone the Project on Local System: https://github.com/zeetkumar/Phoenix-Inwarranty-Flow.git
 2. Install Nodejs and NPM from https://nodejs.org/en
 3. Install Newman using``` npm install -g newman```
 4. Install Newman-reporter-htmlextra``` npm install -g newman-reporter-htmlextra```
 5. Run the Newman Command:
```
         newman run "Inwarranty-flow Collection.postman_collection.json" \
          -e "QA.postman_environment.json" \
          -d "testdata.csv" \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html
```
