<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes" />
    <title>Rori Community FC | Official Website</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Open+Sans:wght@400;600&family=Playfair+Display:ital,wght@0,400;0,700;1,700&family=Poppins:wght@400;500;600;700;800;900&display=swap" rel="stylesheet" />
    <style>
        /* ── Reset & Base ── */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            background-color: #0a0f24;
            color: #e0e0e0;
            font-family: 'Poppins', 'Open Sans', sans-serif;
            font-size: 18px;
            font-weight: 500;
            line-height: 1.7;
            scroll-behavior: smooth;
        }
        h1,
        h2,
        h3,
        .bebas {
            font-family: 'Poppins', 'Bebas Neue', cursive;
            letter-spacing: 1px;
            text-transform: uppercase;
        }
        .gold {
            color: #FFD600;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ── Navbar ── */
        nav {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px 30px;
            background: #0d1137;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.6);
            flex-wrap: wrap;
            gap: 8px 12px;
        }
        .nav-logo img {
            height: 55px;
            width: 55px;
            border-radius: 50%;
            border: 2px solid #FFD600;
            object-fit: cover;
            background: #0d1137;
            display: block;
        }
        .nav-links {
            display: flex;
            gap: 18px;
            flex-wrap: wrap;
            align-items: center;
        }
        .nav-links a {
            color: #ddd;
            text-decoration: none;
            font-weight: 600;
            font-size: 0.95rem;
            transition: color 0.3s;
            white-space: nowrap;
        }
        .nav-links a:hover,
        .nav-links a:focus-visible {
            color: #FFD600;
            outline: 2px solid #FFD600;
            outline-offset: 4px;
            border-radius: 2px;
        }

        /* ── Hero ── */
        .hero {
            position: relative;
            background:
                linear-gradient(135deg, rgba(26, 35, 126, 0.85), rgba(10, 15, 36, 0.92)),
                url('https://images.unsplash.com/photo-1574629810360-7efbbe195018?w=1600&h=900&fit=crop&crop=center&q=80') center / cover no-repeat;
            background-color: #0a0f24;
            padding: 60px 20px 50px;
            text-align: center;
            overflow: hidden;
            min-height: 70vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: -50%;
            width: 200%;
            height: 4px;
            background: repeating-linear-gradient(90deg, #FFD600 0px, #FFD600 10px, transparent 10px, transparent 20px);
            animation: scanline 4s linear infinite;
            opacity: 0.4;
            pointer-events: none;
        }
        @keyframes scanline {
            0% {
                transform: translateY(-100%);
            }
            100% {
                transform: translateY(100vh);
            }
        }

        /* ── RORI Profile Logo ── */
        .rori-profile {
            text-align: center;
            padding: 10px 15px;
            position: relative;
            z-index: 2;
        }

        .rori-logo {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 50%;
            display: block;
            margin: 0 auto 20px;
            box-shadow: 0 0 50px rgba(212, 166, 45, 0.6);
            border: 4px solid #FFD600;
            animation: floatBadge 3s ease-in-out infinite;
            background: #0d1137;
        }

        @keyframes floatBadge {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-14px);
            }
            100% {
                transform: translateY(0px);
            }
        }

        .rori-profile h1 {
            margin: 0;
            font-size: 3.8rem;
            font-weight: 900;
            letter-spacing: 3px;
            color: #FFD600;
            text-shadow: 4px 4px 0 #1A237E, 0 0 30px rgba(255, 214, 0, 0.2);
            font-family: 'Poppins', sans-serif;
            text-transform: uppercase;
        }

        .rori-profile p {
            margin-top: 10px;
            font-size: 1.4rem;
            letter-spacing: 6px;
            color: #fff;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
            font-weight: 600;
            text-shadow: 0 2px 15px rgba(0, 0, 0, 0.5);
        }

        /* ── Stats & CTA ── */
        .stats-bar {
            display: flex;
            justify-content: center;
            gap: 50px;
            margin: 35px 0 25px;
            flex-wrap: wrap;
            position: relative;
            z-index: 2;
        }
        .stat-item {
            background: rgba(255, 255, 255, 0.06);
            padding: 20px 35px;
            border-radius: 16px;
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 214, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .stat-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(255, 214, 0, 0.1);
        }
        .stat-number {
            font-size: 3rem;
            color: #FFD600;
            font-weight: 900;
        }
        .stat-item .stat-label {
            font-size: 0.95rem;
            color: #ccc;
            font-weight: 500;
            letter-spacing: 1px;
        }
        .cta-buttons {
            margin-top: 20px;
            position: relative;
            z-index: 2;
        }

        /* ── Buttons ── */
        .btn {
            display: inline-block;
            background: #FFD600;
            color: #1A237E;
            font-weight: 800;
            padding: 16px 38px;
            border-radius: 50px;
            text-decoration: none;
            margin: 0 10px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-family: 'Poppins', sans-serif;
            font-size: 1.2rem;
            letter-spacing: 1px;
            box-shadow: 0 4px 20px rgba(255, 214, 0, 0.3);
        }
        .btn-outline {
            background: transparent;
            border: 2px solid #FFD600;
            color: #FFD600;
            box-shadow: none;
        }
        .btn:hover,
        .btn:focus-visible {
            transform: scale(1.06) translateY(-3px);
            box-shadow: 0 8px 35px rgba(255, 214, 0, 0.4);
            outline: 2px solid #FFD600;
            outline-offset: 3px;
        }
        .btn-outline:hover {
            background: rgba(255, 214, 0, 0.1);
            box-shadow: 0 0 30px rgba(255, 214, 0, 0.2);
        }

        /* ── Sections ── */
        section {
            padding: 70px 20px;
        }
        .section-title {
            font-size: 2.8rem;
            color: #FFD600;
            text-align: center;
            margin-bottom: 45px;
            font-weight: 800;
            position: relative;
            letter-spacing: 2px;
        }
        .section-title::after {
            content: "";
            display: block;
            width: 100px;
            height: 5px;
            background: #FFD600;
            margin: 15px auto 0;
            border-radius: 4px;
        }

        /* ── Welcome Section ── */
        .welcome-section {
            background: linear-gradient(135deg, #0d1137, #121836);
            border-top: 4px solid #FFD600;
            border-bottom: 4px solid #FFD600;
        }
        .welcome-container {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }
        .welcome-content {
            background: rgba(18, 24, 54, 0.6);
            border-radius: 24px;
            padding: 45px 50px;
            border: 1px solid rgba(255, 214, 0, 0.15);
            position: relative;
            backdrop-filter: blur(8px);
        }
        .welcome-content::before {
            content: "“";
            font-size: 6rem;
            color: #FFD600;
            opacity: 0.12;
            position: absolute;
            top: -10px;
            left: 25px;
            font-family: serif;
        }
        .welcome-content p {
            font-size: 1.2rem;
            line-height: 2;
            margin-bottom: 18px;
            color: #e8e8e8;
            font-weight: 500;
        }
        .welcome-content p:last-of-type {
            margin-bottom: 0;
        }
        .welcome-content .greeting-highlight {
            color: #FFD600;
            font-weight: 800;
            font-size: 1.5rem;
            font-family: 'Poppins', sans-serif;
            letter-spacing: 2px;
        }
        .welcome-content .closing {
            margin-top: 25px;
            padding-top: 25px;
            border-top: 3px solid rgba(255, 214, 0, 0.25);
            font-size: 1.3rem;
            font-weight: 700;
            color: #FFD600;
        }
        .welcome-content .closing .amharic {
            display: block;
            font-size: 1.5rem;
            margin-top: 8px;
            font-family: 'Poppins', sans-serif;
            letter-spacing: 1px;
        }

        /* ── About ── */
        .about-profile {
            max-width: 900px;
            margin: 0 auto 45px;
            background: rgba(18, 24, 54, 0.7);
            border-left: 8px solid #FFD600;
            padding: 35px 45px;
            border-radius: 16px;
            font-size: 1.2rem;
            line-height: 2;
            text-align: center;
            color: #e8e8e8;
            font-weight: 500;
        }
        .about-profile .motto-highlight {
            color: #FFD600;
            font-weight: 800;
            font-size: 1.4rem;
            display: block;
            margin-top: 15px;
            font-family: 'Poppins', sans-serif;
            letter-spacing: 1px;
        }

        /* ── Cards ── */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 25px;
        }
        .card {
            background: #121836;
            border-radius: 20px;
            padding: 30px 25px;
            transition: all 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94);
            border: 1px solid rgba(255, 214, 0, 0.15);
            text-align: center;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }
        .card:hover {
            transform: translateY(-12px);
            box-shadow: 0 20px 40px rgba(255, 214, 0, 0.12);
            border-color: #FFD600;
        }
        .card h3 {
            color: #FFD600;
            margin: 18px 0 12px;
            font-size: 2rem;
            font-weight: 800;
        }
        .card p {
            font-size: 1.05rem;
            font-weight: 500;
            color: #d0d0d0;
        }
        .card a {
            color: #FFD600;
            text-decoration: none;
            font-weight: 600;
        }
        .card a:hover {
            text-decoration: underline;
        }
        .card ul {
            list-style: none;
            padding: 0;
            text-align: left;
        }
        .card ul li {
            padding: 8px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            font-weight: 500;
        }
        .card ul li:last-child {
            border-bottom: none;
        }

        /* ── Fund section ── */
        .fund-section {
            max-width: 1000px;
            margin: 0 auto;
        }
        .fund-description {
            background: rgba(18, 24, 54, 0.7);
            border-radius: 20px;
            padding: 35px 45px;
            margin-bottom: 30px;
            border: 1px solid rgba(255, 214, 0, 0.15);
            font-size: 1.15rem;
            line-height: 2;
            text-align: center;
            font-weight: 500;
        }
        .fund-description p {
            margin-bottom: 14px;
        }
        .fund-description p:last-child {
            margin-bottom: 0;
        }
        .fund-benefits {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 18px;
            margin: 25px 0 35px;
        }
        .fund-benefits .benefit-item {
            background: #1A237E;
            padding: 20px 15px;
            border-radius: 14px;
            border: 1px solid rgba(255, 214, 0, 0.25);
            font-weight: 700;
            font-size: 1rem;
            text-align: center;
            transition: all 0.3s ease;
        }
        .fund-benefits .benefit-item:hover {
            border-color: #FFD600;
            transform: scale(1.04);
            box-shadow: 0 8px 25px rgba(255, 214, 0, 0.1);
        }
        .fund-benefits .benefit-item .icon {
            display: block;
            font-size: 2.2rem;
            margin-bottom: 8px;
        }
        .bank-details {
            background: linear-gradient(135deg, #1A237E, #0d1137);
            border: 3px solid #FFD600;
            border-radius: 20px;
            padding: 30px 35px;
            text-align: center;
            margin-top: 15px;
            box-shadow: 0 0 40px rgba(255, 214, 0, 0.05);
        }
        .bank-details .bank-label {
            font-size: 1.1rem;
            color: #ccc;
            margin-bottom: 8px;
            font-weight: 600;
        }
        .bank-details .account-number {
            font-size: 2.5rem;
            font-weight: 900;
            color: #FFD600;
            font-family: 'Poppins', sans-serif;
            letter-spacing: 4px;
            word-break: break-all;
        }
        .bank-details .copy-btn {
            background: transparent;
            border: 2px solid #FFD600;
            color: #FFD600;
            padding: 8px 24px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: 700;
            margin-top: 10px;
            transition: all 0.3s ease;
        }
        .bank-details .copy-btn:hover {
            background: #FFD600;
            color: #1A237E;
            transform: scale(1.05);
        }
        .bank-details .account-name {
            font-size: 1.3rem;
            color: #fff;
            margin-top: 10px;
            font-weight: 700;
        }
        .bank-details .telebirr {
            font-size: 1.7rem;
            color: #FFD600;
            margin-top: 8px;
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            letter-spacing: 2px;
        }

        /* ── Contributions Table ── */
        .contributions-section {
            max-width: 900px;
            margin: 0 auto;
        }
        .contributions-intro {
            text-align: center;
            font-size: 1.2rem;
            margin-bottom: 28px;
            color: #ccc;
            font-weight: 500;
        }
        .contributions-table-wrapper {
            background: #121836;
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid rgba(255, 214, 0, 0.15);
            margin-bottom: 28px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }
        .contributions-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 1.05rem;
        }
        .contributions-table thead {
            background: #1A237E;
            border-bottom: 3px solid #FFD600;
        }
        .contributions-table thead th {
            padding: 16px 22px;
            text-align: left;
            color: #FFD600;
            font-family: 'Poppins', sans-serif;
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: 1px;
        }
        .contributions-table thead th:last-child {
            text-align: right;
        }
        .contributions-table tbody tr {
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            transition: background 0.3s;
        }
        .contributions-table tbody tr:hover {
            background: rgba(26, 35, 126, 0.3);
        }
        .contributions-table tbody tr:last-child {
            border-bottom: none;
        }
        .contributions-table tbody td {
            padding: 14px 22px;
            color: #e0e0e0;
            font-weight: 500;
        }
        .contributions-table tbody td:first-child {
            font-weight: 700;
            color: #FFD600;
            width: 60px;
            text-align: center;
        }
        .contributions-table tbody td:last-child {
            text-align: right;
            font-weight: 700;
            color: #FFD600;
        }
        .contributions-table .highlight-row {
            background: rgba(255, 214, 0, 0.08);
            border-top: 3px solid #FFD600;
            border-bottom: 3px solid #FFD600;
        }
        .contributions-table .highlight-row td {
            font-weight: 800;
            font-size: 1.2rem;
            color: #FFD600;
            padding: 18px 22px;
        }
        .contributions-table .highlight-row td:last-child {
            font-size: 1.4rem;
        }
        .contributions-thanks {
            background: rgba(18, 24, 54, 0.7);
            border-left: 8px solid #FFD600;
            border-radius: 16px;
            padding: 30px 35px;
            text-align: center;
            font-size: 1.15rem;
            line-height: 2;
            color: #e8e8e8;
            font-weight: 500;
        }
        .contributions-thanks .thanks-icon {
            font-size: 3rem;
            display: block;
            margin-bottom: 10px;
        }

        /* ── Regulations ── */
        .regulations-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 35px;
            max-width: 1100px;
            margin: 0 auto;
        }
        .regulations-grid .card {
            text-align: left;
        }
        .regulations-grid .card h3 {
            text-align: center;
            font-size: 2rem;
        }
        .regulations-grid .card ul li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            display: flex;
            align-items: flex-start;
            gap: 12px;
            font-weight: 500;
            font-size: 1.05rem;
        }
        .regulations-grid .card ul li::before {
            content: "▸";
            color: #FFD600;
            font-weight: bold;
            flex-shrink: 0;
            font-size: 1.2rem;
        }
        .regulations-grid .card ul li:last-child {
            border-bottom: none;
        }

        /* ── Motto banner ── */
        .motto-banner {
            background: linear-gradient(135deg, #1A237E, #0d1137);
            border: 3px solid #FFD600;
            border-radius: 24px;
            padding: 45px 35px;
            margin: 45px auto 0;
            max-width: 850px;
            text-align: center;
            box-shadow: 0 0 50px rgba(255, 214, 0, 0.08);
        }
        .motto-banner .motto-text {
            font-size: 2.6rem;
            font-weight: 900;
            color: #FFD600;
            font-family: 'Poppins', sans-serif;
            letter-spacing: 3px;
            line-height: 1.4;
        }
        .motto-banner .motto-sub {
            color: #ccc;
            font-size: 1.1rem;
            margin-top: 10px;
            font-weight: 500;
            letter-spacing: 2px;
        }

        /* ── Squad ── */
        .squad-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
            gap: 22px;
        }
        .player-card {
            background: #1A237E;
            border-radius: 16px;
            padding: 18px 12px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid #2a3480;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
        }
        .player-card:hover {
            border-color: #FFD600;
            transform: scale(1.05) translateY(-5px);
            box-shadow: 0 12px 30px rgba(255, 214, 0, 0.1);
        }
        .jersey-number {
            font-size: 2.2rem;
            font-weight: 900;
            color: #FFD600;
        }
        .player-card div:last-child {
            font-weight: 600;
            font-size: 1.05rem;
            margin-top: 4px;
        }

        /* ── Chat ── */
        .chat-container {
            background: #0b0f1f;
            border-radius: 24px;
            padding: 25px;
            margin-top: 35px;
            border: 2px solid #FFD600;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.3);
        }
        .chat-container h3 {
            font-size: 1.6rem;
            font-weight: 800;
        }
        .chat-messages {
            height: 220px;
            overflow-y: auto;
            background: #121836;
            padding: 18px;
            border-radius: 14px;
            margin-bottom: 18px;
        }
        .chat-messages p {
            margin-bottom: 8px;
            font-weight: 500;
        }
        .chat-input-area {
            display: flex;
            gap: 12px;
        }
        .chat-input-area input {
            flex: 1;
            padding: 14px 20px;
            border-radius: 30px;
            border: none;
            background: #1e2245;
            color: white;
            font-size: 1rem;
            font-weight: 500;
        }
        .chat-input-area input:focus-visible {
            outline: 2px solid #FFD600;
        }
        .chat-input-area button {
            background: #FFD600;
            border: none;
            border-radius: 30px;
            padding: 0 30px;
            font-weight: 800;
            cursor: pointer;
            color: #1A237E;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }
        .chat-input-area button:hover,
        .chat-input-area button:focus-visible {
            outline: 2px solid #FFD600;
            outline-offset: 2px;
            transform: scale(1.05);
        }

        /* ── Anthem Section ── */
        .anthem-container {
            max-width: 800px;
            margin: 0 auto;
            background: rgba(18, 24, 54, 0.7);
            border-radius: 24px;
            padding: 45px 50px;
            border: 2px solid rgba(255, 214, 0, 0.2);
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        .anthem-container::before {
            content: "♫";
            font-size: 12rem;
            position: absolute;
            right: -20px;
            bottom: -40px;
            color: rgba(255, 214, 0, 0.04);
            font-family: serif;
            pointer-events: none;
        }
        .anthem-content {
            color: #e0e0e0;
            position: relative;
            z-index: 2;
        }
        .anthem-content .verse,
        .anthem-content .chorus,
        .anthem-content .outro {
            margin-bottom: 28px;
            padding-bottom: 24px;
            border-bottom: 1px solid rgba(255, 214, 0, 0.08);
        }
        .anthem-content .verse:last-of-type,
        .anthem-content .chorus:last-of-type,
        .anthem-content .outro:last-of-type {
            border-bottom: none;
            margin-bottom: 0;
            padding-bottom: 0;
        }
        .anthem-content p {
            font-size: 1.1rem;
            line-height: 2;
            margin-bottom: 4px;
            font-weight: 500;
        }
        .anthem-content p strong {
            color: #FFD600;
            font-size: 1.2rem;
            font-weight: 800;
            letter-spacing: 1px;
            display: inline-block;
            margin-bottom: 4px;
        }
        .anthem-content .chorus p {
            color: #FFD600;
            font-weight: 600;
        }
        .anthem-content .chorus p strong {
            color: #fff;
            font-weight: 800;
        }
        .anthem-content .outro p {
            font-size: 1.3rem;
            font-weight: 700;
            color: #FFD600;
            text-align: center;
            letter-spacing: 3px;
        }
        .anthem-content .outro p strong {
            color: #fff;
            font-weight: 800;
        }
        .anthem-title-sub {
            text-align: center;
            color: #ccc;
            font-style: italic;
            margin-bottom: 30px;
            font-size: 1.1rem;
            letter-spacing: 2px;
        }

        /* ═══════════════════════════════════════ */
        /* ── HEAD COACH SECTION ── */
        /* ═══════════════════════════════════════ */

        .coach-section {
            padding: 60px 20px;
            background: linear-gradient(135deg, #0a192f 0%, #112240 100%);
            color: #ffffff;
            text-align: center;
            border-top: 3px solid #d4af37;
            border-bottom: 3px solid #d4af37;
        }

        .coach-card {
            max-width: 400px;
            margin: 30px auto;
            background: #ffffff;
            color: #111111;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
            border: 4px solid #d4af37;
            transition: transform 0.4s ease, box-shadow 0.4s ease;
        }

        .coach-card:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 20px 40px rgba(212, 175, 55, 0.4);
        }

        .coach-img-wrapper {
            position: relative;
            width: 100%;
            height: 380px;
            overflow: hidden;
        }

        .coach-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .coach-card:hover .coach-img {
            transform: scale(1.08);
        }

        .badge-tag {
            position: absolute;
            bottom: 15px;
            left: 15px;
            background: #d4af37;
            color: #0a192f;
            font-weight: 800;
            padding: 6px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            letter-spacing: 1px;
        }

        .coach-details {
            padding: 25px 20px;
        }

        .coach-details h3 {
            font-size: 2.2rem;
            font-weight: 800;
            margin-bottom: 5px;
            color: #0a192f;
        }

        .coach-details .role {
            font-size: 1.1rem;
            font-weight: 700;
            color: #0056b3;
            margin-bottom: 15px;
        }

        .coach-details .bio {
            font-size: 1rem;
            color: #555555;
            line-height: 1.5;
        }

        /* ── Gallery ── (unchanged) ── */
        .gallery-section {
            padding: 60px 20px;
            background: linear-gradient(135deg, #0a0f24, #121836);
            text-align: center;
            border-top: 3px solid #FFD600;
            border-bottom: 3px solid #FFD600;
        }
        .gallery-title {
            font-size: 2.8rem;
            font-weight: 900;
            color: #FFD600;
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-family: 'Poppins', sans-serif;
        }
        .gallery-subtitle {
            font-size: 1.2rem;
            font-weight: 600;
            color: #e0e0e0;
            margin-bottom: 45px;
            letter-spacing: 2px;
        }
        .gallery-subtitle span {
            color: #FFD600;
        }
        .gallery-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
            justify-content: center;
            max-width: 1200px;
            margin: 0 auto;
        }
        .gallery-card {
            width: 300px;
            border-radius: 16px;
            overflow: hidden;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.35);
            background: #121836;
            border: 2px solid rgba(255, 214, 0, 0.1);
            transition: transform 0.4s cubic-bezier(0.25, 0.46, 0.45, 0.94),
                        box-shadow 0.4s ease,
                        border-color 0.4s ease;
        }
        .gallery-card:hover {
            transform: translateY(-12px) scale(1.02);
            box-shadow: 0 20px 50px rgba(255, 214, 0, 0.12);
            border-color: #FFD600;
        }
        .gallery-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            display: block;
            transition: transform 0.6s cubic-bezier(0.25, 0.46, 0.45, 0.94);
        }
        .gallery-card:hover .gallery-img {
            transform: scale(1.06);
        }
        .img-caption {
            font-size: 1.2rem;
            font-weight: 700;
            padding: 16px 18px 18px;
            color: #FFD600;
            background: #121836;
            text-align: left;
            font-family: 'Poppins', sans-serif;
            border-top: 1px solid rgba(255, 214, 0, 0.06);
        }
        .img-caption small {
            display: block;
            font-size: 0.85rem;
            font-weight: 500;
            color: #b0b0b0;
            margin-top: 2px;
            letter-spacing: 0.5px;
        }

        /* ── Footer ── */
        footer {
            text-align: center;
            padding: 35px;
            background: #0a0f24;
            border-top: 3px solid #FFD600;
            margin-top: 50px;
            font-weight: 500;
            font-size: 1.05rem;
        }

        /* ── SILLA COFFEE SHOP ── (unchanged) ── */
        .cafe-section {
            background: #2b1b14;
            color: #f5f1ea;
            padding: 0 20px 70px;
            font-family: 'Poppins', 'Open Sans', sans-serif;
        }
        .cafe-section .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        .partner-section {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(212, 175, 55, 0.2);
            border-radius: 20px;
            padding: 35px 30px 30px;
            margin-bottom: 45px;
            text-align: center;
        }
        .partner-section .partner-label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 6px;
            color: #d4af37;
            opacity: 0.7;
            margin-bottom: 20px;
            font-weight: 700;
            font-family: 'Poppins', sans-serif;
        }
        .partner-section .partner-label::before {
            content: "✦ ";
            color: #d4af37;
        }
        .partner-section .partner-label::after {
            content: " ✦";
            color: #d4af37;
        }
        .partner-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 20px;
        }
        .partner-card {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(212, 175, 55, 0.15);
            border-radius: 14px;
            padding: 20px 16px;
            transition: all 0.3s ease;
            text-align: center;
        }
        .partner-card:hover {
            border-color: #d4af37;
            background: rgba(255, 255, 255, 0.08);
            transform: translateY(-6px);
            box-shadow: 0 12px 30px rgba(0, 0, 0, 0.3);
        }
        .partner-card .variant-tag {
            font-size: 0.65rem;
            text-transform: uppercase;
            letter-spacing: 3px;
            color: #d4af37;
            opacity: 0.5;
            font-weight: 600;
            margin-bottom: 8px;
        }
        .partner-card .variant-text {
            font-family: 'Playfair Display', serif;
            font-size: 1.15rem;
            color: #f5f1ea;
            line-height: 1.6;
        }
        .partner-card .variant-text .gold {
            color: #d4af37;
            font-weight: 700;
        }
        .partner-card .variant-text .icon {
            font-size: 1.4rem;
            margin: 0 2px;
        }
        .partner-card .variant-divider {
            width: 40px;
            height: 2px;
            background: #d4af37;
            margin: 10px auto 8px;
            opacity: 0.3;
        }

        .cafe-hero {
            position: relative;
            background: linear-gradient(135deg, rgba(43, 27, 20, 0.85), rgba(20, 12, 8, 0.95)),
                url('https://images.unsplash.com/photo-1495474472287-4d71bcdd2085?w=1600&h=600&fit=crop&crop=center&q=80') center / cover no-repeat;
            padding: 90px 20px 70px;
            text-align: center;
            border-radius: 0 0 50px 50px;
            margin-bottom: 55px;
            border-bottom: 4px solid #d4af37;
            position: relative;
        }
        .cafe-hero::after {
            content: "☕";
            font-size: 4.5rem;
            position: absolute;
            bottom: -35px;
            left: 50%;
            transform: translateX(-50%);
            background: #2b1b14;
            padding: 0 25px;
            border: 4px solid #d4af37;
            border-radius: 50%;
            width: 90px;
            height: 90px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #d4af37;
        }
        .cafe-hero h2 {
            font-family: 'Playfair Display', serif;
            font-size: 5rem;
            color: #f5f1ea;
            font-weight: 700;
            letter-spacing: 2px;
            text-shadow: 2px 2px 15px rgba(0, 0, 0, 0.8);
            margin-bottom: 12px;
        }
        .cafe-hero h2 span {
            color: #d4af37;
            font-style: italic;
        }
        .cafe-hero p {
            font-size: 1.4rem;
            color: #f5f1ea;
            opacity: 0.9;
            font-weight: 300;
            letter-spacing: 5px;
            text-transform: uppercase;
            font-family: 'Poppins', sans-serif;
        }
        .cafe-hero .gold-line {
            width: 140px;
            height: 4px;
            background: #d4af37;
            margin: 18px auto 0;
            border-radius: 4px;
        }

        .cafe-title {
            font-family: 'Playfair Display', serif;
            font-size: 3.2rem;
            color: #f5f1ea;
            text-align: center;
            margin-bottom: 35px;
            font-weight: 700;
        }
        .cafe-title span {
            color: #d4af37;
            font-style: italic;
        }
        .cafe-title::after {
            content: "";
            display: block;
            width: 100px;
            height: 4px;
            background: #d4af37;
            margin: 15px auto;
            border-radius: 4px;
        }

        .cafe-category-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            color: #d4af37;
            margin: 45px 0 25px;
            padding-bottom: 12px;
            border-bottom: 3px solid rgba(212, 175, 55, 0.3);
            display: flex;
            align-items: center;
            gap: 14px;
            font-weight: 700;
        }
        .cafe-category-title .icon {
            font-size: 2.2rem;
        }

        .cafe-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
            gap: 28px;
        }
        .cafe-card {
            background: rgba(255, 255, 255, 0.04);
            border: 1px solid rgba(212, 175, 55, 0.2);
            border-radius: 18px;
            padding: 28px 22px;
            text-align: center;
            transition: all 0.3s ease;
            backdrop-filter: blur(4px);
        }
        .cafe-card:hover {
            transform: translateY(-10px);
            border-color: #d4af37;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
            background: rgba(255, 255, 255, 0.08);
        }
        .cafe-card .emoji {
            font-size: 3.2rem;
            margin-bottom: 12px;
            display: block;
        }
        .cafe-card h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            color: #f5f1ea;
            margin-bottom: 8px;
            font-weight: 700;
        }
        .cafe-card p {
            font-size: 1rem;
            color: #d4c5b5;
            line-height: 1.5;
            margin-bottom: 0;
            font-weight: 400;
        }
        .cafe-card.special {
            border-color: #d4af37;
            background: linear-gradient(135deg, rgba(212, 175, 55, 0.12), rgba(43, 27, 20, 0.8));
        }
        .cafe-card.special h4 {
            color: #d4af37;
        }
        .cafe-card.special .badge {
            background: #d4af37;
            color: #2b1b14;
            font-size: 0.75rem;
            font-weight: 700;
            padding: 4px 16px;
            border-radius: 14px;
            display: inline-block;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .cafe-order-btn {
            display: inline-block;
            background: #d4af37;
            color: #2b1b14;
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            font-size: 1.4rem;
            padding: 18px 55px;
            border-radius: 50px;
            text-decoration: none;
            transition: all 0.3s ease;
            border: 2px solid #d4af37;
            margin-top: 25px;
            letter-spacing: 2px;
        }
        .cafe-order-btn:hover {
            background: transparent;
            color: #d4af37;
            box-shadow: 0 0 35px rgba(212, 175, 55, 0.3);
            transform: scale(1.04);
        }

        .cafe-footer-note {
            text-align: center;
            margin-top: 55px;
            padding-top: 35px;
            border-top: 1px solid rgba(212, 175, 55, 0.2);
            font-size: 1.05rem;
            color: #d4c5b5;
            letter-spacing: 2px;
            font-weight: 500;
        }
        .cafe-footer-note strong {
            color: #d4af37;
            font-family: 'Playfair Display', serif;
            font-size: 1.2rem;
        }

        /* ── Fixtures Table ── (unchanged) ── */
        .fixtures-section {
            max-width: 1000px;
            margin: 0 auto;
        }
        .fixtures-table-wrapper {
            background: #121836;
            border-radius: 20px;
            overflow: hidden;
            border: 1px solid rgba(255, 214, 0, 0.15);
            margin-bottom: 28px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }
        .fixtures-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 1.05rem;
        }
        .fixtures-table thead {
            background: #1A237E;
            border-bottom: 3px solid #FFD600;
        }
        .fixtures-table thead th {
            padding: 16px 22px;
            text-align: left;
            color: #FFD600;
            font-family: 'Poppins', sans-serif;
            font-size: 1.2rem;
            font-weight: 700;
            letter-spacing: 1px;
        }
        .fixtures-table thead th:first-child {
            width: 60px;
            text-align: center;
        }
        .fixtures-table tbody tr {
            border-bottom: 1px solid rgba(255, 255, 255, 0.06);
            transition: background 0.3s;
        }
        .fixtures-table tbody tr:hover {
            background: rgba(26, 35, 126, 0.3);
        }
        .fixtures-table tbody tr:last-child {
            border-bottom: none;
        }
        .fixtures-table tbody td {
            padding: 14px 22px;
            color: #e0e0e0;
            font-weight: 500;
        }
        .fixtures-table tbody td:first-child {
            font-weight: 700;
            color: #FFD600;
            text-align: center;
        }
        .fixtures-table .category-badge {
            display: inline-block;
            background: rgba(255, 214, 0, 0.12);
            color: #FFD600;
            padding: 4px 16px;
            border-radius: 14px;
            font-size: 0.85rem;
            font-weight: 700;
            border: 1px solid rgba(255, 214, 0, 0.2);
        }

        /* ── Registration Form ── (unchanged) ── */
        .registration-form {
            max-width: 600px;
            margin: 0 auto;
            background: #121836;
            padding: 35px;
            border-radius: 24px;
            border: 1px solid rgba(255, 214, 0, 0.15);
            box-shadow: 0 4px 30px rgba(0, 0, 0, 0.2);
        }
        .registration-form label {
            display: block;
            font-weight: 700;
            margin-top: 16px;
            color: #ccc;
            font-size: 1rem;
        }
        .registration-form label:first-of-type {
            margin-top: 0;
        }
        .registration-form input,
        .registration-form select {
            width: 100%;
            padding: 14px 18px;
            margin-top: 6px;
            background: #1e2245;
            border: 2px solid #2a3480;
            border-radius: 30px;
            color: white;
            font-size: 1rem;
            font-weight: 500;
            transition: border-color 0.3s ease;
        }
        .registration-form input:focus-visible,
        .registration-form select:focus-visible {
            outline: none;
            border-color: #FFD600;
        }
        .registration-form .btn {
            width: 100%;
            margin-top: 25px;
        }

        /* ── Toast ── */
        .toast {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #FFD600;
            color: #1A237E;
            padding: 18px 30px;
            border-radius: 30px;
            font-weight: 800;
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.7);
            z-index: 999;
            display: none;
            max-width: 450px;
            animation: slideUp 0.5s ease-out;
            font-size: 1.05rem;
        }
        .toast.show {
            display: block;
        }
        .toast .toast-close {
            background: none;
            border: none;
            color: #1A237E;
            font-size: 1.4rem;
            font-weight: bold;
            margin-left: 15px;
            cursor: pointer;
            padding: 0 6px;
        }
        @keyframes slideUp {
            0% {
                opacity: 0;
                transform: translateY(40px);
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ── Responsive ── */
        @media (max-width: 992px) {
            .partner-grid {
                grid-template-columns: 1fr 1fr;
                gap: 15px;
            }
        }
        @media (max-width: 768px) {
            .rori-profile h1 {
                font-size: 2.8rem;
            }
            .rori-logo {
                width: 150px;
                height: 150px;
            }
            .rori-profile p {
                font-size: 1.1rem;
                letter-spacing: 3px;
            }
            .nav-links {
                gap: 10px;
                justify-content: center;
            }
            .nav-links a {
                font-size: 0.8rem;
            }
            nav {
                padding: 10px 16px;
                justify-content: center;
            }
            .nav-logo img {
                height: 40px;
                width: 40px;
            }
            .stats-bar {
                gap: 16px;
            }
            .stat-item {
                padding: 12px 20px;
            }
            .stat-number {
                font-size: 2.2rem;
            }
            .regulations-grid {
                grid-template-columns: 1fr;
                gap: 25px;
            }
            .motto-banner .motto-text {
                font-size: 1.8rem;
            }
            .about-profile {
                padding: 25px 20px;
                font-size: 1.05rem;
            }
            .bank-details .account-number {
                font-size: 1.6rem;
            }
            .fund-description {
                padding: 25px 20px;
                font-size: 1rem;
            }
            .fund-benefits {
                grid-template-columns: 1fr 1fr;
                gap: 12px;
            }
            .contributions-table-wrapper {
                overflow-x: auto;
            }
            .contributions-table {
                font-size: 0.9rem;
                min-width: 500px;
            }
            .contributions-table thead th,
            .contributions-table tbody td {
                padding: 10px 14px;
            }
            .contributions-table .highlight-row td {
                font-size: 1rem;
            }
            .welcome-content {
                padding: 25px 20px;
            }
            .welcome-content p {
                font-size: 1.05rem;
            }
            .welcome-content .closing .amharic {
                font-size: 1.2rem;
            }
            .cafe-hero h2 {
                font-size: 3rem;
            }
            .cafe-hero p {
                font-size: 1rem;
                letter-spacing: 2px;
            }
            .cafe-title {
                font-size: 2.2rem;
            }
            .cafe-category-title {
                font-size: 1.6rem;
            }
            .cafe-grid {
                grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
                gap: 16px;
            }
            .cafe-hero::after {
                width: 70px;
                height: 70px;
                font-size: 2.8rem;
                bottom: -30px;
            }
            .partner-grid {
                grid-template-columns: 1fr 1fr;
                gap: 12px;
            }
            .partner-card .variant-text {
                font-size: 1rem;
            }
            .fixtures-table-wrapper {
                overflow-x: auto;
            }
            .fixtures-table {
                font-size: 0.9rem;
                min-width: 500px;
            }
            .fixtures-table thead th,
            .fixtures-table tbody td {
                padding: 10px 14px;
            }
            .section-title {
                font-size: 2.2rem;
            }
            .hero {
                min-height: 60vh;
                padding: 40px 16px 30px;
            }
            .btn {
                font-size: 1rem;
                padding: 14px 28px;
            }
            section {
                padding: 50px 16px;
            }
            .anthem-container {
                padding: 30px 25px;
            }
            .anthem-content p {
                font-size: 1rem;
            }
            .anthem-content .outro p {
                font-size: 1.1rem;
            }
            .gallery-grid {
                gap: 20px;
            }
            .gallery-card {
                width: 280px;
            }
            .gallery-img {
                height: 220px;
            }
            .gallery-title {
                font-size: 2.2rem;
            }
            .gallery-subtitle {
                font-size: 1rem;
            }
            .coach-img-wrapper {
                height: 300px;
            }
            .coach-card {
                max-width: 350px;
            }
        }
        @media (max-width: 480px) {
            .rori-profile h1 {
                font-size: 2.2rem;
            }
            .rori-logo {
                width: 120px;
                height: 120px;
            }
            .rori-profile p {
                font-size: 0.9rem;
                letter-spacing: 2px;
            }
            .btn {
                font-size: 0.95rem;
                padding: 12px 24px;
            }
            .section-title {
                font-size: 1.8rem;
            }
            .nav-links a {
                font-size: 0.7rem;
            }
            .motto-banner .motto-text {
                font-size: 1.4rem;
            }
            .motto-banner {
                padding: 25px 18px;
            }
            .fund-benefits {
                grid-template-columns: 1fr;
                gap: 12px;
            }
            .bank-details .account-number {
                font-size: 1.2rem;
            }
            .bank-details {
                padding: 20px 16px;
            }
            .bank-details .telebirr {
                font-size: 1.3rem;
            }
            .welcome-content::before {
                font-size: 3.5rem;
                left: 12px;
            }
            .cafe-hero h2 {
                font-size: 2.2rem;
            }
            .cafe-grid {
                grid-template-columns: 1fr 1fr;
                gap: 12px;
            }
            .cafe-card .emoji {
                font-size: 2.2rem;
            }
            .cafe-card h4 {
                font-size: 1rem;
            }
            .cafe-card p {
                font-size: 0.85rem;
            }
            .cafe-order-btn {
                font-size: 1rem;
                padding: 14px 30px;
            }
            .partner-grid {
                grid-template-columns: 1fr 1fr;
                gap: 10px;
            }
            .partner-card {
                padding: 14px 10px;
            }
            .partner-card .variant-text {
                font-size: 0.85rem;
            }
            .partner-card .variant-tag {
                font-size: 0.5rem;
            }
            .hero {
                min-height: 50vh;
                padding: 30px 12px 25px;
            }
            .stat-number {
                font-size: 1.8rem;
            }
            .stat-item {
                padding: 10px 16px;
            }
            .stats-bar {
                gap: 10px;
            }
            section {
                padding: 40px 12px;
            }
            .card-grid {
                grid-template-columns: 1fr 1fr;
                gap: 14px;
            }
            .card {
                padding: 18px 14px;
            }
            .card h3 {
                font-size: 1.4rem;
                margin: 12px 0 8px;
            }
            .card p {
                font-size: 0.95rem;
            }
            .squad-grid {
                grid-template-columns: repeat(auto-fill, minmax(110px, 1fr));
                gap: 12px;
            }
            .player-card {
                padding: 12px 8px;
            }
            .jersey-number {
                font-size: 1.6rem;
            }
            .player-card div:last-child {
                font-size: 0.9rem;
            }
            .chat-container {
                padding: 16px;
            }
            .chat-container h3 {
                font-size: 1.2rem;
            }
            .chat-input-area input {
                padding: 10px 16px;
                font-size: 0.9rem;
            }
            .chat-input-area button {
                padding: 0 18px;
                font-size: 0.9rem;
            }
            .registration-form {
                padding: 20px;
            }
            .registration-form input {
                padding: 12px 16px;
                font-size: 0.9rem;
            }
            .contributions-table {
                font-size: 0.8rem;
                min-width: 400px;
            }
            .contributions-table thead th,
            .contributions-table tbody td {
                padding: 8px 12px;
            }
            .contributions-table .highlight-row td {
                font-size: 0.9rem;
                padding: 12px 12px;
            }
            .contributions-thanks {
                padding: 20px 18px;
                font-size: 1rem;
            }
            .fixtures-table {
                font-size: 0.8rem;
                min-width: 400px;
            }
            .fixtures-table thead th,
            .fixtures-table tbody td {
                padding: 8px 12px;
            }
            .about-profile {
                padding: 20px 16px;
                font-size: 1rem;
            }
            .about-profile .motto-highlight {
                font-size: 1.1rem;
            }
            .fund-description {
                padding: 20px 16px;
                font-size: 0.95rem;
            }
            .welcome-content {
                padding: 20px 16px;
            }
            .welcome-content p {
                font-size: 0.95rem;
            }
            .welcome-content .greeting-highlight {
                font-size: 1.1rem;
            }
            .welcome-content .closing {
                font-size: 1.1rem;
            }
            .welcome-content .closing .amharic {
                font-size: 1.1rem;
            }
            .cafe-hero {
                padding: 60px 16px 50px;
            }
            .cafe-hero::after {
                width: 60px;
                height: 60px;
                font-size: 2.2rem;
                bottom: -25px;
            }
            .cafe-category-title {
                font-size: 1.3rem;
                margin: 30px 0 16px;
            }
            .cafe-category-title .icon {
                font-size: 1.6rem;
            }
            .cafe-title {
                font-size: 1.8rem;
            }
            .toast {
                left: 16px;
                right: 16px;
                bottom: 16px;
                max-width: none;
                font-size: 0.95rem;
                padding: 14px 20px;
            }
            footer {
                font-size: 0.9rem;
                padding: 25px 16px;
            }
            .anthem-container {
                padding: 25px 18px;
            }
            .anthem-content p {
                font-size: 0.95rem;
            }
            .anthem-content .outro p {
                font-size: 1rem;
            }
            .anthem-container::before {
                font-size: 6rem;
                right: -10px;
                bottom: -20px;
            }
            .gallery-grid {
                gap: 16px;
            }
            .gallery-card {
                width: 100%;
                max-width: 340px;
            }
            .gallery-img {
                height: 200px;
            }
            .gallery-title {
                font-size: 1.8rem;
            }
            .img-caption {
                font-size: 1rem;
                padding: 14px 16px 16px;
            }
            .coach-img-wrapper {
                height: 250px;
            }
            .coach-card {
                max-width: 100%;
                margin: 20px 10px;
            }
            .coach-details h3 {
                font-size: 1.8rem;
            }
            .coach-details .role {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>

    <!-- ─── Navigation ─── -->
    <nav aria-label="Main navigation">
        <div class="nav-logo">
            <img id="navLogo" src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='48' fill='%230d1137' stroke='%23FFD600' stroke-width='4'/%3E%3Ctext x='50' y='52' font-family='Bebas Neue, cursive' font-size='22' fill='%23FFD600' text-anchor='middle' dominant-baseline='central'%3ERFC%3C/text%3E%3C/svg%3E" alt="Rori Community FC Logo" />
        </div>
        <div class="nav-links">
            <a href="#home">Home</a>
            <a href="#welcome">Welcome</a>
            <a href="#about">About</a>
            <a href="#team">Team</a>
            <a href="#coach">Coach</a>
            <a href="#health">Health</a>
            <a href="#gym">Gym</a>
            <a href="#fund">Fund</a>
            <a href="#contributions">Contributions</a>
            <a href="#regulations">Regulations</a>
            <a href="#anthem">Anthem</a>
            <a href="#fixtures">Fixtures</a>
            <a href="#cafe">Café</a>
            <a href="#news">News</a>
            <a href="#gallery">Gallery</a>
            <a href="#register">Register</a>
            <a href="#contact">Contact</a>
        </div>
    </nav>

    <!-- ─── Hero ─── -->
    <section class="hero" id="home">
        <div class="rori-profile">
            <img
                src="rori-fc-logo.png"
                alt="RORI Community FC Logo"
                class="rori-logo"
            />
            <h1>RORI COMMUNITY FC</h1>
            <p>HAWASSA • UNITY • HEALTH • COMMUNITY</p>
        </div>

        <div class="stats-bar">
            <div class="stat-item"><span class="stat-number">47</span><br /><span class="stat-label">Members</span></div>
            <div class="stat-item"><span class="stat-number">2</span><br /><span class="stat-label">Training Days</span></div>
            <div class="stat-item"><span class="stat-number">2024</span><br /><span class="stat-label">Est.</span></div>
        </div>
        <div class="cta-buttons">
            <a href="#register" class="btn">Join Us</a>
            <a href="#contact" class="btn btn-outline">Contact</a>
        </div>
    </section>

    <!-- ─── Welcome Section ─── -->
    <section class="welcome-section" id="welcome">
        <div class="welcome-container">
            <h2 class="section-title">Welcome | ዳኤ ቡሹ <span style="font-size:1.8rem; color:#fff;">(Da’e Bushu)</span></h2>
            <div class="welcome-content">
                <p>Welcome to Rori Community FC &amp; Rori Health Team official website.</p>
                <p><span class="greeting-highlight">ዳኤ ቡሹ (Da’e Bushu)</span> is a traditional Sidama greeting that means "Welcome" and carries a deep sense of respect, warmth, and unity within the community.</p>
                <p>We are proud to share this space with our players, staff, and supporters who are building a strong culture of football, health, discipline, and teamwork in Hawassa.</p>
                <p>At Rori Community FC, we believe in more than just football. We believe in growth, wellness, and community spirit. This platform brings together our club updates, health programs, training schedules, and development projects.</p>
                <p>Step inside, explore, and be part of our journey.</p>
                <div class="closing">
                    <span class="greeting-highlight">ዳኤ ቡሹ</span> — ለቤታችን እንኳን ደህና መጡ!
                    <span class="amharic">(Welcome to our home!)</span>
                </div>
            </div>
        </div>
    </section>

    <!-- ─── About ─── -->
    <section id="about">
        <h2 class="section-title">ስለ ሮሪ ኤፍሲ</h2>
        <div class="about-profile">
            <p>ሮሪ ሆቴል ኤፍሲ በሀዋሳ ከተማ መሀል የሚገኝ ሲሆን፣ ሙያዊ እግር ኳስን ከማህበረሰብ ተሳትፎ እና ከጤና ጋር የሚያገናኝ ቡድን ነው። እ.ኤ.አ. በ2024 የተመሠረተው ክለባችን ወጣቶችን ችሎታ ማጎልበት፣ ጤናማ የአኗኗር ልምድ ማስፋፋት እና በክብር ለመወዳደር ቁርጠኛ ነው።</p>
            <span class="motto-highlight">"ተሰጥኦን እናበቃለን፤ ሻምፒዮኖችን እንፈጥራለን!"</span>
            <p style="margin-top:15px; font-size:1rem; color:#ccc; font-weight:500;">በቡድን መንፈስ፣ በትጋት እና በተግሣጽ የተገነባው ሮሪ ሆቴል ኤፍሲ፣ ለአትሌቶች እንዲሁም ለደጋፊዎች ሁለተኛ ቤት መሆንን ያለም ያምናል።</p>
        </div>
        <div class="card-grid">
            <div class="card"><h3>👁️ Vision</h3><p>To be a leading community football club in Ethiopia, inspiring through sport and wellness.</p></div>
            <div class="card"><h3>🎯 Mission</h3><p>Develop talent, promote healthy lifestyle, and compete with honor in regional leagues.</p></div>
            <div class="card"><h3>💎 Values</h3><p>Discipline, Respect, Teamwork, and continuous improvement — on and off the pitch.</p></div>
            <div class="card"><h3>⚕️ Health Philosophy</h3><p>Every player follows a holistic wellness program: fitness, nutrition, mental health, and recovery.</p></div>
        </div>
    </section>

    <!-- ─── Team ─── -->
    <section id="team">
        <h2 class="section-title">Members &amp; Staff</h2>
        <h3 style="color:#FFD600; text-align:center; margin-bottom:25px; font-size:1.8rem; font-weight:800;">Full Roster (47 Members)</h3>
        <div class="squad-grid" id="squadContainer"></div>
        <h3 style="color:#FFD600; text-align:center; margin:45px 0 25px; font-size:1.8rem; font-weight:800;">Coaching &amp; Management</h3>
        <div class="card-grid">
            <div class="card"><h3>🧢 Head Coach</h3><p><strong>Nebiyu Yonas</strong></p></div>
            <div class="card"><h3>🩺 Team Doctor</h3><p><strong>Dr. Yonas Tadesse</strong></p></div>
            <div class="card"><h3>💪 S&amp;C Coach</h3><p><strong>Coach Yedidiya</strong></p></div>
        </div>
    </section>

    <!-- ─── Head Coach Section ─── -->
    <section class="coach-section" id="coach">
        <div class="container">
            <h2 class="section-title">👨‍🏫 Head Coach</h2>
            <div class="coach-card">
                <div class="coach-img-wrapper">
                    <!-- 
                        ⚠️ REPLACE THE `src` BELOW WITH YOUR COACH'S PHOTO.
                        Place the image in an `images` folder or use a full URL.
                        Suggested: images/nebiyu-yonas.jpg
                    -->
                    <img class="coach-img" src="https://images.unsplash.com/photo-1574629810360-7efbbe195018?w=800&h=1000&fit=crop&crop=center&q=80" alt="Nebiyu Yonas - Head Coach">
                    <span class="badge-tag">Head Coach</span>
                </div>
                <div class="coach-details">
                    <h3>Nebiyu Yonas</h3>
                    <p class="role">⚽ Head Coach • RORI Community FC</p>
                    <p class="bio">
                        Nebiyu Yonas is a passionate and experienced football coach dedicated to developing young talent. 
                        With a strong emphasis on discipline, teamwork, and tactical awareness, he leads RORI Community FC 
                        with a vision of building a competitive and united team that represents the spirit of Hawassa.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- ─── Health ─── -->
    <section id="health">
        <h2 class="section-title">Health &amp; Wellness</h2>
        <div class="card-grid">
            <div class="card"><h3>🏋️ Fitness</h3><p>Strength &amp; conditioning sessions twice a week.</p></div>
            <div class="card"><h3>🥗 Nutrition</h3><p>Personalized meal plans for peak performance.</p></div>
            <div class="card"><h3>🧘 Physiotherapy</h3><p>Injury prevention and recovery routines.</p></div>
            <div class="card"><h3>🧠 Mental Health</h3><p>Mindfulness and resilience workshops.</p></div>
            <div class="card"><h3>🩺 Medical</h3><p>Regular check-ups and first-aid support.</p></div>
            <div class="card"><h3>😴 Sleep</h3><p>Sleep hygiene education for optimal recovery.</p></div>
        </div>
    </section>

    <!-- ─── Gym ─── -->
    <section id="gym">
        <h2 class="section-title">የጂም አባላት ጥሪ</h2>
        <div style="max-width:900px; margin:0 auto 35px; text-align:center; font-size:1.2rem; font-weight:500;">
            <p>ሮሪ ጤና ቡድን አዳዲስ የጂም አባላትን በደስታ ይቀበላል!</p>
            <p style="margin-top:8px;">ጤናማ አኗኗር የሚወዱ፣ የአካል ብቃታቸውን ማሻሻል የሚፈልጉ እና ከቡድን ጋር በትብብር ለመስራት ፈቃደኛ የሆኑ ሁሉ እንዲቀላቀሉን እንጋብዛለን።</p>
        </div>
        <div style="display:grid; grid-template-columns: 1fr 1fr; gap:30px; max-width:1000px; margin:0 auto;">
            <div class="card" style="text-align:left;">
                <h3 style="text-align:center; font-size:1.8rem;">መስፈርቶች</h3>
                <ul><li>ለጤና እና ለስፖርት ፍላጎት ያለው</li><li>የቡድን መንፈስ ያለው</li><li>ስልጠናን በመደበኛነት ለመከታተል ፈቃደኛ</li><li>የሮሪ ሆቴል ሰራተኛ ወይም በቡድኑ የሚፈቀድ አባል</li></ul>
            </div>
            <div class="card" style="text-align:left;">
                <h3 style="text-align:center; font-size:1.8rem;">የምዝገባ ጥቅሞች</h3>
                <ul><li>የመደበኛ የጂም ስልጠና</li><li>የጤና እና የአካል ብቃት ምክር</li><li>የስፖርት እና የጤና ፕሮግራሞች</li><li>ከአባላት ጋር የትብብር እና የወዳጅነት አካባቢ</li></ul>
            </div>
        </div>
        <div style="text-align:center; margin-top:35px; font-size:1.6rem; font-weight:900; color:#FFD600; letter-spacing:2px;">"ጤናማ ሰው፣ ጠንካራ ቡድን፣ የተሻለ ውጤት!"</div>
    </section>

    <!-- ─── Fund ─── -->
    <section id="fund">
        <h2 class="section-title">⚽ Support RORI FC</h2>
        <div class="fund-section">
            <div class="fund-description">
                <p>Rori Health Team is a community-based initiative established in Hawassa, Ethiopia, working to improve the health, fitness, and overall wellbeing of young athletes and staff members connected to Rori Community Football Club.</p>
                <p>The program was formed through the collaboration of the club's leadership, coaching staff, gym members, and employees, with a shared vision of building a stronger, healthier, and more disciplined sports community.</p>
                <p>Our goal is simple: to support players and members with proper training equipment, fitness development programs, medical support, nutrition guidance, and structured wellness activities. We believe that strong health builds strong performance, both on and off the field.</p>
            </div>
            <h3 style="color:#FFD600; text-align:center; font-size:2rem; font-weight:800; margin-bottom:20px;">Through this fundraiser, we aim to raise funds to support:</h3>
            <div class="fund-benefits">
                <div class="benefit-item"><span class="icon">🏋️</span> Sports &amp; gym equipment for training</div>
                <div class="benefit-item"><span class="icon">🩺</span> Health &amp; medical support for players</div>
                <div class="benefit-item"><span class="icon">🥗</span> Nutrition &amp; wellness programs</div>
                <div class="benefit-item"><span class="icon">🏆</span> Team development &amp; local competitions</div>
                <div class="benefit-item"><span class="icon">⚽</span> Youth football growth &amp; community engagement</div>
            </div>
            <div class="fund-description" style="border:2px solid #FFD600;">
                <p><em>Every contribution will directly help improve the quality of training and create better opportunities for young players who are committed to developing their talent and discipline.</em></p>
                <p style="font-weight:800; color:#FFD600; font-size:1.2rem; margin-top:12px;">This is more than just a football project. It is a movement to build healthier lives, stronger teamwork, and a brighter future for our community.</p>
                <p style="margin-top:12px; font-weight:600;">Thank you for your support and belief in our vision.</p>
            </div>
            <div class="bank-details">
                <div class="bank-label">🏦 Bank Account</div>
                <div class="account-number" id="accountNumber">1000775018627</div>
                <button class="copy-btn" onclick="copyAccount()">📋 Copy Account Number</button>
                <div class="account-name">👤 Account Name: <strong>RORI FC</strong></div>
                <div class="telebirr">📱 Telebirr: 0926523487</div>
                <p style="font-size:1rem; color:#aaa; margin-top:14px; font-weight:500;">🙏 Your support helps RORI FC grow and develop the community through football. ❤️⚽</p>
            </div>
        </div>
    </section>

    <!-- ─── Contributions ─── -->
    <section id="contributions">
        <h2 class="section-title">የቡድኑ አባላት የድጋፍ አስተዋጽኦ ዝርዝር</h2>
        <div class="contributions-section">
            <p class="contributions-intro">እስከአሁን ድረስ ለሮሪ ጤና ቡድን እና ለክለቡ ልማት በብር የተደረገ ድጋፍ ዝርዝር፦</p>
            <div class="contributions-table-wrapper">
                <table class="contributions-table">
                    <thead><tr><th>#</th><th>ስም</th><th>የብር መጠን</th></tr></thead>
                    <tbody>
                        <tr><td>1</td><td>በሀይሉ ቦጃ</td><td>1,000 ብር</td></tr>
                        <tr><td>2</td><td>ዳዊት ሰለሞን</td><td>5,000 ብር</td></tr>
                        <tr><td>3</td><td>ተስፋሁን ነከረ</td><td>1,000 ብር</td></tr>
                        <tr><td>4</td><td>አበባየሁ ክፍሌ</td><td>1,000 ብር</td></tr>
                        <tr><td>5</td><td>ኦርዮን ሰለሞን</td><td>2,000 ብር</td></tr>
                        <tr><td>6</td><td>አብዮት</td><td>1,000 ብር</td></tr>
                        <tr><td>7</td><td>አበበ ተሾመ</td><td>1,000 ብር</td></tr>
                        <tr><td>8</td><td>ፍላጎት አሰሙ</td><td>1,000 ብር</td></tr>
                        <tr><td>9</td><td>ታረቀኝ ህፋሞ</td><td>2,000 ብር</td></tr>
                        <tr><td>10</td><td>ሙሉቀን ጋደፈው</td><td>5,000 ብር</td></tr>
                        <tr><td>11</td><td>አሸነፈ ደምሴ</td><td>3,000 ብር</td></tr>
                        <tr><td>12</td><td>መስፍን ራሪቲ</td><td>2,100 ብር</td></tr>
                        <tr class="highlight-row"><td colspan="2"><strong>አጠቃላይ አስተዋጽኦ</strong></td><td><strong>25,100 ብር</strong></td></tr>
                    </tbody>
                </table>
            </div>
            <div class="contributions-thanks">
                <span class="thanks-icon">🙏</span>
                <p><strong>ምስጋና</strong></p>
                <p>ለሁሉም የቡድኑ አባላት ለሰጡት ድጋፍ ከልብ እናመሰግናለን። ይህ አስተዋጽኦ ለቡድኑ እድገት፣ ለስልጠና መሻሻል እና ለወጣቶች የተሻለ የስፖርት እድል ለመፍጠር ትልቅ አስተዋጽኦ ነው።</p>
            </div>
        </div>
    </section>

    <!-- ─── Regulations ─── -->
    <section id="regulations">
        <h2 class="section-title">የክለቡ ደንቦች</h2>
        <div class="regulations-grid">
            <div class="card">
                <h3>📋 ደንቦች</h3>
                <ul>
                    <li>ሁሉም ተጫዋቾች በሰዓታቸው ለልምምድ መገኘት አለባቸው።</li>
                    <li>የአሰልጣኞችን መመሪያ ማክበር ግዴታ ነው።</li>
                    <li>ተጫዋቾች ለቡድን አባላት፣ አሰልጣኞች እና ተቀናቃኞች ክብር ማሳየት አለባቸው።</li>
                    <li>ማንኛውም ዓይነት ጸብ፣ ስድብ ወይም አድሎ አይፈቀድም።</li>
                    <li>የክለቡን ንብረት በኃላፊነት መጠቀም አለባቸው።</li>
                    <li>ተጫዋቾች የስፖርት ልብሳቸውን በሚገባ መጠቀም አለባቸው።</li>
                    <li>ከክለቡ ስም እና ክብር ጋር የሚጋጩ ተግባራት አይፈቀዱም።</li>
                </ul>
            </div>
            <div class="card">
                <h3>⭐ የተጫዋቾች ሥነ-ምግባር</h3>
                <ul>
                    <li>ታማኝ መሆን</li>
                    <li>ትጉህ መሆን</li>
                    <li>የቡድን መንፈስ ማሳየት</li>
                    <li>ጤናማ አኗኗር መከተል</li>
                    <li>ለክለቡ ጥሩ አምባሳደር መሆን</li>
                </ul>
            </div>
        </div>
        <div class="motto-banner">
            <div class="motto-text">"ተሰጥኦን እናበቃለን፤ ሻምፒዮኖችን እንፈጥራለን!"</div>
            <div class="motto-sub">⚽🏆 ሮሪ ሆቴል ኤፍሲ – ሻምፒዮናችን እንገነባለን!</div>
        </div>
    </section>

    <!-- ─── Anthem Section ─── -->
    <section id="anthem">
        <h2 class="section-title">🎵 Club Anthem</h2>
        <div class="anthem-container">
            <div class="anthem-content">
                <h3 style="color: #FFD600; font-size: 2.2rem; text-align: center; margin-bottom: 4px; font-weight: 900; letter-spacing: 2px;">RORI Forever</h3>
                <p class="anthem-title-sub">(Rori Community FC Anthem)</p>

                <div class="verse">
                    <p><strong>Verse 1</strong></p>
                    <p>As I walk down the Hawassa road,<br>
                    A stone's throw from the pitch,<br>
                    I see the spirit of the pride,<br>
                    That never loses its itch.<br>
                    Through the gates of our home ground,<br>
                    I hear the fans all cheer,<br>
                    I see the faces of the boys,<br>
                    As the kick-off time is near.</p>
                </div>

                <div class="verse">
                    <p><strong>Verse 2</strong></p>
                    <p>And the roar of the Rori stands,<br>
                    Where we gather side by side,<br>
                    We're shouting out our name,<br>
                    We're shouting out our name!</p>
                </div>

                <div class="chorus">
                    <p><strong>Chorus</strong></p>
                    <p>RORI forever,<br>
                    Whatever the weather,<br>
                    These streets are our own,<br>
                    And my heart will leave here never.<br>
                    My blood runs the colors,<br>
                    Of the gold and the blue,<br>
                    And the lion on my chest,<br>
                    Is the badge that is true.<br>
                    RORI forever,<br>
                    RORI forever!</p>
                </div>

                <div class="verse">
                    <p><strong>Verse 3</strong></p>
                    <p>And the gym on the corner,<br>
                    Is packed to the brim,<br>
                    With the Rori community,<br>
                    Working hard, looking trim.<br>
                    With the young ones making promises,<br>
                    They know they'll always keep.</p>
                </div>

                <div class="chorus">
                    <p><strong>Chorus</strong></p>
                    <p>RORI forever,<br>
                    Whatever the weather,<br>
                    These streets are our own,<br>
                    And my heart will leave here never.<br>
                    My blood runs the colors,<br>
                    Of the gold and the blue,<br>
                    And the lion on my chest,<br>
                    Is the badge that is true.<br>
                    RORI forever,<br>
                    RORI forever!</p>
                </div>

                <div class="outro">
                    <p><strong>Outro</strong></p>
                    <p>RORI forever,<br>
                    RORI forever!</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ─── Fixtures / Match Schedule ─── -->
    <section id="fixtures">
        <h2 class="section-title">⚽ Match Schedule / Fixtures</h2>
        <div class="fixtures-section">
            <div class="fixtures-table-wrapper">
                <table class="fixtures-table">
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>Home Team</th>
                            <th>Away Team</th>
                            <th>Match Category</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>RORI FC</td>
                            <td>Haile Resort Hotel FC</td>
                            <td><span class="category-badge">Hawassa Hotel Derby</span></td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>RORI FC</td>
                            <td>Ker Awud International Hotel FC</td>
                            <td><span class="category-badge">Hawassa Hotel Derby</span></td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>RORI FC</td>
                            <td>Ethiopian Skylight Hotel FC</td>
                            <td><span class="category-badge">National Hospitality Cup</span></td>
                        </tr>
                        <tr>
                            <td>4</td>
                            <td>RORI FC</td>
                            <td>Hilton Hotel FC</td>
                            <td><span class="category-badge">National Hospitality Cup</span></td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td>RORI FC</td>
                            <td>Sheraton Addis Hotel FC</td>
                            <td><span class="category-badge">National Hospitality Cup</span></td>
                        </tr>
                    </tbody>
                </table>
            </div>
            <p style="text-align:center; color:#aaa; font-size:1.05rem; font-weight:500;">Upcoming matches – stay tuned for dates and venues.</p>
        </div>
    </section>

    <!-- ─── Café ─── -->
    <section class="cafe-section" id="cafe">
        <div class="container">
            <div class="partner-section">
                <div class="partner-label">Official Partner</div>
                <div class="partner-grid">
                    <div class="partner-card"><div class="variant-tag">Variant 1</div><div class="variant-text"><span class="icon">☕</span><br />Official Partner: <span class="gold">Silla Coffee</span> 🏨</div><div class="variant-divider"></div></div>
                    <div class="partner-card"><div class="variant-tag">Variant 2</div><div class="variant-text"><span class="icon">⚡</span><br />Powered by <span class="gold">Silla Coffee</span></div><div class="variant-divider"></div></div>
                    <div class="partner-card"><div class="variant-tag">Variant 3</div><div class="variant-text"><span class="icon">🔥</span><br />Fuel Partner: <span class="gold">Silla Coffee</span> ☕</div><div class="variant-divider"></div></div>
                    <div class="partner-card"><div class="variant-tag">Variant 4</div><div class="variant-text"><span class="gold">Silla Coffee</span><br /><span style="font-size:0.95rem; color:#d4c5b5;">— Official Club Supporter</span></div><div class="variant-divider"></div></div>
                </div>
            </div>
            <div class="cafe-hero">
                <h2>Silla <span>Coffee</span> Shop</h2>
                <p>Inside Rori Hotel · Hawassa</p>
                <div class="gold-line"></div>
            </div>
            <h2 class="cafe-title">Our <span>Menu</span></h2>
            <h3 class="cafe-category-title"><span class="icon">☕</span> Hot Coffee</h3>
            <div class="cafe-grid">
                <div class="cafe-card"><span class="emoji">🇪🇹</span><h4>Ethiopian Bunna</h4><p>Traditional fresh coffee</p></div>
                <div class="cafe-card"><span class="emoji">🥛</span><h4>Macchiato</h4><p>Strong espresso with milk</p></div>
                <div class="cafe-card"><span class="emoji">⚡</span><h4>Espresso</h4><p>Pure strong coffee shot</p></div>
            </div>
            <h3 class="cafe-category-title"><span class="icon">🍃</span> Tea &amp; Drinks</h3>
            <div class="cafe-grid">
                <div class="cafe-card"><span class="emoji">🫖</span><h4>Black Tea</h4><p>Classic bold flavor</p></div>
                <div class="cafe-card"><span class="emoji">🥛</span><h4>Milk Tea</h4><p>Rich & creamy</p></div>
                <div class="cafe-card"><span class="emoji">🍋</span><h4>Lemon Tea</h4><p>Refreshing citrus blend</p></div>
            </div>
            <h3 class="cafe-category-title"><span class="icon">🍰</span> Snacks</h3>
            <div class="cafe-grid">
                <div class="cafe-card"><span class="emoji">🍞</span><h4>Fresh Bread</h4><p>Baked daily</p></div>
                <div class="cafe-card"><span class="emoji">🎂</span><h4>Cake Slice</h4><p>Homemade delight</p></div>
                <div class="cafe-card"><span class="emoji">🍳</span><h4>Light Breakfast Set</h4><p>Eggs, toast &amp; fruit</p></div>
            </div>
            <h3 class="cafe-category-title"><span class="icon">⚽</span> Special (Rori FC)</h3>
            <div class="cafe-grid">
                <div class="cafe-card special"><span class="badge">⚡ Match Day</span><span class="emoji">🔥</span><h4>Energy Coffee</h4><p>Before training boost</p></div>
                <div class="cafe-card special"><span class="badge">🛡️ Recovery</span><span class="emoji">💪</span><h4>Recovery Coffee</h4><p>After match relaxation</p></div>
                <div class="cafe-card special"><span class="badge">🏆 Captain's Pick</span><span class="emoji">☕</span><h4>Team Special Blend</h4><p>Honoring our champions</p></div>
            </div>
            <div style="text-align:center; margin-top:45px;">
                <a href="#contact" class="cafe-order-btn">📞 Order Now</a>
                <p style="color:#d4c5b5; margin-top:14px; font-size:0.95rem; font-weight:400;">Visit us inside Rori Hotel · Hawassa</p>
            </div>
            <div class="cafe-footer-note"><strong>☕ Silla Coffee Shop</strong> — A proud part of <strong>Rori Hotel</strong></div>
        </div>
    </section>

    <!-- ─── News ─── -->
    <section id="news">
        <h2 class="section-title">Club News &amp; AI Assistant</h2>
        <div class="card-grid">
            <div class="card"><h3>📰 New Training Kit</h3><p>2026 jerseys unveiled – navy &amp; gold stripes.</p></div>
            <div class="card"><h3>🏆 Friendly Match</h3><p>Rori FC vs Hawassa City – Saturday 3:00 PM.</p></div>
            <div class="card"><h3>🎓 Youth Trial</h3><p>Open trials for U-17 next month. Register below.</p></div>
        </div>
        <div class="chat-container">
            <h3 style="color:#FFD600; margin-bottom:12px;">🤖 Ask Rori FC Anything</h3>
            <div class="chat-messages" id="chatMessages" role="log" aria-live="polite">
                <p><strong>Bot:</strong> Hello! Ask me about training, squad, Telegram, or anything Rori FC.</p>
            </div>
            <div class="chat-input-area">
                <input type="text" id="userQuestion" placeholder="e.g., What is the training schedule?" aria-label="Ask a question" />
                <button onclick="sendMessage()">Send</button>
            </div>
        </div>
    </section>

    <!-- ════════════════════════════════════════════════════ -->
    <!-- ─── የተሻሻለ ጋለሪ ሴክሽን (Flexbox Layout) ─── -->
    <!-- ════════════════════════════════════════════════════ -->
    <section class="gallery-section" id="gallery">
        <div class="container">
            <h2 class="gallery-title">📸 Our Gallery</h2>
            <p class="gallery-subtitle">Moments captured from <span>RORI Community FC</span></p>

            <div class="gallery-grid">

                <!-- NEW: Fitness Zone / Rori Health Club -->
                <div class="gallery-card">
                    <img class="gallery-img" src="images/gym1.jpg" alt="Rori Hotel Fitness Center">
                    <div class="img-caption">
                        Fitness Zone
                        <small>Rori Health Club</small>
                    </div>
                </div>

                <!-- ካርድ 1 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1580587771525-78b9dba3b914?w=800&h=800&fit=crop&crop=center&q=80" alt="RORI HOTEL Logo">
                    <div class="img-caption">
                        🏨 RORI HOTEL
                        <small>Official Club Logo</small>
                    </div>
                </div>

                <!-- ካርድ 2 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1566073771259-6a8506099945?w=1200&h=800&fit=crop&crop=center&q=80" alt="RORI HOTEL Banner">
                    <div class="img-caption">
                        🏨 RORI HOTEL
                        <small>Premium Hotel Banner</small>
                    </div>
                </div>

                <!-- ካርድ 3 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1580582932707-520aed937b7b?w=800&h=800&fit=crop&crop=center&q=80" alt="Hawassa Sunshine School">
                    <div class="img-caption">
                        📍 Hawassa
                        <small>Sunshine School</small>
                    </div>
                </div>

                <!-- ካርድ 4 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1517466787929-bc90951d0974?w=800&h=800&fit=crop&crop=center&q=80" alt="Messi 4K Action">
                    <div class="img-caption">
                        🐐 Messi 4K
                        <small>#1 • Magic on the pitch</small>
                    </div>
                </div>

                <!-- ካርድ 5 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1522778119026-d647f0596c20?w=800&h=800&fit=crop&crop=center&q=80" alt="Messi 4K Celebration">
                    <div class="img-caption">
                        🐐 Messi 4K
                        <small>#2 • Celebration moment</small>
                    </div>
                </div>

                <!-- ካርድ 6 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1574629810360-7efbbe195018?w=800&h=800&fit=crop&crop=center&q=80" alt="Messi 4K Portrait">
                    <div class="img-caption">
                        🐐 Messi 4K
                        <small>#3 • Portrait of a legend</small>
                    </div>
                </div>

                <!-- ካርድ 7 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1459865264687-595d652de67e?w=800&h=800&fit=crop&crop=center&q=80" alt="CR7 4K Action">
                    <div class="img-caption">
                        🐐 CR7 4K
                        <small>#1 • Power and precision</small>
                    </div>
                </div>

                <!-- ካርድ 8 -->
                <div class="gallery-card">
                    <img class="gallery-img" src="https://images.unsplash.com/photo-1431324155629-1a6deb1dec8d?w=800&h=800&fit=crop&crop=center&q=80" alt="CR7 4K Celebration">
                    <div class="img-caption">
                        🐐 CR7 4K
                        <small>#2 • Siuuu! Celebration</small>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- ─── Registration ─── -->
    <section id="register">
        <h2 class="section-title">Player Registration</h2>
        <form class="registration-form" id="registrationForm" action="https://formspree.io/f/mdaredbw" method="POST">
            <label for="regName">Full Name *</label>
            <input type="text" id="regName" name="name" placeholder="Full Name" required />
            <label for="regAge">Age *</label>
            <input type="number" id="regAge" name="age" placeholder="Age" min="14" max="45" required />
            <label for="regPosition">Preferred Position *</label>
            <input type="text" id="regPosition" name="position" placeholder="e.g., Forward, Midfielder, Defender, Goalkeeper" required />
            <label for="regEmail">Email *</label>
            <input type="email" id="regEmail" name="email" placeholder="you@example.com" required />
            <label for="regPhone">Phone *</label>
            <input type="tel" id="regPhone" name="phone" placeholder="+251 9XXXXXXXX" required />
            <button type="submit" class="btn">Register</button>
            <p style="font-size:0.9rem; color:#aaa; margin-top:14px; text-align:center; font-weight:500;">* Required fields. Your data is sent securely.</p>
        </form>
        <div class="toast" id="welcomeToast" role="alert">
            <span id="toastMessage">🎉 Welcome! Registration received.</span>
            <button class="toast-close" onclick="closeToast()" aria-label="Close notification">&times;</button>
        </div>
    </section>

    <!-- ─── Contact ─── -->
    <section id="contact">
        <h2 class="section-title">Contact &amp; Training</h2>
        <div class="card-grid">
            <div class="card"><h3>📍 Location</h3><p>Rori Hotel, Hawassa, Ethiopia</p></div>
            <div class="card"><h3>📞 Phone</h3><p>+251 931444901</p></div>
            <div class="card"><h3>📧 Email</h3><p><a href="mailto:info@rorihotelfc.com">info@rorihotelfc.com</a></p></div>
            <div class="card"><h3>⏰ Training Schedule</h3><p><strong>Tuesday &amp; Saturday</strong><br />12:00 – 2:30 PM</p></div>
            <div class="card"><h3>📘 Facebook</h3><p><a href="https://www.facebook.com/rorihotel" target="_blank" rel="noopener">facebook.com/rorihotel</a></p></div>
            <div class="card"><h3>📷 Instagram</h3><p>Coming Soon</p></div>
            <div class="card"><h3>📱 TikTok</h3><p><a href="https://www.tiktok.com/@rorihotel" target="_blank" rel="noopener">@rorihotel</a></p></div>
            <div class="card"><h3>📱 Telegram Group</h3><p><a href="https://t.me/+hq9-Z1AsY-g2OTk0" target="_blank" rel="noopener">Join Rori FC Telegram Group</a></p></div>
        </div>
        <div style="text-align:center; margin-top:35px;">
            <a href="https://t.me/+hq9-Z1AsY-g2OTk0" target="_blank" rel="noopener" class="btn">Join Telegram Group</a>
        </div>
    </section>

    <!-- ─── Footer ─── -->
    <footer>
        <p>&copy; 2026 Rori Community Football Club – Built with passion &amp; gold.</p>
    </footer>

    <!-- ─── JavaScript ─── -->
    <script>
        // ── Full 47‑member roster (coach & owner handled separately) ──
        const fullRoster = [
            "ሕዝቅኤል 🧤",
            "Edom adinew 🐍",
            "Amir Rori",
            "Bahilu F B",
            "Gm Mule Ro",
            "Tata Mu",
            "Amanu",
            "Nati",
            "Yido Tim",
            "Yohannes Yosef",
            "Abiy Ase",
            "A.B Ye.....",
            "ⒶⓂⓊ💸🌿",
            "Tare",
            "Amir",
            "Gezer",
            "hayimi kahinu Haymiyekiyu",
            "Itachi Uchiha",
            "Mohammed Husan",
            "Alelign Molla",
            "Gado G",
            "Gedion Mark",
            "orent",
            "Yared Ro",
            "Abebayew Ro",
            "ትንሳኤ ❤️",
            "Nebiyu yonas",
            "filagot",
            "Abay@1221 Teshome",
            "Abel",
            "Yitbarek Berakaa",
            "Hope Car Market",
            "Gech",
            "Dany Tere",
            "Mesud David",
            "Nehemiya",
            "Tedy",
            "ወንድዬ @21",
            "tesfa mike",
            "Asgedom Mehari",
            "Tesfu Ro",
            "Dave",
            "Tsegaye",
            "melese",
            "Tesfaye ⚡",
            "Tesfahun 🌟",
            "Chernet 🔥"
        ];

        const squadContainer = document.getElementById('squadContainer');
        fullRoster.forEach((name, index) => {
            const div = document.createElement('div');
            div.className = 'player-card';
            div.innerHTML = `<div class="jersey-number">#${index + 1}</div><div>${name}</div>`;
            squadContainer.appendChild(div);
        });

        // ── AI Chatbot ──
        function sendMessage() {
            const input = document.getElementById('userQuestion');
            const question = input.value.trim();
            if (!question) return;
            appendMessage('You', question);
            input.value = '';
            const response = getAIResponse(question.toLowerCase());
            setTimeout(() => appendMessage('Bot', response), 400);
        }

        function appendMessage(sender, text) {
            const chatDiv = document.getElementById('chatMessages');
            const msg = document.createElement('p');
            const strong = document.createElement('strong');
            strong.textContent = sender + ': ';
            const span = document.createElement('span');
            span.textContent = text;
            msg.appendChild(strong);
            msg.appendChild(span);
            chatDiv.appendChild(msg);
            chatDiv.scrollTop = chatDiv.scrollHeight;
        }

        function getAIResponse(q) {
            const responses = {
                'training schedule': "Training is every Tuesday & Saturday from 12:00 to 2:30 PM. Be on time!",
                'telegram': "Join our Telegram group: https://t.me/+hq9-Z1AsY-g2OTk0",
                'telegram group': "Join our Telegram group: https://t.me/+hq9-Z1AsY-g2OTk0",
                'captain': "Our captain is Anbel Bahilu. He leads with passion and discipline.",
                'facebook': "Follow us on Facebook: https://www.facebook.com/rorihotel",
                'squad': "We have 47 members in our roster. Check the Members section!",
                'players': "We have 47 members in our roster. Check the Members section!",
                'members': "We have 47 members in our roster. Check the Members section!",
                'instagram': "Instagram is coming soon. Stay tuned!",
                'tiktok': "Follow us on TikTok: https://www.tiktok.com/@rorihotel",
                'health': "Rori FC follows a holistic health program: fitness, nutrition, physio, mental health, medical & sleep.",
                'doctor': "Our team doctor is Dr. Yonas Tadesse. He oversees all player health matters.",
                'coach': "Our head coach is Nebiyu Yonas. He leads the team with dedication.",
                'welcome': "ዳኤ ቡሹ (Da'e Bushu) – Welcome! We're glad you're here.",
                'bushu': "ዳኤ ቡሹ (Da'e Bushu) means 'Welcome' in Sidama. It carries respect, warmth, and unity.",
                'owner': "The ownership structure is currently being updated. For inquiries, please contact our management team.",
                'coffee': "Visit Silla Coffee Shop inside Rori Hotel! We serve Ethiopian Bunna, Macchiato, Espresso, teas, and Rori FC special blends.",
                'menu': "Our café menu includes Hot Coffee, Tea & Drinks, Snacks, and Rori FC Special blends. Check out the Café section!",
                'cafe': "Silla Coffee Shop is inside Rori Hotel. We have Ethiopian Bunna, macchiato, espresso, teas, fresh bread, cakes, and our Team Special Blend!",
                'anthem': "Here are the lyrics to our club anthem, RORI Forever! 🎵 Check the Anthem section for the full song."
            };
            for (const [key, reply] of Object.entries(responses)) {
                if (q.includes(key)) return reply;
            }
            return "I'm Rori FC AI assistant. Ask me about training, squad, Telegram, our café menu, anthem, or health programs!";
        }

        document.getElementById('userQuestion').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') sendMessage();
        });

        // ── Toast ──
        function showToast(message) {
            const toast = document.getElementById('welcomeToast');
            document.getElementById('toastMessage').textContent = message;
            toast.classList.add('show');
            if (window.toastTimer) clearTimeout(window.toastTimer);
            window.toastTimer = setTimeout(() => {
                toast.classList.remove('show');
            }, 6000);
        }

        function closeToast() {
            const toast = document.getElementById('welcomeToast');
            toast.classList.remove('show');
            if (window.toastTimer) clearTimeout(window.toastTimer);
        }

        // ── Copy account number ──
        function copyAccount() {
            const accountText = document.getElementById('accountNumber').textContent;
            navigator.clipboard.writeText(accountText).then(() => {
                showToast('✅ Account number copied: ' + accountText);
            }).catch(() => {
                const textArea = document.createElement('textarea');
                textArea.value = accountText;
                document.body.appendChild(textArea);
                textArea.select();
                document.execCommand('copy');
                document.body.removeChild(textArea);
                showToast('✅ Account number copied: ' + accountText);
            });
        }

        // ── Form handling ──
        const form = document.getElementById('registrationForm');
        form.addEventListener('submit', async function(e) {
            e.preventDefault();

            const name = document.getElementById('regName').value.trim();
            const age = document.getElementById('regAge').value.trim();
            const position = document.getElementById('regPosition').value.trim();
            const email = document.getElementById('regEmail').value.trim();
            const phone = document.getElementById('regPhone').value.trim();

            if (!name) { showToast('⚠️ Please enter your full name.'); return; }
            if (!age || parseInt(age) < 14 || parseInt(age) > 45) {
                showToast('⚠️ Age must be between 14 and 45.');
                return;
            }
            if (!position) { showToast('⚠️ Please enter your preferred position.'); return; }
            if (!email || !/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)) {
                showToast('⚠️ Please enter a valid email address.');
                return;
            }
            if (!phone || !/^[0-9+\-\s]{10,15}$/.test(phone.replace(/\s/g, ''))) {
                showToast('⚠️ Please enter a valid phone number (10–15 digits).');
                return;
            }

            const formData = new FormData(form);
            formData.append('_subject', 'New Rori FC Registration');

            try {
                showToast('⏳ Submitting...');
                const response = await fetch(form.action, {
                    method: 'POST',
                    body: formData,
                    headers: { 'Accept': 'application/json' }
                });

                if (response.ok) {
                    showToast(`🎉 Welcome, ${name}! Your registration is confirmed. The coach will contact you soon.`);
                    form.reset();
                } else {
                    let errorMessage = 'Something went wrong. Please try again.';
                    try {
                        const data = await response.json();
                        if (data.error) errorMessage = data.error;
                    } catch (e) {
                        if (response.status === 404) errorMessage = 'Form not found. Please check the URL.';
                        else if (response.status === 429) errorMessage = 'Too many submissions. Please try again later.';
                        else if (response.status === 500) errorMessage = 'Server error. Please try again.';
                        else errorMessage = `Error ${response.status}. Please try again.`;
                    }
                    showToast(`❌ ${errorMessage}`);
                }
            } catch (err) {
                console.error('🚨 Network error:', err);
                showToast('❌ Network error. Please check your connection and try again.');
            }
        });

        console.log('🏆 Rori Community FC website loaded successfully with Head Coach section!');
    </script>
</body>
</html>
