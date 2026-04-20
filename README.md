# Postman API Automation Integration with Github Actions #
This repository is a demonstration for poc for integrating postman with github actions. the tests are written in postman and they are executed on the vm with help of 
newman and newman-reporter-htmlextra.
github actions will trigger the project execution on every push to the main branch. you can also execute the project manually using workflow_dispatch. the project run the 
schedule time with help of cron job.

The html report is archived and kept in the artifact section for team to download it. along with that they can view the report directly from page: 
https://vishal-ingawale.github.io/Phoenix-Inwarranty-flow/.
The latest report is mailed ti the team members using GMAIL SMTP.

## About Me ##
Hi, My name is Vishal. I have 3.5 Years of Experience in Automation Testing & DevOps. My skillset includes UI Automation with Selenium Webdriver, Playwrite and for API Testing
I use Rest Assured and Postman. You can connect with me over: LinkedIn

## Testing Coverage ##
1. Happy Flow testing
2. Negative Testing Edge case Testing
3. Token Testing
4. Data Driven Testing with csv
5. Schema Validation
6. Secrets management with Github secrets

## Tech Stack ##
1. Postman
2. nodejs 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github actions
6. Gmail smtp
7. Github pages
8. csv for data driven testing
9. AWS-EC2 instance for self hosted github runner

## GitHub Pages ##
You can directly view the latest Test report of the postman test at the GitHub page link:
https://vishal-ingawale.github.io/Phoenix-Inwarranty-flow/

## HTML Report ##
The Report will be created in the newman folder

![Postman Report](https://github.com/Vishal-Ingawale/Phoenix-Inwarranty-flow/blob/static-content/Screenshot%202026-04-20%20145742.png)


## Project Structure ##
```
Phoenix inwarranty flow
├─ Inwarranty-flow collection Copy.postman_collection.json # Collection File
├─ QA.postman_environment.json # Environment File
└─ testdata.csv # Test Data File

```

## How to run the project ##
you can run the project on your local system for that:

1. Clone the project on local system: 
https://github.com/Vishal-Ingawale/Phoenix-Inwarranty-flow.git
2. Install nodejs and npm from 
https://nodejs.org/en
3. Install newman using npm install -g newman
4. Install newman-reporter-htmlextra npm install -g newman-reporter-htmlextra
5. Run the newman command:
```
          newman run 'Inwarranty-flow\ collection\ Copy.postman_collection.json' \
          -e QA.postman_environment.json \
          -d testdata.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html
```











