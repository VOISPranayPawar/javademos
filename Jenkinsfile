pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn -f javademos-master/ssgsems/pom.xml -B -DskipTests clean package'
        archiveArtifacts(artifacts: '**/target/*.war', fingerprint: true)
        sh '''mkdir /home/Pranay/buildoutput/${BUILD_NUMBER}
cp **/target/*.war /home/Pranay/buildoutput/${BUILD_NUMBER}'''
      }
    }

  }
}