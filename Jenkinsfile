pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir /s /q ASD_coaching_portal"
                bat "git clone https://github.com/prathamdh18/ASD_coaching_portal.git"
                bat "mvn clean -f ASD_coaching_portal"
            }
         }
         stage('install') {
             steps {
                  bat "mvn install -f ASD_coaching_portal"
             }
         }
         stage('test') {
             steps {
                 bat "mvn test -f ASD_coaching_portal"
             }
         }
         stage('package') {
             steps {
                bat "mvn package -f ASD_coaching_portal"
             }
         }
   }
}
   
   
            
