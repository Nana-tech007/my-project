pipeline {
  2     agent any
  3     parameters {
  4          choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '    ')
  5          booleanParam(name: 'executeTests', defaultValue: true, description: '')
  6     }
  7     stages {
  8         stage('build') {
  9             steps {
 10                  echo 'building the application...'
 11             }   
 12         }
 13         stage('test') {
 14             when {
 15                 expression {
 16                     params.excuteTests
 17                 }
 18            }
 19             steps {
 20                     echo 'testing the application...'
 21             }
 22         }
 23         stage('deploy') {
 24             steps {
 25                     echo 'deploying the application...'
 26                     echo "deploying the version ${VERSION}"
 27             }
 28         }
 29     }
 30 }
