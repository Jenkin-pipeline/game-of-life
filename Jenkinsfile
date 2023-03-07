pipeline{
  agent{label 'JDK_8'}
   tools {
                jdk 'JDK_8'
            }
   stages{
     stage('vcm')
     {
        steps {
            git url :'https://github.com/Jenkin-pipeline/game-of-life.git',
              branch : 'jenkin-declarative'
        }
     }
     stage('build'){
               steps {
            sh 'mvn build'
        }
     }
      stage('package'){      
        steps {
            sh 'mvn package'
        }
     }

   }

}