#!/usr/bin/env groovy
import hudson.model.*
import hudson.EnvVars
import java.net.URL

node{
    stage('Git Checkout'){
        git 'https://github.com/edureka-git/DevOpsClassCodes.git'
    }
    stage('AB Compile'){
        withMaven(maven:'MyMaven'){
            sh 'mvn compile'
        }
    }
    stage('AB Review'){
        withMaven(maven:'MyMaven'){
            sh 'mvn pmd:pmd'
        }
    }
    stage('AB Package'){
        withMaven(maven:'MyMaven'){
            sh 'mvn package'
        }
    }
    
}
