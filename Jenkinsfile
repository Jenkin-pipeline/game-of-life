pipeline{
  agent{label 'JDK_8'}
     stages{
        stage('vcm')
        {
            steps {
                git url :'https://github.com/Jenkin-pipeline/game-of-life.git',
                branch : 'jenkin-declarative'
            }
        }
        stage('package'){  
            tools {
                jdk 'JDK_8'
            }    
            steps {
                sh 'mvn package'
            }
        }
        stage('post build') {
            steps {
                archiveArtifacts artifacts: '**/target/gameoflife.war',
                                 onlyIfSuccessful: true
                junit testResults: '**/surefire-reports/TEST-*.xml'
            }
        }

   }

}