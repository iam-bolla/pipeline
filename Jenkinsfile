stage('Run') {
    agent {
        docker {
            image 'eclipse-temurin:17-jre'
        }
    }
    steps {
        script {
            echo 'Running HelloWorld class'
        }
        sh '''
            cd multi-stage-multi-agent
            if [ ! -f target/classes/com/sravya/HelloWorld.class ]; then
                echo "Compiled class not found!"
                ls -R target
                exit 1
            fi
            java -cp target/classes com.sravya.HelloWorld
        '''
    }
}
