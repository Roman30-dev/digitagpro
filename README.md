<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Évaluation</title>
    <style>
        /* Votre CSS existant ici */
        .rating-container {
            text-align: center;
            padding: 20px;
            margin: 20px 0;
            background-color: #f9f9f9;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        .rating-title {
            font-size: 24px;
            margin-bottom: 10px;
        }
        .rating-text {
            font-size: 16px;
            margin-bottom: 20px;
        }
        .rating-boxes {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .rating-box {
            width: 220px;
            height: 80px;
            margin: 10px 0;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #4CAF50;
            border-radius: 10px;
            text-decoration: none;
            transition: transform 0.3s, box-shadow 0.3s;
            padding: 10px;
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2), inset 0 1px 0 rgba(255,255,255,0.1);
        }
        .rating-box:before {
            content: "";
            position: absolute;
            top: 50%;
            left: 50%;
            width: 300%;
            height: 300%;
            background: rgba(255, 255, 255, 0.1);
            transform: translate(-50%, -50%) rotate(45deg);
            transition: all 0.3s;
        }
        .rating-box:hover:before {
            width: 400%;
            height: 400%;
            background: rgba(255, 255, 255, 0.2);
        }
        .star {
            font-size: 24px;
            color: #FFD700;
        }
        .empty-star {
            font-size: 24px;
            color: #ddd;
        }
        .rating-box:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(0,0,0,0.3), inset 0 1px 0 rgba(255,255,255,0.2);
            background-color: #45a049;
        }
        .rating-text-box {
            font-size: 18px;
            color: white;
            margin-left: 5px;
        }
    </style>
</head>
<body>
    <div class="rating-container">
        <h1 class="rating-title">Mettez un avis</h1>
        <p class="rating-text">Nous apprécions vos retours. Veuillez évaluer notre service :</p>
        <div class="rating-boxes">
            <a href="#" id="gmb-link1" class="rating-box"> 
                <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span>
                <span class="rating-text-box">5/5</span> 
            </a> 
            <a href="#" id="gmb-link2" class="rating-box"> 
                <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="empty-star">★</span>
                <span class="rating-text-box">4/5</span> 
            </a> 
            <a href="#" id="gmb-link3" class="rating-box"> 
                <span class="star">★</span><span class="star">★</span><span class="star">★</span><span class="empty-star">★</span><span class="empty-star">★</span>
                <span class="rating-text-box">3/5</span> 
            </a> 
            <a href="#" id="gmb-link4" class="rating-box"> 
                <span class="star">★</span><span class="star">★</span><span class="empty-star">★</span><span class="empty-star">★</span><span class="empty-star">★</span>
                <span class="rating-text-box">2/5</span> 
            </a> 
            <a href="#" id="gmb-link5" class="rating-box"> 
                <span class="star">★</span><span class="empty-star">★</span><span class="empty-star">★</span><span class="empty-star">★</span><span class="empty-star">★</span>
                <span class="rating-text-box">1/5</span> 
            </a>
        </div>
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var nouveauLien = localStorage.getItem('nouveauLienGMB');
            var email = localStorage.getItem('emailClient');
            document.getElementById('gmb-link1').href = nouveauLien;
            document.getElementById('gmb-link2').href = nouveauLien;
            document.getElementById('gmb-link3').href = "https://digitagpro.fr/pages/test-2?email=" + encodeURIComponent(email);
            document.getElementById('gmb-link4').href = "https://digitagpro.fr/pages/test-2?email=" + encodeURIComponent(email);
            document.getElementById('gmb-link5').href = "https://digitagpro.fr/pages/test-2?email=" + encodeURIComponent(email);
        });
    </script>
</body>
</html>
