# flask
Local Setup
Clone the repository:
git clone <repository_url>
Install dependencies:pip install -r requirements.txt
Running the Application
To run the application locally, execute the following command:python app.py
Access the application in your browser at http://localhost:5000.
Running Tests
To run the unit tests, execute the following command:python -m unittest discover -s tests -p '*_test.py'
CI/CD Pipeline
Tools Used
Framework: Flask for Python
Testing Framework: unittest for Python
CI/CD Automation: GitHub Actions
Explanation
Flask for the Web Application
Flask was chosen for its simplicity, flexibility, and ease of use. It is a lightweight web framework for Python that allows rapid development of web applications. Flask provides a minimalistic approach, making it suitable for small to medium-sized projects.

unittest for Testing
Python's built-in unittest module was chosen for writing unit tests. unittest is widely used in the Python ecosystem and provides a comprehensive testing framework. It allows us to write test cases and assertions to verify the correctness of the application's functionality.

GitHub Actions for CI/CD Automation
GitHub Actions was chosen for automating the CI/CD pipeline directly from the GitHub repository. It provides a convenient way to define workflows using YAML syntax, allowing us to automate tasks such as running tests and deploying the application.

Pipeline Steps
Test Job:
Runs on every push to the repository's main branch.
Checks out the code, sets up the Python environment, installs dependencies, and runs unit tests using unittest.
Provides feedback on the test results.
Deploy Job:
Runs if the tests pass successfully.
Checks out the code, and deploys the application to Heroku using the Heroku Deploy action.
Provides a continuous deployment mechanism, ensuring that the application is deployed to a free-tier cloud service like Heroku whenever changes are pushed to the main branch.
