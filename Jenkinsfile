pipe line {
  agent any
      stages { 
        
        stage ('compling stage') {  
            steps {
                withMaven(maven: 'maven_3_3_9') { 
                    sh 'mvn clean compile'
                }
            }
        } 
        
        stage ('testing stage') {  
            steps { 
                withMaven(maven: 'maven_3_3_9') {  
                    sh 'mvn test'
                }
            }
        }
        
        stage ('Deploying stage') {
            steps {
                withMaven(maven: 'maven_3_3_9') {
                    sh 'mvn deploy'
                }
            }
        }
     }
  }
