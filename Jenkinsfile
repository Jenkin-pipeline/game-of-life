pipeline{
  agent{label 'JDK_8'}
   stages{
     stage('Build')
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

   }

}