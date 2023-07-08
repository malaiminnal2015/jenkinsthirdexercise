pipeline {
    
    agent any 
    stages {
        stage('Cleaning') { 
            steps {
              
               echo "****** Its  not necessary to clone, because the Jenkinsfile way will automatically clone ********"
               sh "mvn clean"

            }
        }
        stage('Test') { 
            steps {
                echo "Its ****** TESTING ****** now"
                sh "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Its ****** DEPLOYING ****** now"
                sh "mvn package"
                sh "java -jar /var/lib/jenkins/workspace/Varman-Banks-Pipeline-Jenkinsfile/jenkinsthirdexercise/target/jenkinsthirdexercise.jar com.jenkins.exercise.FirstJenkinExercise"
            }
        }
    }
}
