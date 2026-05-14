<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vista IPA Learning App</title>
  <style>
    :root {
      --orange: #f97316;
      --orange-dark: #ea580c;
      --blue: #0f172a;
      --soft: #fff7ed;
      --light: #f8fafc;
      --border: #e2e8f0;
      --text: #1e293b;
      --muted: #64748b;
      --green: #16a34a;
      --red: #dc2626;
      --shadow: 0 18px 45px rgba(15, 23, 42, 0.12);
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, Helvetica, sans-serif;
      background: linear-gradient(135deg, #fff7ed 0%, #ffffff 42%, #eff6ff 100%);
      color: var(--text);
      min-height: 100vh;
    }

    header {
      padding: 28px 18px 20px;
      background: radial-gradient(circle at top left, rgba(249, 115, 22, 0.18), transparent 38%), #ffffffcc;
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 20;
    }

    .header-inner {
      max-width: 1180px;
      margin: auto;
      display: grid;
      grid-template-columns: 1.2fr 0.8fr;
      gap: 20px;
      align-items: center;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-bottom: 8px;
    }

    .logo {
      width: 46px;
      height: 46px;
      display: grid;
      place-items: center;
      border-radius: 16px;
      background: linear-gradient(135deg, var(--orange), #fb923c);
      color: white;
      font-weight: 900;
      font-size: 22px;
      box-shadow: 0 10px 24px rgba(249, 115, 22, 0.28);
    }

    h1 {
      margin: 0;
      font-size: clamp(28px, 4vw, 48px);
      letter-spacing: -1px;
      color: var(--blue);
      line-height: 1.06;
    }

    .subtitle {
      margin: 12px 0 0;
      color: var(--muted);
      font-size: 16px;
      line-height: 1.55;
      max-width: 760px;
    }

    .hero-card {
      background: #ffffff;
      border: 1px solid var(--border);
      border-radius: 28px;
      padding: 22px;
      box-shadow: var(--shadow);
    }

    .hero-card strong {
      color: var(--orange-dark);
    }

    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
      margin-top: 16px;
    }

    .stat {
      background: var(--soft);
      border: 1px solid #fed7aa;
      border-radius: 18px;
      padding: 12px;
      text-align: center;
    }

    .stat b {
      display: block;
      font-size: 22px;
      color: var(--orange-dark);
    }

    .stat span {
      font-size: 12px;
      color: var(--muted);
    }

    main {
      max-width: 1180px;
      margin: 24px auto 60px;
      padding: 0 18px;
    }

    .toolbar {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 18px;
    }

    .tabs, .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    button, .filter-btn {
      border: 0;
      cursor: pointer;
      font-weight: 700;
      border-radius: 999px;
      padding: 11px 16px;
      transition: 0.2s ease;
      font-size: 14px;
    }

    .tab-btn {
      background: white;
      color: var(--blue);
      border: 1px solid var(--border);
    }

    .tab-btn.active, .filter-btn.active {
      background: var(--orange);
      color: white;
      box-shadow: 0 8px 20px rgba(249, 115, 22, 0.25);
    }

    .filter-btn {
      background: #f1f5f9;
      color: var(--blue);
      border: 1px solid var(--border);
    }

    .search-box {
      display: flex;
      gap: 10px;
      align-items: center;
      background: white;
      border: 1px solid var(--border);
      border-radius: 999px;
      padding: 8px 14px;
      min-width: min(100%, 310px);
      box-shadow: 0 8px 25px rgba(15, 23, 42, 0.05);
    }

    .search-box input {
      border: 0;
      outline: 0;
      width: 100%;
      font-size: 15px;
    }

    .panel {
      display: none;
    }

    .panel.active {
      display: block;
      animation: fadeIn 0.25s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(8px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .ipa-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(230px, 1fr));
      gap: 14px;
    }

    .sound-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 24px;
      padding: 18px;
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
      transition: 0.22s ease;
      position: relative;
      overflow: hidden;
    }

    .sound-card::after {
      content: "";
      position: absolute;
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: rgba(249, 115, 22, 0.08);
      right: -32px;
      top: -32px;
    }

    .sound-card:hover {
      transform: translateY(-4px);
      box-shadow: var(--shadow);
      border-color: #fdba74;
    }

    .symbol {
      font-size: 42px;
      font-weight: 900;
      color: var(--orange-dark);
      line-height: 1;
    }

    .label {
      margin: 8px 0 6px;
      font-weight: 800;
      color: var(--blue);
    }

    .sound-line {
      margin: 8px 0;
      background: #f8fafc;
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 10px;
      font-size: 14px;
      line-height: 1.45;
    }

    .sound-line b {
      color: var(--orange-dark);
    }

    .example {
      color: var(--muted);
      font-size: 14px;
      line-height: 1.45;
    }

    .practice-words {
      margin-top: 10px;
      background: #fff7ed;
      border: 1px solid #fed7aa;
      border-radius: 16px;
      padding: 10px;
      font-size: 13px;
      line-height: 1.5;
      color: #7c2d12;
    }

    .practice-words b {
      color: var(--orange-dark);
    }

    .tag {
      display: inline-block;
      margin-top: 10px;
      background: #f1f5f9;
      color: #475569;
      border-radius: 999px;
      padding: 5px 9px;
      font-size: 12px;
      font-weight: 700;
    }

    .btn-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      margin-top: 14px;
    }

    .speak-btn {
      background: var(--blue);
      color: white;
      width: 100%;
      padding-left: 8px;
      padding-right: 8px;
      font-size: 13px;
    }

    .ipa-btn {
      background: var(--orange);
      color: white;
      width: 100%;
      padding-left: 8px;
      padding-right: 8px;
      font-size: 13px;
    }

    .speak-btn:hover {
      background: #020617;
    }

    .ipa-btn:hover {
      background: var(--orange-dark);
    }

    .section-title {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 16px;
      margin: 30px 0 16px;
    }

    .section-title h2 {
      margin: 0;
      font-size: 26px;
      color: var(--blue);
    }

    .note {
      background: #fffbeb;
      border: 1px solid #fde68a;
      color: #854d0e;
      padding: 14px 16px;
      border-radius: 18px;
      margin-bottom: 18px;
      line-height: 1.5;
    }

    .mouth-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 16px;
    }

    .mouth-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 24px;
      padding: 18px;
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.06);
    }

    .mouth-card h3 {
      margin: 0 0 8px;
      color: var(--orange-dark);
    }

    .mouth-card p {
      margin: 0;
      color: var(--muted);
      line-height: 1.55;
    }

    .quiz-box {
      background: white;
      border: 1px solid var(--border);
      border-radius: 28px;
      box-shadow: var(--shadow);
      padding: 24px;
    }

    .quiz-question {
      font-size: 22px;
      font-weight: 900;
      color: var(--blue);
      margin-bottom: 16px;
    }

    .options {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
      gap: 12px;
    }

    .option {
      background: #f8fafc;
      border: 1px solid var(--border);
      color: var(--blue);
      border-radius: 16px;
      padding: 14px;
      font-size: 18px;
    }

    .option.correct {
      background: #dcfce7;
      border-color: #86efac;
      color: #166534;
    }

    .option.wrong {
      background: #fee2e2;
      border-color: #fecaca;
      color: #991b1b;
    }

    .quiz-actions {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      margin-top: 18px;
    }

    .primary-btn {
      background: var(--orange);
      color: white;
    }

    .primary-btn:hover {
      background: var(--orange-dark);
    }

    .secondary-btn {
      background: #f1f5f9;
      color: var(--blue);
      border: 1px solid var(--border);
    }

    .feedback {
      margin-top: 16px;
      font-weight: 800;
    }

    .footer {
      margin-top: 36px;
      text-align: center;
      color: var(--muted);
      font-size: 14px;
    }

    @media (max-width: 780px) {
      .header-inner {
        grid-template-columns: 1fr;
      }

      .stats {
        grid-template-columns: 1fr 1fr 1fr;
      }

      .toolbar {
        align-items: stretch;
      }

      .search-box {
        width: 100%;
      }
    }
  </style>
</head>
<body>
  <header>
    <div class="header-inner">
      <div>
        <div class="brand">
          <div class="logo">V</div>
          <div>
            <strong>Vista Learning Hub</strong><br />
            <span style="color:#64748b">IPA Interactive Web App</span>
          </div>
        </div>
        <h1>Bảng phiên âm quốc tế IPA</h1>
        <p class="subtitle">
          Học phát âm tiếng Anh qua bảng IPA tương tác: xem cách đọc riêng từng ký hiệu, nghe âm mẫu, nghe từ mẫu, học khẩu hình và luyện tập nhanh.
        </p>
      </div>

      <div class="hero-card">
        <strong>Mục tiêu bài học</strong>
        <p style="line-height:1.55;color:#64748b;margin-bottom:0">
          Học sinh nhận diện được âm IPA, biết cách mở miệng - đặt lưỡi - bật hơi, sau đó liên hệ âm với từ vựng quen thuộc.
        </p>
        <div class="stats">
          <div class="stat"><b>20</b><span>Nguyên âm</span></div>
          <div class="stat"><b>24</b><span>Phụ âm</span></div>
          <div class="stat"><b>2</b><span>Nút nghe</span></div>
        </div>
      </div>
    </div>
  </header>

  <main>
    <div class="toolbar">
      <div class="tabs">
        <button class="tab-btn active" onclick="showPanel('chart', this)">📘 Bảng IPA</button>
        <button class="tab-btn" onclick="showPanel('guide', this)">🎯 Cách học</button>
        <button class="tab-btn" onclick="showPanel('quiz', this)">🧠 Luyện tập</button>
      </div>

      <div class="search-box">
        🔎
        <input id="searchInput" type="text" placeholder="Tìm âm, từ mẫu, cách đọc..." oninput="renderCards()" />
      </div>
    </div>

    <section id="chart" class="panel active">
      <div class="filters">
        <button class="filter-btn active" onclick="setFilter('all', this)">Tất cả</button>
        <button class="filter-btn" onclick="setFilter('monophthong', this)">Nguyên âm đơn</button>
        <button class="filter-btn" onclick="setFilter('diphthong', this)">Nguyên âm đôi</button>
        <button class="filter-btn" onclick="setFilter('voiceless', this)">Phụ âm vô thanh</button>
        <button class="filter-btn" onclick="setFilter('voiced', this)">Phụ âm hữu thanh</button>
      </div>

      <div class="section-title">
        <h2>Danh sách âm IPA</h2>
      </div>

      <div class="note">
        Mỗi thẻ có 2 nút: <b>Nghe âm IPA</b> để nghe âm/syllable mô phỏng riêng của ký hiệu, và <b>Nghe từ mẫu</b> để nghe âm đó trong một từ thật. Trình duyệt không luôn đọc được ký hiệu IPA cô lập tuyệt đối, nên app dùng âm mô phỏng gần nhất kết hợp với hướng dẫn khẩu hình.
      </div>

      <div id="ipaGrid" class="ipa-grid"></div>
    </section>

    <section id="guide" class="panel">
      <div class="section-title">
        <h2>Cách học IPA hiệu quả</h2>
      </div>

      <div class="mouth-grid">
        <div class="mouth-card">
          <h3>1. Phân biệt âm và chữ</h3>
          <p>Chữ cái là cách viết, còn IPA là cách đọc. Ví dụ chữ “a” có thể đọc là /æ/ trong “cat”, /eɪ/ trong “cake”, hoặc /ə/ trong “about”.</p>
        </div>
        <div class="mouth-card">
          <h3>2. Học theo khẩu hình</h3>
          <p>Không chỉ nhìn ký hiệu. Hãy quan sát miệng mở rộng hay hẹp, lưỡi cao hay thấp, âm có rung cổ hay không.</p>
        </div>
        <div class="mouth-card">
          <h3>3. Học theo cặp dễ nhầm</h3>
          <p>Ưu tiên luyện các cặp như /iː/ - /ɪ/, /æ/ - /e/, /ʃ/ - /s/, /tʃ/ - /ʃ/, /θ/ - /t/ để tránh lỗi phát âm phổ biến.</p>
        </div>
        <div class="mouth-card">
          <h3>4. Nghe - nhại - ghi âm</h3>
          <p>Bấm nghe âm IPA trước, đọc nhại lại 3 lần, sau đó nghe từ mẫu. Cuối cùng tự ghi âm và so sánh.</p>
        </div>
      </div>

      <div class="section-title">
        <h2>Nhóm âm trọng tâm cho học sinh Việt Nam</h2>
      </div>

      <div class="mouth-grid">
        <div class="mouth-card">
          <h3>/θ/ và /ð/</h3>
          <p>Đặt đầu lưỡi nhẹ giữa hai hàm răng. /θ/ là âm vô thanh trong “think”, /ð/ là âm hữu thanh trong “this”.</p>
        </div>
        <div class="mouth-card">
          <h3>/ʃ/ và /tʃ/</h3>
          <p>/ʃ/ như trong “she”, kéo hơi dài. /tʃ/ như trong “chair”, có âm bật ở đầu.</p>
        </div>
        <div class="mouth-card">
          <h3>/iː/ và /ɪ/</h3>
          <p>/iː/ dài và căng hơn trong “sheep”. /ɪ/ ngắn và thả lỏng hơn trong “ship”.</p>
        </div>
        <div class="mouth-card">
          <h3>Âm cuối</h3>
          <p>Không bỏ âm cuối trong các từ như “book”, “name”, “liked”, “dogs”. Âm cuối giúp người nghe hiểu đúng nghĩa.</p>
        </div>
      </div>
    </section>

    <section id="quiz" class="panel">
      <div class="section-title">
        <h2>Luyện tập nhanh</h2>
      </div>

      <div class="quiz-box">
        <div id="quizQuestion" class="quiz-question"></div>
        <div id="quizOptions" class="options"></div>
        <div id="quizFeedback" class="feedback"></div>
        <div class="quiz-actions">
          <button class="primary-btn" onclick="newQuestion()">Câu tiếp theo</button>
          <button class="secondary-btn" onclick="speak(currentQuestion.word, 0.78)">Nghe từ mẫu</button>
        </div>
      </div>
    </section>

    <div class="footer">
      © Vista Learning Hub - Web app học IPA bằng HTML, CSS và JavaScript thuần.
    </div>
  </main>

  <script>
    const sounds = [
      { symbol: "iː", type: "monophthong", label: "Nguyên âm dài", soundName: "i dài", soundText: "ee", guide: "Miệng kéo ngang, lưỡi nâng cao, đọc dài như âm 'i' kéo dài.", word: "sheep", ipa: "/ʃiːp/", meaning: "con cừu" },
      { symbol: "ɪ", type: "monophthong", label: "Nguyên âm ngắn", soundName: "i ngắn", soundText: "it", guide: "Miệng thả lỏng hơn /iː/, âm ngắn, không kéo dài.", word: "ship", ipa: "/ʃɪp/", meaning: "con tàu" },
      { symbol: "e", type: "monophthong", label: "Nguyên âm ngắn", soundName: "e ngắn", soundText: "egg", guide: "Miệng mở vừa, đọc gần giống 'e' trong tiếng Việt nhưng ngắn và gọn.", word: "bed", ipa: "/bed/", meaning: "cái giường" },
      { symbol: "æ", type: "monophthong", label: "Nguyên âm ngắn", soundName: "e bẹt / a bẹt", soundText: "cat", guide: "Miệng mở rộng, môi kéo ngang, âm nằm giữa 'e' và 'a'.", word: "cat", ipa: "/kæt/", meaning: "con mèo" },
      { symbol: "ɑː", type: "monophthong", label: "Nguyên âm dài", soundName: "a dài sâu", soundText: "ah", guide: "Miệng mở rộng, lưỡi hạ thấp, đọc âm 'a' dài và sâu.", word: "car", ipa: "/kɑːr/", meaning: "xe hơi" },
      { symbol: "ɒ", type: "monophthong", label: "Nguyên âm ngắn", soundName: "o ngắn", soundText: "hot", guide: "Miệng tròn nhẹ, âm ngắn, thường gặp trong giọng Anh - Anh.", word: "hot", ipa: "/hɒt/", meaning: "nóng" },
      { symbol: "ɔː", type: "monophthong", label: "Nguyên âm dài", soundName: "o dài", soundText: "or", guide: "Môi tròn, kéo dài âm 'o', hàm mở vừa.", word: "horse", ipa: "/hɔːs/", meaning: "con ngựa" },
      { symbol: "ʊ", type: "monophthong", label: "Nguyên âm ngắn", soundName: "u ngắn", soundText: "book", guide: "Môi tròn nhẹ, lưỡi nâng cao, âm ngắn hơn /uː/.", word: "book", ipa: "/bʊk/", meaning: "quyển sách" },
      { symbol: "uː", type: "monophthong", label: "Nguyên âm dài", soundName: "u dài", soundText: "oo", guide: "Môi tròn rõ, lưỡi nâng cao, kéo dài âm 'u'.", word: "food", ipa: "/fuːd/", meaning: "đồ ăn" },
      { symbol: "ʌ", type: "monophthong", label: "Nguyên âm ngắn", soundName: "ă / â ngắn", soundText: "up", guide: "Miệng mở tự nhiên, âm bật ngắn ở giữa miệng.", word: "cup", ipa: "/kʌp/", meaning: "cái cốc" },
      { symbol: "ɜː", type: "monophthong", label: "Nguyên âm dài", soundName: "ơ dài", soundText: "er", guide: "Môi thả lỏng, âm 'ơ' kéo dài, không cong lưỡi quá mạnh.", word: "bird", ipa: "/bɜːd/", meaning: "con chim" },
      { symbol: "ə", type: "monophthong", label: "Âm schwa", soundName: "ơ nhẹ", soundText: "about", guide: "Âm rất nhẹ và ngắn, miệng thả lỏng, thường nằm ở âm tiết không nhấn.", word: "about", ipa: "/əˈbaʊt/", meaning: "về, khoảng" },
      { symbol: "eɪ", type: "diphthong", label: "Nguyên âm đôi", soundName: "êi", soundText: "ay", guide: "Bắt đầu từ /e/, trượt dần sang /ɪ/. Không đọc rời thành hai âm.", word: "cake", ipa: "/keɪk/", meaning: "bánh" },
      { symbol: "aɪ", type: "diphthong", label: "Nguyên âm đôi", soundName: "ai", soundText: "eye", guide: "Bắt đầu từ âm /a/, trượt lên /ɪ/, giống âm 'ai' nhưng gọn hơn.", word: "bike", ipa: "/baɪk/", meaning: "xe đạp" },
      { symbol: "ɔɪ", type: "diphthong", label: "Nguyên âm đôi", soundName: "oi", soundText: "boy", guide: "Bắt đầu môi tròn ở /ɔː/, trượt sang /ɪ/.", word: "boy", ipa: "/bɔɪ/", meaning: "cậu bé" },
      { symbol: "aʊ", type: "diphthong", label: "Nguyên âm đôi", soundName: "ao", soundText: "ow", guide: "Bắt đầu mở rộng /a/, rồi tròn môi dần về /ʊ/.", word: "house", ipa: "/haʊs/", meaning: "ngôi nhà" },
      { symbol: "əʊ", type: "diphthong", label: "Nguyên âm đôi", soundName: "ơu", soundText: "oh", guide: "Bắt đầu từ âm /ə/, trượt sang /ʊ/, môi tròn dần.", word: "phone", ipa: "/fəʊn/", meaning: "điện thoại" },
      { symbol: "ɪə", type: "diphthong", label: "Nguyên âm đôi", soundName: "iə", soundText: "ear", guide: "Bắt đầu từ /ɪ/, trượt nhẹ về /ə/.", word: "near", ipa: "/nɪə/", meaning: "gần" },
      { symbol: "eə", type: "diphthong", label: "Nguyên âm đôi", soundName: "eə", soundText: "air", guide: "Bắt đầu từ /e/, trượt nhẹ về /ə/, miệng mở vừa.", word: "hair", ipa: "/heə/", meaning: "tóc" },
      { symbol: "ʊə", type: "diphthong", label: "Nguyên âm đôi", soundName: "uə", soundText: "tour", guide: "Bắt đầu từ /ʊ/, trượt nhẹ về /ə/, môi tròn rồi thả lỏng.", word: "tour", ipa: "/tʊə/", meaning: "chuyến tham quan" },
      { symbol: "p", type: "voiceless", label: "Phụ âm vô thanh", soundName: "p bật hơi", soundText: "puh", guide: "Hai môi khép lại rồi bật ra, không rung cổ họng.", word: "pen", ipa: "/pen/", meaning: "bút" },
      { symbol: "b", type: "voiced", label: "Phụ âm hữu thanh", soundName: "b", soundText: "buh", guide: "Hai môi khép lại rồi bật ra, có rung cổ họng.", word: "book", ipa: "/bʊk/", meaning: "sách" },
      { symbol: "t", type: "voiceless", label: "Phụ âm vô thanh", soundName: "t bật hơi", soundText: "tuh", guide: "Đầu lưỡi chạm lợi trên rồi bật ra, không rung cổ họng.", word: "tea", ipa: "/tiː/", meaning: "trà" },
      { symbol: "d", type: "voiced", label: "Phụ âm hữu thanh", soundName: "d", soundText: "duh", guide: "Đầu lưỡi chạm lợi trên rồi bật ra, có rung cổ họng.", word: "dog", ipa: "/dɒg/", meaning: "chó" },
      { symbol: "k", type: "voiceless", label: "Phụ âm vô thanh", soundName: "k bật hơi", soundText: "kuh", guide: "Gốc lưỡi chạm vòm mềm rồi bật ra, không rung cổ họng.", word: "key", ipa: "/kiː/", meaning: "chìa khóa" },
      { symbol: "g", type: "voiced", label: "Phụ âm hữu thanh", soundName: "g", soundText: "guh", guide: "Gốc lưỡi chạm vòm mềm rồi bật ra, có rung cổ họng.", word: "go", ipa: "/gəʊ/", meaning: "đi" },
      { symbol: "f", type: "voiceless", label: "Phụ âm vô thanh", soundName: "f", soundText: "fff", guide: "Răng trên chạm môi dưới, đẩy hơi ra, không rung cổ họng.", word: "fish", ipa: "/fɪʃ/", meaning: "cá" },
      { symbol: "v", type: "voiced", label: "Phụ âm hữu thanh", soundName: "v", soundText: "vvv", guide: "Răng trên chạm môi dưới, đẩy hơi ra, có rung cổ họng.", word: "very", ipa: "/ˈveri/", meaning: "rất" },
      { symbol: "θ", type: "voiceless", label: "Phụ âm vô thanh", soundName: "th vô thanh", soundText: "think", guide: "Đầu lưỡi đặt nhẹ giữa hai hàm răng, đẩy hơi ra, không rung cổ họng.", word: "think", ipa: "/θɪŋk/", meaning: "nghĩ" },
      { symbol: "ð", type: "voiced", label: "Phụ âm hữu thanh", soundName: "th hữu thanh", soundText: "this", guide: "Đầu lưỡi đặt nhẹ giữa hai hàm răng, đẩy hơi ra, có rung cổ họng.", word: "this", ipa: "/ðɪs/", meaning: "này" },
      { symbol: "s", type: "voiceless", label: "Phụ âm vô thanh", soundName: "s", soundText: "sss", guide: "Đầu lưỡi gần lợi trên, hơi đi qua khe hẹp, không rung cổ họng.", word: "sun", ipa: "/sʌn/", meaning: "mặt trời" },
      { symbol: "z", type: "voiced", label: "Phụ âm hữu thanh", soundName: "z", soundText: "zzz", guide: "Giống /s/ nhưng có rung cổ họng.", word: "zoo", ipa: "/zuː/", meaning: "sở thú" },
      { symbol: "ʃ", type: "voiceless", label: "Phụ âm vô thanh", soundName: "sh", soundText: "sh", guide: "Môi hơi chu, lưỡi nâng gần vòm miệng, âm gió dài, không rung cổ họng.", word: "she", ipa: "/ʃiː/", meaning: "cô ấy" },
      { symbol: "ʒ", type: "voiced", label: "Phụ âm hữu thanh", soundName: "zh", soundText: "vision", guide: "Giống /ʃ/ nhưng có rung cổ họng, thường gặp trong 'vision'.", word: "vision", ipa: "/ˈvɪʒn/", meaning: "tầm nhìn" },
      { symbol: "h", type: "voiceless", label: "Phụ âm vô thanh", soundName: "h", soundText: "huh", guide: "Đẩy hơi nhẹ từ cổ họng, không rung mạnh, miệng mở tự nhiên.", word: "hat", ipa: "/hæt/", meaning: "mũ" },
      { symbol: "tʃ", type: "voiceless", label: "Phụ âm vô thanh", soundName: "ch", soundText: "ch", guide: "Âm bật: đầu lưỡi bật ra rồi chuyển nhanh sang âm gió /ʃ/.", word: "chair", ipa: "/tʃeə/", meaning: "ghế" },
      { symbol: "dʒ", type: "voiced", label: "Phụ âm hữu thanh", soundName: "j", soundText: "judge", guide: "Giống /tʃ/ nhưng có rung cổ họng, như âm đầu trong 'jam'.", word: "jam", ipa: "/dʒæm/", meaning: "mứt" },
      { symbol: "m", type: "voiced", label: "Phụ âm hữu thanh", soundName: "m", soundText: "mmm", guide: "Hai môi khép, âm đi qua mũi, có rung.", word: "man", ipa: "/mæn/", meaning: "người đàn ông" },
      { symbol: "n", type: "voiced", label: "Phụ âm hữu thanh", soundName: "n", soundText: "nnn", guide: "Đầu lưỡi chạm lợi trên, âm đi qua mũi, có rung.", word: "name", ipa: "/neɪm/", meaning: "tên" },
      { symbol: "ŋ", type: "voiced", label: "Phụ âm hữu thanh", soundName: "ng", soundText: "sing", guide: "Gốc lưỡi nâng lên, âm đi qua mũi, giống âm cuối trong 'sing'.", word: "sing", ipa: "/sɪŋ/", meaning: "hát" },
      { symbol: "l", type: "voiced", label: "Phụ âm hữu thanh", soundName: "l", soundText: "lll", guide: "Đầu lưỡi chạm lợi trên, hơi đi hai bên lưỡi, có rung.", word: "leg", ipa: "/leg/", meaning: "chân" },
      { symbol: "r", type: "voiced", label: "Phụ âm hữu thanh", soundName: "r", soundText: "red", guide: "Lưỡi cong nhẹ hoặc kéo lùi, không chạm mạnh vào lợi như tiếng Việt.", word: "red", ipa: "/red/", meaning: "màu đỏ" },
      { symbol: "j", type: "voiced", label: "Phụ âm hữu thanh", soundName: "y", soundText: "yes", guide: "Âm giống 'y' trong tiếng Việt, lưỡi nâng cao, có rung.", word: "yes", ipa: "/jes/", meaning: "vâng" },
      { symbol: "w", type: "voiced", label: "Phụ âm hữu thanh", soundName: "w", soundText: "we", guide: "Môi tròn rồi mở nhanh, có rung, giống bắt đầu của từ 'we'.", word: "water", ipa: "/ˈwɔːtə/", meaning: "nước" }
    ];

    const practiceBank = {
      "iː": ["sheep", "green", "teacher", "three", "sea", "key", "meet", "sleep"],
      "ɪ": ["ship", "sit", "fish", "milk", "window", "picture", "little", "city"],
      "e": ["bed", "pen", "ten", "red", "head", "friend", "letter", "breakfast"],
      "æ": ["cat", "man", "bag", "family", "apple", "happy", "black", "traffic"],
      "ɑː": ["car", "father", "park", "class", "start", "garden", "market", "party"],
      "ɒ": ["hot", "dog", "box", "shop", "clock", "orange", "sorry", "hospital"],
      "ɔː": ["horse", "door", "four", "sport", "morning", "short", "talk", "water"],
      "ʊ": ["book", "good", "look", "cook", "foot", "put", "sugar", "woman"],
      "uː": ["food", "school", "moon", "blue", "room", "student", "June", "music"],
      "ʌ": ["cup", "bus", "sun", "mother", "brother", "money", "study", "country"],
      "ɜː": ["bird", "girl", "work", "world", "word", "learn", "early", "turn"],
      "ə": ["about", "banana", "teacher", "doctor", "family", "problem", "today", "again"],
      "eɪ": ["cake", "name", "day", "play", "great", "station", "table", "eight"],
      "aɪ": ["bike", "time", "five", "my", "like", "white", "high", "smile"],
      "ɔɪ": ["boy", "toy", "coin", "voice", "choice", "enjoy", "noise", "point"],
      "aʊ": ["house", "now", "cow", "town", "brown", "flower", "shower", "about"],
      "əʊ": ["phone", "go", "home", "open", "old", "road", "show", "window"],
      "ɪə": ["near", "ear", "clear", "dear", "here", "idea", "year", "beer"],
      "eə": ["hair", "chair", "pair", "where", "there", "care", "share", "parent"],
      "ʊə": ["tour", "poor", "sure", "cure", "tourist", "during", "secure", "pure"],
      "p": ["pen", "paper", "pencil", "happy", "open", "people", "map", "stop"],
      "b": ["book", "bag", "baby", "table", "brother", "black", "job", "club"],
      "t": ["tea", "teacher", "table", "city", "water", "student", "cat", "sit"],
      "d": ["dog", "day", "door", "student", "family", "good", "red", "friend"],
      "k": ["key", "cat", "school", "class", "book", "clock", "milk", "like"],
      "g": ["go", "girl", "green", "garden", "again", "big", "bag", "dog"],
      "f": ["fish", "family", "food", "phone", "photo", "coffee", "laugh", "safe"],
      "v": ["very", "video", "visit", "village", "seven", "never", "live", "love"],
      "θ": ["think", "three", "thank", "thin", "math", "birthday", "healthy", "month"],
      "ð": ["this", "that", "these", "those", "mother", "father", "brother", "weather"],
      "s": ["sun", "sit", "school", "class", "city", "lesson", "bus", "rice"],
      "z": ["zoo", "zero", "busy", "music", "easy", "does", "boys", "cars"],
      "ʃ": ["she", "ship", "shop", "English", "special", "sure", "station", "finish"],
      "ʒ": ["vision", "television", "usually", "measure", "pleasure", "decision", "treasure", "garage"],
      "h": ["hat", "house", "home", "hello", "happy", "behind", "who", "hair"],
      "tʃ": ["chair", "teacher", "children", "watch", "kitchen", "picture", "question", "choose"],
      "dʒ": ["jam", "job", "June", "orange", "village", "bridge", "large", "page"],
      "m": ["man", "mother", "morning", "family", "summer", "music", "room", "time"],
      "n": ["name", "nine", "new", "student", "morning", "green", "pen", "listen"],
      "ŋ": ["sing", "song", "English", "morning", "young", "long", "thing", "reading"],
      "l": ["leg", "like", "look", "school", "family", "yellow", "girl", "table"],
      "r": ["red", "rice", "room", "right", "friend", "green", "story", "carry"],
      "j": ["yes", "year", "young", "yellow", "student", "use", "music", "beautiful"],
      "w": ["water", "we", "window", "white", "what", "where", "weather", "swim"]
    };

    sounds.forEach(item => {
      item.practiceWords = practiceBank[item.symbol] || [item.word];
    });

    let activeFilter = "all";
    let currentQuestion = null;

    function showPanel(id, btn) {
      document.querySelectorAll('.panel').forEach(panel => panel.classList.remove('active'));
      document.getElementById(id).classList.add('active');
      document.querySelectorAll('.tab-btn').forEach(tab => tab.classList.remove('active'));
      btn.classList.add('active');
      if (id === 'quiz' && !currentQuestion) newQuestion();
    }

    function setFilter(filter, btn) {
      activeFilter = filter;
      document.querySelectorAll('.filter-btn').forEach(button => button.classList.remove('active'));
      btn.classList.add('active');
      renderCards();
    }

    function renderCards() {
      const grid = document.getElementById('ipaGrid');
      const search = document.getElementById('searchInput').value.toLowerCase().trim();

      const filtered = sounds.filter(item => {
        const matchesFilter = activeFilter === 'all' || item.type === activeFilter;
        const text = `${item.symbol} ${item.soundName} ${item.soundText} ${item.guide} ${item.word} ${item.ipa} ${item.meaning} ${item.label} ${item.practiceWords ? item.practiceWords.join(' ') : ''}`.toLowerCase();
        const matchesSearch = text.includes(search);
        return matchesFilter && matchesSearch;
      });

      grid.innerHTML = filtered.map(item => `
        <article class="sound-card">
          <div class="symbol">/${item.symbol}/</div>
          <div class="label">${item.label}</div>
          <div class="sound-line">
            <b>Cách đọc âm:</b> /${item.symbol}/ = ${item.soundName}<br />
            <b>Khẩu hình:</b> ${item.guide}
          </div>
          <div class="example">
            Từ mẫu: <b>${item.word}</b> ${item.ipa}<br />
            Nghĩa: ${item.meaning}
          </div>
          <div class="practice-words">
            <b>Từ luyện tập:</b> ${(item.practiceWords || [item.word]).join(' · ')}
          </div>
          <span class="tag">${typeName(item.type)}</span>
          <div class="btn-row">
            <button class="ipa-btn" onclick="speak('${item.soundText}', 0.6)">🔊 Nghe âm IPA</button>
            <button class="speak-btn" onclick="speak('${item.word}', 0.78)">🔊 Nghe từ mẫu</button>
          </div>
        </article>
      `).join('');

      if (!filtered.length) {
        grid.innerHTML = `<div class="note">Không tìm thấy âm phù hợp. Hãy thử từ khóa khác.</div>`;
      }
    }

    function typeName(type) {
      const names = {
        monophthong: 'Nguyên âm đơn',
        diphthong: 'Nguyên âm đôi',
        voiceless: 'Vô thanh',
        voiced: 'Hữu thanh'
      };
      return names[type] || type;
    }

    function speak(text, rate = 0.75) {
      if (!('speechSynthesis' in window)) {
        alert('Trình duyệt của bạn chưa hỗ trợ phát âm tự động.');
        return;
      }
      window.speechSynthesis.cancel();
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = 'en-US';
      utterance.rate = rate;
      utterance.pitch = 1;
      window.speechSynthesis.speak(utterance);
    }

    function shuffleArray(array) {
      return [...array].sort(() => Math.random() - 0.5);
    }

    function buildOptions(answer, type) {
      const sameGroup = sounds
        .filter(item => item.type === type && item.symbol !== answer)
        .map(item => item.symbol);
      return shuffleArray([answer, ...shuffleArray(sameGroup).slice(0, 3)]);
    }

    const quizData = sounds.flatMap(item => {
      return (item.practiceWords || [item.word]).map(word => ({
        word,
        answer: item.symbol,
        options: buildOptions(item.symbol, item.type)
      }));
    });

    function newQuestion() {
      currentQuestion = quizData[Math.floor(Math.random() * quizData.length)];
      document.getElementById('quizQuestion').innerHTML = `Từ <span style="color:#f97316">${currentQuestion.word}</span> chứa âm nào?`;
      document.getElementById('quizFeedback').textContent = '';
      document.getElementById('quizOptions').innerHTML = currentQuestion.options.map(option => `
        <button class="option" onclick="checkAnswer(this, '${option}')">/${option}/</button>
      `).join('');
    }

    function checkAnswer(btn, selected) {
      const allOptions = document.querySelectorAll('.option');
      allOptions.forEach(option => option.disabled = true);

      if (selected === currentQuestion.answer) {
        btn.classList.add('correct');
        document.getElementById('quizFeedback').innerHTML = `<span style="color:var(--green)">✅ Chính xác! ${currentQuestion.word} chứa âm /${currentQuestion.answer}/.</span>`;
      } else {
        btn.classList.add('wrong');
        allOptions.forEach(option => {
          if (option.textContent.includes(`/${currentQuestion.answer}/`)) {
            option.classList.add('correct');
          }
        });
        document.getElementById('quizFeedback').innerHTML = `<span style="color:var(--red)">❌ Chưa đúng. Đáp án đúng là /${currentQuestion.answer}/.</span>`;
      }
      speak(currentQuestion.word, 0.78);
    }

    renderCards();
  </script>
</body>
</html>
