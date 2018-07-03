node {
   stage('VCS') {
    git 'https://github.com/nitinnb/game-of-life.git'
   }
   
   stage('build & package'){
       sh 'mvn package'
   }
   
   stage('results'){
       archiveArtifacts 'gameoflife-web/target/gameoflife.war'
       junit 'gameoflife-web/target/surefire-reports/*.xml'
   }
 
}