# RESTELICA-
<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body { display: flex; justify-content: center; align-items: center; height: 100vh; font-family: sans-serif; background: #000; color: #fff; }
        #timer { font-size: 3rem; }
    </style>
</head>
<body>
    <div id="timer">Loading...</div>
    <script>
        const targetDate = new Date("Dec 31, 2026 23:59:59").getTime();
        setInterval(() => {
            const now = new Date().getTime();
            const diff = targetDate - now;
            const d = Math.floor(diff / (1000 * 60 * 60 * 24));
            const h = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const m = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
            const s = Math.floor((diff % (1000 * 60)) / 1000);
            document.getElementById("timer").innerHTML = `${d}d ${h}h ${m}m ${s}s`;
        }, 1000);
    </script>
</body>
</html>
