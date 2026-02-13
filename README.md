@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&family=Amiri:wght@700&display=swap');

:root {
    --primary: #ff2e63;
    --secondary: #ff758f;
}

body {
    margin: 0;
    padding: 0;
    background: linear-gradient(-45deg, #0f0c29, #302b63, #24243e, #4b1212);
    background-size: 400% 400%;
    animation: gradientBG 15s ease infinite;
    color: #fff;
    font-family: 'Cairo', sans-serif;
    overflow-x: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

@keyframes gradientBG {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.main-card {
    background: rgba(255, 255, 255, 0.07);
    backdrop-filter: blur(20px);
    border: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 40px;
    padding: 40px;
    max-width: 650px;
    text-align: center;
    box-shadow: 0 25px 50px rgba(0,0,0,0.5);
    z-index: 5;
    margin: 20px;
    animation: slideUp 1.5s ease;
}

@keyframes slideUp {
    from { opacity: 0; transform: translateY(50px); }
    to { opacity: 1; transform: translateY(0); }
}

.photo-gallery {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 30px;
}

.photo-gallery img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 4px solid var(--primary);
    object-fit: cover;
    transition: 0.5s;
    box-shadow: 0 0 20px rgba(255, 46, 99, 0.4);
}

.photo-gallery img:hover {
    transform: scale(1.15) rotate(5deg);
    border-color: #fff;
}

h1 {
    font-family: 'Amiri', serif;
    font-size: 2.8rem;
    color: var(--secondary);
    text-shadow: 2px 2px 10px rgba(0,0,0,0.3);
    margin-bottom: 25px;
}

.message-box {
    font-size: 1.2rem;
    line-height: 1.9;
    background: rgba(0, 0, 0, 0.3);
    padding: 25px;
    border-radius: 20px;
    border-right: 5px solid var(--primary);
}

.btn-love {
    background: linear-gradient(45deg, var(--primary), var(--secondary));
    color: white;
    border: none;
    padding: 15px 40px;
    border-radius: 50px;
    font-size: 1.2rem;
    font-weight: bold;
    cursor: pointer;
    margin-top: 30px;
    transition: 0.3s;
    box-shadow: 0 10px 20px rgba(255, 46, 99, 0.3);
}

.btn-love:hover {
    transform: scale(1.1);
    box-shadow: 0 15px 30px rgba(255, 46, 99, 0.5);
}

.floating-heart {
    position: fixed;
    top: -10%;
    font-size: 24px;
    color: var(--primary);
    pointer-events: none;
    z-index: 1;
    animation: fall linear forwards;
}

@keyframes fall {
    to { transform: translateY(110vh) rotate(360deg); }
}

.particle {
    position: absolute;
    pointer-events: none;
    z-index: 100;
    animation: explode 1.5s ease-out forwards;
}

@keyframes explode {
    0% { transform: scale(1) translate(0, 0); opacity: 1; }
    100% { transform: scale(0) translate(var(--dx), var(--dy)); opacity: 0; }
}
