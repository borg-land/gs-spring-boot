node('ops') {
  stage('init') {
      checkout scm
   }
   stage('build') {
      sh '''
         mvn clean package
         cd target
         cp ../src/main/resources/web.config web.config
         cp gs-spring-boot-0.1.0.jar app.jar 
         zip todo.zip app.jar web.config
      '''
   }
}
