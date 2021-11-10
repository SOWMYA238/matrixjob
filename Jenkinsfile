pipeline {
    agent any
    stages {
        stage('one') {
            matrix {
           
                axes {
                    axis {
                        name 'PLATFORM'
                        values 'windows'
                    }
                    axis {
                        name 'BROWSER'
                        values 'firefox', 'edge'
                    }
                }
                stages {
                    stage('Build') {
                        steps {
                            echo "Do Build for ${PLATFORM} - ${BROWSER}"
                        }
                    }
                    stage('Test') {
                        steps {
                            echo "Do Test for ${PLATFORM} - ${BROWSER}"
                        }
                    }
                }
            }
        }
    }
}
