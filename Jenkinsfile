pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Mengambil kode dari Git...'
            }
        }
     stage('Deploy') {
            steps {
                echo 'Menjalankan Server PHP...'
                // Langsung gas nyalain server
                bat 'start /B C:\\xampp\\php\\php.exe -S localhost:8000'
                sleep 10
            }
        }
        // stage('Performance Test') {
        //     steps {
        //         echo 'Menjalankan JMeter Test...'
        //         // Di sini nanti tempat kamu panggil file .jmx
        //         echo 'Testing selesai!'
        //     }
        //}
    }
}