<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>April Fool!</title>
    <style>
        body { 
            text-align: center; 
            font-family: Arial, sans-serif; 
            background-color: #ffeb3b; 
        }
        h1 { 
            font-size: 50px; 
            margin-top: 20%; 
        }
        img { 
            width: 300px; 
            margin-top: 20px; 
            border-radius: 10px; 
        }
    </style>
</head>
<body>
    <h1>🎉 APRIL FOOLS! 🎉</h1>
    <p>You really thought there was a secret study hack? 😂</p>

    <!-- Prank Image -->
    <img src="7334409_3570349.jpg" alt="Gotcha!">

    <!-- Hidden Audio -->
    <audio id="prankAudio">
        <source src="laugh-like-crazy-257881.mp3" type="audio/mpeg">
    </audio>

    <!-- Hidden Play Button (Auto-Clicks to Enable Audio) -->
    <button id="hiddenPlay" style="display:none;">Play</button>

    <script>
        window.onload = function() {
            var audio = document.getElementById("prankAudio");

            // Try to play automatically
            audio.play().catch(function(error) {
                console.log("Autoplay blocked, requiring interaction");

                // Show a button if autoplay is blocked
                var btn = document.getElementById("hiddenPlay");
                btn.style.display = "block";
                btn.onclick = function() {
                    audio.play();
                    btn.style.display = "none"; // Hide after playing
                };
            });
        };
    </script>
</body>
</html>
