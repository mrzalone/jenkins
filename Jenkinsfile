pipeline {
    agent any
   
    stages {
        stage('Addition') {
            steps {
                script {
                    def number1 = 5
                    def number2 = 3
                    def sum = number1 + number2
                    echo "The sum is: ${sum}"
                    env.SUM = sum.toString()
                }
            }
        }
        
        stage('Division') {
            steps {
                script {
                    def sum = env.SUM.toInteger()
                    def result = sum / 2
                    echo "The division result is: ${result}"
                    env.R = result.toString()
                }
            }
        }
        
        stage('Final Result') {
            steps {
                script {
                    echo "The final result is: ${env.R}"
                }
            }
        }
    }
}
