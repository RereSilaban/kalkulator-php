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
                echo 'Menjalankan Server Kalkulator...'
                // Perintah ini menyalakan server PHP di port 8000
                bat 'start /B C:\\xampp\\php\\php.exe -S localhost:8000'
            }
        }
        // stage('Performance Test') {
        //     steps {
        //         echo 'Menjalankan JMeter Test...'
        //         // Di sini nanti tempat kamu panggil file .jmx
        //         echo 'Testing selesai!'
        //     }
        }
    }
}