<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday</title>
    <style>
        body {
            background-color: #ffe6f0;
            font-family: 'Comic Sans MS', sans-serif;
            text-align: center;
            margin: 0;
            overflow: hidden;
            transition: background-color 1s;
        }

        .envelope-container {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            animation: fadeIn 1.5s ease-in-out;
        }

        .envelope {
            position: relative;
            width: 150px;
            height: 100px;
            background-color: pink;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.4s ease;
        }

        .envelope:before,
        .envelope:after {
            content: '';
            position: absolute;
            width: 150px;
            height: 100px;
            background: white;
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .envelope:before {
            top: 0;
            left: 0;
            transform: rotate(45deg);
            transform-origin: 0 0;
        }

        .envelope:after {
            top: 0;
            left: 0;
            transform: rotate(-45deg);
            transform-origin: 100% 0;
        }

        .envelope:hover {
            transform: scale(1.05);
        }

        .envelope:active {
            transform: scale(0.9);
        }

        .heart-animation {
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 50px;
            color: red;
            display: none;
            animation: heartBeat 1s infinite;
        }

        @keyframes heartBeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.2);
            }
        }

        .card {
            display: none;
            background-color: #fff;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.2);
            margin: 20px auto;
            max-width: 400px;
            text-align: center;
            position: relative;
            overflow-y: auto;
            max-height: 80vh;
            animation: fadeInUp 1s ease-in-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(50px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        h1 {
            color: #ff399c;
            animation: fadeIn 1.5s ease-in-out;
        }

        p {
            color: #555;
            margin: 15px 0;
        }

        .birthday {
            max-width: 100%;
            border-radius: 10px;
            margin-bottom: 20px;
            opacity: 0;
            animation: fadeIn 2s ease-in-out forwards;
        }

        .muted {
            font-style: italic;
            color: #888;
        }

        audio {
            margin-top: 20px;
            opacity: 0;
            animation: fadeIn 3s ease-in-out forwards;
        }

        .options {
            margin-top: 20px;
        }

        .option-button {
            background-color: #ff66b3;
            color: white;
            border: none;
            border-radius: 5px;
            padding: 10px 20px;
            margin: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .option-button:hover {
            background-color: #ff3385;
        }

        .option-message {
            display: none;
            background-color: #fff;
            border-radius: 10px;
            padding: 10px;
            margin-top: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: left;
            opacity: 0;
            animation: fadeInMessage 0.5s ease-in-out forwards;
        }

        @keyframes fadeInMessage {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>

<body>

    <!-- Amplop Valentine -->
    <div class="envelope-container">
        <div class="envelope" onclick="openCard()">
            <div class="heart-animation">❤</div>
        </div>
    </div>

    <!-- Kartu Ucapan Ulang Tahun -->
    <div class="card">
        <img src="https://i.pinimg.com/736x/91/6f/ae/916fae595dbd3ae065891eb8e7f0bd94.jpg" alt="birthday" class="birthday">
        <div class="text">
            <h1>Hiii Bijarr!</h1>
            <p>Happy birthday! Hii, how's your day? Happy sweet seventeen yya Abijayyy a.k.a Bizzare. Aku bakalan doain semua yang terbaik buat kamuw, semoga hari hari mu di lancarkan, di jauhkan dari segala masalah. Semoga 17 kamu lebih baik lagi dari 16 kemarin.</p>
            <p>Dari sekian banyaknya orang baik yang aku temuin, kamu adalah salah satu yang paling terbaik, thank you for being the best person in my life, gaada yang sesabar kamu flish, semoga kamu dipertemukan dengan orang orang baik selalu yya.</p>
            <p>Thank you for coming in my life, i'm happy when i'm with you, when people come and go, but.. can you be with me forever?</p>
            <p class="muted">- Meyey -</p>
        </div>
        <audio controls autoplay>
            <source src="The 1975 - About You.mp3" type="audio/mp3">
        </audio>
        <div class="options">
            <button class="option-button" onclick="showMessage(1)">🐸</button>
            <button class="option-button" onclick="showMessage(2)">🌹</button>
            <button class="option-button" onclick="showMessage(3)">🌼</button>
            <button class="option-button" onclick="showMessage(4)">🪻</button>
            <button class="option-button" onclick="showMessage(5)">🌺</button>
        </div>
        <div id="message1" class="option-message">"The 1975 - About You" lagu yang ngingatin aku ke kamu, gtw juga sih kenapa tapi pas aku dengar lagunya kayak nyimpen kamu aja hehe</div>
        <div id="message2" class="option-message">Happy sweet seventeen bijarr, wish you all the best be happy in level up todayy!! semoga di ulang tahun yang sekarang kamu bisa menggapain apa yang kamu mau yaaa. i wish the best for you, be better and just be yourself dan jangan lupa lebih bersyukur lagi kedepannya menjadi jati diri yang lebih baik lagii, happy birthdayy yaa sekali lagi! jaga kesehatan, makan yang banyak, minum air yang cukupp, jangan nahan pipis berak yaww</div>
        <div id="message3" class="option-message">terima kasih banyak yya udah selalu dengar ceritakuu, walau aku sgt amat berisik dan sllu gangguin kamuu, aku bener-bener apresiasi setiap waktu yang km luangin buat dengerin aku, meskipun aku tahu kadang bisa ganggu banget, jangan jauhin aku yaa abijarr, aku harap kita bisa terus ada satu sama lain sampai nanti saatnya kita harus sibuk dengan kehidupan kita masing masing nantinya! </div>
        <div id="message4" class="option-message">semoga kamu bahagia teruss, gaboleh patah semangatt yya abijar, im here n always supporting u everydayy wahai manusia 173cm</div>
        <div id="message5" class="option-message">maaf yya aku cuman bisa ngasih kamu ini, jangan cari teman baru cepat cepat yya abijar nanti aku sedih, kata kamu kalo aku sedih nanti jadi tambah kecil kan</div>
    </div>

    <script>
        let colorIndex = 0;
        const colors = ['#aec6cf', '#d8bfd8', '#f6c1c1', '#ffffff', '#ffb7db'];

        function openCard() {
            // Transisi amplop
            const envelopeContainer = document.querySelector('.envelope-container');
            envelopeContainer.style.transition = 'opacity 1s ease-out';
            envelopeContainer.style.opacity = '0';

            // Setelah animasi amplop selesai, sembunyikan amplop dan tampilkan kartu ucapan
            setTimeout(() => {
                envelopeContainer.style.display = 'none';
                document.querySelector('.card').style.display = 'block';
            }, 1000);

            // Tampilkan animasi hati merah
            document.querySelector('.heart-animation').style.display = 'block';
        }

        function showMessage(number) {
            // Sembunyikan semua pesan
            const messages = document.querySelectorAll('.option-message');
            messages.forEach(msg => msg.style.display = 'none');

            // Tampilkan pesan yang dipilih
            const selectedMessage = document.getElementById('message' + number);
            selectedMessage.style.display = 'block';

            // Tambahkan animasi saat pesan ditampilkan
            selectedMessage.classList.add('fadeInMessage');

            // Ubah tema warna
            document.body.style.backgroundColor = colors[colorIndex];
            colorIndex = (colorIndex + 1) % colors.length;
        }
    </script>
</body>

</html>
