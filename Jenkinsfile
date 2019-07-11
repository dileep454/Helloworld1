#!groovy
import hudson.model.*
import hudson.EnvVars
import groovy.json.JsonSlurperClassic
import groovy.json.JsonBuilder
import groovy.json.JsonOutput
import java.net.URL


node {
   def GIT_URL = 'https://github.com/dileep454/game-of-life.git'
   def GIT_BRANCH = 'master'
   def SONAR_BRANCH = 'master'
   def MAVEN_GOALS = 'clean install  package'
   def MAVEN_HOME = tool 'M2_HOME'
   def SONAR_URL = 'http://3.16.57.187:9000/'
   def SONAR_LOGIN='admin'
   def SONAR_PASSWORD='admin'
   def artifactory_user='admin'
   def artifactory_password='admin123'
   def dversion='$TAG'
   
   
   /*******************************************
   *  Build stage to trigger the maven build
   ********************************************/
   stage('Compile and execute Unit test')
   {
    
         withEnv(["MVN_HOME=$MAVEN_HOME"]) {

            sh '"$MVN_HOME/bin/mvn" -Dmaven.test.failure.ignore clean package'               
   }
}

}
