<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>L'ÉTAT UNIQUE</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
            padding: 60px 40px;
            max-width: 600px;
            text-align: center;
            animation: fadeIn 0.8s ease-in;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .map-container {
            margin-bottom: 40px;
            animation: slideUp 1s ease-out;
        }

        @keyframes slideUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .map-svg {
            width: 100%;
            max-width: 400px;
            height: auto;
            stroke: #333;
            stroke-width: 2;
            fill: white;
            filter: drop-shadow(0 4px 8px rgba(0, 0, 0, 0.1));
        }

        .map-svg:hover {
            filter: drop-shadow(0 8px 16px rgba(0, 0, 0, 0.2));
            transition: filter 0.3s ease;
        }

        h1 {
            font-size: 2.5em;
            color: #333;
            letter-spacing: 3px;
            font-weight: 300;
            margin-top: 30px;
            animation: fadeInText 1.2s ease-out;
        }

        @keyframes fadeInText {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        p {
            color: #666;
            font-size: 1.1em;
            line-height: 1.8;
            margin-top: 20px;
        }

        .accent {
            color: #4a90e2;
            font-weight: 500;
        }

        @media (max-width: 768px) {
            .container {
                padding: 40px 25px;
            }

            h1 {
                font-size: 1.8em;
                letter-spacing: 2px;
            }

            p {
                font-size: 1em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="map-container">
            <svg class="map-svg" viewBox="0 0 400 450" xmlns="http://www.w3.org/2000/svg">
                <!-- 地图轮廓 -->
                <path d="M 200 80 
                         Q 280 100 320 180 
                         Q 340 220 330 280 
                         Q 320 340 260 380 
                         Q 200 400 140 380 
                         Q 80 340 70 280 
                         Q 60 220 80 180 
                         Q 120 100 200 80 Z" 
                      fill="white" stroke="#333" stroke-width="2"/>
            </svg>
        </div>

        <h1>L'ÉTAT UNIQUE</h1>
        
        <p>
            独一无二的<span class="accent">国度</span>
        </p>
        
        <p style="margin-top: 40px; font-size: 0.95em; color: #999;">
            唯一的存在，永恒的象征
        </p>
    </div>

    <script>
        // 页面加载完成
        document.addEventListener('DOMContentLoaded', function() {
            console.log('欢迎访问，L\'ÉTAT UNIQUE');
        });

        // 地图悬停效果
        const mapSvg = document.querySelector('.map-svg');
        mapSvg.addEventListener('mouseover', function() {
            this.style.transform = 'scale(1.05)';
            this.style.transition = 'transform 0.3s ease';
        });

        mapSvg.addEventListener('mouseout', function() {
            this.style.transform = 'scale(1)';
        });
    </script>
</body>
</html>
