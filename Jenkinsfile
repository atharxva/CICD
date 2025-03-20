pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                        sudo apt-get install python3.11-venv
                        cd myapp
                        python3 -m venv venv  # Create virtual environment
                        source venv/bin/activate  # Activate it
                        pip install --upgrade pip  # Upgrade pip
                        pip install -r requirements.txt  # Install dependencies
                    '''
                }
            }
        }
        stage('Test') {
            steps {
                echo "Running tests..."
            }
        }
        stage('Deliver') {
            steps {
                echo "Deploying..."
            }
        }
    }
}
