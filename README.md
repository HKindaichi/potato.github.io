
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>NeoAI Sentinel</title>
  <link rel="stylesheet" href="style.css">
  <link rel="icon" href="favicon.png" type="image/x-icon">
  <style>
    body {
        margin: 0;
        background-color: black;
        color: #0F0;
        font-family: 'Courier New', Courier, monospace;
        overflow: auto; /* Allow scrolling */
    }
    canvas {
            position: fixed;
            top: 0;
            left: 0;
        }
    #messageContainer {
        font-size: 20px;
        margin: 0;
        padding: 10px;
        border: 2px solid #0F0; /* Green border */
        border-radius: 10px; /* Rounded corners */
        background-color: rgba(0, 0, 0, 0.7); /* Dark background */
        display: inline-block; /* Adjust size to fit text */
        position: absolute; /* Keeps the message in place */
        top: 15px; /* Fixed top distance from the viewport */
        left: 15px; /* Fixed left distance from the viewport */
        z-index: 10; /* Make sure it's visible on top */
        width: auto; /* Width should fit the content */
    }

    .message {
        display: inline-block;
    }

    .typing {
        border-right: 2px solid #0F0;
        animation: blink-caret 0.75s step-end infinite;
    }

    @keyframes blink-caret {
        50% {
            border-color: transparent;
        }
    }
</style>

</head>

<body>
	<div id="messageContainer"></div>
    <script>
        const messageContainer = document.getElementById('messageContainer');
        const message = "Wake up, Neo...";

        function typeMessage(callback) {
            let charIndex = 0;
            const messageElement = document.createElement('div');
            messageElement.classList.add('message', 'typing');
            messageElement.innerHTML = '';
            messageContainer.innerHTML = '';  // Clear previous messages
            messageContainer.appendChild(messageElement);

            const typingInterval = setInterval(() => {
                messageElement.innerHTML += message.charAt(charIndex);
                charIndex++;
                if (charIndex === message.length) {
                    clearInterval(typingInterval);
                    setTimeout(() => {
                        setTimeout(() => {
                            deleteMessage(callback);
                        }, 3000); // Wait for 2 seconds (blinking cursor)
                    }, 5000); // Hold the message for 5 seconds
                }
            }, 100);
        }

        function deleteMessage(callback) {
            const messageElement = messageContainer.lastElementChild;
            let charIndex = message.length;
            const deletingInterval = setInterval(() => {
                messageElement.innerHTML = messageElement.innerHTML.slice(0, -1);
                charIndex--;
                if (charIndex === 0) {
                    clearInterval(deletingInterval);
                    setTimeout(() => {
                        callback(); // Call the typeMessage again
                    }, 2000); // Wait for 2 seconds (blinking cursor)
                }
            }, 100);
        }

        function startConversation() {
            typeMessage(startConversation); // Start the typing and deletion loop
        }

        // Start the conversation when the page loads
        window.onload = startConversation;
    </script>
	<div class="matrix-bg"></div>
    <canvas id="canvas"></canvas>
    
        <div id="content">
        <div class="main-text">
        Not All <span class="green-bold"><strong>A</strong></span><span class="red-bold"><strong>.I</strong></span> Are What They Appear to Be
        </div>
		<div class="bordered-text-ca">
          CA: GkpWd67P5oANfxwnhYETnbEPKuCWurY1eux272kepump
        </div>
		<a href="https://jup.ag/swap/SOL-GkpWd67P5oANfxwnhYETnbEPKuCWurY1eux272kepump" class="button" target="_blank">BUY $NeoAI</a>
		<img src="keanu_front.jpg" alt="Neo AI Logo" class="main-image">
        <div class="bordered-text">
          <span class="green-bold"><strong>NeoAI</strong></span> ($NeoAI) is an <span class="green-bold"><strong>AI Sentinel Agent</strong></span> that helps protect society from <span class="red-bold"><strong>harmful AI agents</strong></span>. It tracks and ranks AI agents based on their behavior, giving a risk score to highlight potential threats. With blockchain and community involvement, <span class="green-bold"><strong>NeoAI</strong></span> ensures transparency and accountability in AI systems.
        </div>
        <div class="bordered-text">
            <span class="green-bold"><strong>Mission: </strong></span> To protect humanity by monitoring and mitigating risks from <span class="red-bold"><strong>harmful AI agents </strong></span>through transparent analysis, ranking, and community engagement. With blockchain and community involvement, <span class="green-bold"><strong>NeoAI</strong></span> is an <span class="green-bold"><strong>AI agent </strong></span>that helps protect society.
          </div>
        
        <div class="social-links">
	    <a href="LITEPAPER v01.pdf" target="_blank">Litepaper</a>
            <a href="https://dexscreener.com/solana/gn2emhb1jyyfvnqpwguawkzvrqitdyc5ghbkazejebgn" target="_blank">Dexscreener</a>
            <a href="https://x.com/NeoAISentinel" target="_blank">X</a>
            <a href="https://t.me/neoai_sentinel" target="_blank">Telegram</a>
	    <a href="https://pump.fun/coin/GkpWd67P5oANfxwnhYETnbEPKuCWurY1eux272kepump" target="_blank">Pumpfun</a>
            </div>
		<section class="team-section">
        <h2>Meet Our Team</h2>
        <div class="team-container">
            <div class="team-member">
                <img src="The Architect.jpg" alt="The Architect">
                <h3>The Architect</h3>
                <p>Designing the Core of Neo AI Agents</p>              
            </div>
            <div class="team-member">
                <img src="The Oracle.jpg" alt="The Oracle">
                <h3>The Oracle</h3>
                <p>Passionate about advancing technology</p>        
          </div>
            <div class="team-member">
                <img src="The Operator.jpg" alt="The Operator">
                <h3>The Operator</h3>
                <p>Bridging the AI and Crypto Worlds</p>              
            </div>
        </div>
			<section class="team-section">
			<h3>Tokenomics</h3>
			<img src="Tokenomicnew.png" alt="Tokenomics" class="tokenomic">
		</section>
		  </section>
		</div>
    <script src="script.js"></script>
	<footer>
        <p>&copy; 2025 NeoAI Sentinel. All rights reserved</p>
        <p>
         
        </p>
    </footer>
</body>
</html>
