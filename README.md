# apigee-ci-cd-for-azure-devops

- Fork this repo
- In the [pom file](pom.xml), update the `apigee.org`,`domain`  property under `dev`, `test` and `prod` POM profile to point to your Apigee org. Feel free to update the pom to your setup
- To run it locally, execute `mvn clean install -P{profile} -Dfile={path_to_service_account_file}`
- Create a Service Account in GCP IAM with `Apigee Org Admin` role and download the JSON file. Upload the same as a Secure file in DevOps as `config.json`. This is used in the pipeline to pass to the Maven plugin to generate the token to call the Apigee Management APIs
