pipeline {
    agent {
        label'master'
    }
    stages {
         stage('checkout scm') {
             steps {
                 git branch: 'master',
                     credentialsId: 'github_jenkins',
                         url: 'https://github.com/oscarose/testparams.git'
             }
         }
         stage('check python and ansible version') {
             steps {
                 sh """
                 echo ${ds.dbname}	
                 ls -altr
                 ansible --version
                 docker info
                 """
             }
         }
    }
}
