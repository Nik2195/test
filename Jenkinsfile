pipeline
{
agent {
  label 'dev'
}

tools {
  maven 'maven_test'
}

stages{

    stage ('build')
    {
        steps{
            sh 'mvn clean package'
        }
        post {
        success {
            archiveArtifacts artifacts: '**/target/*.war'
                }
            }
    }

}
}
