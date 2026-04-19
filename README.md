# trainingStaffGuide
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Florida State Roleplay • Staff Training</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

:root {
--primary: #00ccff;
--accent: #00ffcc;
--bg: #0a1f3d;
--card: rgba(255,255,255,0.085);
}

* {
margin: 0;
padding: 0;
box-sizing: border-box;
}

body {
font-family: 'Inter', system-ui, sans-serif;
background: linear-gradient(135deg, #0a1f3d 0%, #001122 100%);
color: #e0f0ff;
min-height: 100vh;
line-height: 1.6;
overflow-x: hidden;
}

.header {
background: rgba(10, 31, 61, 0.98);
backdrop-filter: blur(12px);
padding: 18px 20px;
position: sticky;
top: 0;
z-index: 100;
border-bottom: 2px solid var(--primary);
display: flex;
align-items: center;
justify-content: space-between;
box-shadow: 0 4px 20px rgba(0, 204, 255, 0.15);
}

.logo {
font-size: 1.65rem;
font-weight: 700;
color: var(--primary);
letter-spacing: -0.5px;
}

.tab-container {
display: flex;
gap: 12px;
background: rgba(255,255,255,0.08);
padding: 6px;
border-radius: 12px;
}

.tab {
padding: 10px 24px;
border-radius: 10px;
font-weight: 600;
font-size: 0.98rem;
cursor: pointer;
transition: all 0.3s ease;
white-space: nowrap;
}

.tab.active {
background: var(--primary);
color: #001122;
box-shadow: 0 4px 12px rgba(0, 204, 255, 0.4);
}

.main-content {
max-width: 960px;
margin: 24px auto;
padding: 0 20px;
}

.layout {
display: flex;
gap: 24px;
}

.sidebar {
width: 260px;
background: var(--card);
border: 1px solid var(--primary);
border-radius: 16px;
padding: 24px 20px;
height: fit-content;
position: sticky;
top: 100px;
box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}

.sidebar h3 {
color: var(--primary);
margin-bottom: 16px;
font-size: 1.25rem;
}

.sidebar p {
opacity: 0.85;
margin-bottom: 12px;
font-size: 0.95rem;
}

.content-area {
flex: 1;
background: var(--card);
border: 1px solid var(--primary);
border-radius: 16px;
padding: 28px;
box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
}

.page {
display: none;
}

.page.active {
display: block;
}

.section {
background: rgba(255,255,255,0.06);
border: 1px solid rgba(0, 204, 255, 0.25);
border-radius: 14px;
padding: 22px;
margin-bottom: 22px;
}

.section h2 {
color: var(--primary);
margin-bottom: 14px;
font-size: 1.35rem;
border-bottom: 1px solid rgba(0, 204, 255, 0.3);
padding-bottom: 8px;
}

ul {
padding-left: 22px;
margin: 12px 0;
}

li {
margin-bottom: 9px;
opacity: 0.95;
}

.copy-btn {
background: var(--primary);
color: #001122;
border: none;
padding: 12px 24px;
border-radius: 10px;
font-weight: 700;
font-size: 0.95rem;
cursor: pointer;
transition: all 0.3s;
margin-top: 12px;
width: 100%;
box-shadow: 0 4px 12px rgba(0, 204, 255, 0.3);
}

.copy-btn:hover {
background: var(--accent);
transform: translateY(-2px);
}

.copy-btn:active {
transform: scale(0.97);
}

.trainer-note {
margin-top: 30px;
padding: 18px;
background: rgba(0, 100, 150, 0.25);
border: 1px dashed var(--primary);
border-radius: 12px;
font-size: 0.9rem;
color: #a0e0ff;
}

/* Mobile Optimizations */
@media (max-width: 768px) {
.layout {
flex-direction: column;
}
.sidebar {
width: 100%;
position: static;
}
.header {
flex-direction: column;
gap: 16px;
padding: 16px 20px;
}
.tab-container {
width: 100%;
justify-content: center;
}
.main-content {
margin: 16px auto;
padding: 0 16px;
}
.content-area {
padding: 20px;
}
}
</style>
</head>
<body>

<!-- Header -->
<div class="header">
<div class="logo">Florida State Roleplay</div>

<div class="tab-container">
<div class="tab active" id="tab-rules" onclick="switchTab(0)">Rules</div>
<div class="tab" id="tab-guide" onclick="switchTab(1)">Staff Guide</div>
</div>
</div>

<div class="main-content">

<div class="layout">

<!-- Sidebar -->
<div class="sidebar">
<h3>Navigation</h3>
<p>Select a page using the buttons above.</p>
<p><strong>Current Page:</strong> <span id="current-page">Rules Page</span></p>
</div>

<!-- Content Area -->
<div class="content-area">

<!-- Rules Page -->
<div id="rules-page" class="page active">
<h2 style="text-align:center; color:var(--primary); margin-bottom:24px;">Florida State Roleplay Staff Training Rules</h2>

<div class="section">
<h2>Training Rules</h2>
<p>While this training is underway, these rules must be followed at all times.</p>
<p>Excellent spelling, grammar, and punctuation (SPaG) are mandatory. Any immaturity, dishonesty, or disrespect will result in instant dismissal.</p>
<p>You may not go AFK without permission. In a genuine emergency, speak up immediately.</p>
<p>Treat everyone with full respect and listen carefully to all instructions.</p>
<button class="copy-btn" onclick="copySection(this)">Copy Rules Part 1</button>
<button class="copy-btn" onclick="copySection(this)" style="margin-top:8px; background:#0099cc;">Copy Rules Part 2</button>
</div>

<div class="trainer-note">
<strong>Important:</strong> Professionalism is expected from the start of training.
</div>
</div>

<!-- Staff Guide Page -->
<div id="guide-page" class="page">

<h2 style="color:var(--primary); margin-bottom:20px;">Normal Staff Training Guide</h2>

<!-- Opening -->
<div class="section">
<h2>Opening Statement</h2>
<p>PTS is now enabled. Please remain silent until given permission to speak.</p>
<p>Hello everyone. My name is [Full Rank] [Username]. I will be your instructor today. Address me as [Rank] or [Sir/Ma’am]. Do you understand?</p>
<button class="copy-btn" onclick="copySection(this)">Copy Opening</button>
</div>

<!-- Training Rules (Chat) -->
<div class="section">
<h2>Training Rules</h2>
<p>Excellent SPaG is required at all times. Immaturity or disrespect will result in instant dismissal.</p>
<p>You may not go AFK without permission. Respond to questions with “Yes, [Rank].” or “Yes, [Sir/Ma’am].”</p>
<button class="copy-btn" onclick="copySection(this)">Copy Training Rules</button>
</div>

<!-- Control Questions -->
<div class="section">
<h2>Control Questions</h2>
<p>What does RDM mean? What does VDM mean?</p>
<p>What does NITRP stand for? What do MA and AA stand for?</p>
<p>Player Alex kills someone purely for fun. What punishment?</p>
<p>Player Jordan shoots a vehicle until it explodes. What punishment?</p>
<button class="copy-btn" onclick="copySection(this)">Copy Control Questions</button>
</div>

<!-- Core Expectations -->
<div class="section">
<h2>Core Expectations</h2>
<p>Always treat players and staff with respect. Disrespect can lead to infractions.</p>
<p>When issuing a kick, explain the reason clearly. Example: “You are being kicked for [reason]. Wait 30 minutes before rejoining.”</p>
<p>Never use commands like “all” or “others”. Mass commands result in automatic blacklist.</p>
<button class="copy-btn" onclick="copySection(this)">Copy Expectations Part 1</button>
<button class="copy-btn" onclick="copySection(this)" style="margin-top:8px; background:#0099cc;">Copy Expectations Part 2</button>
</div>

<!-- Mod Call Procedure -->
<div class="section">
<h2>Mod Call Procedure</h2>
<p>Greet the player professionally: “Hello! This is [Rank] [Username]. How may I assist you today?”</p>
<p>Before ending, ask: “Is there anything more I can do for you today?”</p>
<p>All actions are handled through Melonly.</p>
<button class="copy-btn" onclick="copySection(this)">Copy Mod Call Procedure</button>
</div>

<!-- Closing -->
<div class="section">
<h2>Closing Statement</h2>
<p>We will now begin the hands-on portion of the training.</p>
<button class="copy-btn" onclick="copySection(this)">Copy Closing</button>
</div>

<div class="trainer-note">
<strong>Trainer Notes (Do Not Read Aloud):</strong><br>
Driving Test: DMV to Florida State Police HQ. Score /10, need 8+ to pass.<br>
Mod Call Simulations: Run at least 4 calls. Provide feedback and mark fail if needed.
</div>
</div>

</div>
</div>
</div>

<script>
function switchTab(tabIndex) {
document.querySelectorAll('.tab').forEach(tab => tab.classList.remove('active'));

if (tabIndex === 0) {
document.getElementById('tab-rules').classList.add('active');
document.getElementById('rules-page').classList.add('active');
document.getElementById('guide-page').classList.remove('active');
document.getElementById('current-page').textContent = 'Rules Page';
} else {
document.getElementById('tab-guide').classList.add('active');
document.getElementById('rules-page').classList.remove('active');
document.getElementById('guide-page').classList.add('active');
document.getElementById('current-page').textContent = 'Staff Guide';
}
}

function copySection(btn) {
const section = btn.parentElement;
let text = '';

// Only copy the p and li elements, keeping each short
section.querySelectorAll('p').forEach(p => {
if (p.textContent.trim().length > 0) {
text += p.textContent.trim() + '\n\n';
}
});

navigator.clipboard.writeText(text.trim()).then(() => {
const originalText = btn.textContent;
btn.textContent = '✅ Copied!';
btn.style.background = '#00ffcc';

setTimeout(() => {
btn.textContent = originalText;
btn.style.background = '';
}, 1800);
});
}

window.onload = () => {
switchTab(0);
};
</script>

</body>
</html>
