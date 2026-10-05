

<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>To Cher Kathleen 🎉</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display&family=Fredoka+One&family=Montserrat:wght@500;600&display=swap" rel="stylesheet" />

    <style>
        /* Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }
        body,
        html {
            height: 100%;
            overflow: hidden;
            background: black;
            color: white;
        }
        .page {
            display: none;
            height: 100%;
            width: 100%;
            position: absolute;
            top: 0;
            left: 0;
            text-align: center;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            padding: 20px;
            transition: opacity 1s ease-in-out;
        }
        .active {
            display: flex;
            opacity: 1;
        }
        button {
            padding: 15px 30px;
            font-size: 1.2em;
            border: none;
            border-radius: 25px;
            cursor: pointer;
            background: linear-gradient(45deg, #ff4dc4, #9b59b6);
            color: white;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            font-weight: bold;
        }
        button:hover {
            transform: scale(1.1);
            box-shadow: 0 0 15px #fff;
        }
        /* Page 1 */
        #page1 {
            background: linear-gradient(135deg, #dbb1bf, #b5fffc);
            animation: float 5s infinite alternate ease-in-out;
            color: #333;
            font-weight: bold;
        }
        #page1 h1 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 20px;
            user-select: none;
        }
        /* ----- Page 2 (Replaced) ----- */
        #page2 {
            position: relative;
            background: #FFD6E0;
            font-family: 'Montserrat', sans-serif;
            color: #B30047;
            overflow: hidden;
        }
        .container {
            text-align: center;
            max-width: 90%;
        }
        .birthday-header {
            font-family: 'Fredoka One', cursive;
            margin-bottom: 8px;
            display: flex;
            justify-content: center;
            gap: 6px;
            flex-wrap: nowrap;
            white-space: nowrap;
            font-size: clamp(1.8rem, 5vw, 3.5rem);
        }
        .birthday-letter {
            display: inline-block;
            opacity: 0;
            transform: translateY(40px) scale(0.9);
            animation: letterBounce 0.8s forwards;
            font-weight: 900;
        }
        .letter-happy {
            color: white;
            -webkit-text-stroke: 2px black;
            text-shadow: 2px 2px 3px rgba(0, 0, 0, 0.7);
        }
        .birthday {
            background: linear-gradient(90deg, #FF4C84, #B30047);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        @keyframes letterBounce {
            0% {
                opacity: 0;
                transform: translateY(40px) scale(0.9);
            }
            60% {
                opacity: 1;
                transform: translateY(-8px) scale(1.05);
            }
            100% {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }
        .love-text {
            font-size: clamp(0.9rem, 2.5vw, 1.2rem);
            color: #B30047;
            margin-bottom: 10px;
            font-weight: 600;
        }
        .date-btn {
            background: #ff3366;
            color: #fff;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: clamp(0.7rem, 2vw, 0.9rem);
            font-weight: bold;
            margin-bottom: 14px;
            display: inline-block;
            box-shadow: 0 4px 10px rgba(255, 51, 102, 0.5);
        }
        .profile-name-block {
            opacity: 0;
            transform: translateY(100px);
            animation: imageSlideUp 1.4s forwards;
            animation-delay: 2.2s;
        }
        @keyframes imageSlideUp {
            0% {
                opacity: 0;
                transform: translateY(100px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .profile-image-container {
            position: relative;
            width: clamp(140px, 35vw, 220px);
            height: clamp(140px, 35vw, 220px);
            margin: 0 auto 16px;
            border-radius: 50%;
            padding: 6px;
            background: linear-gradient(45deg, #FF4C84, #B30047, #ffffff);
            animation: borderShift 6s ease infinite;
            box-shadow: 0 0 25px rgba(255, 76, 132, 0.6), 0 8px 20px rgba(255, 76, 132, 0.3);
        }
        .profile-image-container img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
        }
        @keyframes borderShift {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }
        .name-tag {
            background: #FF3366;
            padding: 8px 20px;
            border-radius: 30px;
            color: white;
            font-weight: 700;
            font-size: clamp(0.8rem, 2.5vw, 1.2rem);
            display: inline-block;
            box-shadow: 0 6px 14px rgba(255, 51, 102, 0.7);
        }
        .balloon {
            position: absolute;
            width: 12px;
            height: 18px;
            border-radius: 50%;
            opacity: 0.7;
            animation: fall linear infinite;
        }
        @keyframes fall {
            0% {
                transform: translateY(-10vh);
                opacity: 1;
            }
            100% {
                transform: translateY(110vh);
                opacity: 0;
            }
        }
        /* Gift in corner */
        .gift-container {
            position: absolute;
            top: 25px;
            right: 25px;
            cursor: pointer;
            text-align: center;
            z-index: 1000;
            user-select: none;
        }
        .gift {
            font-size: 2.5rem;
            color: #B30047;
            animation: pulse 2s infinite;
            filter: drop-shadow(0 0 6px #ff0080);
        }
        .gift-container:hover .gift {
            animation: shake 0.5s infinite;
            transform: scale(1.3);
            filter: drop-shadow(0 0 15px #ff1493);
        }
        .arrow {
            font-size: 1.5rem;
            color: #B30047;
            margin-top: 5px;
            animation: bounce 1s infinite;
        }
        .gift-text {
            font-size: 1rem;
            margin-top: 3px;
            font-weight: bold;
            animation: glowText 2s infinite;
        }
        @keyframes pulse {
            0%, 100% {
                filter: drop-shadow(0 0 6px #ff0080);
            }
            50% {
                filter: drop-shadow(0 0 18px #ff69b4);
            }
        }
        @keyframes shake {
            0%, 100% {
                transform: translateX(0);
            }
            25% {
                transform: translateX(-5px);
            }
            50% {
                transform: translateX(5px);
            }
        }
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(5px);
            }
        }
        @keyframes glowText {
            0% {
                color: #fff;
            }
            50% {
                color: #ff0;
            }
            100% {
                color: #fff;
            }
        }
        /* Page 3 */
        #page3 {
            background: rgb(224, 187, 210);
            overflow: hidden;
            color: #b31217;
            font-family: Arial, sans-serif;
        }
        #page3 h1 {
            font-size: 3.5rem;
            margin-top: 100px;
            font-weight: 1000;
            text-align: center;
            color: #b31217;
        }
        .premium-image-container {
            width: 230px;
            height: 230px;
            margin: 30px auto 0;
            border-radius: 18px;
            padding: 6px;
            background: linear-gradient(270deg, #ff0000, #ff69b4, #ffffff);
            background-size: 600% 600%;
            animation: gradientFlow 8s ease infinite;
            box-shadow: 0 0 15px 6px rgba(255, 255, 255, 0.6), 0 0 35px 8px rgba(255, 192, 203, 0.4);
            display: flex;
            justify-content: center;
            align-items: center;
        }
        @keyframes gradientFlow {
            0% {
                background-position: 0% 50%;
            }
            50% {
                background-position: 100% 50%;
            }
            100% {
                background-position: 0% 50%;
            }
        }
        .premium-image-container img {
            width: 218px;
            height: 218px;
            border-radius: 15px;
            border: 2.5px solid white;
            object-fit: cover;
            box-shadow: 0 0 15px 4px rgba(255, 255, 255, 0.85);
            animation: heartbeat 5s ease-in-out infinite;
        }
        @keyframes heartbeat {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.07);
            }
        }
        #page3 p {
            font-size: 1.2rem;
            color: #b31217;
            text-align: center;
            margin-top: 50px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <!-- Music -->
    <audio id="bg-music" autoplay loop>
        <source src="SaveTik.io_7648527747593080082.mp3" type="audio/mpeg" />
    </audio>

    <!-- Page 1 -->
    <div class="page active" id="page1">
        <h1 class="to our" id="to our"></h1>
        <h1>Click it to See it 👀</h1>
        <button onclick="nextPage(2)">Click Here</button>
    </div>

    <!-- Page 2 -->
    <div class="page" id="page2">
        <main class="container">
            <div class="love-text">To our Dss ❤️</div>
                <div class="name-tag">Kathleen Ann Aguilar</div>

<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
div.scroll-container {
  background-color: #c596b5;
  overflow: auto;
  white-space: nowrap;
  padding: 10px;
}

div.scroll-container img {
  padding: 10px;
}
</style>
</head>
<body>

<div class="scroll-container">
    <img src="https://scontent.fcrk2-3.fna.fbcdn.net/v/t39.30808-6/659692312_1719867088995163_377970462551901067_n.jpg?stp=dst-jpg_tt6&cstp=mx2048x2029&ctp=s2048x2029&_nc_cat=110&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=a5f93a&_nc_eui2=AeGBYqWtM6zIreYZma9V1aNcorJ4TgLMJZ2isnhOAswlnc3nW6m1Fz6OfHy5B3OTH5m8TsDLBdVsl23jJW3jA7QI&_nc_ohc=0jOgPIeX318Q7kNvwHcxa-z&_nc_oc=Adq9cihcjWjgoyeWgjPhY9e7Tq95ZsUxNd1tnbW10Aayk53Xo62FNZ48KECevL_3qsk&_nc_zt=23&_nc_ht=scontent.fcrk2-3.fna&_nc_gid=6Tdbeyhcc1y1mxgJf-VIFA&_nc_ss=7b2a8&oh=00_AQNQDODqPQ9nA2Nar6tuknZ5LC5YSrQ5mD-PCjRCvMQ32Q&oe=6AC931C6 alt="Mountains" width="600" height="400">
  <img src="https://scontent.fcrk2-6.fna.fbcdn.net/v/t39.30808-6/813429137_1865882857726918_8882869633286709609_n.jpg?stp=dst-jpg_tt6&cstp=mx1440x1920&ctp=s1440x1920&_nc_cat=106&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeGrQF9CX6BezsiW9RwuLGubIeS1HKXJ14Mh5LUcpcnXg13-JbD_x1-rYJQ5BON_S7KHt64sCOgUQNpn8FCnHPXe&_nc_ohc=QKDPYu800kUQ7kNvwGMBSiH&_nc_oc=AdoREo9_BDUq3zsvGCsXiLlYw53iw7wMsB2l4UWT6N878nVx7dtKmqPZNdGUkIR9htc&_nc_zt=23&_nc_ht=scontent.fcrk2-6.fna&_nc_gid=LmffAe63Rhwkxp19crhvFg&_nc_ss=7b2a8&oh=00_AQOR-nYm0yN_X9asO8qeB39YcmUPpNwulZyyK5FQJ7UjZA&oe=6AC90985" alt="Cinque Terre" width="600" height="400">
  <img src="https://scontent.fcrk2-5.fna.fbcdn.net/v/t39.30808-6/813825540_1865882934393577_6650275252898879371_n.jpg?stp=dst-jpg_tt6&cstp=mx1536x2048&ctp=s1536x2048&_nc_cat=106&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeF2fbxbRR1BgbA5OeoewIOpfOcq0RWkJ8p85yrRFaQnyrgiRnW7peKo98lmLzqDOOXQCkm03ybaTpoxlHSc_X2G&_nc_ohc=y5qGrdt-F_sQ7kNvwEtVgUh&_nc_oc=Adp_o8IBlKh-ShVtClDt_AwT8Uyc3OCoBHZGXq9gslnU7Ggza2iLrJSFGNcsfN28URw&_nc_zt=23&_nc_ht=scontent.fcrk2-5.fna&_nc_gid=KMMaFMOKlSAGloWDrnBNuw&_nc_ss=7b2a8&oh=00_AQN8Je2YsQiyhqkDIX-448tJ0cLdw5QheVcBnyOvrYwqmw&oe=6AC90137" alt="Forest" width="600" height="400">
  <img src="https://scontent.fcrk2-2.fna.fbcdn.net/v/t39.30808-6/480660342_1405637220418153_2133426437201927567_n.jpg?stp=dst-jpg_tt6&cstp=mx1536x2048&ctp=s1536x2048&_nc_cat=105&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeETJ7e0GBIChjaqGbriwjQB4L6QmLzKfBjgvpCYvMp8GCMCfnMVbSmM3Vn0tAdHXl7NhYidhqp36XobnM9k8G6Z&_nc_ohc=o1OTuxEgl2YQ7kNvwHkecb_&_nc_oc=AdoHRDYPcErP8RlsCbcJ-UdjIq4mQvckGHo83DoMKFVMkbAZpwhJd-Lkowkl7doCsAI&_nc_zt=23&_nc_ht=scontent.fcrk2-2.fna&_nc_gid=pN2Ldl7v2Q5N2oo397PL6A&_nc_ss=7b2a8&oh=00_AQO2cTVD95HdAfrNypqj9J0XTAMmW_Rw0BQL7moy4z12Ow&oe=6AC903EE" alt="Northern Lights" width="600" height="400">
  <img src="https://scontent.fcrk2-5.fna.fbcdn.net/v/t39.30808-6/668840983_1726345051680700_983763898837911848_n.jpg?stp=dst-jpg_tt6&cstp=mx1365x2048&ctp=s1365x2048&_nc_cat=104&_nc_map=urlgen_bucketless&ccb=1-7&_nc_sid=833d8c&_nc_eui2=AeGvNNH7TEBtI6XqRCBRoJ-qBM4KEI9bZTYEzgoQj1tlNgr1zE4GEgBaGts-b4Fzyg9WykfqymLPS2c7sfZv8neN&_nc_ohc=YihAKsX_Fo0Q7kNvwEi2Jub&_nc_oc=Adq8_7YHewO4demUCxIpA4dZJAYxVqhBPvb6ASx3MC50hRzZon_aW-NxFDwkk74T9Uo&_nc_zt=23&_nc_ht=scontent.fcrk2-5.fna&_nc_gid=XsjTaI8nQ_OlA8_tAd8Zbg&_nc_ss=7b2a8&oh=00_AQMg3tdnc32uGKP-D5apkvirPlqfteWhcKB_Vsvy20R4tQ&oe=6AC91018" alt="Mountains" width="600" height="400">
</div>

            </div>
        </main>
        <div class="gift-container" onclick="nextPage(3)">
            <div class="gift">🎁</div>
            <div class="arrow">⬇</div>
            <p class="gift-text">Click here to see more</p>
        </div>
    </div>

    <!-- Page 3 -->
    <div class="page" id="page3">
        <h1>Happy Teacher's Day 💕</h1>
        <div class="premium-image-container">
            <img src="https://i.pinimg.com/1200x/68/a1/48/68a14894f37c6659176c61a20a57bb0d.jpg" alt="Rose" />
        </div>


</body>
</html>


        <p>From Alexisss💕</p>
    </div>
    

    <script>
        function nextPage(num) {
            document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
            const page = document.getElementById('page' + num);
            page.classList.add('active');
        }
        const happyText = "To";
        const birthdayText = "our DSS";
        const birthdayContainer = document.getElementById('To our DSS-text');
        function createLetterSpan(char, index, isBirthday = false) {
            const span = document.createElement('span');
            span.textContent = char;
            span.classList.add('oUR-letter');
            if (isBirthday) span.classList.add('birthday');
            else span.classList.add('letter-To');
            span.style.animationDelay = `${index * 0.15}s`;
            return span;
        }
        [...happyText].forEach((c, i) => birthdayContainer.appendChild(createLetterSpan(c, i, false)));
        birthdayContainer.appendChild(document.createElement('span'));
        [...birthdayText].forEach((c, i) => birthdayContainer.appendChild(createLetterSpan(c, i + happyText.length + 1, true)));
        function createBalloon() {
            const balloon = document.createElement("div");
            balloon.classList.add("balloon");
            document.body.appendChild(balloon);
            const colors = ["#FF4C84", "#FFB347", "#6FA8DC", "#77DD77", "#FFD700"];
            balloon.style.background = colors[Math.floor(Math.random() * colors.length)];
            balloon.style.left = Math.random() * 100 + "vw";
            balloon.style.animationDuration = (3 + Math.random() * 4) + "s";
            setTimeout(() => balloon.remove(), 7000);
        }
        setInterval(createBalloon, 400);
    </script>
</body>

</html>


