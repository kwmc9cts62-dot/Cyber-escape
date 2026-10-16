<!DOCTYPE html>

<html lang="ar" dir="rtl">

<head>

<meta charset="UTF-8">

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>CYBER ESCAPE</title>

<style>

:root {

  --green: #00ff88;

  --dark: #050a08;

  --panel: #0a1510;

  --red: #ff405c;

}

* {

  box-sizing: border-box;

}

body {

  margin: 0;

  min-height: 100vh;

  background:

    radial-gradient(ellipse at top, #10251a 0%, #050a08 65%);

  color: var(--green);

  font-family: Tahoma, Arial, sans-serif;

  padding: 20px 12px;

}

body::before {

  content: "";

  position: fixed;

  inset: 0;

  pointer-events: none;

  background: repeating-linear-gradient(

    transparent 0px,

    transparent 3px,

    #00ff8805 4px

  );

}

.container {

  position: relative;

  width: 100%;

  max-width: 480px;

  margin: auto;

}

header {

  text-align: center;

  padding: 22px 10px;

  border-bottom: 1px solid #00ff8840;

}

.logo {

  font-size: 11px;

  letter-spacing: 4px;

  color: #78cda0;

}

h1 {

  font-size: 30px;

  letter-spacing: 2px;

  margin: 13px 0 8px;

  text-shadow: 0 0 16px #00ff8870;

}

.subtitle {

  color: #799c87;

  font-size: 12px;

}

.stats {

  display: grid;

  grid-template-columns: repeat(3, 1fr);

  gap: 8px;

  margin: 18px 0;

}

.stat {

  text-align: center;

  padding: 12px 5px;

  background: #0a1510;

  border: 1px solid #00ff8830;

  border-radius: 8px;

}

.stat span {

  display: block;

  font-size: 10px;

  color: #80a890;

  margin-bottom: 8px;

}

.stat strong {

  font-size: 19px;

}

.panel {

  padding: 20px 16px;

  border: 1px solid #00ff8850;

  border-radius: 12px;

  background: #08110c;

  box-shadow: 0 0 25px #00ff880a;

}

.level-label {

  font-size: 11px;

  color: #81b795;

  letter-spacing: 2px;

}

h2 {

  font-size: 21px;

  color: white;

  margin: 13px 0;

}

.description {

  font-size: 13px;

  color: #a0b8a8;

  line-height: 1.9;

}

.riddle {

  margin: 20px 0;

  padding: 18px 12px;

  background: #020704;

  border: 1px dashed #00ff8860;

  border-radius: 8px;

  text-align: center;

  line-height: 2;

  font-size: 15px;

}

.code {

  font-family: monospace;

  font-size: 24px;

  letter-spacing: 5px;

  color: #00ff88;

  direction: ltr;

  margin: 12px 0;

  text-shadow: 0 0 10px #00ff8855;

}

input {

  display: block;

  width: 100%;

  padding: 15px;

  background: #020704;

  border: 1px solid #286d47;

  border-radius: 7px;

  color: white;

  font-size: 18px;

  text-align: center;

  outline: none;

}

input:focus {

  border-color: var(--green);

  box-shadow: 0 0 12px #00ff8825;

}

button {

  padding: 14px;

  border: 1px solid var(--green);

  border-radius: 7px;

  background: var(--green);

  color: #031008;

  font-size: 15px;

  font-weight: bold;

  cursor: pointer;

}

button:active {

  transform: scale(.98);

}

button:disabled {

  opacity: .4;

  cursor: not-allowed;

}

.main-btn {

  width: 100%;

  margin-top: 12px;

}

.secondary-btn {

  background: transparent;

  color: var(--green);

}

#feedback {

  min-height: 30px;

  margin-top: 14px;

  text-align: center;

  font-size: 13px;

  line-height: 1.8;

}

.hint {

  color: #a6a6a6;

  font-size: 12px;

  text-align: center;

  margin-top: 15px;

}

.progress-wrap {

  margin: 18px 0;

}

.progress-info {

  display: flex;

  justify-content: space-between;

  font-size: 11px;

  color: #87ae96;

  margin-bottom: 8px;

}

.progress {

  height: 5px;

  background: #17261c;

  border-radius: 10px;

  overflow: hidden;

}

#progressFill {

  width: 0%;

  height: 100%;

  background: var(--green);

  transition: width .4s;

  box-shadow: 0 0 10px var(--green);

}

.terminal {

  margin-top: 16px;

  padding: 12px;

  background: #020704;

  color: #508b67;

  font-family: monospace;

  font-size: 11px;

  line-height: 2;

  direction: ltr;

  text-align: left;

  overflow-wrap: anywhere;

}

.green { color: var(--green); }

.red { color: var(--red) !important; }

.white { color: white; }

.center {

  text-align: center;

  padding: 24px 5px;

}

.big-icon {

  font-size: 55px;

  margin-bottom: 15px;

}

.hidden {

  display: none !important;

}

footer {

  text-align: center;

  margin: 22px 0 5px;

  color: #45634e;

  font-size: 10px;

  letter-spacing: 1px;

}

@keyframes glow {

  0%, 100% { text-shadow: 0 0 8px #00ff8850; }

  50% { text-shadow: 0 0 22px #00ff88; }

}

.pulse {

  animation: glow 2s infinite;

}

</style>

</head>

<body>

<div class="container">

<header>

  <div class="logo">CLASSIFIED // DIGITAL SYSTEM</div>

  <h1 class="pulse">CYBER ESCAPE</h1>

  <div class="subtitle">أربع مراحل تفصلك عن الخروج من النظام</div>

</header>

<div class="stats">

  <div class="stat">

    <span>الوقت المتبقي</span>

    <strong id="timer">03:00</strong>

  </div>

  <div class="stat">

    <span>المحاولات</span>

    <strong id="attempts">3</strong>

  </div>

  <div class="stat">

    <span>المراحل</span>

    <strong id="levelCount">0/4</strong>

  </div>

</div>

<div class="progress-wrap">

  <div class="progress-info">

    <span>تقدم المهمة</span>

    <span id="progressText">0%</span>

  </div>

  <div class="progress">

    <div id="progressFill"></div>

  </div>

</div>

<section id="welcome" class="panel center">

  <div class="big-icon">⌘</div>

  <h2>هل تستطيع الهروب؟</h2>

  <p class="description">

    تم إغلاق أبواب الغرفة الرقمية.<br>

    حل الألغاز، واكتشف الرموز السرية، وافتح جميع البوابات قبل انتهاء الوقت.

  </p>

  <p class="green">4 مراحل • 180 ثانية • 3 محاولات لكل لغز</p>

  <button class="main-btn" onclick="startGame()">

    ▶ ابدأ المهمة

  </button>

</section>

<section id="game" class="panel hidden">

  <div class="level-label" id="levelLabel">LEVEL 01</div>

  <h2 id="levelTitle">البوابة الأولى</h2>

  <p class="description" id="levelDescription"></p>

  <div class="riddle">

    <div id="riddleText"></div>

    <div class="code" id="codeText"></div>

  </div>

  <label for="answer" class="description">

    أدخل الرمز السري:

  </label>

  <input

    id="answer"

    type="text"

    placeholder="اكتب إجابتك هنا..."

    autocomplete="off"

    autocapitalize="characters"

  >

  <button id="submitBtn" class="main-btn" onclick="checkAnswer()">

    تحقق من الرمز

  </button>

  <div id="feedback" aria-live="polite"></div>

  <button

    id="hintBtn"

    class="main-btn secondary-btn"

    onclick="showHint()"

  >

    💡 تلميح

  </button>

  <div class="hint" id="hintText"></div>

  <div class="terminal" id="terminal">

    &gt; SYSTEM READY<br>

    &gt; WAITING FOR INPUT...

  </div>

</section>

<section id="ending" class="panel center hidden">

  <div class="big-icon" id="endIcon">🏆</div>

  <h2 id="endTitle">تم فتح النظام!</h2>

  <p id="endText" class="description"></p>

  <button class="main-btn" onclick="startGame()">

    ↻ العب مرة ثانية

  </button>

</section>

<footer>

  SIMULATION MODE // GAME ONLY // NO REAL SYSTEM ACCESS

</footer>

</div>

<script>

const levels = [

  {

    title: "البوابة الأولى",

    description: "الأنظمة القديمة تستخدم الأرقام. اكتشف الرقم التالي في التسلسل.",

    riddle: "ما الرقم الذي يكمل النمط؟",

    code: "2 - 4 - 6 - ?",

    answer: "8",

    hint: "أضف 2 في كل مرة.",

    success: "تم فتح البوابة الأولى!"

  },

  {

    title: "شفرة الأرقام",

    description: "كل رقم يمثل ترتيب حرف في الأبجدية الإنجليزية.",

    riddle: "فك الشفرة واكتب الكلمة الناتجة:",

    code: "3 - 1 - 20",

    answer: "CAT",

    hint: "A = 1، B = 2، C = 3... اقرأ الأرقام كحروف.",

    success: "تم فك الشفرة بنجاح!"

  },

  {

    title: "المصفوفة السرية",

    description: "ركز في النمط المنطقي، فكل صف يتبع قاعدة بسيطة.",

    riddle: "ما الرقم المفقود؟",

    code: "3, 6, 12, 24, ?",

    answer: "48",

    hint: "كل رقم يساوي ضعف الرقم الذي قبله.",

    success: "المصفوفة أصبحت تحت سيطرتك!"

  },

  {

    title: "الرمز النهائي",

    description: "هذه آخر بوابة. فك ترتيب الحروف لتحصل على كلمة تقنية معروفة.",

    riddle: "رتب الحروف لتكوين كلمة تعني نظامًا أو نمطًا:",

    code: "X - I - R - T - A - M",

    answer: "MATRIX",

    hint: "تبدأ بحرف M وتنتهي بحرف X. الحروف الستة أمامك.",

    success: "تم فتح البوابة الأخيرة!"

  }

];

let currentLevel = 0;

let attemptsLeft = 3;

let secondsLeft = 180;

let timerInterval = null;

let running = false;

let locked = false;

let completed = 0;

let hintUsed = false;

const $ = id => document.getElementById(id);

function startGame() {

  clearInterval(timerInterval);

  currentLevel = 0;

  attemptsLeft = 3;

  secondsLeft = 180;

  completed = 0;

  running = true;

  locked = false;

  $("welcome").classList.add("hidden");

  $("ending").classList.add("hidden");

  $("game").classList.remove("hidden");

  $("timer").classList.remove("red");

  $("attempts").classList.remove("red");

  updateStats();

  loadLevel();

  timerInterval = setInterval(() => {

    if (!running) return;

    secondsLeft--;

    updateStats();

    if (secondsLeft <= 0) {

      finishGame(false, "انتهى الوقت!");

    }

  }, 1000);

}

function loadLevel() {

  locked = false;

  hintUsed = false;

  const level = levels[currentLevel];

  $("levelLabel").textContent =

    "LEVEL " + String(currentLevel + 1).padStart(2, "0");

  $("levelTitle").textContent = level.title;

  $("levelDescription").textContent = level.description;

  $("riddleText").textContent = level.riddle;

  $("codeText").textContent = level.code;

  $("answer").value = "";

  $("answer").disabled = false;

  $("submitBtn").disabled = false;

  $("submitBtn").textContent = "تحقق من الرمز";

  $("hintBtn").disabled = false;

  $("hintText").textContent = "";

  $("feedback").textContent = "";

  $("feedback").className = "";

  $("terminal").innerHTML =

    "&gt; CONNECTION ESTABLISHED<br>" +

    "&gt; LEVEL " + (currentLevel + 1) + " LOADED<br>" +

    "&gt; AWAITING SECRET CODE...";

  $("answer").focus();

  updateStats();

}

function updateStats() {

  const mins = Math.floor(secondsLeft / 60);

  const secs = secondsLeft % 60;

  $("timer").textContent =

    String(mins).padStart(2, "0") + ":" +

    String(secs).padStart(2, "0");

  $("attempts").textContent = attemptsLeft;

  $("levelCount").textContent = completed + "/4";

  const progress = Math.round(completed / levels.length * 100);

  $("progressText").textContent = progress + "%";

  $("progressFill").style.width = progress + "%";

  if (secondsLeft <= 30) {

    $("timer").classList.add("red");

  }

  if (attemptsLeft <= 1) {

    $("attempts").classList.add("red");

  }

}

function checkAnswer() {

  if (!running || locked) return;

  const input = $("answer").value.trim().toUpperCase();

  if (!input) {

    $("feedback").textContent = "اكتب الرمز أولًا!";

    $("feedback").className = "red";

    return;

  }

  const level = levels[currentLevel];

  if (input === level.answer) {

    completed++;

    locked = true;

    $("feedback").textContent = "✓ " + level.success;

    $("feedback").className = "green";

    $("terminal").innerHTML +=

      "<br>&gt; ACCESS GRANTED<br>&gt; CODE ACCEPTED";

    $("answer").disabled = true;

    $("submitBtn").disabled = true;

    $("hintBtn").disabled = true;

    updateStats();

    if (completed === levels.length) {

      setTimeout(() => finishGame(true), 1000);

    } else {

      $("submitBtn").textContent = "الانتقال للمرحلة التالية";

      $("submitBtn").disabled = false;

      $("submitBtn").onclick = nextLevel;

    }

  } else {

    attemptsLeft--;

    updateStats();

    $("feedback").textContent =

      "✗ الرمز غير صحيح! المحاولات المتبقية: " + attemptsLeft;

    $("feedback").className = "red";

    $("terminal").innerHTML += "<br>&gt; INVALID CODE";

    if (attemptsLeft <= 0) {

      locked = true;

      $("answer").disabled = true;

      $("submitBtn").disabled = true;

      $("hintBtn").disabled = true;

      $("feedback").textContent =

        "انتهت المحاولات! ستُعاد المرحلة من البداية.";

      $("submitBtn").textContent = "إعادة المرحلة";

      $("submitBtn").disabled = false;

      $("submitBtn").onclick = retryLevel;

    }

  }

}

function nextLevel() {

  if (!running) return;

  $("submitBtn").onclick = checkAnswer;

  currentLevel++;

  attemptsLeft = 3;

  loadLevel();

}

function retryLevel() {

  if (!running) return;

  $("submitBtn").onclick = checkAnswer;

  attemptsLeft = 3;

  loadLevel();

}

function showHint() {

  if (!running || hintUsed || locked) return;

  hintUsed = true;

  $("hintText").textContent = "💡 " + levels[currentLevel].hint;

  $("hintBtn").disabled = true;

}

function finishGame(won, customTitle) {

  running = false;

  locked = true;

  clearInterval(timerInterval);

  $("game").classList.add("hidden");

  $("ending").classList.remove("hidden");

  if (won) {

    $("endIcon").textContent = "🏆";

    $("endTitle").textContent = "تم الهروب بنجاح!";

    $("endText").textContent =

      "أسطورة! فتحت جميع البوابات الأربع. " +

      "الوقت المتبقي: " +

      $("timer").textContent +

      ". نتيجتك: " + completed + "/4.";

  } else {

    $("endIcon").textContent = "🔒";

    $("endTitle").textContent = customTitle || "انتهت المهمة";

    $("endText").textContent =

      "لم تتمكن من فتح جميع البوابات هذه المرة. " +

      "جرّب مرة أخرى واكتشف الرموز السرية!";

  }

}

$("answer").addEventListener("keydown", function(event) {

  if (event.key === "Enter") {

    if ($("submitBtn").textContent === "الانتقال للمرحلة التالية") {

      nextLevel();

    } else if ($("submitBtn").textContent === "إعادة المرحلة") {

      retryLevel();

    } else {

      checkAnswer();

    }

  }

});

</script>

</body>

    </html> 
