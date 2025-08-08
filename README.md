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
            backgroun
