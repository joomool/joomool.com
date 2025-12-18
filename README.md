<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>아트토이 작가 포트폴리오</title>
    <link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.css" />
    <style>
        :root {
            --point-color: #39FF14; /* 형광 그린 포인트 컬러 */
            --bg-color: #ffffff;
            --text-main: #111111;
            --text-sub: #666666;
            --card-bg: #f9f9f9;
        }

        body {
            margin: 0;
            padding: 0;
            font-family: 'Pretendard', -apple-system, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* 헤더 */
        header {
            padding: 20px 5%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            background: rgba(255, 255, 255, 0.9);
            backdrop-filter: blur(10px);
            z-index: 100;
            border-bottom: 1px solid #eee;
        }

        .logo { 
            font-size: 1.4rem; 
            font-weight: 800; 
            letter-spacing: -0.5px;
            color: var(--text-main);
        }

        nav a { 
            color: var(--text-main); 
            text-decoration: none; 
            margin-left: 25px; 
            font-size: 0.95rem; 
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover { color: var(--point-color); }

        /* 히어로 섹션 */
        .hero {
            height: 60vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 5%;
        }

        .hero h1 { 
            font-size: 3.5rem; 
            margin-bottom: 20px; 
            font-weight: 800;
            word-break: keep-all;
        }

        .hero h1 span {
            background-color: var(--point-color);
            padding: 0 10px;
        }

        .hero p { font-size: 1.25rem; color: var(--text-sub); font-weight: 400; }

        /* 섹션 공통 */
        .container { padding: 100px 5%; max-width: 1200px; margin: 0 auto; }
        .section-title { 
            font-size: 1.8rem; 
            margin-bottom: 50px; 
            display: flex;
            align-items: center;
            gap: 15px;
        }
        .section-title::before {
            content: "";
            width: 40px;
            height: 4px;
            background-color: var(--point-color);
            display: inline-block;
        }

        /* 작품 그리드 */
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 40px;
        }

        .item {
            background: var(--card-bg);
            border-radius: 20px;
            overflow: hidden;
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            border: 1px solid #eee;
        }

        .item:hover { 
            transform: translateY(-15px); 
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .item img { 
            width: 100%; 
            height: 450px; 
            object-fit: cover; 
            background-color: #eee;
        }

        .item-info { padding: 30px; }
        .item-info h3 { margin: 0; font-size: 1.3rem; font-weight: 700; }
        .item-info p { color: var(--text-sub); margin: 10px 0 20px 0; font-size: 0.95rem; }

        /* 버튼 스타일 */
        .btn-buy {
            display: inline-block;
            padding: 12px 25px;
            background-color: var(--text-main);
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            border-radius: 50px;
            transition: all 0.3s;
            font-size: 0.9rem;
        }

        .btn-buy:hover { 
            background-color: var(--point-color); 
            color: #000;
        }

        /* 하단 정보 */
        footer { 
            background: #f1f1f1;
            text-align: center; 
            padding: 60px 5%; 
            color: #888; 
            font-size: 0.9rem; 
        }

        .insta-link {
            color: var(--text-main);
            text-decoration: none;
            font-weight: bold;
            display: block;
            margin-bottom: 10px;
            font-size: 1.1rem;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">ARTIST NAME</div>
        <nav>
            <a href="#portfolio">포트폴리오</a>
            <a href="#shop">판매 작품</a>
            <a href="#about">소개</a>
        </nav>
    </header>

    <section class="hero">
        <h1>Welcome to <span>My Universe</span></h1>
        <p>작고 단단한 세계를 만드는 아트토이 작가 OOO입니다.</p>
    </section>

    <div class="container" id="portfolio">
        <h2 class="section-title">최신 작품 및 판매</h2>
        <div class="grid">
            <div class="item">
                <img src="작품이미지1.jpg" alt="Work 01"> <div class="item-info">
                    <h3>The Dreamer</h3>
                    <p>레진, 아크릴 채색 | 2024</p>
                    <a href="#" class="btn-buy">작품 상세 보기</a>
                </div>
            </div>
            
            <div class="item">
                <img src="작품이미지2.jpg" alt="Work 02"> <div class="item-info">
                    <h3>Midnight Cat</h3>
                    <p>바이닐, 혼합 매체 | 2024</p>
                    <a href="#" class="btn-buy">작품 상세 보기</a>
                </div>
            </div>

            <div class="item" id="shop">
                <img src="angma_005.png" alt="Shop 01"> <div class="item-info">
                    <h3>한정판 No.1</h3>
                    <p>₩ 150,000 (구매 가능)</p>
                    <a href="작가님 인스타 혹은 오픈채팅 주소" class="btn-buy" style="background-color: var(--point-color); color: #000;">구매 문의하기</a>
                </div>
            </div>
        </div>
    </div>

    <footer>
        <a href="https://instagram.com/joomool_joo" class="insta-link">@joomool_joo</a>
        &copy; 2024 Artist Name. All rights reserved. <br>
        모든 작품의 저작권은 작가에게 있습니다.
    </footer>

</body>
</html>
