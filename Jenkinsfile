pipeline{
    agent any
    tools{
        maven 'maven-3.5.0'
    }
     stages{
         stage('check-out'){
             steps{
             git 'https://github.com/SundeepBinaylal/mavenproject.git'
             }
         }
       stage('build'){
           steps{
           
                   sh 'mvn clean install'
              
           }
       }
      stage('deploy'){
          steps{
              sh "sudo su - test -c 'ansible-playbook /home/test/deploy.yml'"
          }
      }
     }
     
}
