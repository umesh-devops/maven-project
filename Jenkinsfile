pipeline
{
 agent any
 stages{

     stage('scm checkout')
     {steps {  git branch: 'master', url: 'https://github.com/prakashk0301/maven-project' }    }

     stage ('unit test framework')
     { steps {  withMaven(jdk: 'jdk-1.8', maven: 'my_maven') 
          { sh 'mvn test' }  }  }

     stage ('code Build')
     { steps {  withMaven(jdk: 'jdk-1.8', maven: 'my_maven') 
          { sh 'mvn clean package' }  }  }


     
 }
}
