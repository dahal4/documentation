pipeline {
    agent any 
    stages {
        stage('Setup Virtual Environment, Install Dependencies') {
            steps {
                // Create a virtual environment named 'myenv' in the 'venvs' directory
                sh 'python3 -m venv venv'

                // Activate the virtual environment
                sh '''
                    bash -c ". venv/bin/activate"
                '''
                // Now, you can install any required packages using pip
                // For example, to install numpy:
                // sh 'pip install numpy'

                // After setting up the environment and installing dependencies,
                // proceed with your compilation and execution steps
            }
        }
        stage('Compile and Run Hello World') {
            steps {
                // Assuming you've moved the hello_world.py into the workspace
                sh 'python3 test.py'
            }
        }
    }
}