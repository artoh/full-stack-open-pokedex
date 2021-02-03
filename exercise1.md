CI/CD on Python

pylint was the de-facto linter for Python, but flake8 may be more poplar today. Python has official coding style PEP 8. Luckily there is good support for coding styles in good IDE editors and code formatters like black to help developer keeping this step green.

unittest and pytest are the most common testing frameworks for Python and they work well in CI. Django has own testing framework based on unittest. Pytest is suitable for ui testing too.

There is no need to build step (Python is script language), but we need to install dependencies with pip. We can use twine to automatically push to package registry like pypi or we can use heroku-deploy to deploy our application to Heroku.

-- alternatives to Jenkins and GitHub Actions (CircleCI...)

--- self-hosted or cloud-based

