<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>VELORA HEALTH | Mohamed Saed</title>

<meta name="description" content="VELORA HEALTH - تجربة رعاية صحية عصرية">

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;500;600;700;800;900&family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>

/* =====================================================
   ROOT
===================================================== */

:root{
    --bg:#061114;
    --bg2:#091a1e;
    --card:rgba(255,255,255,.055);
    --card2:rgba(255,255,255,.035);

    --text:#f5fbfb;
    --muted:#91a5aa;

    --mint:#79e6d5;
    --mint2:#36c9b4;
    --gold:#e8c875;

    --border:rgba(255,255,255,.09);

    --shadow:0 30px 90px rgba(0,0,0,.35);
}

/* =====================================================
   RESET
===================================================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    background:
        radial-gradient(circle at 10% 10%,rgba(71,205,184,.10),transparent 28%),
        radial-gradient(circle at 90% 20%,rgba(232,200,117,.07),transparent 25%),
        linear-gradient(180deg,#061114,#07171a 50%,#061114);
    color:var(--text);
    font-family:"Cairo",sans-serif;
    overflow-x:hidden;
}

a{
    text-decoration:none;
    color:inherit;
}

button,
input,
select,
textarea{
    font-family:inherit;
}

/* =====================================================
   BACKGROUND EFFECTS
===================================================== */

body::before{
    content:"";
    position:fixed;
    inset:0;
    pointer-events:none;
    background-image:
        linear-gradient(rgba(255,255,255,.018) 1px,transparent 1px),
        linear-gradient(90deg,rgba(255,255,255,.018) 1px,transparent 1px);
    background-size:55px 55px;
    mask-image:linear-gradient(to bottom,black,transparent);
    z-index:-2;
}

.glow{
    position:fixed;
    width:400px;
    height:400px;
    border-radius:50%;
    filter:blur(100px);
    opacity:.12;
    pointer-events:none;
    z-index:-1;
}

.glow.one{
    background:var(--mint);
    top:10%;
    left:-180px;
}

.glow.two{
    background:var(--gold);
    bottom:5%;
    right:-180px;
}

/* =====================================================
   NAVBAR
===================================================== */

.navbar{
    position:fixed;
    top:0;
    left:0;
    right:0;
    z-index:1000;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:18px 7%;

    background:rgba(5,16,19,.70);
    backdrop-filter:blur(22px);
    border-bottom:1px solid rgba(255,255,255,.06);
}

.brand{
    display:flex;
    align-items:center;
    gap:12px;
}

.brand-mark{
    width:44px;
    height:44px;
    border-radius:14px;

    display:grid;
    place-items:center;

    font-family:"Inter",sans-serif;
    font-size:20px;
    font-weight:900;

    color:#051214;

    background:
        linear-gradient(135deg,var(--mint),#d7fff7);

    box-shadow:
        0 0 30px rgba(121,230,213,.25);
}

.brand-name{
    font-family:"Inter",sans-serif;
    font-size:17px;
    font-weight:900;
    letter-spacing:1px;
    direction:ltr;
}

.brand-name span{
    color:var(--mint);
}

.brand-name small{
    display:block;
    margin-top:2px;
    color:var(--mint);
    font-family:"Inter",sans-serif;
    font-size:7px;
    letter-spacing:2.5px;
}

.nav-links{
    display:flex;
    align-items:center;
    gap:30px;
}

.nav-links a{
    color:#b7c6ca;
    font-size:13px;
    font-weight:600;
    transition:.3s;
}

.nav-links a:hover{
    color:var(--mint);
}

.nav-button{
    padding:11px 20px;
    border-radius:50px;

    background:rgba(121,230,213,.10);
    border:1px solid rgba(121,230,213,.30);

    color:var(--mint)!important;
}

.menu-btn{
    display:none;
    font-size:25px;
    cursor:pointer;
}

/* =====================================================
   HERO
===================================================== */

.hero{
    min-height:100vh;
    padding:150px 7% 90px;

    display:grid;
    grid-template-columns:1.1fr .9fr;
    align-items:center;
    gap:70px;
}

.hero-mini{
    color:var(--mint);
    font-family:"Inter",sans-serif;
    font-size:11px;
    font-weight:800;
    letter-spacing:4px;
    margin-bottom:18px;
    direction:ltr;
}

.hero h1{
    font-size:clamp(42px,6vw,78px);
    line-height:1.05;
    font-weight:900;
    margin-bottom:25px;
}

.hero h1 span{
    color:var(--mint);
}

.hero-description{
    color:var(--muted);
    max-width:650px;
    font-size:16px;
    line-height:2;
    margin-bottom:30px;
}

.mohamed-signature{
    display:inline-flex;
    align-items:center;
    gap:12px;

    padding:10px 17px;
    margin-bottom:28px;

    border-radius:50px;

    background:rgba(121,230,213,.055);
    border:1px solid rgba(121,230,213,.20);
}

.mohamed-signature span{
    color:#778d92;
    font-family:"Inter",sans-serif;
    font-size:8px;
    letter-spacing:2px;
    direction:ltr;
}

.mohamed-signature strong{
    color:var(--mint);
    font-family:"Inter",sans-serif;
    font-size:14px;
    direction:ltr;
}

.hero-buttons{
    display:flex;
    gap:14px;
    flex-wrap:wrap;
}

.btn{
    border:none;
    cursor:pointer;

    padding:15px 25px;
    border-radius:15px;

    font-weight:800;
    transition:.35s;
}

.btn-primary{
    color:#061114;

    background:linear-gradient(
        135deg,
        var(--mint),
        #b8fff4
    );

    box-shadow:
        0 12px 40px rgba(121,230,213,.18);
}

.btn-primary:hover{
    transform:translateY(-4px);
    box-shadow:
        0 18px 55px rgba(121,230,213,.28);
}

.btn-secondary{
    color:white;

    background:rgba(255,255,255,.045);
    border:1px solid rgba(255,255,255,.10);
}

.btn-secondary:hover{
    transform:translateY(-4px);
    border-color:rgba(121,230,213,.35);
}

/* =====================================================
   HERO VISUAL
===================================================== */

.hero-visual{
    position:relative;
    min-height:520px;

    display:grid;
    place-items:center;
}

.medical-orb{
    width:min(420px,85vw);
    height:min(420px,85vw);

    border-radius:50%;

    display:grid;
    place-items:center;

    position:relative;

    background:
        radial-gradient(circle at 35% 30%,
        rgba(121,230,213,.18),
        rgba(255,255,255,.025) 45%,
        transparent 70%);

    border:1px solid rgba(121,230,213,.15);

    box-shadow:
        inset 0 0 80px rgba(121,230,213,.04),
        0 0 100px rgba(121,230,213,.06);

    animation:float 6s ease-in-out infinite;
}

.medical-orb::before{
    content:"";
    position:absolute;
    inset:30px;
    border-radius:50%;
    border:1px dashed rgba(121,230,213,.25);
    animation:spin 25s linear infinite;
}

.medical-cross{
    width:115px;
    height:115px;

    display:grid;
    place-items:center;

    border-radius:35px;

    font-size:65px;
    font-weight:200;

    color:var(--mint);

    background:rgba(121,230,213,.055);
    border:1px solid rgba(121,230,213,.22);

    box-shadow:
        0 0 70px rgba(121,230,213,.12);
}

.floating-card{
    position:absolute;

    padding:16px 20px;

    border-radius:20px;

    background:rgba(7,22,26,.78);
    backdrop-filter:blur(18px);

    border:1px solid rgba(255,255,255,.10);

    box-shadow:var(--shadow);
}

.floating-card.one{
    top:8%;
    right:3%;
}

.floating-card.two{
    bottom:12%;
    left:0;
}

.floating-card strong{
    display:block;
    font-family:"Inter",sans-serif;
    color:var(--mint);
    font-size:22px;
    direction:ltr;
}

.floating-card small{
    color:#8ca0a5;
}

/* =====================================================
   SECTION
===================================================== */

.section{
    padding:110px 7%;
}

.section-kicker{
    color:var(--mint);
    font-family:"Inter",sans-serif;
    font-size:10px;
    font-weight:800;
    letter-spacing:4px;
    direction:ltr;
}

.section-title{
    margin-top:15px;
    font-size:clamp(34px,5vw,60px);
    line-height:1.1;
}

.section-title span{
    color:var(--mint);
}

.section-description{
    max-width:700px;
    margin-top:20px;

    color:var(--muted);
    line-height:2;
}

/* =====================================================
   SERVICES
===================================================== */

.services-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
    margin-top:55px;
}

.service-card{
    position:relative;

    padding:32px;

    border-radius:28px;

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.065),
            rgba(255,255,255,.025)
        );

    border:1px solid var(--border);

    overflow:hidden;

    transition:.4s;
}

.service-card:hover{
    transform:translateY(-8px);
    border-color:rgba(121,230,213,.30);
    box-shadow:0 25px 70px rgba(0,0,0,.25);
}

.service-number{
    position:absolute;
    top:22px;
    left:25px;

    color:rgba(255,255,255,.12);

    font-family:"Inter",sans-serif;
    font-weight:900;
    font-size:40px;
    direction:ltr;
}

.service-icon{
    width:62px;
    height:62px;

    display:grid;
    place-items:center;

    margin-bottom:25px;

    border-radius:20px;

    color:var(--mint);

    background:rgba(121,230,213,.07);
    border:1px solid rgba(121,230,213,.15);

    font-size:27px;
}

.service-card h3{
    font-size:20px;
    margin-bottom:12px;
}

.service-card p{
    color:var(--muted);
    line-height:1.9;
    font-size:14px;
}

/* =====================================================
   ABOUT
===================================================== */

.about{
    display:grid;
    grid-template-columns:.9fr 1.1fr;
    gap:70px;
    align-items:center;
}

.about-panel{
    min-height:440px;

    padding:40px;

    border-radius:35px;

    background:
        radial-gradient(
            circle at center,
            rgba(121,230,213,.12),
            transparent 60%
        ),
        rgba(255,255,255,.035);

    border:1px solid rgba(255,255,255,.08);

    display:grid;
    place-items:center;
}

.about-emblem{
    width:230px;
    height:230px;

    border-radius:50%;

    display:grid;
    place-items:center;

    border:1px solid rgba(121,230,213,.22);

    color:var(--mint);

    font-family:"Inter",sans-serif;
    font-size:60px;
    font-weight:900;

    box-shadow:
        0 0 80px rgba(121,230,213,.10);
}

.about-text p{
    color:var(--muted);
    line-height:2;
    margin-top:25px;
}

.about-list{
    margin-top:30px;

    display:grid;
    gap:14px;
}

.about-list div{
    display:flex;
    gap:12px;
    align-items:center;

    color:#c8d5d8;
}

.check{
    width:24px;
    height:24px;

    display:grid;
    place-items:center;

    border-radius:50%;

    color:#061114;
    background:var(--mint);

    font-size:12px;
    font-weight:900;
}

/* =====================================================
   STATS
===================================================== */

.stats{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:18px;
    margin-top:60px;
}

.stat{
    text-align:center;

    padding:30px 20px;

    border-radius:24px;

    background:rgba(255,255,255,.035);
    border:1px solid rgba(255,255,255,.07);
}

.stat strong{
    display:block;

    color:var(--mint);

    font-family:"Inter",sans-serif;
    font-size:35px;
    direction:ltr;
}

.stat span{
    color:#899da2;
    font-size:12px;
}

/* =====================================================
   BOOKING
===================================================== */

.booking-section{
    padding:110px 7%;
}

.booking-box{
    max-width:1100px;
    margin:auto;

    padding:45px;

    border-radius:35px;

    background:
        linear-gradient(
            145deg,
            rgba(121,230,213,.075),
            rgba(255,255,255,.025)
        );

    border:1px solid rgba(121,230,213,.15);

    box-shadow:var(--shadow);
}

.booking-head{
    text-align:center;
    margin-bottom:40px;
}

.booking-head h2{
    font-size:clamp(34px,5vw,55px);
}

.booking-head h2 span{
    color:var(--mint);
}

.booking-head p{
    color:var(--muted);
    margin-top:12px;
}

.booking-form{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:18px;
}

.field{
    display:flex;
    flex-direction:column;
    gap:8px;
}

.field.full{
    grid-column:1/-1;
}

.field label{
    color:#a9bbbf;
    font-size:12px;
    font-weight:700;
}

.field input,
.field select,
.field textarea{
    width:100%;

    padding:15px 17px;

    color:white;

    background:rgba(0,0,0,.20);

    border:1px solid rgba(255,255,255,.10);

    border-radius:15px;

    outline:none;

    transition:.3s;
}

.field input:focus,
.field select:focus,
.field textarea:focus{
    border-color:rgba(121,230,213,.45);
    box-shadow:0 0 0 4px rgba(121,230,213,.05);
}

.field select option{
    background:#07181c;
    color:white;
}

.field textarea{
    min-height:120px;
    resize:vertical;
}

.booking-submit{
    grid-column:1/-1;
    margin-top:10px;
}

/* =====================================================
   REVIEWS
===================================================== */

.reviews-section{
    padding:110px 7%;
}

.section-head{
    display:flex;
    justify-content:space-between;
    align-items:end;
    gap:30px;
    margin-bottom:55px;
}

.section-head h2{
    font-size:clamp(34px,5vw,60px);
    line-height:1.05;
    margin-top:15px;
}

.section-head h2 span{
    color:var(--mint);
}

.rating-summary{
    display:flex;
    align-items:center;
    gap:15px;

    padding:15px 20px;

    border:1px solid rgba(121,230,213,.20);
    border-radius:20px;

    background:rgba(255,255,255,.04);
    backdrop-filter:blur(15px);
}

.rating-number{
    font-family:"Inter",sans-serif;
    font-size:38px;
    font-weight:900;
    direction:ltr;
}

.stars,
.review-stars{
    color:#ffd76a;
    letter-spacing:3px;
}

.rating-summary small{
    color:#84969f;
}

.reviews-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.review-card{
    position:relative;

    padding:27px;

    border-radius:28px;

    border:1px solid rgba(255,255,255,.08);

    background:
        linear-gradient(
            145deg,
            rgba(255,255,255,.07),
            rgba(255,255,255,.025)
        );

    backdrop-filter:blur(20px);

    transition:.4s;

    overflow:hidden;
}

.review-card::before{
    content:"";

    position:absolute;

    width:100px;
    height:100px;

    top:-50px;
    right:-50px;

    background:var(--mint);
    opacity:.08;

    filter:blur(30px);

    border-radius:50%;
}

.review-card:hover{
    transform:translateY(-8px);

    border-color:rgba(121,230,213,.35);

    box-shadow:
        0 20px 60px rgba(0,0,0,.25);
}

.review-card.featured{
    border-color:rgba(121,230,213,.35);
    transform:translateY(-8px);
}

.review-top{
    display:flex;
    align-items:center;
    gap:12px;
    margin-bottom:20px;
}

.review-avatar{
    width:48px;
    height:48px;

    display:grid;
    place-items:center;

    border-radius:50%;

    font-size:18px;
    font-weight:900;

    background:
        linear-gradient(
            135deg,
            #263b43,
            #101b20
        );

    border:1px solid rgba(255,255,255,.15);
}

.review-avatar.female{
    background:
        linear-gradient(
            135deg,
            #513e55,
            #172d35
        );

    border-color:rgba(255,160,220,.25);
}

.review-top strong{
    display:block;
    font-size:15px;
}

.review-top span{
    display:block;

    color:#80919a;
    font-size:11px;

    margin-top:3px;
}

.review-stars{
    margin-right:auto;
    font-size:12px;
    direction:ltr;
}

.review-card p{
    color:#c5d0d4;

    line-height:1.9;

    font-size:14px;

    min-height:105px;
}

.verified{
    margin-top:20px;

    color:var(--mint);

    font-size:11px;
    font-weight:700;
}

/* =====================================================
   CTA
===================================================== */

.cta{
    margin:50px 7% 110px;

    padding:65px 8%;

    border-radius:38px;

    text-align:center;

    background:
        radial-gradient(
            circle at center,
            rgba(121,230,213,.13),
            transparent 55%
        ),
        rgba(255,255,255,.035);

    border:1px solid rgba(121,230,213,.14);
}

.cta h2{
    font-size:clamp(35px,5vw,60px);
    line-height:1.1;
}

.cta h2 span{
    color:var(--mint);
}

.cta p{
    color:var(--muted);
    max-width:650px;
    margin:20px auto 30px;
    line-height:2;
}

/* =====================================================
   FOOTER
===================================================== */

footer{
    padding:70px 7% 25px;

    border-top:1px solid rgba(255,255,255,.07);

    background:rgba(0,0,0,.15);
}

.footer-grid{
    display:grid;
    grid-template-columns:1.4fr 1fr 1fr;
    gap:50px;
}

.footer-brand{
    font-family:"Inter",sans-serif;
    font-weight:900;
    font-size:24px;
    direction:ltr;
}

.footer-brand span{
    color:var(--mint);
}

.footer-text{
    color:#7e9297;
    margin-top:14px;
    line-height:1.9;
    font-size:13px;
}

.footer-title{
    font-weight:800;
    margin-bottom:18px;
}

.footer-links{
    display:grid;
    gap:10px;
}

.footer-links a{
    color:#819499;
    font-size:13px;
    transition:.3s;
}

.footer-links a:hover{
    color:var(--mint);
}

.footer-credit{
    margin-top:25px;

    display:inline-flex;
    align-items:center;
    gap:8px;

    padding:9px 14px;

    border-radius:50px;

    background:rgba(121,230,213,.05);
    border:1px solid rgba(121,230,213,.14);

    color:#819499;

    font-size:11px;
}

.footer-credit strong{
    color:var(--mint);
    font-family:"Inter",sans-serif;
    direction:ltr;
}

.footer-bottom{
    margin-top:50px;
    padding-top:20px;

    border-top:1px solid rgba(255,255,255,.06);

    display:flex;
    justify-content:space-between;
    gap:20px;

    color:#667b80;
    font-size:11px;
}

.footer-bottom span{
    color:var(--mint);
}

/* =====================================================
   WHATSAPP
===================================================== */

.whatsapp{
    position:fixed;

    left:22px;
    bottom:22px;

    width:58px;
    height:58px;

    display:grid;
    place-items:center;

    border-radius:50%;

    color:white;

    background:#1fc46b;

    font-size:25px;

    box-shadow:
        0 10px 40px rgba(31,196,107,.30);

    z-index:999;

    transition:.3s;
}

.whatsapp:hover{
    transform:scale(1.1);
}

/* =====================================================
   ANIMATIONS
===================================================== */

@keyframes float{
    0%,100%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-15px);
    }
}

@keyframes spin{
    from{
        transform:rotate(0deg);
    }

    to{
        transform:rotate(360deg);
    }
}

.reveal{
    animation:reveal .9s ease both;
}

@keyframes reveal{
    from{
        opacity:0;
        transform:translateY(25px);
    }

    to{
        opacity:1;
        transform:translateY(0);
    }
}

/* =====================================================
   RESPONSIVE
===================================================== */

@media(max-width:1000px){

    .hero{
        grid-template-columns:1fr;
        text-align:center;
    }

    .hero-description{
        margin-left:auto;
        margin-right:auto;
    }

    .hero-buttons{
        justify-content:center;
    }

    .hero-visual{
        min-height:450px;
    }

    .about{
        grid-template-columns:1fr;
    }

    .services-grid{
        grid-template-columns:repeat(2,1fr);
    }

    .reviews-grid{
        grid-template-columns:repeat(2,1fr);
    }

}

@media(max-width:700px){

    .navbar{
        padding:14px 5%;
    }

    .nav-links{
        display:none;
    }

    .menu-btn{
        display:block;
    }

    .hero{
        padding:135px 5% 70px;
    }

    .section,
    .booking-section,
    .reviews-section{
        padding:80px 5%;
    }

    .services-grid,
    .reviews-grid{
        grid-template-columns:1fr;
    }

    .stats{
        grid-template-columns:repeat(2,1fr);
    }

    .booking-box{
        padding:25px 18px;
    }

    .booking-form{
        grid-template-columns:1fr;
    }

    .field.full,
    .booking-submit{
        grid-column:auto;
    }

    .section-head{
        align-items:flex-start;
        flex-direction:column;
    }

    .review-card.featured{
        transform:none;
    }

    .footer-grid{
        grid-template-columns:1fr;
        gap:35px;
    }

    .footer-bottom{
        flex-direction:column;
    }

}

@media(max-width:430px){

    .brand-mark{
        width:39px;
        height:39px;
    }

    .brand-name{
        font-size:14px;
    }

    .brand-name small{
        font-size:6px;
    }

    .hero h1{
        font-size:39px;
    }

    .medical-orb{
        width:300px;
        height:300px;
    }

    .medical-cross{
        width:90px;
        height:90px;
        font-size:50px;
    }

    .floating-card{
        padding:11px 14px;
    }

}

</style>
</head>


<body>

<div class="glow one"></div>
<div class="glow two"></div>


<!-- =====================================================
     NAVBAR
===================================================== -->

<nav class="navbar">

    <a href="#home" class="brand">

        <div class="brand-mark">
            V
        </div>

        <div class="brand-name">
            VELORA <span>HEALTH</span>
            <small>MOHAMED SAED</small>
        </div>

    </a>


    <div class="nav-links">

        <a href="#home">الرئيسية</a>
        <a href="#services">الخدمات</a>
        <a href="#about">عن VELORA</a>
        <a href="#reviews">التقييمات</a>

        <a href="#booking" class="nav-button">
            احجز الآن
        </a>

    </div>


    <div class="menu-btn">
        ☰
    </div>

</nav>



<!-- =====================================================
     HERO
===================================================== -->

<section class="hero" id="home">

    <div class="hero-content reveal">

        <div class="hero-mini">
            PREMIUM HEALTHCARE EXPERIENCE
        </div>


        <div class="mohamed-signature">

            <span>CREATED WITH</span>

            <strong>
                Mohamed Saed
            </strong>

        </div>


        <h1>
            صحتك تستحق
            <span>تجربة مختلفة.</span>
        </h1>


        <p class="hero-description">

            أهلاً بك في VELORA HEALTH
            تجربة صحية عصرية تجمع بين
            الرعاية والراحة والتكنولوجيا
            في مكان واحد.

        </p>


        <div class="hero-buttons">

            <a href="#booking" class="btn btn-primary">
                احجز موعدك الآن
            </a>

            <a href="#services" class="btn btn-secondary">
                اكتشف خدماتنا
            </a>

        </div>

    </div>



    <div class="hero-visual">

        <div class="medical-orb">

            <div class="medical-cross">
                +
            </div>

        </div>


        <div class="floating-card one">

            <strong>
                24/7
            </strong>

            <small>
                رعاية واهتمام
            </small>

        </div>


        <div class="floating-card two">

            <strong>
                4.9 ★
            </strong>

            <small>
                تقييم تجريبي
            </small>

        </div>

    </div>

</section>



<!-- =====================================================
     SERVICES
===================================================== -->

<section class="section" id="services">

    <span class="section-kicker">
        OUR SERVICES
    </span>

    <h2 class="section-title">
        خدمات طبية
        <span>بمستوى مختلف.</span>
    </h2>

    <p class="section-description">

        مجموعة من الخدمات المصممة لتوفير
        تجربة صحية منظمة ومريحة للمريض.

    </p>


    <div class="services-grid">


        <div class="service-card">

            <div class="service-number">
                01
            </div>

            <div class="service-icon">
                ✚
            </div>

            <h3>
                الاستقبال والطوارئ
            </h3>

            <p>
                استقبال الحالات وتنظيم إجراءات
                الوصول والتعامل الأولي مع المريض.
            </p>

        </div>


        <div class="service-card">

            <div class="service-number">
                02
            </div>

            <div class="service-icon">
                ♡
            </div>

            <h3>
                الباطنة
            </h3>

            <p>
                متابعة الحالات والفحوصات الطبية
                وتقديم الرعاية المناسبة.
            </p>

        </div>


        <div class="service-card">

            <div class="service-number">
                03
            </div>

            <div class="service-icon">
                ◉
            </div>

            <h3>
                العناية المركزة
            </h3>

            <p>
                رعاية ومتابعة الحالات التي تحتاج
                إلى مراقبة مستمرة.
            </p>

        </div>


        <div class="service-card">

            <div class="service-number">
                04
            </div>

            <div class="service-icon">
                ✚
            </div>

            <h3>
                التحاليل والفحوصات
            </h3>

            <p>
                تنظيم طلبات الفحوصات والتحاليل
                ومتابعة الإجراءات.
            </p>

        </div>


        <div class="service-card">

            <div class="service-number">
                05
            </div>

            <div class="service-icon">
                ♧
            </div>

            <h3>
                متابعة المرضى
            </h3>

            <p>
                تنظيم مواعيد المتابعة والتواصل
                مع المريض بصورة سهلة.
            </p>

        </div>


        <div class="service-card">

            <div class="service-number">
                06
            </div>

            <div class="service-icon">
                ◌
            </div>

            <h3>
                استشارات صحية
            </h3>

            <p>
                حجز وتنظيم الاستشارات والخدمات
                الصحية المختلفة.
            </p>

        </div>


    </div>

</section>



<!-- =====================================================
     ABOUT
===================================================== -->

<section class="section" id="about">

    <div class="about">


        <div class="about-panel">

            <div class="about-emblem">
                V
            </div>

        </div>



        <div class="about-text">

            <span class="section-kicker">
                ABOUT VELORA
            </span>

            <h2 class="section-title">
                مش مجرد
                <span>موقع طبي.</span>
            </h2>


            <p>

                VELORA HEALTH هو تصور لتجربة
                رعاية صحية عصرية تجمع بين
                التصميم الراقي وسهولة الاستخدام
                وتنظيم الخدمات والحجز.

            </p>


            <div class="about-list">

                <div>
                    <span class="check">✓</span>
                    تجربة استخدام سهلة
                </div>

                <div>
                    <span class="check">✓</span>
                    تصميم طبي عصري
                </div>

                <div>
                    <span class="check">✓</span>
                    حجز سريع من الموبايل
                </div>

                <div>
                    <span class="check">✓</span>
                    تواصل مباشر عبر WhatsApp
                </div>

            </div>

        </div>

    </div>


    <div class="stats">

        <div class="stat">
            <strong>24/7</strong>
            <span>رعاية مستمرة</span>
        </div>

        <div class="stat">
            <strong>6+</strong>
            <span>خدمات صحية</span>
        </div>

        <div class="stat">
            <strong>4.9</strong>
            <span>تقييم تجريبي</span>
        </div>

        <div class="stat">
            <strong>100%</strong>
            <span>تجربة رقمية</span>
        </div>

    </div>

</section>



<!-- =====================================================
     BOOKING
===================================================== -->

<section class="booking-section" id="booking">

    <div class="booking-box">

        <div class="booking-head">

            <span class="section-kicker">
                ONLINE BOOKING
            </span>

            <h2>
                احجز
                <span>موعدك.</span>
            </h2>

            <p>
                املأ البيانات وسيتم تجهيز رسالة الحجز على WhatsApp.
            </p>

        </div>


        <form class="booking-form" id="bookingForm">


            <div class="field">

                <label>
                    اسم المريض
                </label>

                <input
                    type="text"
                    id="patientName"
                    placeholder="اكتب اسم المريض"
                    required
                >

            </div>


            <div class="field">

                <label>
                    السن
                </label>

                <input
                    type="number"
                    id="age"
                    placeholder="مثال: 25"
                    min="1"
                    max="120"
                    required
                >

            </div>


            <div class="field">

                <label>
                    رقم الهاتف
                </label>

                <input
                    type="tel"
                    id="phone"
                    placeholder="01xxxxxxxxx"
                    required
                >

            </div>


            <div class="field">

                <label>
                    الخدمة المطلوبة
                </label>

                <select id="service" required>

                    <option value="">
                        اختر الخدمة
                    </option>

                    <option>
                        الاستقبال والطوارئ
                    </option>

                    <option>
                        الباطنة
                    </option>

                    <option>
                        العناية المركزة
                    </option>

                    <option>
                        التحاليل والفحوصات
                    </option>

                    <option>
                        متابعة المرضى
                    </option>

                    <option>
                        استشارة صحية
                    </option>

                </select>

            </div>


            <div class="field">

                <label>
                    العنوان
                </label>

                <input
                    type="text"
                    id="address"
                    placeholder="العنوان"
                    required
                >

            </div>


            <div class="field">

                <label>
                    الموعد المفضل
                </label>

                <input
                    type="datetime-local"
                    id="date"
                    required
                >

            </div>


            <div class="field full">

                <label>
                    ملاحظات إضافية
                </label>

                <textarea
                    id="notes"
                    placeholder="اكتب أي تفاصيل إضافية..."
                ></textarea>

            </div>


            <div class="booking-submit">

                <button
                    type="submit"
                    class="btn btn-primary"
                    style="width:100%;"
                >
                    تأكيد الحجز عبر WhatsApp
                </button>

            </div>


        </form>

    </div>

</section>



<!-- =====================================================
     REVIEWS
===================================================== -->

<section class="reviews-section" id="reviews">

    <div class="section-head">

        <div>

            <span class="section-kicker">
                PATIENT REVIEWS
            </span>

            <h2>
                ناس جرّبت VELORA
                <br>
                <span>وقالت رأيها ❤️</span>
            </h2>

        </div>


        <div class="rating-summary">

            <div class="rating-number">
                4.9
            </div>

            <div>

                <div class="stars">
                    ★★★★★
                </div>

                <small>
                    تقييم تجريبي للموقع
                </small>

            </div>

        </div>

    </div>



    <div class="reviews-grid">


        <div class="review-card">

            <div class="review-top">

                <div class="review-avatar female">
                    م
                </div>

                <div>
                    <strong>
                        مريم أحمد
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "بجد المكان شكله تحفة والخدمة منظمة جدًا ❤️
                أكتر حاجة عجبتني إن كل حاجة واضحة وسهلة من أول الحجز."
            </p>

      <div class="verified"
                > 
            </div>

        </div>



        <div class="review-card featured">

            <div class="review-top">

                <div class="review-avatar female">
                    س
                </div>

                <div>
                    <strong>
                        سارة محمد
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "بصراحة أول مرة أشوف موقع طبي شيك كده ❤️
                التصميم مريح جدًا والحجز بسيط ومش محتاج ألف خطوة."
            </p>

            <div class="verified">
            </div>

        </div>



        <div class="review-card">

            <div class="review-top">

                <div class="review-avatar">
                    أ
                </div>

                <div>
                    <strong>
                        أحمد علي
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "التعامل كان محترم جدًا والمعلومات الموجودة
                في الموقع خلت الموضوع أسهل بكتير."
            </p>

            <div class="verified">
            </div>

        </div>



        <div class="review-card">

            <div class="review-top">

                <div class="review-avatar female">
                    ن
                </div>

                <div>
                    <strong>
                        نورهان خالد
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "أنا حبيت جدًا شكل الموقع ❤️
                خصوصًا تفاصيل الحجز وطريقة عرض الخدمات."
            </p>

            <div class="verified">
            </div>

        </div>



        <div class="review-card">

            <div class="review-top">

                <div class="review-avatar female">
                    ر
                </div>

                <div>
                    <strong>
                        روان محمود
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "الخدمة شكلها محترم جدًا والموقع سريع ومريح للعين.
                بجد التصميم مختلف عن المواقع الطبية التقليدية."
            </p>

            <div class="verified">
            </div>

        </div>



        <div class="review-card">

            <div class="review-top">

                <div class="review-avatar">
                    ي
                </div>

                <div>
                    <strong>
                        يوسف حسن
                    </strong>

                    <span>
                        Alexandria
                    </span>
                </div>

                <div class="review-stars">
                    ★★★★★
                </div>

            </div>

            <p>
                "واجهة ممتازة والحجز معمول بطريقة بسيطة جدًا.
                كل حاجة قدامك ومش محتاج تدور كتير."
            </p>

            <div class="verified">
            </div>

        </div>


    </div>

</section>



<!-- =====================================================
     CTA
===================================================== -->

<section class="cta">

    <span class="section-kicker">
        VELORA HEALTH
    </span>

    <h2>
        صحتك أولاً.
        <span>دائمًا.</span>
    </h2>

    <p>
        ابدأ تجربة الحجز الرقمية الآن
        واستمتع بتجربة صحية بسيطة وعصرية.
    </p>

    <a href="#booking" class="btn btn-primary">
        ابدأ الحجز
    </a>

</section>



<!-- =====================================================
     FOOTER
===================================================== -->

<footer>

    <div class="footer-grid">


        <div>

            <div class="footer-brand">
                VELORA <span>HEALTH</span>
            </div>

            <div class="footer-text">
                Modern Healthcare. Human Care.
                <br>
                تجربة صحية عصرية مصممة للموبايل.
            </div>


            <div class="footer-credit">

                Designed with ❤️ by

                <strong>
                    Mohamed Saed
                </strong>

            </div>

        </div>



        <div>

            <div class="footer-title">
                روابط سريعة
            </div>

            <div class="footer-links">

                <a href="#home">
                    الرئيسية
                </a>

                <a href="#services">
                    الخدمات
                </a>

                <a href="#about">
                    عن VELORA
                </a>

                <a href="#reviews">
                    التقييمات
                </a>

                <a href="#booking">
                    الحجز
                </a>

            </div>

        </div>



        <div>

            <div class="footer-title">
                تواصل معنا
            </div>

            <div class="footer-links">

                <a href="tel:01013490493">
                    01013490493
                </a>

                <a
                    href="https://wa.me/201013490493"
                    target="_blank"
                >
                    WhatsApp
                </a>

                <a href="#">
                    Alexandria, Egypt
                </a>

            </div>

        </div>


    </div>


    <div class="footer-bottom">

        <div>
            © 2026 VELORA HEALTH
        </div>

        <div>
            Crafted by
            <span>
                Mohamed Saed
            </span>
        </div>

    </div>

</footer>



<!-- =====================================================
     WHATSAPP BUTTON
===================================================== -->

<a
    class="whatsapp"
    href="https://wa.me/201013490493"
    target="_blank"
    aria-label="WhatsApp"
>
    ☎
</a>



<!-- =====================================================
     JAVASCRIPT
===================================================== -->

<script>

/* =====================================================
   BOOKING -> WHATSAPP
===================================================== */

document
.getElementById("bookingForm")
.addEventListener("submit",function(e){

    e.preventDefault();


    const name =
        document.getElementById("patientName").value.trim();

    const age =
        document.getElementById("age").value.trim();

    const phone =
        document.getElementById("phone").value.trim();

    const service =
        document.getElementById("service").value;

    const address =
        document.getElementById("address").value.trim();

    const date =
        document.getElementById("date").value;

    const notes =
        document.getElementById("notes").value.trim();


    const message =

`🏥 *VELORA HEALTH*

📋 *طلب حجز جديد*

👤 اسم المريض: ${name}

🎂 السن: ${age}

📱 رقم الهاتف: ${phone}

🩺 الخدمة المطلوبة: ${service}

📍 العنوان: ${address}

📅 الموعد المفضل: ${date}

📝 ملاحظات:
${notes || "لا يوجد"}

━━━━━━━━━━━━━━

Made through VELORA HEALTH`;



    const whatsappURL =
        "https://wa.me/201013490493?text="
        + encodeURIComponent(message);


    window.open(
        whatsappURL,
        "_blank"
    );

});


/* =====================================================
   MOBILE MENU
===================================================== */

const menuBtn =
    document.querySelector(".menu-btn");

const navLinks =
    document.querySelector(".nav-links");


menuBtn.addEventListener("click",function(){

    if(
        navLinks.style.display === "flex"
    ){

        navLinks.style.display = "none";

    }else{

        navLinks.style.display = "flex";

        navLinks.style.position = "absolute";
        navLinks.style.top = "76px";
        navLinks.style.right = "5%";
        navLinks.style.left = "5%";

        navLinks.style.flexDirection = "column";
        navLinks.style.padding = "25px";

        navLinks.style.borderRadius = "22px";

        navLinks.style.background =
            "rgba(5,16,19,.96)";

        navLinks.style.border =
            "1px solid rgba(255,255,255,.08)";

    }

});


/* =====================================================
   CLOSE MOBILE MENU
===================================================== */

document
.querySelectorAll(".nav-links a")
.forEach(function(link){

    link.addEventListener("click",function(){

        if(window.innerWidth <= 700){

            navLinks.style.display = "none";

        }

    });

});


/* =====================================================
   CURRENT YEAR
===================================================== */

console.log(
    "VELORA HEALTH — Mohamed Saed"
);

</script>


</body>
</html>