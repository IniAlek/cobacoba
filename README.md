<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Camera Stream</title>
</head>
<body>
    <h1>Camera Stream from Phone</h1>
    <video id="video" width="640" height="480" autoplay></video>

    <script>
        // Menyusun kode untuk mengakses kamera
        async function startCamera() {
            try {
                // Mengakses kamera perangkat
                const stream = await navigator.mediaDevices.getUserMedia({ video: true });

                // Mendapatkan elemen video dan menetapkan stream ke elemen tersebut
                const videoElement = document.getElementById('video');
                videoElement.srcObject = stream;
            } catch (err) {
                // Menangani error jika kamera tidak bisa diakses
                console.error('Error accessing the camera: ', err);
            }
        }

        // Menjalankan fungsi startCamera saat halaman dimuat
        startCamera();
    </script>
</body>
</html>
# cobacoba
