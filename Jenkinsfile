pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
    agent any
    stages {
        stage('Build') {
           steps {
               // Étape de construction avec Gradle
               sh './gradlew assemble'
           }
       }
       stage('Test') {
           steps {
               // Étape de test avec Gradle
               sh './gradlew test'
           }
       }

       post {
           success {
               // Étape exécutée en cas de succès du pipeline
               echo 'Build successful!'
           }
           failure {
               // Étape exécutée en cas d'échec du pipeline
               echo 'Build failed!'
           }
       }
   }
}
