pipeline {
    agent {
        docker {
            image 'node' 
            args '-p 3000:3000' 
        }
    }
       stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
           
        stage('Deliver') { 
            steps {
                sh 'npm run build'
                sh 'npm start &'
                echo 'Visit http://localhost:3000 to see your Node.js/React application in action.'
                echo '(This is why you specified the "args ''-p 3000:3000''" parameter when you'
                echo 'created your initial Pipeline as a Jenkinsfile.)'
            }
        }
    }
}
