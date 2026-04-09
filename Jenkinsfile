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
                echo 'Membersihkan proses lama dan menjalankan server...'
                bat "taskkill /F /IM php.exe /T || echo Tidak ada proses PHP sebelumnya."
                
                // Menjalankan server baru
                bat 'start /B C:\\xampp\\php\\php.exe -S localhost:8000'
                
                echo 'Menunggu server stabil (5 detik)...'
                sleep 5
            }
        }
        stage('Verify Deploy') {
            steps {
                echo 'Memastikan server merespon dengan benar...'
                // Perintah ini akan mencoba mengambil isi halaman localhost:8000
                bat 'curl -I http://localhost:8000'
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