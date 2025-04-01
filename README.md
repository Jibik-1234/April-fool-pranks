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
    <p>You’ve been pranked! 😂 Now it's your turn to prank someone else!</p>

    <!-- Prank Image -->
    <img src="7334409_3570349.jpg" alt="Gotcha!">

    <!-- Hidden Audio -->
    <audio id="prankAudio">
        <source src="laugh-like-crazy-257881.mp3" type="audio/mpeg">
    </audio>

    <script>
        document.addEventListener("DOMContentLoaded", function() {
            var audio = document.getElementById("prankAudio");

            // Try autoplaying with user interaction
            var playAudio = function() {
                audio.play().then(() => {
                    console.log("Audio played automatically!");
                }).catch(error => {
                    console.log("Autoplay blocked, retrying...");
                    audio.muted = true; // Start muted to allow autoplay
                    audio.play().then(() => {
                        audio.muted = false; // Unmute after playing starts
                    });
                });
            };

            // Try playing immediately
            playAudio();

            // If autoplay is blocked, try again when user interacts
            document.body.addEventListener("click", playAudio, { once: true });
        });
    </script>
</body>
</html>
