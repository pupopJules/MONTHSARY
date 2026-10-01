<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Happy Monthsary, Mommy 💜</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html,
body {
    width: 100%;
    height: 100%;
    overflow: hidden;
}

body {
    font-family: "Trebuchet MS", Arial, sans-serif;
    background:
        radial-gradient(circle at center, #35145e 0%, #160522 45%, #07020d 100%);
    color: white;
}


/* =========================================
   BACKGROUND
========================================= */

.background {
    position: fixed;
    inset: 0;
    z-index: 0;
}

.background::before {
    content: "";
    position: absolute;
    inset: 0;

    background-image:
        linear-gradient(rgba(255,255,255,.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.025) 1px, transparent 1px);

    background-size: 30px 30px;

    opacity: .4;
}


/* =========================================
   FLOATING HEARTS
========================================= */

#hearts {
    position: fixed;
    inset: 0;

    overflow: hidden;
    pointer-events: none;

    z-index: 2;
}

.heart {
    position: absolute;
    bottom: -40px;

    color: #d49aff;

    text-shadow:
        0 0 8px #b65cff,
        0 0 20px #8d3eff;

    animation: heartFloat linear forwards;
}

@keyframes heartFloat {

    0% {
        transform:
            translateY(0)
            rotate(0deg)
            scale(.7);

        opacity: 0;
    }

    10% {
        opacity: .8;
    }

    90% {
        opacity: .5;
    }

    100% {
        transform:
            translateY(-120vh)
            rotate(360deg)
            scale(1.2);

        opacity: 0;
    }
}


/* =========================================
   FLOATING PHOTOS
========================================= */

.photo-wall {
    position: fixed;
    inset: 0;

    overflow: hidden;

    pointer-events: none;

    z-index: 3;
}

.photo-wall::after {
    content: "";

    position: absolute;
    inset: 0;

    background:
        radial-gradient(
            ellipse at center,
            rgba(10,2,20,.92) 0%,
            rgba(10,2,20,.65) 32%,
            rgba(10,2,20,.15) 70%,
            transparent 100%
        );

    z-index: 10;
}

.photo {
    position: absolute;

    width: clamp(115px, 13vw, 190px);

    aspect-ratio: 4 / 5;

    object-fit: cover;

    padding: 6px;

    background: white;

    border-radius: 6px;

    box-shadow:
        0 12px 35px rgba(0,0,0,.6),
        0 0 30px rgba(164,80,255,.55);

    opacity: .9;

    animation:
        photoFloat linear infinite;

    will-change: transform;
}


/* PHOTO POSITIONS */

.photo:nth-child(1) {
    left: 2%;
    animation-duration: 18s;
    animation-delay: -5s;
    transform: rotate(-7deg);
}

.photo:nth-child(2) {
    left: 15%;
    animation-duration: 22s;
    animation-delay: -12s;
    transform: rotate(6deg);
}

.photo:nth-child(3) {
    left: 28%;
    animation-duration: 20s;
    animation-delay: -7s;
    transform: rotate(-5deg);
}

.photo:nth-child(4) {
    right: 28%;
    animation-duration: 23s;
    animation-delay: -14s;
    transform: rotate(6deg);
}

.photo:nth-child(5) {
    right: 15%;
    animation-duration: 19s;
    animation-delay: -5s;
    transform: rotate(-6deg);
}

.photo:nth-child(6) {
    right: 2%;
    animation-duration: 21s;
    animation-delay: -12s;
    transform: rotate(7deg);
}

.photo:nth-child(7) {
    left: 8%;
    animation-duration: 25s;
    animation-delay: -17s;
    transform: rotate(4deg);
}

.photo:nth-child(8) {
    right: 8%;
    animation-duration: 24s;
    animation-delay: -9s;
    transform: rotate(-4deg);
}

.photo:nth-child(9) {
    left: 44%;
    animation-duration: 26s;
    animation-delay: -20s;
    transform: rotate(3deg);
}


@keyframes photoFloat {

    0% {
        top: 110vh;
        opacity: 0;
    }

    8% {
        opacity: .9;
    }

    88% {
        opacity: .9;
    }

    100% {
        top: -35vh;
        opacity: 0;
    }
}


/* =========================================
   LANDING PAGE
========================================= */

.landing {
    position: fixed;
    inset: 0;

    display: flex;
    flex-direction: column;

    justify-content: center;
    align-items: center;

    text-align: center;

    padding: 25px;

    z-index: 15;

    transition:
        opacity .9s ease,
        transform .9s ease,
        filter .9s ease;
}

.landing.hide {
    opacity: 0;

    transform: scale(1.12);

    filter: blur(12px);

    pointer-events: none;
}


.small-text {
    font-size: 12px;

    letter-spacing: 5px;

    color: #d9b9ff;

    margin-bottom: 18px;

    text-shadow:
        0 0 10px #8f43d8;
}


.landing h1 {
    font-size: clamp(40px, 7vw, 78px);

    line-height: .95;

    letter-spacing: 2px;

    text-shadow:
        0 0 12px #b96cff,
        0 0 35px rgba(167,76,255,.7);

    animation: titleGlow 3s ease-in-out infinite;
}

.landing h1 span {
    color: #d79aff;

    animation: pulse 1.5s infinite;
}


.subtitle {
    margin-top: 22px;

    font-size: 18px;

    color: #e8d8ff;
}


.open-button {
    margin-top: 40px;

    padding: 17px 30px;

    border: 1px solid #d9a8ff;

    border-radius: 12px;

    background:
        linear-gradient(
            135deg,
            #7132ce,
            #a74cff
        );

    color: white;

    font-size: 14px;

    font-weight: bold;

    letter-spacing: 1px;

    cursor: pointer;

    box-shadow:
        0 0 20px rgba(165,75,255,.55);

    transition:
        transform .3s ease,
        box-shadow .3s ease;
}

.open-button:hover {
    transform:
        scale(1.08)
        translateY(-4px);

    box-shadow:
        0 0 45px rgba(194,111,255,.9);
}


.hint {
    margin-top: 14px;

    font-size: 11px;

    color: #9f85b8;
}


@keyframes titleGlow {

    0%,
    100% {
        text-shadow:
            0 0 12px #b96cff,
            0 0 35px rgba(167,76,255,.6);
    }

    50% {
        text-shadow:
            0 0 20px #d09aff,
            0 0 55px rgba(190,100,255,.9);
    }
}


@keyframes pulse {

    0%,
    100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.2);
    }
}


/* =========================================
   LETTER OVERLAY
========================================= */

.letter-overlay {
    position: fixed;
    inset: 0;

    display: flex;

    justify-content: center;
    align-items: center;

    padding: 20px;

    z-index: 30;

    background:
        rgba(8,2,15,.58);

    backdrop-filter: blur(8px);

    opacity: 0;

    visibility: hidden;

    transition:
        opacity .7s ease,
        visibility .7s ease;
}

.letter-overlay.show {
    opacity: 1;

    visibility: visible;
}


/* =========================================
   LETTER BOX
========================================= */

.letter-box {
    position: relative;

    width: min(650px, 90vw);

    max-height: 88vh;

    transform:
        translateY(80px)
        scale(.82);

    opacity: 0;

    transition:
        transform .8s cubic-bezier(.2,.8,.2,1),
        opacity .8s ease;
}

.letter-overlay.show .letter-box {
    transform:
        translateY(0)
        scale(1);

    opacity: 1;
}


.letter {
    max-height: 88vh;

    overflow-y: auto;

    padding: 45px;

    border-radius: 22px;

    background:
        linear-gradient(
            145deg,
            #fffaff,
            #f0ddff
        );

    color: #382044;

    border:
        2px solid
        rgba(174,96,255,.6);

    box-shadow:
        0 30px 90px rgba(0,0,0,.65),
        0 0 50px rgba(174,87,255,.4);
}


.letter::-webkit-scrollbar {
    width: 6px;
}

.letter::-webkit-scrollbar-thumb {
    background: #9b51e8;

    border-radius: 10px;
}


.close {
    position: absolute;

    right: -12px;
    top: -12px;

    width: 42px;
    height: 42px;

    border: 2px solid #dfb9ff;

    border-radius: 50%;

    background: #7b38df;

    color: white;

    font-size: 25px;

    cursor: pointer;

    z-index: 40;

    transition:
        transform .25s ease;
}

.close:hover {
    transform:
        rotate(90deg)
        scale(1.1);
}


.decor {
    text-align: center;

    color: #a04ee3;

    font-size: 20px;

    letter-spacing: 8px;
}


.letter h2 {
    margin:
        18px 0 25px;

    text-align: center;

    color: #7138a0;

    font-size:
        clamp(25px, 4vw, 36px);
}


.message {
    font-size: 16px;

    line-height: 1.85;
}

.message p {
    margin-bottom: 17px;
}


.signature {
    margin-top: 28px;

    text-align: right;

    color: #7138a0;

    line-height: 1.6;
}


.bottom {
    margin-top: 25px;

    text-align: center;

    font-size: 22px;

    color: #a04ee3;
}


/* =========================================
   MUSIC BUTTON
========================================= */

.music-button {
    position: fixed;

    right: 22px;
    bottom: 22px;

    width: 52px;
    height: 52px;

    border:
        1px solid
        #dfb7ff;

    border-radius: 50%;

    background:
        linear-gradient(
            135deg,
            #7132ce,
            #a74cff
        );

    color: white;

    font-size: 21px;

    cursor: pointer;

    z-index: 100;

    box-shadow:
        0 0 20px
        rgba(165,75,255,.6);

    transition:
        transform .25s ease,
        box-shadow .25s ease;
}

.music-button:hover {
    transform: scale(1.1);

    box-shadow:
        0 0 35px
        rgba(194,111,255,.9);
}

.music-button.playing {
    animation:
        musicPulse 1.2s infinite;
}

@keyframes musicPulse {

    0%,
    100% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.12);
    }
}


/* =========================================
   MOBILE
========================================= */

@media (max-width: 600px) {

    .photo {
        width: 95px;
    }

    .photo:nth-child(3),
    .photo:nth-child(9) {
        display: none;
    }

    .photo:nth-child(1) {
        left: 1%;
    }

    .photo:nth-child(2) {
        left: 11%;
    }

    .photo:nth-child(4) {
        right: 11%;
    }

    .photo:nth-child(5) {
        right: 1%;
    }

    .photo:nth-child(6) {
        right: 3%;
    }

    .photo:nth-child(7) {
        left: 4%;
    }

    .photo:nth-child(8) {
        right: 4%;
    }

    .landing h1 {
        font-size: 40px;
    }

    .small-text {
        font-size: 8px;

        letter-spacing: 3px;
    }

    .subtitle {
        font-size: 15px;
    }

    .open-button {
        padding:
            14px 20px;

        font-size: 12px;
    }

    .letter {
        padding:
            30px 22px;
    }

    .message {
        font-size: 14px;

        line-height: 1.75;
    }

    .music-button {
        width: 45px;
        height: 45px;

        right: 15px;
        bottom: 15px;

        font-size: 18px;
    }
}

</style>
</head>


<body>


<!-- =========================================
     BACKGROUND
========================================= -->

<div class="background"></div>


<!-- =========================================
     FLOATING HEARTS
========================================= -->

<div id="hearts"></div>


<!-- =========================================
     9 FLOATING PHOTOS
========================================= -->

<div class="photo-wall">
    <img class="photo" src="images/photo1.png" alt="Our memory">
    <img class="photo" src="images/photo2.png" alt="Our memory">
    <img class="photo" src="images/photo3.png" alt="Our memory">
    <img class="photo" src="images/photo4.png" alt="Our memory">
    <img class="photo" src="images/photo5.png" alt="Our memory">
    <img class="photo" src="images/photo6.png" alt="Our memory">
    <img class="photo" src="images/photo7.png" alt="Our memory">
    <img class="photo" src="images/photo8.png" alt="Our memory">
    <img class="photo" src="images/photo9.png" alt="Our memory">
</div>


<audio id="bgMusic" loop>
    <source src="ikaw_at_ako.mp3" type="audio/mpeg">
</audio>

<!-- =========================================
     LANDING PAGE
========================================= -->

<main
    class="landing"
    id="landing">

    <div class="small-text">
        A LITTLE SOMETHING FOR YOU
    </div>


    <h1>

        HAPPY<br>

        MONTHSARY

        <span>💜</span>

    </h1>


    <p class="subtitle">
        For my beautiful Mommy
    </p>


    <button
        class="open-button"
        id="openButton">

        💌 CLICK TO OPEN 💌

    </button>


    <p class="hint">
        Made with love, just for you.
    </p>

</main>


<!-- =========================================
     LETTER
========================================= -->

<section
    class="letter-overlay"
    id="letterOverlay">


    <div class="letter-box">


        <button
            class="close"
            id="closeButton">

            ×

        </button>


        <article class="letter">


            <div class="decor">
                ♡ ✦ ♡
            </div>


            <h2>
                Happy Monthsary, Mommy! 💜
            </h2>


            <div class="message">


                <p>
                    Happy monthsary, Mommy! 💜
                </p>


                <p>
                    I just want to say thank you for every
                    moment we share. Thank you for all the
                    little things, the happy moments, the
                    random conversations, and even the
                    difficult days that taught us to
                    understand each other more.
                </p>


                <p>
                    I know not every day is perfect, but I
                    hope that no matter what happens, we
                    continue to understand, care for, and
                    choose each other.
                </p>


                <p>
                    You are someone very special to me,
                    Mommy, and I am always thankful that
                    I get to make memories with you.
                </p>


                <p>
                    Thank you for the laughter, the memories,
                    the silly moments, and all the little
                    things that make our time together
                    special.
                </p>


                <p>
                    Sorry din moomy for the tampuhan and sa 
                    mga times na feel mo wara ako labot,
                    sa totoo lang nagsungon ako kagabi kay naki
                    baylehan ka na waran paaram.
                </p>


                <p>
                    Here's to another month together,
                    and to many more beautiful memories,
                    smiles, adventures, and moments that
                    we can look back on someday. 💜
                </p>


                <p>
                    I hope this little letter makes you
                    smile, even just a little.
                </p>


                <p>
                    I love you so much, Mommy.
                    Thank you for being you. 🥺💜
                </p>


            </div>


            <div class="signature">

                With all my love,<br>

                <strong>
                    Your Baby 💜
                </strong>

            </div>


            <div class="bottom">
                ♡
            </div>


        </article>


    </div>

</section>


<!-- =========================================
     MUSIC
========================================= -->
   


<button
    class="music-button"
    id="musicButton"
    title="Music">
<audio id="bgMusic" loop>
    <source src="ikaw_at_ako.mp3" type="audio/mp3">
    🎵

</button>


<script>

/* =========================================
   ELEMENTS
========================================= */

const landing =
    document.getElementById("landing");

const openButton =
    document.getElementById("openButton");

const closeButton =
    document.getElementById("closeButton");

const letterOverlay =
    document.getElementById("letterOverlay");

const hearts =
    document.getElementById("hearts");

const bgMusic =
    document.getElementById("bgMusic");

const musicButton =
    document.getElementById("musicButton");


/* =========================================
   MUSIC
========================================= */

bgMusic.volume = 0.35;


/* Try to autoplay when website opens */

window.addEventListener("load", () => {

    bgMusic.play()
        .then(() => {

            musicButton.classList.add("playing");
            musicButton.textContent = "🔊";

        })
        .catch(() => {

            /*
                Browser blocked autoplay.
                Music will start after
                the first user interaction.
            */

            console.log(
                "Autoplay blocked by browser."
            );

        });

});


/* =========================================
   START MUSIC AFTER FIRST CLICK
========================================= */

document.addEventListener(
    "click",
    () => {

        if (bgMusic.paused) {

            bgMusic.play()
                .then(() => {

                    musicButton.classList.add(
                        "playing"
                    );

                    musicButton.textContent =
                        "🔊";

                })
                .catch(() => {});

        }

    },
    { once: true }
);


/* =========================================
   OPEN LETTER
========================================= */

openButton.addEventListener(
    "click",
    () => {

        bgMusic.play()
            .then(() => {

                musicButton.classList.add(
                    "playing"
                );

                musicButton.textContent =
                    "🔊";

            })
            .catch(() => {});


        landing.classList.add("hide");


        setTimeout(() => {

            letterOverlay.classList.add("show");

        }, 250);

    }
);


/* =========================================
   CLOSE LETTER
========================================= */

function closeLetter() {

    letterOverlay.classList.remove("show");

    setTimeout(() => {

        landing.classList.remove("hide");

    }, 300);

}


closeButton.addEventListener(
    "click",
    closeLetter
);


/* =========================================
   CLICK OUTSIDE LETTER
========================================= */

letterOverlay.addEventListener(
    "click",
    (event) => {

        if (event.target === letterOverlay) {

            closeLetter();

        }

    }
);


/* =========================================
   ESC KEY
========================================= */

document.addEventListener(
    "keydown",
    (event) => {

        if (
            event.key === "Escape" &&
            letterOverlay.classList.contains("show")
        ) {

            closeLetter();

        }

    }
);


/* =========================================
   MUSIC BUTTON
========================================= */

musicButton.addEventListener(
    "click",
    (event) => {

        event.stopPropagation();

        if (bgMusic.paused) {

            bgMusic.play()
                .then(() => {

                    musicButton.classList.add(
                        "playing"
                    );

                    musicButton.textContent =
                        "🔊";

                });

        } else {

            bgMusic.pause();

            musicButton.classList.remove(
                "playing"
            );

            musicButton.textContent =
                "🎵";

        }

    }
);


/* =========================================
   FLOATING HEARTS
========================================= */

function createHeart() {

    const heart =
        document.createElement("div");

    heart.className = "heart";

    heart.textContent =
        Math.random() > .5
            ? "♥"
            : "♡";

    heart.style.left =
        Math.random() * 100 + "%";

    heart.style.fontSize =
        10 + Math.random() * 18 + "px";

    const duration =
        7 + Math.random() * 8;

    heart.style.animationDuration =
        duration + "s";

    hearts.appendChild(heart);

    setTimeout(() => {

        heart.remove();

    }, duration * 1000);

}


/* =========================================
   INITIAL HEARTS
========================================= */

for (let i = 0; i < 25; i++) {

    createHeart();

}


/* =========================================
   CONTINUOUS HEARTS
========================================= */

setInterval(
    createHeart,
    650
);

</script>

</body>
</html>
