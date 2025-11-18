<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <title>Vita K – 맞춤 비타민 솔루션</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- Pretendard 폰트 -->
  <link rel="stylesheet" as="style" crossorigin
        href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.min.css" />
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    body {
      font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
      background-image:
        linear-gradient(135deg, rgba(218, 255, 240, 0.9), rgba(225, 245, 255, 0.85)),
        url('https://images.unsplash.com/photo-1617212525490-52a79c2c1e54?auto=format&fit=crop&w=1600&q=80');
      background-size: cover;
      background-attachment: fixed;
    }
    .page { display: none; }
    .page.active { display: block; }
    .nav-active { background-color: rgba(13, 148, 136, 0.15); border-radius: 999px; }

    /* Custom Large Checkbox */
    .big-check {
      width: 20px;
      height: 20px;
    }
    .big-check:checked {
      accent-color: #0d9488; /* teal-600 */
    }
  </style>
</head>
<body class="min-h-screen text-slate-800">

<div class="min-h-screen bg-white/70 backdrop-blur-md">

  <!-- HEADER -->
  <header class="sticky top-0 z-30 border-b border-teal-100 bg-teal-50/70 backdrop-blur-md">
    <div class="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
      <button onclick="location.reload()" class="flex items-center gap-3 font-bold text-2xl text-teal-900 hover:text-teal-700">
        <div class="w-10 h-10 rounded-xl bg-teal-500 flex items-center justify-center text-white text-lg shadow">K</div>
        Vita K
      </button>
      <nav class="hidden md:flex items-center gap-4 text-sm font-semibold">
        <button onclick="location.reload()" class="px-3 py-2 hover:bg-teal-100 rounded-full">홈</button>
        <button data-target="fat" class="nav-btn px-3 py-2 hover:bg-teal-100 rounded-full">지용성 비타민</button>
        <button data-target="water" class="nav-btn px-3 py-2 hover:bg-teal-100 rounded-full">수용성 비타민</button>
        <button data-target="contact" class="nav-btn px-3 py-2 hover:bg-teal-100 rounded-full">문의하기</button>
      </nav>
      <button id="mobileMenuBtn" class="md:hidden p-2 bg-teal-600 text-white rounded">☰</button>
    </div>

    <!-- Mobile Menu -->
    <div id="mobileMenu" class="hidden md:hidden border-t border-teal-100 bg-white">
      <div class="px-4 py-2 flex flex-col gap-2 text-sm font-medium">
        <button onclick="location.reload()" class="p-2 rounded hover:bg-teal-100 text-left">홈</button>
        <button data-target="fat" class="nav-btn p-2 rounded hover:bg-teal-100 text-left">지용성 비타민</button>
        <button data-target="water" class="nav-btn p-2 rounded hover:bg-teal-100 text-left">수용성 비타민</button>
        <button data-target="contact" class="nav-btn p-2 rounded hover:bg-teal-100 text-left">문의하기</button>
      </div>
    </div>
  </header>

  <!-- MAIN -->
  <main class="max-w-6xl mx-auto px-4 py-10 space-y-10">

    <!-- HOME -->
    <section id="home" class="page active space-y-10">

      <div class="text-center space-y-4">
        <h1 class="text-4xl font-extrabold text-teal-900">🎯 나에게 맞는 비타민을 찾아보세요</h1>
        <p class="text-teal-700 text-sm">증상을 선택하면 필요한 비타민을 맞춤 추천해드려요!</p>
      </div>

      <!-- CHECKBOXES -->
      <section class="p-6 bg-white rounded-2xl shadow-md border border-teal-100 space-y-4">
        <h3 class="text-lg font-semibold text-teal-900">오늘 해당되는 증상을 선택하세요 📋</h3>

        <div class="grid sm:grid-cols-3 gap-4">
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="eye" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">👁️ 눈 피로/건조</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="blood" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🩸 혈액순환/혈관</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="dizzy" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🌪️ 어지러움</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="joint" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🦵 관절/뼈 약화</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="skin" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🧴 피부 트러블</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="stress" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">😮‍💨 스트레스</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="memory" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🧠 기억력 저하</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="gum" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">😬 잇몸 문제</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="sleep" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">😴 수면 문제</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="anemia" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">😵 빈혈</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="headache" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🤕 두통</span>
          </label>
          <label class="flex items-center gap-3 p-3 bg-teal-50 border border-teal-100 rounded-xl hover:bg-teal-100 cursor-pointer">
            <input type="checkbox" value="stomach" class="big-check" />
            <span class="text-sm text-teal-900 font-medium">🤢 소화 불편</span>
          </label>
        </div>

        <button id="calculateBtn"
          class="w-full px-6 py-3 bg-teal-600 text-white rounded-full font-semibold hover:bg-teal-700 transition">
          🎯 추천 비타민 보기
        </button>

        <div id="resultBox" class="hidden bg-teal-50 border border-teal-100 rounded-xl p-4 mt-6">
          <h4 class="text-xl text-teal-800 font-semibold mb-2">🔍 추천 비타민</h4>
          <ul id="resultList" class="text-sm text-teal-800 space-y-1"></ul>

          <div id="shoppingLinks" class="mt-4">
            <h5 class="text-sm font-semibold text-teal-900">🛒 사이트별 최저가 비교:</h5>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-2 mt-2"></div>
          </div>
        </div>
      </section>
    </section>

    <!-- FAT SOLUBLE VITAMINS -->
    <section id="fat" class="page space-y-6">
      <h2 class="text-3xl font-bold text-teal-900">🟢 지용성 비타민 (A, D, E, K)</h2>
      <p class="text-sm text-teal-800">지용성 비타민은 체내에 저장되기 때문에 과다 섭취에 주의하세요.</p>
      <ul class="grid sm:grid-cols-2 gap-4 text-sm">
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 A – 시력, 면역, 피부</li>
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 D – 뼈·관절, 칼슘흡수</li>
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 E – 항산화, 세포막 보호</li>
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 K – 혈액 응고, 뼈 건강</li>
      </ul>
      <button data-target="water" class="nav-btn bg-white border border-teal-300 text-teal-700 px-6 py-2 rounded-full shadow hover:bg-teal-100">
        수용성 비타민 보기 →
      </button>
    </section>

    <!-- WATER SOLUBLE VITAMINS -->
    <section id="water" class="page space-y-6">
      <h2 class="text-3xl font-bold text-teal-900">🔵 수용성 비타민 (B군 · C)</h2>
      <p class="text-sm text-teal-800">수용성 비타민은 체내에 저장되지 않기 때문에 매일 섭취가 필요합니다.</p>
      <ul class="grid sm:grid-cols-2 gap-4 text-sm">
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 B군 – 에너지, 신경 기능</li>
        <li class="bg-white p-4 rounded-xl border border-teal-100 shadow">비타민 C – 항산화, 면역, 피부</li>
      </ul>
      <button data-target="fat" class="nav-btn bg-white border border-teal-300 text-teal-700 px-6 py-2 rounded-full shadow hover:bg-teal-100">
        지용성 비타민 보기 →
      </button>
    </section>

<!-- CONTACT SECTION -->
<section id="contact" class="page space-y-6">
  <h2 class="text-3xl font-bold text-teal-900">문의하기 📩</h2>
  <form id="contactForm" class="bg-white p-6 rounded-xl border border-teal-100 shadow space-y-4 max-w-md">

    <!-- 문의 유형 -->
    <label class="block">
      <span class="text-sm font-medium text-teal-900">문의 유형</span>
      <select name="type" class="w-full px-4 py-2 border rounded-lg mt-1 text-sm" required>
            <option value="">문의 분류 선택</option>
            <option value="fat">지용성 비타민 관련</option>
            <option value="water">수용성 비타민 관련</option>
            <option value="price">가격/구매처 문의</option>
            <option value="feature">기능 제안</option>
            <option value="etc">기타 문의</option>
      </select>
    </label>

    <!-- 기존 폼 -->
    <input type="text" name="name" class="w-full px-4 py-2 border rounded-lg" placeholder="이름" required />
    <input type="email" name="email" class="w-full px-4 py-2 border rounded-lg" placeholder="이메일" required />
    <input type="tel" name="phone" class="w-full px-4 py-2 border rounded-lg" placeholder="전화번호 (선택)" />
    <textarea name="message" rows="4" class="w-full px-4 py-2 border rounded-lg" placeholder="문의 내용" required></textarea>

    <button class="bg-teal-600 hover:bg-teal-700 text-white px-5 py-2 rounded-lg shadow w-full">
      문의 보내기
    </button>
  </form>
</section>

  </main>

  <!-- FOOTER -->
  <footer class="text-center text-xs text-teal-700 py-8 border-t border-teal-100">
    © 2025 Vita K | 건강한 비타민 정보 페이지
  </footer>
</div>

<!-- SCRIPT -->
<script>
  // Navigation Logic
  const pages = document.querySelectorAll('.page');
  const navButtons = document.querySelectorAll('.nav-btn');
  const mobileMenuBtn = document.getElementById('mobileMenuBtn');
  const mobileMenu = document.getElementById('mobileMenu');

  function showPage(id) {
    pages.forEach(p => p.classList.toggle('active', p.id === id));
    navButtons.forEach(btn => btn.classList.toggle('nav-active', btn.dataset.target === id));
    if (!mobileMenu.classList.contains('hidden')) mobileMenu.classList.add('hidden');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  navButtons.forEach(btn => btn.addEventListener('click', () => showPage(btn.dataset.target)));
  mobileMenuBtn.addEventListener('click', () => mobileMenu.classList.toggle('hidden'));

  // Symptom-based recommendation
  const vitaminMap = {
    eye: { name: '비타민 A / 루테인', links: ['A'] },
    blood: { name: '비타민 E / K / 오메가3', links: ['E', 'K'] },
    dizzy: { name: '비타민 D / B12 / 철분', links: ['D', 'B'] },
    joint: { name: '비타민 D / K / 칼슘', links: ['D', 'K'] },
    skin: { name: '비타민 C / E / 콜라겐', links: ['C', 'E'] },
    stress: { name: '마그네슘 / 비타민 B군', links: ['B'] },
    memory: { name: '오메가3 / 비타민 B12 / E', links: ['B', 'E'] },
    gum: { name: '비타민 C / 코엔자임Q10', links: ['C'] },
    sleep: { name: '마그네슘 / 비타민 D', links: ['D'] },
    anemia: { name: '철분 / 비타민 B12 / C', links: ['B', 'C'] },
    headache: { name: '마그네슘 / 비타민 B2', links: ['B'] },
    stomach: { name: '비타민 B군 / 소화효소', links: ['B'] },
  };

  const shoppingPlatforms = [
    { name: '쿠팡', url: 'https://www.coupang.com/np/search?q=' },
    { name: '네이버쇼핑', url: 'https://search.shopping.naver.com/search/all?query=' },
    { name: '11번가', url: 'https://search.11st.co.kr/Search.tmall?kwd=' },
    { name: 'iHerb', url: 'https://kr.iherb.com/search?kw=' },
    { name: '스마트스토어', url: 'https://smartstore.naver.com/main/search?q=' }
  ];

  document.getElementById('calculateBtn').addEventListener('click', () => {
    const checked = [...document.querySelectorAll('.big-check:checked')].map(el => el.value);
    const resultBox = document.getElementById('resultBox');
    const resultList = document.getElementById('resultList');
    const shoppingLinksDiv = document.getElementById('shoppingLinks').querySelector('div');

    resultList.innerHTML = '';
    shoppingLinksDiv.innerHTML = '';

    if (!checked.length) {
      resultBox.classList.add('hidden');
      alert('증상을 한 가지 이상 선택해주세요!');
      return;
    }

    const recommendations = new Set();
    const neededVitamins = new Set();
    checked.forEach(symptom => {
      const data = vitaminMap[symptom];
      if (data) {
        recommendations.add(`🟢 ${data.name}`);
        data.links.forEach(v => neededVitamins.add(v));
      }
    });

    resultList.innerHTML = [...recommendations].map(r => `<li>${r}</li>`).join('');
    neededVitamins.forEach(v => {
      shoppingPlatforms.forEach(platform => {
        shoppingLinksDiv.innerHTML += `
          <a href="${platform.url}비타민 ${v}" target="_blank"
             class="text-xs bg-white border border-teal-200 p-2 rounded-lg shadow hover:bg-teal-50">
            ${platform.name} – 비타민 ${v} →
          </a>
        `;
      });
    });

    resultBox.classList.remove('hidden');
  });

  // Contact Form - Webhook Integration
  document.getElementById('contactForm')?.addEventListener('submit', async e => {
    e.preventDefault();
    const form = e.target;
    const data = Object.fromEntries(new FormData(form).entries());

    await fetch('https://hook.us2.make.com/757vvlqw1r1l3tmhn159oe7fooko3dak', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(data)
    });

    alert('문의가 정상적으로 접수되었습니다! 😊');
    form.reset();
  });
</script>

</body>
</html>
