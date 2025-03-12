node {
    checkout scm

    // Deploy ke environment development
    stage("Build") {
        docker.image('shippingdocker/php-composer:7.4').inside('-u root') {
            sh 'rm -f composer.lock'
            sh 'composer install'
        }
    }

    // Testing
    stage("Test") {
        docker.image('debian').inside('-u root') {
            sh 'echo "Ini adalah test"'
        }
    }
}

