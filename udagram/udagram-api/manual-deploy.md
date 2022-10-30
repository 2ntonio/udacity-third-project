## Follow these steps to deploy an elastic beanstalk application

1. Start by connecting the EB CLI to the environment with `eb use <application-name>`.
2. To deploy the Application use `eb deploy`. This will zip the server files and start uploading in AWS Elastic Beanstalk.
3. After several minutes if the these lines were available that means everything is `OK` :  
    - INFO: Environment update is starting.
    - INFO: Deploying new version to instance(s).
    - INFO: New application version was deployed to running EC2 instances.
    - INFO: Environment update completed successfully.