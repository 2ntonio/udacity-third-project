## Pipeline Process

- After pushing the code to github:
    1. CircleCI detects new changes then it reads the configuration file from `.circleci/config.yml`
    2. CircleCI first runs the orbs as described in the configuration file to install `node, aws, eb cli`
    3. CircleCI second runs the jobs as described in workflow :
        - Steps of building the app first
            - First: 
                1. Preparing ENV
                2. Installing Node, AWS CLI
                3. Then Checkout step used to check out source code to the configured path
                4. Installing Frontend Dependencies 
                5. Installing Backend Dependencies
                6. Linting Frontend
                7. Building Frontend
                8. Building backend
                9. Waiting for manual approval for deploying the app
            - Second: 
                1. Preparing ENV
                2. Installing Node, AWS CLI, EB CLI
                3. Configuring AWS Access Keys
                4. Checking out
                5. Installing Frontend Dependencies
                6. Installing Backend Dependencies
                7. Building Frontend
                8. Building Backend
                9. Deploying both apps:
                    - Deploying backend first
                    - Deploying frontend last


