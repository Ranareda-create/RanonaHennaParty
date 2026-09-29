# RanonaHennaParty
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ranona's Henna Night 💃</title>
    <style>
        :root {
            --bg-color: #0d0d0d;
            --text-color: #ffffff;
            --accent-gold: #d4af37;
            --accent-burgundy: #800020;
            --accent-red: #ff0033;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            text-align: center;
            overflow-x: hidden;
        }
        .cover-screen {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(135deg, #1a0005, #000000);
            display: flex; flex-direction: column;
            justify-content: center; align-items: center;
            z-index: 9999; transition: opacity 0.5s ease;
            cursor: pointer;
        }
        .cover-screen.hidden { opacity: 0; pointer-events: none; }
        .btn-open {
            background: linear-gradient(45deg, var(--accent-burgundy), var(--accent-red));
            color: white; border: none; padding: 15px 40px;
            font-size: 1.2rem; border-radius: 30px;
            box-shadow: 0 0 20px rgba(255, 0, 51, 0.4);
            animation: pulse 2s infinite; cursor: pointer;
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        .container { max-width: 600px; margin: 0 auto; padding: 20px; }
        .header-title { font-size: 2.5rem; color: var(--accent-gold); margin-bottom: 5px; font-weight: bold; }
        .subtitle { font-style: italic; color: #ccc; margin-bottom: 30px; }
        .details-box {
            background: rgba(255,255,255,0.05); border: 1px solid rgba(212,175,55,0.2);
            padding: 25px; border-radius: 15px; margin: 25px 0;
        }
        .countdown-container { display: flex; justify-content: center; gap: 15px; margin: 20px 0; }
        .countdown-item {
            background: rgba(128, 0, 32, 0.3); padding: 10px 15px;
            border-radius: 10px; min-width: 60px;
        }
        .countdown-val { font-size: 1.8rem; font-weight: bold; color: var(--accent-gold); display: block; }
        .countdown-lbl { font-size: 0.8rem; color: #aaa; text-transform: uppercase; }
        .btn-directions {
            display: inline-block; background-color: transparent;
            border: 2px solid var(--accent-gold); color: var(--accent-gold);
            padding: 10px 25px; border-radius: 20px; text-decoration: none;
            margin-top: 15px; font-weight: bold; transition: 0.3s;
        }
        .btn-directions:hover { background-color: var(--accent-gold); color: black; }
        .theme-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(100px, 1fr)); gap: 10px; margin: 20px 0; }
        .theme-card { padding: 15px; border-radius: 10px; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.1); }
        .wheel-container { position: relative; width: 260px; height: 260px; margin: 30px auto; }
        .wheel {
            width: 100%; height: 100%; border-radius: 50%;
            border: 5px solid var(--accent-gold);
            background: conic-gradient(
                #ff0033 0deg 72deg, #800020 72deg 144deg, 
                #d4af37 144deg 216deg, #000000 216deg 288deg, #ffffff 288deg 360deg
            );
            transition: transform 4s cubic-bezier(0.1, 0.8, 0.3, 1);
        }
        .wheel-pointer {
            position: absolute; top: -15px; left: 50%; transform: translateX(-50%);
            width: 0; height: 0; 
            border-left: 15px solid transparent; border-right: 15px solid transparent;
            border-top: 25px solid var(--accent-gold); z-index: 10;
        }
        .btn-spin {
            background-color: var(--accent-gold); color: black; border: none;
            padding: 12px 30px; font-size: 1rem; font-weight: bold;
            border-radius: 25px; cursor: pointer; margin-top: 15px;
        }
        .dare-result { margin-top: 15px; font-weight: bold; font-size: 1.1rem; min-height: 24px; color: var(--accent-gold); }
        .form-group { text-align: left; margin-bottom: 15px; }
        .form-group label { display: block; margin-bottom: 5px; color: #ccc; font-size: 0.9rem; }
        input[type="text"], select {
            width: 100%; padding: 12px; border-radius: 8px; border: 1px solid #444;
            background-color: #222; color: white; box-sizing: border-box;
        }
        .btn-submit {
            width: 100%; background: linear-gradient(45deg, var(--accent-burgundy), var(--accent-red));
            color: white; border: none; padding: 14px; border-radius: 8px;
            font-size: 1.1rem; font-weight: bold; cursor: pointer; margin-top: 10px;
        }
        footer { margin-top: 5px; padding: 30px 0; font-size: 0.85rem; color: #666; border-top: 1px solid #222; }
    </style>
</head>
<body>

    <!-- Cover Screen Element -->
    <div class="cover-screen" id="coverScreen" onclick="openInvitation()">
        <p style="font-size: 1.5rem; letter-spacing: 2px;">✦ &nbsp;HENNA NIGHT&nbsp; ✦</p>
        <h1 style="color: var(--accent-gold); font-size: 3rem; margin: 10px 0;">Ranona's</h1>
        <button class="btn-open">Touch Me TO OPEN 💃</button>
        <p style="margin-top: 20px; font-size: 0.9rem; color: #888;">— SHE SAID YES — LET'S CELEBRATE —</p>
    </div>

    <div class="container">
        <h1 class="header-title">Ranona's Henna Night 💃</h1>
        <p class="subtitle">A Night of Joy, Music & Sisterhood ✨</p>
        <div style="font-size: 2rem; color: var(--accent-red);">♥</div>
        
        <p>Join us to celebrate a night full of joy, music & unforgettable memories 💋</p>

        <!-- Main Details -->
        <div class="details-box">
            <h2 style="color: var(--accent-gold); margin-top: 0; font-size: 1.8rem;">4 / 12 / 2026</h2>
            <p style="font-size: 1.1rem;">Seven o'clock in the evening</p>
            <p style="color: #aaa; margin-bottom: 5px;">Alexwest Compound · Villa 430</p>
            <div style="font-size: 1.5rem; margin: 10px 0;">🥂🔥💋</div>
            <a href="https://google.com" target="_blank" class="btn-directions">🗺️ Get Directions</a>
        </div>

        <p style="font-style: italic; color: #bbb; max-width: 450px; margin: 20px auto;">
            "One last adventure before she says I do — make it absolutely legendary." <br>
            <span style="color: var(--accent-gold); font-weight: bold;">— HERE'S TO RANA 💃</span>
        </p>

        <!-- Countdown Timer Section -->
        <h3 style="text-transform: uppercase; letter-spacing: 1px; color: #aaa; margin-top: 40px;">Counting Down To The Henna Night</h3>
        <div class="countdown-container">
            <div class="countdown-item"><span class="countdown-val" id="days">--</span><span class="countdown-lbl">Days</span></div>
            <div class="countdown-item"><span class="countdown-val" id="hours">--</span><span class="countdown-lbl">Hours</span></div>
            <div class="countdown-item"><span class="countdown-val" id="minutes">--</span><span class="countdown-lbl">Min</span></div>
            <div class="countdown-item"><span class="countdown-val" id="seconds">--</span><span class="countdown-lbl">Sec</span></div>
        </div>
        <p style="font-size: 0.9rem; color: #888; font-style: italic;">Every second brings us closer to the chaos ♡</p>

        <!-- Dress Code Theme Section -->
        <h3 style="margin-top: 45px; border-bottom: 1px solid #333; padding-bottom: 10px; color: var(--accent-gold);">Dress Code ⚜️</h3>
        <p style="font-size: 0.95rem; color: #ccc;">Come dressed to impress — no exceptions!</p>
        <div class="theme-grid">
            <div class="theme-card"><div style="font-size:1.5rem;">🖤</div><strong>Black</strong><br><span style="font-size:0.8rem;color:#aaa">Sleek · Bold</span></div>
            <div class="theme-card"><div style="font-size:1.5rem;">🤍</div><strong>White</strong><br><span style="font-size:0.8rem;color:#aaa">Pure · Chic</span></div>
            <div class="theme-card"><div style="font-size:1.5rem;">✨</div><strong>Gold</strong><br><span style="font-size:0.8rem;color:#aaa">Elegant · Luxe</span></div>
            <div class="theme-card"><div style="font-size:1.5rem;">🌹</div><strong>Burgundy</strong><br><span style="font-size:0.8rem;color:#aaa">Deep · Regal</span></div>
            <div class="theme-card"><div style="font-size:1.5rem;">💃</div><strong>Red</strong><br><span style="font-size:0.8rem;color:#aaa">Bold · Fierce</span></div>
        </div>
        <p style="font-size: 0.8rem; color: var(--accent-gold); letter-spacing: 1px;">✦ MIX & MATCH — ELEGANCE IS NON-NEGOTIABLE ✦</p>

        <!-- Interactive Dare Wheel Game -->
        <h3 style="margin-top: 45px; color: var(--accent-gold);">The Dare Wheel 🎡</h3>
        <p style="font-size: 0.95rem; color: #ccc; margin-bottom: 5px;">Spin the wheel of chaos! Perform the dare. No excuses!</p>
        <div class="wheel-container">
            <div class="wheel-pointer"></div>
            <div class="wheel" id="wheel"></div>
        </div>
        <button class="btn-spin" onclick="spinWheel()">Spin the Wheel 💋</button>
        <div class="dare-result" id="dareResult"></div>

        <!-- Music Playlist Selection Section -->
        <h3 style="margin-top: 45px; color: var(--accent-gold);">Request a Song 🎵</h3>
        <p style="font-size: 0.95rem; color: #ccc; margin-bottom: 15px;">Help us build the ultimate party playlist!</p>
