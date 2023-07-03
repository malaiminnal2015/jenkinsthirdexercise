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
                sh "cd /var/lib/jenkins/workspace/JenkinsExercisePipeline/jenkinsthirdexercise/target"
                sh "java -jar jenkinsthirdexercise.jar com.jenkins.exercise.FirstJenkinExercise"
                
              
            }
        }
    }
}
