CI/CD on Python

pylint was the de-facto linter for Python, but flake8 may be more poplar today. Python has official coding style PEP 8. Luckily there is good support for coding styles in good IDE editors and code formatters like black to help the developer keeping this step green.

unittest and pytest are the most common testing frameworks for Python and they work well in CI. Django has it's own testing framework based on unittest. Pytest is suitable for ui testing too.

There is no need to build step (Python is script language), but we need to install dependencies with pip. We can use twine to automatically push to package registry like pypi or we can use heroku-deploy to deploy our application to Heroku. Pyinstaller make it possible to distribute desktop Python application on self-executable binaries.

There are some open source self-hosted alternatives to Jenkins (Concourse, Spinnaker, Screwdriver). I consider GoCD may be most attractive alternative with visualized workflows and lots of advanced features. Perhaps Jenkis is still best-documented self-hosted CI/CD system.

GitLab has CI/CD functionalities for repositories hosted by GitLab, and Atlassian has CI/CD in Bitbucker Cloud. AWS has CodePipeline for delivering code to AWS server. CircleCI and Travis can be used with any version control system and deployment server.

I think that the most important question when to choose between cloud-based and self-host CI/CD is how to deploy the application. If we have cloud-based simple workflow GitHub to Heroku, GitHub Actions is the simplest alternative. If we are using AWS Cloud, AWS CodePipeline can be natural choice. But if we plan to deploy with own server we perhaps want to have more customization and full control of our sources and the workflow - and then we install Jekins on our server.

