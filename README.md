<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kahve Teklifi</title>
</head>
<body style="background-color: #f7f7f7; font-family: 'Arial', sans-serif; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; color: #34495e;">

    <div style="background-color: #fff; padding: 40px 60px; border-radius: 20px; text-align: center; box-shadow: 0 20px 30px rgba(0, 0, 0, 0.1); width: 90%; max-width: 450px; transform: scale(0.95); animation: fadeIn 1s ease-out forwards;">
        <h1 style="color: #2c3e50; font-size: 36px; margin-bottom: 20px; animation: slideIn 1s ease-out;">Haydi Kahve İçmeye!</h1>
        <div style="font-size: 80px; color: #e67e22; animation: rotate 4s infinite linear;">☕</div>
        <p style="font-size: 20px; margin-top: 20px; color: #7f8c8d;">Birlikte kahve içmeye ne dersin? 💕</p>
        
        <div style="margin-top: 40px;">
            <button onclick="cevapla('evet')" style="background-color: #e67e22; border: none; padding: 15px 30px; color: white; font-size: 20px; border-radius: 10px; cursor: pointer; margin: 10px 20px; transition: background-color 0.3s ease;">Evet!</button>
            <button onclick="cevapla('hayir')" style="background-color: #e74c3c; border: none; padding: 15px 30px; color: white; font-size: 20px; border-radius: 10px; cursor: pointer; margin: 10px 20px; transition: background-color 0.3s ease;">Hayır</button>
        </div>
        
        <div id="result" style="font-size: 22px; margin-top: 30px; color: #16a085; opacity: 0; transition: opacity 1s ease-out;"></div>
    </div>

    <script>
        function cevapla(cevap) {
            var result = document.getElementById('result');
            var container = document.querySelector('div');
            
            if (cevap === 'evet') {
                result.innerHTML = 'Harika! Kahve içmeye gidelim! ☕';
                result.style.color = '#2ecc71';  // Yeşil renk
            } else if (cevap === 'hayir') {
                result.innerHTML = 'Belki başka zaman... 😢';
                result.style.color = '#e74c3c';  // Kırmızı renk
            }

            result.style.opacity = 1;

            // Butonları tıkladığında bir büyüme efekti
            container.style.transform = 'scale(1.05)';
            setTimeout(() => {
                container.style.transform = 'scale(1)';
            }, 300);
        }
    </script>

    <style>
        @keyframes fadeIn {
            0% { opacity: 0; transform: scale(0.9); }
            100% { opacity: 1; transform: scale(1); }
        }
        @keyframes slideIn {
            0% { opacity: 0; transform: translateY(-50px); }
            100% { opacity: 1; transform: translateY(0); }
        }
        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</body>
</html>
