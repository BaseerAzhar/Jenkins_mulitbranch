pipeline {
    agent any
    stages {
        stage('--build--') 
        {
            steps 
            {
                sh "python3 -m venv env"
                
                sh "python3 -m pip install --upgrade pip"

                sh "pip install -r requirements.txt"

            }
        }
        stage('--test--') 
        {
            steps 
            {
                sh "pytest -v -s -m check"
            }
        }
        stage('--report--') 
        {
            steps 
            {
                sh "pytest -v -s -m webtest"
            }
        }
        
    }
}
