pipeline { 
    agent any 

    tools { 
        maven 'Maven' // Ensure the name matches what is configured in Jenkins Global Tool Configuration
    } 

    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/HarishDevakki2004/Mavenhello.git'  
            } 
        }

        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        }

        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        }

        stage('Run Application') {
            steps {
                bat 'java -jar target/HelloWorld-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}
