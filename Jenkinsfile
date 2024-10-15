pipeline {
    agent any
    stages {
        stage('Checkout') { // добавим новый Stage
            steps {
                git branch: 'main', url: "https://github.com/Esserg/docker-install.git" // используем встроенный в Jenkins плагин Git для скачивания проекта из бранча main
            }
        }
        stage('Deploy') {
            steps {
                sh 'ansible-playbook docker-install.yml' // поскольку скрипты работают в одной папке, на втором шаге мы можем просто запустить плейбук
            }
        }
    }
}
