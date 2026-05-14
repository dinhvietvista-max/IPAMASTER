<!DOCTYPE html>
<html lang="vi" data-theme="light">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Vista IPA & Pronunciation Trainer - Bảng IPA, lý thuyết ngữ âm và luyện bài phát âm/trọng âm theo cấu trúc thi vào 10 THPT." />
  <title>Vista IPA & Pronunciation Trainer</title>
  <style>
    :root {
      --orange:#f97316;
      --orange2:#fb923c;
      --dark:#0f172a;
      --text:#1e293b;
      --muted:#64748b;
      --card:rgba(255,255,255,.95);
      --soft:#f8fafc;
      --border:#e2e8f0;
      --green:#16a34a;
      --greenSoft:#dcfce7;
      --red:#dc2626;
      --redSoft:#fee2e2;
      --yellow:#f59e0b;
      --shadow:0 18px 45px rgba(15,23,42,.10);
    }

    [data-theme="dark"] {
      --dark:#f8fafc;
      --text:#e2e8f0;
      --muted:#94a3b8;
      --card:rgba(15,23,42,.95);
      --soft:#111827;
      --border:#334155;
      --shadow:0 18px 45px rgba(0,0,0,.32);
    }

    * { box-sizing:border-box; }

    body {
      margin:0;
      font-family:Arial, Helvetica, sans-serif;
      color:var(--text);
      min-height:100vh;
      background:
        radial-gradient(circle at top left,rgba(249,115,22,.16),transparent 34%),
        radial-gradient(circle at 90% 5%,rgba(59,130,246,.10),transparent 28%),
        linear-gradient(135deg,#fff7ed 0%,#fff 45%,#eff6ff 100%);
    }

    [data-theme="dark"] body {
      background:
        radial-gradient(circle at top left,rgba(249,115,22,.16),transparent 34%),
        radial-gradient(circle at 90% 5%,rgba(59,130,246,.12),transparent 28%),
        linear-gradient(135deg,#020617,#0f172a 55%,#111827);
    }

    header {
      padding:14px 18px;
      background:var(--card);
      border-bottom:1px solid var(--border);
      backdrop-filter:blur(14px);
      position:relative;
      z-index:10;
    }

    .header-inner {
      max-width:1240px;
      margin:auto;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:16px;
      flex-wrap:wrap;
    }

    .brand {
      display:flex;
      align-items:center;
      gap:12px;
      min-width:0;
    }

    .logo {
      width:46px;
      height:46px;
      border-radius:17px;
      background:linear-gradient(135deg,var(--orange),var(--orange2));
      color:#fff;
      display:grid;
      place-items:center;
      font-weight:900;
      font-size:22px;
      box-shadow:0 10px 25px rgba(249,115,22,.25);
      flex:none;
    }

    h1 {
      margin:0;
      color:var(--dark);
      font-size:clamp(22px,3vw,34px);
      line-height:1.1;
      letter-spacing:-.7px;
    }

    .subtitle {
      margin:4px 0 0;
      color:var(--muted);
      font-size:14px;
      line-height:1.4;
    }

    button, select, input { font-family:inherit; }

    button {
      border:0;
      cursor:pointer;
      border-radius:999px;
      padding:10px 14px;
      font-weight:900;
      font-size:14px;
      transition:.18s ease;
      user-select:none;
    }

    button:hover { filter:brightness(.98); transform:translateY(-1px); }
    button:active { transform:scale(.98); }
    button:disabled { opacity:.74; cursor:not-allowed; }

    .primary {
      background:linear-gradient(135deg,var(--orange),var(--orange2));
      color:#fff;
      box-shadow:0 10px 24px rgba(249,115,22,.22);
    }

    .secondary {
      background:var(--soft);
      color:var(--text);
      border:1px solid var(--border);
    }

    .danger {
      background:var(--redSoft);
      color:#991b1b;
      border:1px solid #fecaca;
    }

    main {
      max-width:1240px;
      margin:16px auto 56px;
      padding:0 18px;
    }

    .stats {
      display:grid;
      grid-template-columns:repeat(4,1fr);
      gap:12px;
      margin-bottom:14px;
    }

    .stat {
      background:var(--card);
      border:1px solid var(--border);
      border-radius:22px;
      padding:14px;
      box-shadow:0 10px 28px rgba(15,23,42,.06);
    }

    .stat b {
      display:block;
      color:var(--orange);
      font-size:24px;
      line-height:1;
      margin-bottom:5px;
    }

    .stat span {
      font-size:13px;
      color:var(--muted);
    }

    .tabs {
      display:flex;
      gap:8px;
      flex-wrap:wrap;
      margin-bottom:14px;
    }

    .tab {
      background:var(--card);
      border:1px solid var(--border);
      color:var(--text);
    }

    .tab.active {
      background:var(--orange);
      border-color:var(--orange);
      color:white;
    }

    .layout {
      display:grid;
      grid-template-columns:320px 1fr;
      gap:16px;
      align-items:start;
    }

    .panel, .card {
      background:var(--card);
      border:1px solid var(--border);
      border-radius:28px;
      box-shadow:var(--shadow);
    }

    .panel {
      padding:16px;
      position:sticky;
      top:16px;
    }

    .card { padding:20px; }

    .panel h2, .card h2 {
      margin:0 0 14px;
      color:var(--dark);
      font-size:20px;
    }

    .field {
      display:block;
      margin:13px 0 7px;
      font-size:13px;
      font-weight:900;
      color:var(--dark);
    }

    select, input {
      width:100%;
      border:1px solid var(--border);
      background:var(--soft);
      color:var(--text);
      border-radius:15px;
      padding:11px 12px;
      outline:none;
      font-size:14px;
    }

    select:focus, input:focus {
      border-color:#fdba74;
      box-shadow:0 0 0 4px rgba(249,115,22,.14);
    }

    .btn-grid {
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:9px;
      margin-top:13px;
    }

    .score-box {
      margin-top:14px;
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:8px;
    }

    .score {
      border:1px solid var(--border);
      background:var(--soft);
      border-radius:16px;
      padding:10px 6px;
      text-align:center;
    }

    .score b {
      display:block;
      color:var(--orange);
      font-size:20px;
    }

    .score span {
      font-size:12px;
      color:var(--muted);
    }

    .mini-note {
      margin:12px 0 0;
      color:var(--muted);
      font-size:13px;
      line-height:1.5;
    }

    .view { display:none; }

    .view.active {
      display:block;
      animation:fadeIn .22s ease;
    }

    @keyframes fadeIn {
      from { opacity:0; transform:translateY(8px); }
      to { opacity:1; transform:translateY(0); }
    }

    .section-title {
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:12px;
      flex-wrap:wrap;
      margin-bottom:14px;
    }

    .section-title p {
      margin:4px 0 0;
      color:var(--muted);
      line-height:1.45;
      font-size:14px;
    }

    .ipa-grid, .theory-grid {
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:14px;
    }

    .ipa-card, .theory-card {
      background:var(--card);
      border:1px solid var(--border);
      border-radius:22px;
      padding:17px;
      box-shadow:0 10px 25px rgba(15,23,42,.06);
      position:relative;
      overflow:hidden;
    }

    .ipa-card:after {
      content:"";
      position:absolute;
      width:120px;
      height:120px;
      border-radius:50%;
      right:-50px;
      top:-50px;
      background:rgba(249,115,22,.08);
    }

    .ipa-symbol {
      position:relative;
      z-index:1;
      font-size:42px;
      line-height:1;
      font-weight:900;
      color:var(--orange);
      margin-bottom:8px;
    }

    .ipa-card h3, .theory-card h3 {
      position:relative;
      z-index:1;
      margin:0 0 8px;
      color:var(--dark);
      font-size:18px;
    }

    .ipa-card p, .theory-card p, .theory-card li {
      position:relative;
      z-index:1;
      color:var(--muted);
      line-height:1.5;
      font-size:14px;
    }

    .ipa-guide {
      position:relative;
      z-index:1;
      background:var(--soft);
      border:1px solid var(--border);
      border-radius:15px;
      padding:10px;
      line-height:1.5;
      color:var(--muted);
      font-size:14px;
    }

    .ipa-guide b { color:var(--orange); }

    .word-list {
      position:relative;
      z-index:1;
      background:#fff7ed;
      border:1px solid #fed7aa;
      color:#7c2d12;
      border-radius:15px;
      padding:10px;
      margin-top:10px;
      line-height:1.5;
      font-size:13px;
    }

    [data-theme="dark"] .word-list {
      background:rgba(249,115,22,.12);
      color:#fdba74;
    }

    .sound-actions {
      position:relative;
      z-index:1;
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:8px;
      margin-top:11px;
    }

    .sound-actions button { font-size:13px; padding:9px 8px; }

    .rule {
      background:var(--soft);
      border:1px solid var(--border);
      border-radius:15px;
      padding:10px;
      margin:10px 0;
      font-weight:800;
      color:var(--text);
    }

    .practice-box {
      background:linear-gradient(135deg,#fff7ed,#fff);
      border:1px solid #fed7aa;
      border-radius:26px;
      padding:22px;
      margin-bottom:14px;
    }

    [data-theme="dark"] .practice-box {
      background:linear-gradient(135deg,rgba(249,115,22,.14),rgba(15,23,42,.7));
    }

    .badge {
      display:inline-flex;
      align-items:center;
      border-radius:999px;
      padding:7px 10px;
      font-size:12px;
      font-weight:900;
      background:var(--soft);
      color:var(--muted);
      border:1px solid var(--border);
    }

    .badge.orange {
      background:#fff7ed;
      color:#c2410c;
      border-color:#fed7aa;
    }

    .question {
      font-size:clamp(20px,2.6vw,30px);
      font-weight:900;
      line-height:1.35;
      color:var(--dark);
      margin-top:10px;
    }

    .prompt {
      color:var(--muted);
      margin-top:8px;
      line-height:1.45;
    }

    .options {
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:11px;
      margin:14px 0;
    }

    .option {
      background:var(--soft);
      border:1px solid var(--border);
      border-radius:18px;
      text-align:left;
      line-height:1.45;
      font-weight:900;
      color:var(--text);
      padding:15px;
      min-height:70px;
    }

    .option.correct {
      background:var(--greenSoft);
      color:#166534;
      border-color:#86efac;
    }

    .option.wrong {
      background:var(--redSoft);
      color:#991b1b;
      border-color:#fecaca;
    }

    .answer {
      display:none;
      border:1px solid #bbf7d0;
      background:#f0fdf4;
      color:#166534;
      border-radius:20px;
      padding:14px;
      line-height:1.55;
      margin-top:12px;
    }

    .answer.show { display:block; }
    .answer b { color:#0f172a; }

    .word u {
      text-decoration:underline;
      text-decoration-thickness:3px;
      text-underline-offset:3px;
      color:var(--orange);
      font-weight:900;
    }

    .exam-grid {
      display:grid;
      gap:12px;
    }

    .exam-item {
      background:var(--card);
      border:1px solid var(--border);
      border-radius:20px;
      padding:15px;
    }

    .exam-item h3 {
      margin:0 0 10px;
      color:var(--dark);
      font-size:16px;
      line-height:1.45;
    }

    .exam-options {
      display:grid;
      grid-template-columns:repeat(2,1fr);
      gap:8px;
    }

    .exam-options button {
      border-radius:14px;
      padding:10px;
      background:var(--soft);
      color:var(--text);
      border:1px solid var(--border);
      text-align:left;
    }

    .exam-options button.selected {
      background:var(--orange);
      color:white;
      border-color:var(--orange);
    }

    .exam-options button.correct {
      background:var(--greenSoft);
      color:#166534;
      border-color:#86efac;
    }

    .exam-options button.wrong {
      background:var(--redSoft);
      color:#991b1b;
      border-color:#fecaca;
    }

    .exam-result {
      display:none;
      margin-bottom:14px;
      padding:14px;
      border-radius:18px;
      background:#f0fdf4;
      border:1px solid #bbf7d0;
      color:#166534;
      font-weight:800;
      line-height:1.55;
    }

    .exam-result.show { display:block; }

    .toast {
      position:fixed;
      right:18px;
      bottom:18px;
      background:var(--dark);
      color:white;
      padding:12px 14px;
      border-radius:16px;
      box-shadow:var(--shadow);
      opacity:0;
      transform:translateY(8px);
      pointer-events:none;
      transition:.25s ease;
      z-index:99;
      max-width:320px;
      font-weight:800;
      line-height:1.45;
    }

    .toast.show {
      opacity:1;
      transform:translateY(0);
    }

    @media(max-width:960px) {
      .layout { grid-template-columns:1fr; }
      .panel { position:static; }
      .stats { grid-template-columns:repeat(2,1fr); }
      .subtitle { display:none; }
    }

    @media(max-width:640px) {
      header { padding:12px 14px; }
      main { padding:0 12px; }
      .stats, .btn-grid, .score-box, .options, .exam-options, .sound-actions { grid-template-columns:1fr; }
      .logo { width:38px; height:38px; border-radius:13px; }
      .header-inner { align-items:flex-start; }
      .tab { flex:1 1 auto; }
      .card, .panel { padding:14px; }
    }
  </style>
</head>
<body>
  <header>
    <div class="header-inner">
      <div class="brand">
        <div class="logo">V</div>
        <div>
          <h1>Vista IPA & Pronunciation Trainer</h1>
          <p class="subtitle">Bảng IPA · cách đọc phiên âm · từ mẫu · lý thuyết dạng bài · luyện đề ngữ âm vào 10</p>
        </div>
      </div>
      <div>
        <button class="secondary" onclick="toggleTheme()">🌓 Sáng/Tối</button>
        <button class="primary" onclick="showView('practice')">Luyện ngay</button>
      </div>
    </div>
  </header>

  <main>
    <div class="stats">
      <div class="stat"><b id="statSounds">0</b><span>Âm IPA trọng tâm</span></div>
      <div class="stat"><b id="statQuestions">0</b><span>Câu hỏi luyện tập</span></div>
      <div class="stat"><b id="statCorrect">0</b><span>Câu đúng</span></div>
      <div class="stat"><b id="statAccuracy">0%</b><span>Tỉ lệ chính xác</span></div>
    </div>

    <div class="tabs">
      <button class="tab active" data-view="ipa" onclick="showView('ipa')">🔤 Bảng IPA</button>
      <button class="tab" data-view="theory" onclick="showView('theory')">📘 Lý thuyết dạng bài</button>
      <button class="tab" data-view="practice" onclick="showView('practice')">🧠 Luyện tập theo đề</button>
    </div>

    <div class="layout">
      <aside class="panel">
        <h2>⚙️ Bộ lọc học tập</h2>

        <label class="field" for="soundGroup">Nhóm âm IPA</label>
        <select id="soundGroup" onchange="renderIpaChart()">
          <option value="all">Tất cả âm IPA</option>
          <option value="vowel">Nguyên âm đơn</option>
          <option value="diphthong">Nguyên âm đôi</option>
          <option value="consonant">Phụ âm</option>
        </select>

        <label class="field" for="questionTypeSelect">Dạng bài luyện tập</label>
        <select id="questionTypeSelect" onchange="refreshPractice()">
          <option value="all">Cả 2 dạng</option>
          <option value="sound">Dạng 1: Gạch chân phát âm khác</option>
          <option value="stress">Dạng 2: Trọng âm khác</option>
        </select>

        <label class="field" for="gradeSelect">Từ vựng theo khối</label>
        <select id="gradeSelect" onchange="refreshPractice()">
          <option value="all">Lớp 7, 8, 9</option>
          <option value="7">Lớp 7</option>
          <option value="8">Lớp 8</option>
          <option value="9">Lớp 9</option>
        </select>

        <label class="field" for="searchInput">Tìm âm/từ khóa</label>
        <input id="searchInput" placeholder="VD: /iː/, sheep, -ed, pollution..." oninput="refreshAll()" />

        <label class="field" for="examSize">Số câu đề luyện</label>
        <select id="examSize">
          <option value="10">10 câu</option>
          <option value="20" selected>20 câu</option>
          <option value="40">40 câu</option>
        </select>

        <div class="btn-grid">
          <button class="primary" onclick="newQuestion()">🎲 Random</button>
          <button class="secondary" onclick="showAnswer()">👀 Đáp án</button>
          <button class="secondary" onclick="createExam(true)">📝 Tạo đề</button>
          <button class="danger" onclick="resetScore()">↺ Xóa điểm</button>
        </div>

        <div class="score-box">
          <div class="score"><b id="correctCount">0</b><span>Đúng</span></div>
          <div class="score"><b id="wrongCount">0</b><span>Sai</span></div>
          <div class="score"><b id="accuracyCount">0%</b><span>Tỉ lệ</span></div>
        </div>

        <p class="mini-note">Ngân hàng hiện có 100 câu luyện tập: 50 câu phát âm phần gạch chân và 50 câu trọng âm. App vẫn giữ đúng 3 phần: IPA, lý thuyết, luyện đề.</p>
      </aside>

      <section>
        <div id="ipaView" class="view active">
          <div class="card">
            <div class="section-title">
              <div>
                <h2>🔤 Bảng phiên âm quốc tế IPA</h2>
                <p>Học ký hiệu IPA, cách đặt khẩu hình, cách đọc phiên âm và nghe từ mẫu. Bấm “Nghe từ” để trình duyệt đọc từ mẫu.</p>
              </div>
            </div>
            <div id="ipaGrid" class="ipa-grid"></div>
          </div>
        </div>

        <div id="theoryView" class="view">
          <div class="card">
            <div class="section-title">
              <div>
                <h2>📘 Lý thuyết về các dạng bài tập ngữ âm</h2>
                <p>Tập trung 2 dạng thường gặp trong cấu trúc đề thi vào 10: phần gạch chân phát âm khác và trọng âm khác.</p>
              </div>
            </div>
            <div id="theoryGrid" class="theory-grid"></div>
          </div>
        </div>

        <div id="practiceView" class="view">
          <div class="card">
            <div class="section-title">
              <div>
                <h2>🧠 Luyện tập theo cấu trúc đề thi</h2>
                <p>Chọn đáp án A/B/C/D, app tự chấm và hiện giải thích. Phím tắt: 1-4 chọn đáp án, Enter sang câu mới, H xem đáp án.</p>
              </div>
            </div>

            <div class="practice-box">
              <span class="badge orange" id="questionType">Dạng bài</span>
              <div class="question" id="questionText">Đang tải câu hỏi...</div>
              <div class="prompt" id="questionPrompt">Chọn đáp án đúng nhất.</div>
            </div>

            <div id="optionBox" class="options"></div>
            <div id="answerBox" class="answer"></div>

            <div class="btn-grid">
              <button class="primary" onclick="newQuestion()">Câu tiếp theo</button>
              <button class="secondary" onclick="speakCurrent()">🔊 Đọc từ</button>
            </div>

            <hr style="border:0;border-top:1px solid var(--border);margin:20px 0">

            <div class="section-title">
              <div>
                <h2>📝 Đề luyện nhanh</h2>
                <p>Tạo đề 10/20/40 câu theo bộ lọc hiện tại, rồi nộp bài để chấm điểm.</p>
              </div>
              <div>
                <button class="primary" onclick="createExam(true)">Tạo đề mới</button>
                <button class="secondary" onclick="submitExam()">Nộp bài</button>
              </div>
            </div>

            <div class="exam-result" id="examResult"></div>
            <div class="exam-grid" id="examGrid"></div>
          </div>
        </div>
      </section>
    </div>
  </main>

  <div id="toast" class="toast"></div>

  <script>
    const ipaSounds = [
      {s:'iː', group:'vowel', name:'i dài', guide:'Miệng kéo ngang, lưỡi nâng cao, đọc dài và căng.', sample:'sheep', ipa:'/ʃiːp/', meaning:'con cừu', words:['sheep','green','teacher','three','sea','key']},
      {s:'ɪ', group:'vowel', name:'i ngắn', guide:'Miệng thả lỏng hơn /iː/, âm ngắn, không kéo dài.', sample:'ship', ipa:'/ʃɪp/', meaning:'con tàu', words:['ship','sit','fish','milk','city','window']},
      {s:'e', group:'vowel', name:'e ngắn', guide:'Miệng mở vừa, âm ngắn và gọn.', sample:'bed', ipa:'/bed/', meaning:'cái giường', words:['bed','pen','ten','red','head','friend']},
      {s:'æ', group:'vowel', name:'e bẹt / a bẹt', guide:'Miệng mở rộng, môi kéo ngang, âm nằm giữa e và a.', sample:'cat', ipa:'/kæt/', meaning:'con mèo', words:['cat','man','bag','family','apple','traffic']},
      {s:'ɑː', group:'vowel', name:'a dài sâu', guide:'Miệng mở rộng, lưỡi hạ thấp, đọc âm a dài và sâu.', sample:'car', ipa:'/kɑːr/', meaning:'xe hơi', words:['car','father','park','class','start','market']},
      {s:'ɒ', group:'vowel', name:'o ngắn', guide:'Miệng tròn nhẹ, âm ngắn, thường gặp trong giọng Anh - Anh.', sample:'hot', ipa:'/hɒt/', meaning:'nóng', words:['hot','dog','box','shop','clock','hospital']},
      {s:'ɔː', group:'vowel', name:'o dài', guide:'Môi tròn, hàm mở vừa, kéo dài âm o.', sample:'horse', ipa:'/hɔːs/', meaning:'con ngựa', words:['horse','door','four','sport','morning','water']},
      {s:'ʊ', group:'vowel', name:'u ngắn', guide:'Môi tròn nhẹ, lưỡi nâng cao, âm ngắn hơn /uː/.', sample:'book', ipa:'/bʊk/', meaning:'sách', words:['book','good','look','cook','foot','put']},
      {s:'uː', group:'vowel', name:'u dài', guide:'Môi tròn rõ, lưỡi nâng cao, kéo dài âm u.', sample:'food', ipa:'/fuːd/', meaning:'đồ ăn', words:['food','school','moon','blue','room','student']},
      {s:'ʌ', group:'vowel', name:'ă / â ngắn', guide:'Miệng mở tự nhiên, âm bật ngắn ở giữa miệng.', sample:'cup', ipa:'/kʌp/', meaning:'cái cốc', words:['cup','bus','sun','mother','study','country']},
      {s:'ɜː', group:'vowel', name:'ơ dài', guide:'Môi thả lỏng, âm ơ kéo dài.', sample:'bird', ipa:'/bɜːd/', meaning:'con chim', words:['bird','girl','work','world','learn','turn']},
      {s:'ə', group:'vowel', name:'ơ nhẹ / schwa', guide:'Âm rất nhẹ, ngắn, miệng thả lỏng, thường ở âm tiết không nhấn.', sample:'about', ipa:'/əˈbaʊt/', meaning:'về/khoảng', words:['about','banana','teacher','doctor','today','again']},

      {s:'eɪ', group:'diphthong', name:'êi', guide:'Bắt đầu từ /e/, trượt sang /ɪ/, không đọc rời hai âm.', sample:'cake', ipa:'/keɪk/', meaning:'bánh', words:['cake','name','day','play','station','eight']},
      {s:'aɪ', group:'diphthong', name:'ai', guide:'Bắt đầu từ /a/, trượt lên /ɪ/.', sample:'bike', ipa:'/baɪk/', meaning:'xe đạp', words:['bike','time','five','my','white','smile']},
      {s:'ɔɪ', group:'diphthong', name:'oi', guide:'Bắt đầu môi tròn ở /ɔː/, trượt sang /ɪ/.', sample:'boy', ipa:'/bɔɪ/', meaning:'cậu bé', words:['boy','toy','coin','voice','choice','enjoy']},
      {s:'aʊ', group:'diphthong', name:'ao', guide:'Bắt đầu mở rộng /a/, rồi tròn môi dần về /ʊ/.', sample:'house', ipa:'/haʊs/', meaning:'ngôi nhà', words:['house','now','cow','town','flower','about']},
      {s:'əʊ', group:'diphthong', name:'ơu', guide:'Bắt đầu từ /ə/, trượt sang /ʊ/, môi tròn dần.', sample:'phone', ipa:'/fəʊn/', meaning:'điện thoại', words:['phone','go','home','open','road','window']},
      {s:'ɪə', group:'diphthong', name:'iə', guide:'Bắt đầu từ /ɪ/, trượt nhẹ về /ə/.', sample:'near', ipa:'/nɪə/', meaning:'gần', words:['near','ear','clear','here','year','idea']},
      {s:'eə', group:'diphthong', name:'eə', guide:'Bắt đầu từ /e/, trượt nhẹ về /ə/, miệng mở vừa.', sample:'hair', ipa:'/heə/', meaning:'tóc', words:['hair','chair','where','there','care','parent']},
      {s:'ʊə', group:'diphthong', name:'uə', guide:'Bắt đầu từ /ʊ/, trượt nhẹ về /ə/.', sample:'tour', ipa:'/tʊə/', meaning:'chuyến tham quan', words:['tour','poor','sure','cure','tourist','pure']},

      {s:'p', group:'consonant', name:'p vô thanh', guide:'Hai môi khép rồi bật ra, không rung cổ họng.', sample:'pen', ipa:'/pen/', meaning:'bút', words:['pen','paper','pencil','happy','map','stop']},
      {s:'b', group:'consonant', name:'b hữu thanh', guide:'Hai môi khép rồi bật ra, có rung cổ họng.', sample:'book', ipa:'/bʊk/', meaning:'sách', words:['book','bag','baby','table','job','club']},
      {s:'t', group:'consonant', name:'t vô thanh', guide:'Đầu lưỡi chạm lợi trên rồi bật ra, không rung cổ họng.', sample:'tea', ipa:'/tiː/', meaning:'trà', words:['tea','teacher','table','student','cat','sit']},
      {s:'d', group:'consonant', name:'d hữu thanh', guide:'Đầu lưỡi chạm lợi trên rồi bật ra, có rung cổ họng.', sample:'dog', ipa:'/dɒg/', meaning:'chó', words:['dog','day','door','student','good','friend']},
      {s:'k', group:'consonant', name:'k vô thanh', guide:'Gốc lưỡi chạm vòm mềm rồi bật ra, không rung cổ họng.', sample:'key', ipa:'/kiː/', meaning:'chìa khóa', words:['key','cat','school','class','book','milk']},
      {s:'g', group:'consonant', name:'g hữu thanh', guide:'Gốc lưỡi chạm vòm mềm rồi bật ra, có rung cổ họng.', sample:'go', ipa:'/gəʊ/', meaning:'đi', words:['go','girl','green','garden','big','dog']},
      {s:'f', group:'consonant', name:'f vô thanh', guide:'Răng trên chạm môi dưới, đẩy hơi ra, không rung.', sample:'fish', ipa:'/fɪʃ/', meaning:'cá', words:['fish','family','food','phone','photo','laugh']},
      {s:'v', group:'consonant', name:'v hữu thanh', guide:'Răng trên chạm môi dưới, đẩy hơi ra, có rung.', sample:'very', ipa:'/ˈveri/', meaning:'rất', words:['very','video','visit','village','seven','love']},
      {s:'θ', group:'consonant', name:'th vô thanh', guide:'Đầu lưỡi đặt nhẹ giữa hai hàm răng, đẩy hơi ra, không rung.', sample:'think', ipa:'/θɪŋk/', meaning:'nghĩ', words:['think','three','thank','thin','math','healthy']},
      {s:'ð', group:'consonant', name:'th hữu thanh', guide:'Đầu lưỡi đặt nhẹ giữa hai hàm răng, đẩy hơi ra, có rung.', sample:'this', ipa:'/ðɪs/', meaning:'này', words:['this','that','these','those','mother','weather']},
      {s:'s', group:'consonant', name:'s vô thanh', guide:'Đầu lưỡi gần lợi trên, hơi đi qua khe hẹp, không rung.', sample:'sun', ipa:'/sʌn/', meaning:'mặt trời', words:['sun','sit','school','class','lesson','bus']},
      {s:'z', group:'consonant', name:'z hữu thanh', guide:'Giống /s/ nhưng có rung cổ họng.', sample:'zoo', ipa:'/zuː/', meaning:'sở thú', words:['zoo','zero','busy','music','easy','cars']},
      {s:'ʃ', group:'consonant', name:'sh vô thanh', guide:'Môi hơi chu, lưỡi nâng gần vòm miệng, âm gió dài.', sample:'she', ipa:'/ʃiː/', meaning:'cô ấy', words:['she','ship','shop','English','special','finish']},
      {s:'ʒ', group:'consonant', name:'zh hữu thanh', guide:'Giống /ʃ/ nhưng có rung, thường gặp trong vision.', sample:'vision', ipa:'/ˈvɪʒn/', meaning:'tầm nhìn', words:['vision','television','usually','measure','decision','garage']},
      {s:'h', group:'consonant', name:'h vô thanh', guide:'Đẩy hơi nhẹ từ cổ họng, không rung mạnh.', sample:'hat', ipa:'/hæt/', meaning:'mũ', words:['hat','house','home','hello','happy','hair']},
      {s:'tʃ', group:'consonant', name:'ch vô thanh', guide:'Âm bật: đầu lưỡi bật ra rồi chuyển nhanh sang âm gió /ʃ/.', sample:'chair', ipa:'/tʃeə/', meaning:'ghế', words:['chair','teacher','children','watch','kitchen','choose']},
      {s:'dʒ', group:'consonant', name:'j hữu thanh', guide:'Giống /tʃ/ nhưng có rung cổ họng.', sample:'jam', ipa:'/dʒæm/', meaning:'mứt', words:['jam','job','June','orange','village','bridge']},
      {s:'m', group:'consonant', name:'m hữu thanh', guide:'Hai môi khép, âm đi qua mũi, có rung.', sample:'man', ipa:'/mæn/', meaning:'người đàn ông', words:['man','mother','morning','family','room','time']},
      {s:'n', group:'consonant', name:'n hữu thanh', guide:'Đầu lưỡi chạm lợi trên, âm đi qua mũi, có rung.', sample:'name', ipa:'/neɪm/', meaning:'tên', words:['name','nine','new','student','green','pen']},
      {s:'ŋ', group:'consonant', name:'ng hữu thanh', guide:'Gốc lưỡi nâng lên, âm đi qua mũi, giống âm cuối trong sing.', sample:'sing', ipa:'/sɪŋ/', meaning:'hát', words:['sing','song','English','morning','young','thing']},
      {s:'l', group:'consonant', name:'l hữu thanh', guide:'Đầu lưỡi chạm lợi trên, hơi đi hai bên lưỡi, có rung.', sample:'leg', ipa:'/leg/', meaning:'chân', words:['leg','like','look','school','family','table']},
      {s:'r', group:'consonant', name:'r hữu thanh', guide:'Lưỡi cong nhẹ hoặc kéo lùi, không chạm mạnh như tiếng Việt.', sample:'red', ipa:'/red/', meaning:'màu đỏ', words:['red','rice','room','right','friend','story']},
      {s:'j', group:'consonant', name:'y hữu thanh', guide:'Âm giống y trong tiếng Việt, lưỡi nâng cao, có rung.', sample:'yes', ipa:'/jes/', meaning:'vâng', words:['yes','year','young','yellow','use','music']},
      {s:'w', group:'consonant', name:'w hữu thanh', guide:'Môi tròn rồi mở nhanh, có rung.', sample:'water', ipa:'/ˈwɔːtə/', meaning:'nước', words:['water','we','window','white','where','weather']}
    ];

    const theory = [
      {
        title:'Dạng 1: Chọn từ có phần gạch chân phát âm khác',
        rule:'Đề cho 4 từ A/B/C/D. Học sinh xác định phần gạch chân trong từ nào có âm khác 3 từ còn lại.',
        points:[
          'Nhìn đúng phần gạch chân, không chọn theo nghĩa.',
          'Đọc âm thật của phần gạch chân trong từng từ.',
          'Tìm 3 từ cùng âm và 1 từ khác âm.',
          'Nhóm thường gặp: -ed, -s/-es, ch, th, ea, oo, ou, ow, a, i, âm câm.'
        ],
        examples:['wanted /ɪd/ khác played, lived, cleaned /d/','books /s/ khác pens, bags, rooms /z/','chef /ʃ/ khác cheap, children, chair /tʃ/']
      },
      {
        title:'Quy tắc phát âm đuôi -ed',
        rule:'Đuôi -ed có 3 cách đọc: /t/, /d/, /ɪd/.',
        points:[
          '/ɪd/: sau /t/, /d/: wanted, needed, visited.',
          '/t/: sau âm vô thanh /p, k, f, s, ʃ, tʃ/: stopped, watched, laughed.',
          '/d/: sau nguyên âm và âm hữu thanh còn lại: played, cleaned, opened.'
        ],
        examples:['watched /t/','needed /ɪd/','played /d/']
      },
      {
        title:'Quy tắc phát âm -s/-es',
        rule:'Đuôi -s/-es có 3 cách đọc: /s/, /z/, /ɪz/.',
        points:[
          '/ɪz/: sau /s, z, ʃ, ʒ, tʃ, dʒ/: watches, classes, buses.',
          '/s/: sau âm vô thanh /p, t, k, f, θ/: books, cups, laughs.',
          '/z/: sau nguyên âm và âm hữu thanh còn lại: pens, rooms, bags.'
        ],
        examples:['books /s/','watches /ɪz/','plays /z/']
      },
      {
        title:'Dạng 2: Chọn từ có trọng âm khác',
        rule:'Đề cho 4 từ. Chọn từ có vị trí trọng âm khác 3 từ còn lại.',
        points:[
          'Đếm số âm tiết trước.',
          'Danh từ/tính từ 2 âm tiết thường nhấn âm 1: teacher, happy.',
          'Động từ 2 âm tiết thường nhấn âm 2: enjoy, invite.',
          'Hậu tố -tion, -sion, -ic, -ity, -ial thường kéo trọng âm về trước hậu tố.',
          'Hậu tố -ee, -eer, -ese thường nhận trọng âm chính.'
        ],
        examples:['ˈteacher, ˈhappy','enˈjoy, inˈvite','eduˈcation, autoˈmatic']
      },
      {
        title:'Cách làm nhanh khi đi thi',
        rule:'Mục tiêu là loại nhanh 3 từ giống nhau và tìm 1 từ khác.',
        points:[
          'Không đọc theo chữ cái tiếng Việt.',
          'Với phát âm, đọc phần gạch chân thành âm IPA gần đúng.',
          'Với trọng âm, đánh dấu âm nhấn bằng dấu ˈ trước âm tiết.',
          'Nếu phân vân, kiểm tra từ loại và hậu tố.',
          'Sau khi chọn, đọc lại cả 4 từ để xác nhận.'
        ],
        examples:['present (n/adj): ˈpresent; present (v): preˈsent','record (n): ˈrecord; record (v): reˈcord']
      }
    ];

    const questions = [
      {
            "type": "sound",
            "grade": 7,
            "rule": "-ed",
            "answer": "A",
            "explain": "wanted đọc /ɪd/ vì kết thúc bằng /t/. Ba từ còn lại played, cleaned, opened đọc /d/.",
            "options": [
                  [
                        "wanted",
                        "ed"
                  ],
                  [
                        "played",
                        "ed"
                  ],
                  [
                        "cleaned",
                        "ed"
                  ],
                  [
                        "opened",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "-ed",
            "answer": "C",
            "explain": "watched đọc /t/ vì âm cuối /tʃ/ là âm vô thanh. Ba từ còn lại listened, enjoyed, played đọc /d/.",
            "options": [
                  [
                        "listened",
                        "ed"
                  ],
                  [
                        "enjoyed",
                        "ed"
                  ],
                  [
                        "watched",
                        "ed"
                  ],
                  [
                        "played",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-ed",
            "answer": "B",
            "explain": "needed đọc /ɪd/ vì kết thúc bằng /d/. Helped, laughed, stopped đọc /t/.",
            "options": [
                  [
                        "helped",
                        "ed"
                  ],
                  [
                        "needed",
                        "ed"
                  ],
                  [
                        "laughed",
                        "ed"
                  ],
                  [
                        "stopped",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "-ed",
            "answer": "D",
            "explain": "visited đọc /ɪd/ vì kết thúc bằng /t/. Lived, moved, opened đọc /d/.",
            "options": [
                  [
                        "lived",
                        "ed"
                  ],
                  [
                        "moved",
                        "ed"
                  ],
                  [
                        "opened",
                        "ed"
                  ],
                  [
                        "visited",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-ed",
            "answer": "A",
            "explain": "stopped đọc /t/. Needed, visited, decided đọc /ɪd/ vì kết thúc bằng /t/ hoặc /d/.",
            "options": [
                  [
                        "stopped",
                        "ed"
                  ],
                  [
                        "needed",
                        "ed"
                  ],
                  [
                        "visited",
                        "ed"
                  ],
                  [
                        "decided",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "-ed",
            "answer": "A",
            "explain": "played đọc /d/ vì âm cuối là nguyên âm. Watched, washed, looked đọc /t/.",
            "options": [
                  [
                        "played",
                        "ed"
                  ],
                  [
                        "watched",
                        "ed"
                  ],
                  [
                        "washed",
                        "ed"
                  ],
                  [
                        "looked",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "-ed",
            "answer": "B",
            "explain": "started đọc /ɪd/ vì kết thúc bằng /t/. Learned, cleaned, opened đọc /d/.",
            "options": [
                  [
                        "learned",
                        "ed"
                  ],
                  [
                        "started",
                        "ed"
                  ],
                  [
                        "cleaned",
                        "ed"
                  ],
                  [
                        "opened",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-ed",
            "answer": "D",
            "explain": "missed đọc /t/. Needed, decided, visited đọc /ɪd/.",
            "options": [
                  [
                        "needed",
                        "ed"
                  ],
                  [
                        "decided",
                        "ed"
                  ],
                  [
                        "visited",
                        "ed"
                  ],
                  [
                        "missed",
                        "ed"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "-s/-es",
            "answer": "A",
            "explain": "books đọc /s/ vì âm cuối /k/ vô thanh. Pens, rooms, bags đọc /z/.",
            "options": [
                  [
                        "books",
                        "s"
                  ],
                  [
                        "pens",
                        "s"
                  ],
                  [
                        "rooms",
                        "s"
                  ],
                  [
                        "bags",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-s/-es",
            "answer": "B",
            "explain": "classes đọc /ɪz/ vì kết thúc bằng /s/. Plays, days, trees đọc /z/.",
            "options": [
                  [
                        "plays",
                        "s"
                  ],
                  [
                        "classes",
                        "es"
                  ],
                  [
                        "days",
                        "s"
                  ],
                  [
                        "trees",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "-s/-es",
            "answer": "D",
            "explain": "laughs đọc /s/ vì âm cuối /f/ vô thanh. Goes, does, studies đọc /z/.",
            "options": [
                  [
                        "goes",
                        "es"
                  ],
                  [
                        "does",
                        "es"
                  ],
                  [
                        "studies",
                        "es"
                  ],
                  [
                        "laughs",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "-s/-es",
            "answer": "A",
            "explain": "watches đọc /ɪz/ vì kết thúc bằng /tʃ/. Cooks, maps, cups đọc /s/.",
            "options": [
                  [
                        "watches",
                        "es"
                  ],
                  [
                        "cooks",
                        "s"
                  ],
                  [
                        "maps",
                        "s"
                  ],
                  [
                        "cups",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-s/-es",
            "answer": "C",
            "explain": "students đọc /s/ vì âm cuối /t/ vô thanh. Teachers, dogs, pens đọc /z/.",
            "options": [
                  [
                        "teachers",
                        "s"
                  ],
                  [
                        "dogs",
                        "s"
                  ],
                  [
                        "students",
                        "s"
                  ],
                  [
                        "pens",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "-s/-es",
            "answer": "A",
            "explain": "buses đọc /ɪz/ vì kết thúc bằng /s/. Rooms, friends, pens đọc /z/.",
            "options": [
                  [
                        "buses",
                        "es"
                  ],
                  [
                        "rooms",
                        "s"
                  ],
                  [
                        "friends",
                        "s"
                  ],
                  [
                        "pens",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "-s/-es",
            "answer": "B",
            "explain": "months đọc /s/ vì âm cuối /θ/ vô thanh. Plays, boys, girls đọc /z/.",
            "options": [
                  [
                        "plays",
                        "s"
                  ],
                  [
                        "months",
                        "s"
                  ],
                  [
                        "boys",
                        "s"
                  ],
                  [
                        "girls",
                        "s"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "-s/-es",
            "answer": "D",
            "explain": "dishes đọc /ɪz/ vì kết thúc bằng /ʃ/. Plays, runs, days đọc /z/.",
            "options": [
                  [
                        "plays",
                        "s"
                  ],
                  [
                        "runs",
                        "s"
                  ],
                  [
                        "days",
                        "s"
                  ],
                  [
                        "dishes",
                        "es"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "ch",
            "answer": "C",
            "explain": "chef có ch đọc /ʃ/. Chair, children, choose có ch đọc /tʃ/.",
            "options": [
                  [
                        "chair",
                        "ch"
                  ],
                  [
                        "children",
                        "ch"
                  ],
                  [
                        "chef",
                        "ch"
                  ],
                  [
                        "choose",
                        "ch"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "ch",
            "answer": "A",
            "explain": "machine có ch đọc /ʃ/. Cheap, chicken, teacher có ch đọc /tʃ/.",
            "options": [
                  [
                        "machine",
                        "ch"
                  ],
                  [
                        "cheap",
                        "ch"
                  ],
                  [
                        "chicken",
                        "ch"
                  ],
                  [
                        "teacher",
                        "ch"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "ch",
            "answer": "B",
            "explain": "school có ch đọc /k/. Chair, chicken, children có ch đọc /tʃ/.",
            "options": [
                  [
                        "chair",
                        "ch"
                  ],
                  [
                        "school",
                        "ch"
                  ],
                  [
                        "chicken",
                        "ch"
                  ],
                  [
                        "children",
                        "ch"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "ch",
            "answer": "D",
            "explain": "Christmas có ch đọc /k/. Chat, child, lunch có ch đọc /tʃ/.",
            "options": [
                  [
                        "chat",
                        "ch"
                  ],
                  [
                        "child",
                        "ch"
                  ],
                  [
                        "lunch",
                        "ch"
                  ],
                  [
                        "Christmas",
                        "Ch"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "th",
            "answer": "D",
            "explain": "weather có th đọc /ð/. Think, thank, healthy có th đọc /θ/.",
            "options": [
                  [
                        "think",
                        "th"
                  ],
                  [
                        "thank",
                        "th"
                  ],
                  [
                        "healthy",
                        "th"
                  ],
                  [
                        "weather",
                        "th"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "th",
            "answer": "A",
            "explain": "this có th đọc /ð/. Three, math, birthday có th đọc /θ/.",
            "options": [
                  [
                        "this",
                        "th"
                  ],
                  [
                        "three",
                        "th"
                  ],
                  [
                        "math",
                        "th"
                  ],
                  [
                        "birthday",
                        "th"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "th",
            "answer": "B",
            "explain": "though có th đọc /ð/. Through, thin, thousand có th đọc /θ/.",
            "options": [
                  [
                        "through",
                        "th"
                  ],
                  [
                        "though",
                        "th"
                  ],
                  [
                        "thin",
                        "th"
                  ],
                  [
                        "thousand",
                        "th"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "th",
            "answer": "C",
            "explain": "breathe có th đọc /ð/. Breath, think, healthy có th đọc /θ/.",
            "options": [
                  [
                        "breath",
                        "th"
                  ],
                  [
                        "think",
                        "th"
                  ],
                  [
                        "breathe",
                        "th"
                  ],
                  [
                        "healthy",
                        "th"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "ea",
            "answer": "B",
            "explain": "great có ea đọc /eɪ/. Teacher, clean, sea có ea đọc /iː/.",
            "options": [
                  [
                        "teacher",
                        "ea"
                  ],
                  [
                        "great",
                        "ea"
                  ],
                  [
                        "clean",
                        "ea"
                  ],
                  [
                        "sea",
                        "ea"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "ea",
            "answer": "C",
            "explain": "head có ea đọc /e/. Speak, teacher, clean có ea đọc /iː/.",
            "options": [
                  [
                        "speak",
                        "ea"
                  ],
                  [
                        "teacher",
                        "ea"
                  ],
                  [
                        "head",
                        "ea"
                  ],
                  [
                        "clean",
                        "ea"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "ea",
            "answer": "A",
            "explain": "break có ea đọc /eɪ/. Bread, head, health có ea đọc /e/.",
            "options": [
                  [
                        "break",
                        "ea"
                  ],
                  [
                        "bread",
                        "ea"
                  ],
                  [
                        "head",
                        "ea"
                  ],
                  [
                        "health",
                        "ea"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "oo",
            "answer": "C",
            "explain": "blood có oo đọc /ʌ/. School, food, moon có oo đọc /uː/.",
            "options": [
                  [
                        "school",
                        "oo"
                  ],
                  [
                        "food",
                        "oo"
                  ],
                  [
                        "blood",
                        "oo"
                  ],
                  [
                        "moon",
                        "oo"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "oo",
            "answer": "A",
            "explain": "book có oo đọc /ʊ/. Food, school, room có oo đọc /uː/.",
            "options": [
                  [
                        "book",
                        "oo"
                  ],
                  [
                        "food",
                        "oo"
                  ],
                  [
                        "school",
                        "oo"
                  ],
                  [
                        "room",
                        "oo"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "oo",
            "answer": "D",
            "explain": "good có oo đọc /ʊ/. Moon, food, blue có âm /uː/.",
            "options": [
                  [
                        "moon",
                        "oo"
                  ],
                  [
                        "food",
                        "oo"
                  ],
                  [
                        "blue",
                        "ue"
                  ],
                  [
                        "good",
                        "oo"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "ou",
            "answer": "A",
            "explain": "country có ou đọc /ʌ/. Sound, about, house có ou đọc /aʊ/.",
            "options": [
                  [
                        "country",
                        "ou"
                  ],
                  [
                        "sound",
                        "ou"
                  ],
                  [
                        "about",
                        "ou"
                  ],
                  [
                        "house",
                        "ou"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "ou",
            "answer": "C",
            "explain": "young có ou đọc /ʌ/. Cloud, shout, mountain có ou đọc /aʊ/.",
            "options": [
                  [
                        "cloud",
                        "ou"
                  ],
                  [
                        "shout",
                        "ou"
                  ],
                  [
                        "young",
                        "ou"
                  ],
                  [
                        "mountain",
                        "ou"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "ow",
            "answer": "B",
            "explain": "know có ow đọc /əʊ/. Now, how, brown có ow đọc /aʊ/.",
            "options": [
                  [
                        "now",
                        "ow"
                  ],
                  [
                        "know",
                        "ow"
                  ],
                  [
                        "how",
                        "ow"
                  ],
                  [
                        "brown",
                        "ow"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "ow",
            "answer": "D",
            "explain": "show có ow đọc /əʊ/. Cow, flower, town có ow đọc /aʊ/.",
            "options": [
                  [
                        "cow",
                        "ow"
                  ],
                  [
                        "flower",
                        "ow"
                  ],
                  [
                        "town",
                        "ow"
                  ],
                  [
                        "show",
                        "ow"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "a",
            "answer": "C",
            "explain": "father có a đọc /ɑː/. Cat, apple, activity có a thường gần /æ/.",
            "options": [
                  [
                        "cat",
                        "a"
                  ],
                  [
                        "apple",
                        "a"
                  ],
                  [
                        "father",
                        "a"
                  ],
                  [
                        "activity",
                        "a"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "a",
            "answer": "A",
            "explain": "many có a đọc /e/. Bag, cat, hat có a đọc /æ/.",
            "options": [
                  [
                        "many",
                        "a"
                  ],
                  [
                        "bag",
                        "a"
                  ],
                  [
                        "cat",
                        "a"
                  ],
                  [
                        "hat",
                        "a"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "a",
            "answer": "B",
            "explain": "water có a đọc /ɔː/. Apple, bag, cat có a đọc /æ/.",
            "options": [
                  [
                        "apple",
                        "a"
                  ],
                  [
                        "water",
                        "a"
                  ],
                  [
                        "bag",
                        "a"
                  ],
                  [
                        "cat",
                        "a"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "a",
            "answer": "D",
            "explain": "class có a đọc /ɑː/ trong giọng Anh - Anh. Apple, cat, hat có a đọc /æ/.",
            "options": [
                  [
                        "apple",
                        "a"
                  ],
                  [
                        "cat",
                        "a"
                  ],
                  [
                        "hat",
                        "a"
                  ],
                  [
                        "class",
                        "a"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "i",
            "answer": "D",
            "explain": "machine có i đọc /iː/. Village, activity, difficult có i thường đọc /ɪ/.",
            "options": [
                  [
                        "village",
                        "i"
                  ],
                  [
                        "activity",
                        "i"
                  ],
                  [
                        "difficult",
                        "i"
                  ],
                  [
                        "machine",
                        "i"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "i",
            "answer": "A",
            "explain": "find có i đọc /aɪ/. Sit, film, milk có i đọc /ɪ/.",
            "options": [
                  [
                        "find",
                        "i"
                  ],
                  [
                        "sit",
                        "i"
                  ],
                  [
                        "film",
                        "i"
                  ],
                  [
                        "milk",
                        "i"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "i",
            "answer": "B",
            "explain": "child có i đọc /aɪ/. City, visit, picture có i đọc /ɪ/.",
            "options": [
                  [
                        "city",
                        "i"
                  ],
                  [
                        "child",
                        "i"
                  ],
                  [
                        "visit",
                        "i"
                  ],
                  [
                        "picture",
                        "i"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "i",
            "answer": "A",
            "explain": "live trong nghĩa 'sống' đọc /lɪv/. Five, time, white có i đọc /aɪ/.",
            "options": [
                  [
                        "live",
                        "i"
                  ],
                  [
                        "five",
                        "i"
                  ],
                  [
                        "time",
                        "i"
                  ],
                  [
                        "white",
                        "i"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "u",
            "answer": "B",
            "explain": "student có u đọc /juː/. Suburb, custom, adult thường có u đọc /ʌ/ hoặc âm khác không phải /juː/.",
            "options": [
                  [
                        "suburb",
                        "u"
                  ],
                  [
                        "student",
                        "u"
                  ],
                  [
                        "custom",
                        "u"
                  ],
                  [
                        "adult",
                        "u"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "u",
            "answer": "A",
            "explain": "put có u đọc /ʊ/. Cup, sun, bus có u đọc /ʌ/.",
            "options": [
                  [
                        "put",
                        "u"
                  ],
                  [
                        "cup",
                        "u"
                  ],
                  [
                        "sun",
                        "u"
                  ],
                  [
                        "bus",
                        "u"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "u",
            "answer": "C",
            "explain": "music có u đọc /juː/. Lunch, summer, study có u đọc /ʌ/.",
            "options": [
                  [
                        "lunch",
                        "u"
                  ],
                  [
                        "summer",
                        "u"
                  ],
                  [
                        "music",
                        "u"
                  ],
                  [
                        "study",
                        "u"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "u",
            "answer": "D",
            "explain": "sugar có u đọc /ʊ/. Sun, cup, luck có u đọc /ʌ/.",
            "options": [
                  [
                        "sun",
                        "u"
                  ],
                  [
                        "cup",
                        "u"
                  ],
                  [
                        "luck",
                        "u"
                  ],
                  [
                        "sugar",
                        "u"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 9,
            "rule": "silent letters",
            "answer": "A",
            "explain": "hour có h câm. House, hobby, healthy có h được phát âm.",
            "options": [
                  [
                        "hour",
                        "h"
                  ],
                  [
                        "house",
                        "h"
                  ],
                  [
                        "hobby",
                        "h"
                  ],
                  [
                        "healthy",
                        "h"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 7,
            "rule": "silent letters",
            "answer": "C",
            "explain": "answer có w câm. Water, window, white có w được phát âm.",
            "options": [
                  [
                        "water",
                        "w"
                  ],
                  [
                        "window",
                        "w"
                  ],
                  [
                        "answer",
                        "w"
                  ],
                  [
                        "white",
                        "w"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "c",
            "answer": "D",
            "explain": "city có c đọc /s/. Community, custom, collect có c đọc /k/.",
            "options": [
                  [
                        "community",
                        "c"
                  ],
                  [
                        "custom",
                        "c"
                  ],
                  [
                        "collect",
                        "c"
                  ],
                  [
                        "city",
                        "c"
                  ]
            ]
      },
      {
            "type": "sound",
            "grade": 8,
            "rule": "gh",
            "answer": "B",
            "explain": "laugh có gh đọc /f/. High, although, through có gh câm.",
            "options": [
                  [
                        "high",
                        "gh"
                  ],
                  [
                        "laugh",
                        "gh"
                  ],
                  [
                        "although",
                        "gh"
                  ],
                  [
                        "through",
                        "gh"
                  ]
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "volunteer nhấn âm cuối: volunˈteer. Hobby, service, healthy thường nhấn âm 1.",
            "options": [
                  "hobby",
                  "service",
                  "healthy",
                  "volunteer"
            ],
            "stress": [
                  "ˈhobby",
                  "ˈservice",
                  "ˈhealthy",
                  "volunˈteer"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "C",
            "explain": "collect là động từ 2 âm tiết, thường nhấn âm 2. Model, music, artist thường nhấn âm 1.",
            "options": [
                  "model",
                  "music",
                  "collect",
                  "artist"
            ],
            "stress": [
                  "ˈmodel",
                  "ˈmusic",
                  "colˈlect",
                  "ˈartist"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "B",
            "explain": "delicious nhấn âm 2. Festival, vegetable, character thường nhấn âm 1.",
            "options": [
                  "festival",
                  "delicious",
                  "vegetable",
                  "character"
            ],
            "stress": [
                  "ˈfestival",
                  "deˈlicious",
                  "ˈvegetable",
                  "ˈcharacter"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "perform là động từ 2 âm tiết, nhấn âm 2. Music, concert, painting thường nhấn âm 1 trong danh từ.",
            "options": [
                  "music",
                  "concert",
                  "painting",
                  "perform"
            ],
            "stress": [
                  "ˈmusic",
                  "ˈconcert",
                  "ˈpainting",
                  "perˈform"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "provide là động từ 2 âm tiết, nhấn âm 2. Breakfast, bottle, sugar thường nhấn âm 1.",
            "options": [
                  "breakfast",
                  "bottle",
                  "sugar",
                  "provide"
            ],
            "stress": [
                  "ˈbreakfast",
                  "ˈbottle",
                  "ˈsugar",
                  "proˈvide"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "A",
            "explain": "donate nhấn âm 2. Artist, actor, painting thường nhấn âm 1.",
            "options": [
                  "donate",
                  "artist",
                  "actor",
                  "painting"
            ],
            "stress": [
                  "doˈnate",
                  "ˈartist",
                  "ˈactor",
                  "ˈpainting"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "traditional nhấn âm 2. Vegetable, calorie, energy thường nhấn âm 1.",
            "options": [
                  "vegetable",
                  "calorie",
                  "energy",
                  "traditional"
            ],
            "stress": [
                  "ˈvegetable",
                  "ˈcalorie",
                  "ˈenergy",
                  "traˈditional"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "A",
            "explain": "musician nhấn âm 2. Actor, artist, painting thường nhấn âm 1.",
            "options": [
                  "musician",
                  "actor",
                  "artist",
                  "painting"
            ],
            "stress": [
                  "muˈsician",
                  "ˈactor",
                  "ˈartist",
                  "ˈpainting"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "C",
            "explain": "enjoy là động từ 2 âm tiết, nhấn âm 2. Lesson, hobby, music thường nhấn âm 1.",
            "options": [
                  "lesson",
                  "hobby",
                  "enjoy",
                  "music"
            ],
            "stress": [
                  "ˈlesson",
                  "ˈhobby",
                  "enˈjoy",
                  "ˈmusic"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "B",
            "explain": "arrive nhấn âm 2. City, country, village thường nhấn âm 1.",
            "options": [
                  "city",
                  "arrive",
                  "country",
                  "village"
            ],
            "stress": [
                  "ˈcity",
                  "aˈrrive",
                  "ˈcountry",
                  "ˈvillage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "communicate nhấn âm 2. Comfortable, teenager, natural thường nhấn âm 1.",
            "options": [
                  "communicate",
                  "comfortable",
                  "teenager",
                  "natural"
            ],
            "stress": [
                  "comˈmunicate",
                  "ˈcomfortable",
                  "ˈteenager",
                  "ˈnatural"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "D",
            "explain": "tradition nhấn âm 2 trước hậu tố -tion. Leisure, custom, village nhấn âm 1.",
            "options": [
                  "leisure",
                  "custom",
                  "village",
                  "tradition"
            ],
            "stress": [
                  "ˈleisure",
                  "ˈcustom",
                  "ˈvillage",
                  "traˈdition"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "B",
            "explain": "technology thường nhấn âm 2. Festival, natural, comfortable thường nhấn âm 1.",
            "options": [
                  "festival",
                  "technology",
                  "natural",
                  "comfortable"
            ],
            "stress": [
                  "ˈfestival",
                  "techˈnology",
                  "ˈnatural",
                  "ˈcomfortable"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "B",
            "explain": "disaster nhấn âm 2. Natural, festival, comfortable thường nhấn âm 1.",
            "options": [
                  "natural",
                  "disaster",
                  "festival",
                  "comfortable"
            ],
            "stress": [
                  "ˈnatural",
                  "diˈsaster",
                  "ˈfestival",
                  "ˈcomfortable"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "C",
            "explain": "automatic nhấn âm 3 trước hậu tố -ic. Appliance, invention, pollution thường nhấn âm 2.",
            "options": [
                  "appliance",
                  "invention",
                  "automatic",
                  "pollution"
            ],
            "stress": [
                  "apˈpliance",
                  "inˈvention",
                  "autoˈmatic",
                  "polˈlution"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "emergency nhấn âm 2. Rescue, victim, damage thường nhấn âm 1.",
            "options": [
                  "emergency",
                  "rescue",
                  "victim",
                  "damage"
            ],
            "stress": [
                  "eˈmergency",
                  "ˈrescue",
                  "ˈvictim",
                  "ˈdamage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "pollution nhấn âm 2. Natural, village, custom thường nhấn âm 1.",
            "options": [
                  "pollution",
                  "natural",
                  "village",
                  "custom"
            ],
            "stress": [
                  "polˈlution",
                  "ˈnatural",
                  "ˈvillage",
                  "ˈcustom"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "invention nhấn âm 2. Festival, leisure, custom thường nhấn âm 1.",
            "options": [
                  "invention",
                  "festival",
                  "leisure",
                  "custom"
            ],
            "stress": [
                  "inˈvention",
                  "ˈfestival",
                  "ˈleisure",
                  "ˈcustom"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "appliance nhấn âm 2. Teenager, pressure, village thường nhấn âm 1.",
            "options": [
                  "appliance",
                  "teenager",
                  "pressure",
                  "village"
            ],
            "stress": [
                  "apˈpliance",
                  "ˈteenager",
                  "ˈpressure",
                  "ˈvillage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "environment nhấn âm 2. Comfortable, natural, festival thường nhấn âm 1.",
            "options": [
                  "environment",
                  "comfortable",
                  "natural",
                  "festival"
            ],
            "stress": [
                  "enˈvironment",
                  "ˈcomfortable",
                  "ˈnatural",
                  "ˈfestival"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "activity nhấn âm 2. Village, leisure, custom thường nhấn âm 1.",
            "options": [
                  "activity",
                  "village",
                  "leisure",
                  "custom"
            ],
            "stress": [
                  "acˈtivity",
                  "ˈvillage",
                  "ˈleisure",
                  "ˈcustom"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "decision nhấn âm 2. Teenager, comfortable, village thường nhấn âm 1.",
            "options": [
                  "decision",
                  "teenager",
                  "comfortable",
                  "village"
            ],
            "stress": [
                  "deˈcision",
                  "ˈteenager",
                  "ˈcomfortable",
                  "ˈvillage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "develop nhấn âm 2. Damage, rescue, victim thường nhấn âm 1.",
            "options": [
                  "develop",
                  "damage",
                  "rescue",
                  "victim"
            ],
            "stress": [
                  "deˈvelop",
                  "ˈdamage",
                  "ˈrescue",
                  "ˈvictim"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "computer nhấn âm 2. Festival, natural, village thường nhấn âm 1.",
            "options": [
                  "computer",
                  "festival",
                  "natural",
                  "village"
            ],
            "stress": [
                  "comˈputer",
                  "ˈfestival",
                  "ˈnatural",
                  "ˈvillage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "A",
            "explain": "modern nhấn âm 1. Appliance, invention, pollution thường nhấn âm 2.",
            "options": [
                  "modern",
                  "appliance",
                  "invention",
                  "pollution"
            ],
            "stress": [
                  "ˈmodern",
                  "apˈpliance",
                  "inˈvention",
                  "polˈlution"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "preserve là động từ 2 âm tiết, nhấn âm 2. Artisan, heritage, village thường nhấn âm 1.",
            "options": [
                  "artisan",
                  "heritage",
                  "village",
                  "preserve"
            ],
            "stress": [
                  "ˈartisan",
                  "ˈheritage",
                  "ˈvillage",
                  "preˈserve"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "comfortable thường nhấn âm 1. Affordable, reliable, bilingual thường nhấn âm 2.",
            "options": [
                  "affordable",
                  "reliable",
                  "bilingual",
                  "comfortable"
            ],
            "stress": [
                  "aˈffordable",
                  "reˈliable",
                  "biˈlingual",
                  "ˈcomfortable"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "C",
            "explain": "destination nhấn âm 3 trước -tion. Confident, cognitive, graduate thường nhấn âm 1.",
            "options": [
                  "confident",
                  "cognitive",
                  "destination",
                  "graduate"
            ],
            "stress": [
                  "ˈconfident",
                  "ˈcognitive",
                  "destiˈnation",
                  "ˈgraduate"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "B",
            "explain": "opportunity nhấn âm 3. Challenge, teenager, pressure nhấn âm 1.",
            "options": [
                  "challenge",
                  "opportunity",
                  "teenager",
                  "pressure"
            ],
            "stress": [
                  "ˈchallenge",
                  "opporˈtunity",
                  "ˈteenager",
                  "ˈpressure"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "academic nhấn âm 3 trước hậu tố -ic. Confident, cognitive, graduate thường nhấn âm 1.",
            "options": [
                  "confident",
                  "cognitive",
                  "graduate",
                  "academic"
            ],
            "stress": [
                  "ˈconfident",
                  "ˈcognitive",
                  "ˈgraduate",
                  "acaˈdemic"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "responsibility nhấn gần cuối theo hậu tố -ity. Challenge, pressure, teenager thường nhấn âm 1.",
            "options": [
                  "challenge",
                  "pressure",
                  "teenager",
                  "responsibility"
            ],
            "stress": [
                  "ˈchallenge",
                  "ˈpressure",
                  "ˈteenager",
                  "responsiˈbility"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "B",
            "explain": "experience nhấn âm 2. Heritage, artisan, confident thường nhấn âm 1.",
            "options": [
                  "heritage",
                  "experience",
                  "artisan",
                  "confident"
            ],
            "stress": [
                  "ˈheritage",
                  "exˈperience",
                  "ˈartisan",
                  "ˈconfident"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "facility nhấn âm 2. Heritage, village, pressure thường nhấn âm 1.",
            "options": [
                  "facility",
                  "heritage",
                  "village",
                  "pressure"
            ],
            "stress": [
                  "faˈcility",
                  "ˈheritage",
                  "ˈvillage",
                  "ˈpressure"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "community nhấn âm 2. Village, heritage, suburb thường nhấn âm 1.",
            "options": [
                  "community",
                  "village",
                  "heritage",
                  "suburb"
            ],
            "stress": [
                  "comˈmunity",
                  "ˈvillage",
                  "ˈheritage",
                  "ˈsuburb"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "metropolitan nhấn âm 3. Reliable, affordable, bilingual thường nhấn âm 2.",
            "options": [
                  "metropolitan",
                  "reliable",
                  "affordable",
                  "bilingual"
            ],
            "stress": [
                  "metroˈpolitan",
                  "reˈliable",
                  "aˈffordable",
                  "biˈlingual"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "skyscraper nhấn âm 1. Facility, reliable, bilingual thường nhấn âm 2.",
            "options": [
                  "skyscraper",
                  "facility",
                  "reliable",
                  "bilingual"
            ],
            "stress": [
                  "ˈskyscraper",
                  "faˈcility",
                  "reˈliable",
                  "biˈlingual"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "independent nhấn âm 3. Confident, cognitive, graduate thường nhấn âm 1.",
            "options": [
                  "independent",
                  "confident",
                  "cognitive",
                  "graduate"
            ],
            "stress": [
                  "indeˈpendent",
                  "ˈconfident",
                  "ˈcognitive",
                  "ˈgraduate"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "assignment nhấn âm 2. Pressure, teenager, challenge thường nhấn âm 1.",
            "options": [
                  "assignment",
                  "pressure",
                  "teenager",
                  "challenge"
            ],
            "stress": [
                  "aˈssignment",
                  "ˈpressure",
                  "ˈteenager",
                  "ˈchallenge"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "profession nhấn âm 2. Challenge, pressure, teenager thường nhấn âm 1.",
            "options": [
                  "profession",
                  "challenge",
                  "pressure",
                  "teenager"
            ],
            "stress": [
                  "proˈfession",
                  "ˈchallenge",
                  "ˈpressure",
                  "ˈteenager"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "A",
            "explain": "career nhấn âm 2. Challenge, pressure, graduate thường nhấn âm 1.",
            "options": [
                  "career",
                  "challenge",
                  "pressure",
                  "graduate"
            ],
            "stress": [
                  "caˈreer",
                  "ˈchallenge",
                  "ˈpressure",
                  "ˈgraduate"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "D",
            "explain": "festival nhấn âm 1. Pollution, invention, tradition đều nhấn âm 2.",
            "options": [
                  "pollution",
                  "invention",
                  "tradition",
                  "festival"
            ],
            "stress": [
                  "polˈlution",
                  "inˈvention",
                  "traˈdition",
                  "ˈfestival"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "D",
            "explain": "appliance nhấn âm 2. Comfortable, natural, festival thường nhấn âm 1.",
            "options": [
                  "comfortable",
                  "natural",
                  "festival",
                  "appliance"
            ],
            "stress": [
                  "ˈcomfortable",
                  "ˈnatural",
                  "ˈfestival",
                  "apˈpliance"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "enjoy là động từ 2 âm tiết, nhấn âm 2. Teacher, student, homework thường nhấn âm 1.",
            "options": [
                  "teacher",
                  "student",
                  "homework",
                  "enjoy"
            ],
            "stress": [
                  "ˈteacher",
                  "ˈstudent",
                  "ˈhomework",
                  "enˈjoy"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "hobby nhấn âm 1. Cartoon, invite, agree thường nhấn âm 2.",
            "options": [
                  "cartoon",
                  "invite",
                  "agree",
                  "hobby"
            ],
            "stress": [
                  "carˈtoon",
                  "inˈvite",
                  "aˈgree",
                  "ˈhobby"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "heritage nhấn âm 1. Protect, prevent, preserve là động từ 2 âm tiết, nhấn âm 2.",
            "options": [
                  "protect",
                  "prevent",
                  "preserve",
                  "heritage"
            ],
            "stress": [
                  "proˈtect",
                  "preˈvent",
                  "preˈserve",
                  "ˈheritage"
            ]
      },
      {
            "type": "stress",
            "grade": 8,
            "answer": "D",
            "explain": "suppose nhấn âm 2. Famous, village, custom thường nhấn âm 1.",
            "options": [
                  "famous",
                  "village",
                  "custom",
                  "suppose"
            ],
            "stress": [
                  "ˈfamous",
                  "ˈvillage",
                  "ˈcustom",
                  "suˈppose"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "artist nhấn âm 1. Improve, provide, collect đều là động từ 2 âm tiết, nhấn âm 2.",
            "options": [
                  "improve",
                  "provide",
                  "collect",
                  "artist"
            ],
            "stress": [
                  "imˈprove",
                  "proˈvide",
                  "colˈlect",
                  "ˈartist"
            ]
      },
      {
            "type": "stress",
            "grade": 7,
            "answer": "D",
            "explain": "decide nhấn âm 2. Window, music, lesson thường nhấn âm 1.",
            "options": [
                  "window",
                  "music",
                  "lesson",
                  "decide"
            ],
            "stress": [
                  "ˈwindow",
                  "ˈmusic",
                  "ˈlesson",
                  "deˈcide"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "village nhấn âm 1. Technology, geography, biology thường nhấn âm 2.",
            "options": [
                  "technology",
                  "geography",
                  "biology",
                  "village"
            ],
            "stress": [
                  "techˈnology",
                  "geˈography",
                  "biˈology",
                  "ˈvillage"
            ]
      },
      {
            "type": "stress",
            "grade": 9,
            "answer": "D",
            "explain": "engineer nhấn âm cuối. Confident, cognitive, concentrate thường nhấn âm 1.",
            "options": [
                  "confident",
                  "cognitive",
                  "concentrate",
                  "engineer"
            ],
            "stress": [
                  "ˈconfident",
                  "ˈcognitive",
                  "ˈconcentrate",
                  "engiˈneer"
            ]
      }
];

    const state = {
      current:null,
      answered:false,
      score:loadJSON('vistaIpaPronScore_v3',{correct:0,wrong:0}),
      exam:[],
      examAns:{},
      submitted:false
    };

    function init() {
      document.documentElement.dataset.theme = localStorage.getItem('vistaIpaPronTheme_v3') || 'light';
      document.getElementById('statSounds').textContent = ipaSounds.length;
      document.getElementById('statQuestions').textContent = questions.length;
      renderIpaChart();
      renderTheory();
      updateScore();
      newQuestion();
      createExam(false);
      setupKeys();
    }

    function showView(view) {
      document.querySelectorAll('.view').forEach(x => x.classList.remove('active'));
      document.getElementById(view + 'View').classList.add('active');

      document.querySelectorAll('.tab').forEach(x => {
        x.classList.toggle('active', x.dataset.view === view);
      });

      if (view === 'ipa') renderIpaChart();
      if (view === 'theory') renderTheory();
      if (view === 'practice' && !state.current) newQuestion();
    }

    function renderIpaChart() {
      const group = document.getElementById('soundGroup').value;
      const keyword = document.getElementById('searchInput').value.trim().toLowerCase();

      const filtered = ipaSounds.filter(item => {
        const groupOk = group === 'all' || item.group === group;
        const text = `${item.s} ${item.name} ${item.guide} ${item.sample} ${item.ipa} ${item.meaning} ${item.words.join(' ')}`.toLowerCase();
        const keywordOk = !keyword || text.includes(keyword);
        return groupOk && keywordOk;
      });

      document.getElementById('ipaGrid').innerHTML = filtered.map(item => `
        <article class="ipa-card">
          <div class="ipa-symbol">/${escapeHtml(item.s)}/</div>
          <h3>${escapeHtml(item.name)}</h3>
          <div class="ipa-guide">
            <b>Cách đọc phiên âm:</b> ${escapeHtml(item.guide)}<br>
            <b>Từ mẫu:</b> ${escapeHtml(item.sample)} ${escapeHtml(item.ipa)} = ${escapeHtml(item.meaning)}
          </div>
          <div class="word-list"><b>Luyện thêm:</b> ${item.words.map(escapeHtml).join(' · ')}</div>
          <div class="sound-actions">
            <button class="primary" onclick="speak('${escapeJs(item.sample)}')">🔊 Nghe từ mẫu</button>
            <button class="secondary" onclick="speak('${escapeJs(item.words.join('. '))}')">🔊 Nghe chuỗi từ</button>
          </div>
        </article>
      `).join('') || '<div class="empty">Không tìm thấy âm/từ phù hợp.</div>';
    }

    function renderTheory() {
      document.getElementById('theoryGrid').innerHTML = theory.map(item => `
        <article class="theory-card">
          <h3>${escapeHtml(item.title)}</h3>
          <div class="rule">${escapeHtml(item.rule)}</div>
          <ul>${item.points.map(p => `<li>${escapeHtml(p)}</li>`).join('')}</ul>
          <p><b>Ví dụ:</b> ${item.examples.map(escapeHtml).join(' · ')}</p>
        </article>
      `).join('');
    }

    function refreshAll() {
      renderIpaChart();
      refreshPractice();
    }

    function refreshPractice() {
      newQuestion();
      createExam(false);
    }

    function filteredQuestions() {
      const type = document.getElementById('questionTypeSelect').value;
      const grade = document.getElementById('gradeSelect').value;
      const keyword = document.getElementById('searchInput').value.trim().toLowerCase();

      return questions.filter(q => {
        const typeOk = type === 'all' || q.type === type;
        const gradeOk = grade === 'all' || String(q.grade) === grade;
        const text = JSON.stringify(q).toLowerCase();
        const keywordOk = !keyword || text.includes(keyword);
        return typeOk && gradeOk && keywordOk;
      });
    }

    function newQuestion() {
      const bank = filteredQuestions();
      state.current = bank[Math.floor(Math.random() * bank.length)];
      state.answered = false;
      document.getElementById('answerBox').classList.remove('show');

      if (!state.current) {
        document.getElementById('questionType').textContent = 'Không có câu hỏi';
        document.getElementById('questionText').textContent = 'Không có dữ liệu phù hợp với bộ lọc hiện tại.';
        document.getElementById('questionPrompt').textContent = 'Hãy đổi dạng bài, khối lớp hoặc xóa từ khóa tìm kiếm.';
        document.getElementById('optionBox').innerHTML = '';
        return;
      }

      renderPracticeQuestion(state.current);
    }

    function renderPracticeQuestion(q) {
      document.getElementById('questionType').textContent = q.type === 'sound'
        ? 'Dạng 1: Chọn từ có phần gạch chân phát âm khác'
        : 'Dạng 2: Chọn từ có trọng âm khác';

      document.getElementById('questionText').innerHTML = q.type === 'sound'
        ? 'Mark the letter A, B, C or D to indicate the word whose underlined part differs from the other three in pronunciation.'
        : 'Mark the letter A, B, C or D to indicate the word that differs from the other three in the position of primary stress.';

      document.getElementById('questionPrompt').textContent = `Từ vựng lớp ${q.grade} · ${q.rule || 'stress'}`;

      const optionData = q.type === 'sound' ? q.options : q.options.map(w => [w, '']);
      document.getElementById('optionBox').innerHTML = optionData.map((op, i) => {
        const letter = String.fromCharCode(65 + i);
        const label = q.type === 'sound' ? underline(op[0], op[1]) : escapeHtml(op[0]);
        return `<button class="option" onclick="chooseAnswer('${letter}', this)">${letter}. <span class="word">${label}</span></button>`;
      }).join('');
    }

    function underline(word, part) {
      if (!part) return escapeHtml(word);
      const lowerWord = word.toLowerCase();
      const lowerPart = part.toLowerCase();
      const index = lowerWord.indexOf(lowerPart);

      if (index < 0) return escapeHtml(word);

      return escapeHtml(word.slice(0, index))
        + '<u>' + escapeHtml(word.slice(index, index + part.length)) + '</u>'
        + escapeHtml(word.slice(index + part.length));
    }

    function chooseAnswer(letter, btn) {
      if (state.answered || !state.current) return;

      state.answered = true;
      const isCorrect = letter === state.current.answer;

      if (isCorrect) {
        state.score.correct++;
        toast('Chính xác!');
      } else {
        state.score.wrong++;
        toast('Chưa đúng, xem giải thích nhé.');
      }

      document.querySelectorAll('#optionBox .option').forEach((button, i) => {
        const optionLetter = String.fromCharCode(65 + i);
        button.disabled = true;
        if (optionLetter === state.current.answer) button.classList.add('correct');
        if (optionLetter === letter && !isCorrect) button.classList.add('wrong');
      });

      showAnswer();
      updateScore();
    }

    function showAnswer() {
      const q = state.current;
      if (!q) return;

      const answerIndex = q.answer.charCodeAt(0) - 65;
      const content = q.type === 'sound'
        ? underline(q.options[answerIndex][0], q.options[answerIndex][1])
        : `${escapeHtml(q.options[answerIndex])} — ${escapeHtml(q.stress[answerIndex])}`;

      document.getElementById('answerBox').innerHTML = `<b>Đáp án: ${q.answer}. ${content}</b><br>${escapeHtml(q.explain)}`;
      document.getElementById('answerBox').classList.add('show');
    }

    function updateScore() {
      const total = state.score.correct + state.score.wrong;
      const accuracy = total ? Math.round(state.score.correct / total * 100) : 0;

      document.getElementById('correctCount').textContent = state.score.correct;
      document.getElementById('statCorrect').textContent = state.score.correct;
      document.getElementById('wrongCount').textContent = state.score.wrong;
      document.getElementById('accuracyCount').textContent = accuracy + '%';
      document.getElementById('statAccuracy').textContent = accuracy + '%';

      saveJSON('vistaIpaPronScore_v3', state.score);
    }

    function resetScore() {
      if (!confirm('Xóa điểm luyện tập?')) return;
      state.score = { correct:0, wrong:0 };
      updateScore();
      toast('Đã xóa điểm.');
    }

    function createExam(show = true) {
      state.examAns = {};
      state.submitted = false;

      const size = Number(document.getElementById('examSize').value || 20);
      const bank = shuffle(filteredQuestions());
      state.exam = bank.slice(0, Math.min(size, bank.length));

      document.getElementById('examResult').classList.remove('show');

      if (!state.exam.length) {
        document.getElementById('examGrid').innerHTML = '<div class="empty">Không có câu hỏi phù hợp để tạo đề.</div>';
        return;
      }

      document.getElementById('examGrid').innerHTML = state.exam.map((q, index) => {
        const optionData = q.type === 'sound' ? q.options : q.options.map(w => [w, '']);
        return `
          <div class="exam-item">
            <h3>${index + 1}. ${q.type === 'sound' ? 'Choose the word whose underlined part is pronounced differently.' : 'Choose the word with different stress pattern.'}</h3>
            <div class="exam-options">
              ${optionData.map((op, i) => {
                const letter = String.fromCharCode(65 + i);
                const label = q.type === 'sound' ? underline(op[0], op[1]) : escapeHtml(op[0]);
                return `<button id="ex-${index}-${letter}" onclick="chooseExam(${index}, '${letter}')">${letter}. <span class="word">${label}</span></button>`;
              }).join('')}
            </div>
          </div>
        `;
      }).join('');

      if (show) toast('Đã tạo đề luyện tập.');
    }

    function chooseExam(index, letter) {
      if (state.submitted) return;
      state.examAns[index] = letter;

      ['A','B','C','D'].forEach(l => {
        const button = document.getElementById(`ex-${index}-${l}`);
        if (button) button.classList.toggle('selected', l === letter);
      });
    }

    function submitExam() {
      if (!state.exam.length || state.submitted) return;

      state.submitted = true;
      let correct = 0;

      state.exam.forEach((q, index) => {
        if (state.examAns[index] === q.answer) correct++;

        ['A','B','C','D'].forEach(letter => {
          const button = document.getElementById(`ex-${index}-${letter}`);
          if (!button) return;
          button.disabled = true;
          if (letter === q.answer) button.classList.add('correct');
          if (state.examAns[index] === letter && letter !== q.answer) button.classList.add('wrong');
        });
      });

      const percent = Math.round(correct / state.exam.length * 100);
      document.getElementById('examResult').innerHTML = `Kết quả: ${correct}/${state.exam.length} câu đúng (${percent}%). ${percent >= 80 ? 'Rất tốt!' : 'Cần xem lại lý thuyết và luyện thêm.'}`;
      document.getElementById('examResult').classList.add('show');
    }

    function speakCurrent() {
      if (!state.current) return;
      const words = state.current.type === 'sound'
        ? state.current.options.map(x => x[0])
        : state.current.options;
      speak(words.join('. '));
    }

    function speak(text) {
      if (!('speechSynthesis' in window)) {
        alert('Trình duyệt chưa hỗ trợ đọc tự động.');
        return;
      }

      speechSynthesis.cancel();
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = 'en-US';
      utterance.rate = .82;
      speechSynthesis.speak(utterance);
    }

    function toggleTheme() {
      const html = document.documentElement;
      html.dataset.theme = html.dataset.theme === 'dark' ? 'light' : 'dark';
      localStorage.setItem('vistaIpaPronTheme_v3', html.dataset.theme);
    }

    function toast(message) {
      const element = document.getElementById('toast');
      element.textContent = message;
      element.classList.add('show');
      clearTimeout(toast.timer);
      toast.timer = setTimeout(() => element.classList.remove('show'), 2200);
    }

    function shuffle(array) {
      return [...array].sort(() => Math.random() - .5);
    }

    function saveJSON(key, value) {
      try {
        localStorage.setItem(key, JSON.stringify(value));
      } catch (error) {}
    }

    function loadJSON(key, fallback) {
      try {
        return JSON.parse(localStorage.getItem(key)) || fallback;
      } catch (error) {
        return fallback;
      }
    }

    function escapeHtml(text) {
      return String(text)
        .replace(/&/g,'&amp;')
        .replace(/</g,'&lt;')
        .replace(/>/g,'&gt;')
        .replace(/"/g,'&quot;')
        .replace(/'/g,'&#039;');
    }

    function escapeJs(text) {
      return String(text).replace(/\\/g, '\\\\').replace(/'/g, "\\'");
    }

    function setupKeys() {
      document.addEventListener('keydown', e => {
        const tag = document.activeElement.tagName.toLowerCase();
        if (tag === 'input' || tag === 'select') return;

        if (e.key === 'Enter') newQuestion();
        if (e.key.toLowerCase() === 'h') showAnswer();

        const number = Number(e.key);
        if (number >= 1 && number <= 4) {
          const button = document.querySelectorAll('#optionBox .option')[number - 1];
          if (button) button.click();
        }
      });
    }

    init();
  </script>
</body>
</html>
