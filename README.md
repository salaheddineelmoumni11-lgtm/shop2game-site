<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shop2Game</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #F0F0F0;
            margin: 0;
            padding: 0;
            direction: rtl;
        }

        /* Header */
        .header {
            background-color: #2A2A2A;
            color: #FF9900;
            text-align: center;
            padding: 15px 0;
        }
        .header h1 {
            font-size: 36px;
            margin: 0;
        }
        .header p {
            font-size: 18px;
            margin: 0;
        }

        /* Game Selection */
        .game-selection {
            display: flex;
            justify-content: center;
            margin-top: 40px;
        }
        .game-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            margin: 0 20px;
            padding: 20px;
            text-align: center;
            width: 200px;
            transition: transform 0.3s ease;
        }
        .game-card:hover {
            transform: scale(1.05);
        }
        .game-card img {
            width: 100%;
            border-radius: 10px;
        }
        .game-card h3 {
            margin-top: 15px;
            font-size: 20px;
            color: #333;
        }
        .game-card p {
            font-size: 16px;
            color: #666;
        }
        .game-card button {
            background-color: #FF9900;
            border: none;
            color: white;
            padding: 12px 25px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 15px;
            width: 100%;
        }
        .game-card button:hover {
            background-color: #E68900;
        }

        /* Modal for payment confirmation */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.6);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            text-align: center;
            width: 400px;
        }
        .modal-content h2 {
            font-size: 24px;
            color: #28A745;
        }
        .modal-content p {
            font-size: 18px;
            color: #333;
        }
        .modal-button {
            background-color: #28A745;
            border: none;
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 18px;
            margin-top: 20px;
        }
        .modal-button:hover {
            background-color: #218838;
        }

        /* Footer */
        .footer {
            background-color: #2A2A2A;
            color: #FF9900;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .footer p {
            margin: 0;
            font-size: 14px;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>Shop2Game</h1>
        <p>اشحن حسابك بالعملات المفضلة بسرعة وسهولة</p>
    </div>

    <div class="game-selection">
        <div class="game-card">
            <img src="https://via.placeholder.com/150" alt="PUBG Mobile">
            <h3>PUBG Mobile</h3>
            <p>اشحن حسابك الآن بأسرع وقت!</p>
            <button onclick="startTransaction('PUBG Mobile')">ابدأ الآن</button>
        </div>
        <div class="game-card">
            <img src="https://via.placeholder.com/150" alt="Free Fire">
            <h3>Free Fire</h3>
            <p>اشحن حسابك بأفضل الأسعار!</p>
            <button onclick="startTransaction('Free Fire')">ابدأ الآن</button>
        </div>
        <div class="game-card">
            <img src="https://via.placeholder.com/150" alt="Call of Duty">
            <h3>Call of Duty</h3>
            <p>اشتري الجواهر والموارد بأسرع وأسهل طريقة!</p>
            <button onclick="startTransaction('Call of Duty')">ابدأ الآن</button>
        </div>
    </div>

    <!-- Modal for Payment -->
    <div class="modal" id="paymentModal">
        <div class="modal-content">
            <h2>تم الشحن بنجاح!</h2>
            <p>تم شحن [عدد الجواهر] إلى حسابك: <span id="playerID"></span></p>
            <p>شكرًا لاستخدامك خدماتنا. تم الشحن بنجاح!</p>
            <button class="modal-button" onclick="closeModal()">إغلاق</button>
        </div>
    </div>

    <div class="footer">
        <p>© 2025 Shop2Game - جميع الحقوق محفوظة</p>
    </div>

    <script>
        function startTransaction(game) {
            const playerID = prompt("أدخل معرف اللاعب (Player ID)"); // طلب ID اللاعب
            const gems = prompt("أدخل عدد الجواهر التي ترغب في شحنها (مثلاً: 1000، 2000)");
            
            if (playerID && gems) {
                // عرض صفحة الدفع المزيف بعد الضغط
                document.getElementById("playerID").textContent = playerID; // عرض المعرف في الرسالة
                document.getElementById("paymentModal").style.display = "flex"; // إظهار النوافذ المنبثقة
            } else {
                alert("يرجى إدخال جميع البيانات");
            }
        }

        function closeModal() {
            document.getElementById("paymentModal").style.display = "none"; // إخفاء النافذة
        }
    </script>

</body>
</html>
