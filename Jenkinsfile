pipeline{
  agent{label 'JDK_17'}
   stages{
     stage('Build')
     {
        steps {
            git url :'https://github.com/Jenkin-pipeline/game-of-life.git',
              branch : 'jenkin-declarative'
        }
     }
     stage('package'){
        steps {
            sh 'mvn package'
        }
     }

   }

}