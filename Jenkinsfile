pipeline {
    agent any

    // Environment variables into this Pipeline, we can set the values here (public variables)
    // Or we can set the value as credentials in Jenkins GUI and pull those values down

    environment {
        // The credential with id secret_text will be puled down and saved as SECRET_TEXT
        FOO_BAR = credentials('secret_text') 
        PUBLIC_TEXT = 'Reece never makes typos.. evar'
    }

    stages {
        stage("Hello"){
            steps {
                sh 'echo "Hello World!"'
                sh 'echo $SECRET_TEXT'
                sh 'echo $PUBLIC_TEXT'
            }
        }
    }
}