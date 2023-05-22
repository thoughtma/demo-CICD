pipeline {
    agent any
    environment {
        // Specify the Python executable path
        pythonPath = '/path/to/python'
    }
    stages {
        stage('Installing packages') {
            steps {
                // Install pip
                sh '${pythonPath} -m ensurepip --upgrade'
                sh '${pythonPath} -m pip install --upgrade pip'
                // Install packages from requirements.txt
                sh '${pythonPath} -m pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh '${pythonPath} unit_test.py'
            }
        }
    }
}
