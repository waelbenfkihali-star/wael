pipeline {
    agent any
    options { timestamps() }
    stages {
        stage('Clone repository') {
            steps {
                git url: 'https://github.com/waelbenfkihali-star/wael.git', branch: 'main'
            }
        }
        stage('Step 1: Check repository status') {
            steps {
                bat 'echo === Step 1: Checking repository ==='
                bat 'git status'
            }
        }
        stage('Step 2: Show project content') {
            steps {
                bat 'echo === Step 2: Showing project files ==='
                bat 'dir'
            }
        }
        stage('Step 3: Simulate local deployment') {
            steps {
                bat 'echo === Step 3: Simulating local deployment ==='
                bat 'echo index.html is ready to be displayed'
            }
        }
        stage('Step 4: Build finished') {
            steps {
                bat 'echo === Step 4: Build complete ==='
                bat 'echo SUCCESS'
            }
        }
    }
    post {
        success { echo 'Build OK ✅' }
        failure { echo 'Build KO ❌' }
    }
}
