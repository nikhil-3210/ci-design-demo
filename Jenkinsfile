pipeline {
  agent any
  options { timestamps(); ansiColor('xterm'); }
  triggers { pollSCM('H/5 * * * *') }

  stages {
    stage('Build') {
      steps { echo 'Task: Build | Tool: Maven (or npm/Gradle)' }
    }
    stage('Unit & Integration Tests') {
      steps { echo 'Task: Tests | Tools: JUnit (or Jest/Mocha)' }
    }
    stage('Code Analysis') {
      steps { echo 'Task: Code Analysis | Tools: ESLint / PMD' }
    }
    stage('Security Scan') {
      steps { echo 'Task: Security Scan | Tools: npm audit / OWASP DC' }
    }
    stage('Deploy to Staging') {
      steps { echo 'Task: Deploy to Staging | Tools: SSH/Ansible/Docker' }
    }
    stage('Integration Tests on Staging') {
      steps { echo 'Task: Staging Integration Tests | Tools: Newman/Cypress' }
    }
    stage('Deploy to Production') {
      steps { echo 'Task: Deploy to Production | Tools: SSH/Ansible/Docker' }
    }
  }
}