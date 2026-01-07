🎁 HBD Love — Birthday Surprise Web Page

A cute birthday surprise web page featuring an animated blooming tree on canvas, a typewriter-style love message, and background music autoplay/play-on-click support.

✨ Features

🌸 Canvas-based animated “love tree” bloom effect

⌨️ Typewriter animation for the birthday message

🎵 Background music (aud.mp3) with autoplay + click-to-play fallback

⏳ Clock text placeholder (can be customized)

📁 Project Structure

Make sure your files are arranged like this:

project/
├─ index.html
├─ aud.mp3
└─ file/
   ├─ default.css
   ├─ jquery.min.js
   ├─ jscex.min.js
   ├─ jscex-parser.js
   ├─ jscex-jit.js
   ├─ jscex-builderbase.min.js
   ├─ jscex-async.min.js
   ├─ jscex-async-powerpack.min.js
   ├─ function.js
   └─ love.js


index.html references assets using file/... paths, so keep the folder name exactly file.

🚀 How to Run (Recommended)

Modern browsers often block autoplay audio unless the user interacts with the page.
For best results, run the page using a local server.

Option A: VS Code Live Server

Open the project folder in VS Code

Install Live Server

Right-click index.html → Open with Live Server

Option B: Python Simple Server

In the project folder terminal:

Python 3

Run: python -m http.server 8000

Open: http://localhost:8000

🎵 Audio Notes (Important)

The page includes <audio autoplay> but most browsers require a click before audio can play.

This project already includes a fallback:

Click on the canvas/seed area triggers playAudio().

If audio doesn’t start automatically, just click anywhere on the canvas.

✍️ Customize the Message

Edit the message lines inside:

<div id="code">
  <span class="say">...</span><br>
</div>


You can change the sender name, emojis, or add/remove lines.

⏳ Customize the Clock Text

Currently it shows:

<span id="clock">577 days 0 hours 0 minutes 0 seconds</span>


You can manually change this text, or update the JS in function.js/love.js (depending on where the clock logic exists) to calculate from a real date.

🌸 Customize the Animation

The tree animation parameters are configured in the opts object inside index.html:

seed controls starting position and scale

branch defines the tree structure

bloom controls the number of flowers

footer controls movement speed

If you want the animation to fit mobile better, reduce:

canvas width/height

bloom num

✅ Browser Support

Works best on:

Google Chrome (latest)

Mozilla Firefox (latest)

If canvas is not supported, the page shows a warning suggesting Chrome/Firefox.

📌 Credits / Libraries Used

jQuery

Jscex async animation libraries

Custom animation scripts: function.js, love.js

📄 License

Personal use only (birthday surprise / greeting page).
If you plan to reuse commercially, review the licenses of included libraries and assets.

<img width="1033" height="604" alt="image" src="https://github.com/user-attachments/assets/5dd75b0f-c294-4183-91aa-f1958f26c195" />
