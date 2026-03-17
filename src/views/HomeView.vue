<script setup lang="ts">
import SoulGlow from '../components/SoulGlow.vue'
</script>

<template>
  <div class="ws">
    <main class="main" id="top">

      <section class="hero">
        <div class="visual">
          <SoulGlow :size="240" />
        </div>
        <div class="content">
          <h1 class="title">流浪靈魂</h1>
          <p class="tagline">以缺點為主題的交友軟體</p>
          <div class="stores">
            <button class="store disabled" type="button" disabled>
              <img src="../assets/app-store.png" alt="App Store" class="store-icon">
              <span class="store-text">
                <span class="store-label">尚未開放</span>
                <span class="store-brand">App Store</span>
              </span>
            </button>
            <button class="store disabled" type="button" disabled>
              <img src="../assets/google-play.png" alt="Google Play" class="store-icon">
              <span class="store-text">
                <span class="store-label">尚未開放</span>
                <span class="store-brand">Google Play</span>
              </span>
            </button>
          </div>
        </div>
      </section>

      <section class="soul-story">
        <div class="soul-story-layout">
          <article class="soul-story-main">
            <p class="soul-story-kicker">匿名交友新方式</p>
            <h2 class="soul-story-title">從缺點開始，才有機會真正被接住</h2>
            <p class="soul-story-text">
              流浪靈魂是一款從「缺點」開始的匿名交友配對 App。你不需要展示完美形象，只要誠實放上自己的標籤，像是固執、玻璃心、社交恐懼。
            </p>
            <p class="soul-story-text">
              也許有人會喜歡你的優點，但更難得的是，有人願意理解你的不完美。
            </p>
          </article>

          <aside class="soul-story-side">
            <p class="soul-story-quote">「擁抱缺點，接受不完美」</p>
            <div class="soul-story-tags">
              <span>匿名聊天</span>
              <span>交友配對</span>
              <span>找人說說話</span>
            </div>
          </aside>
        </div>
      </section>

      <section class="features">
        <article class="feature-showcase">
          <div class="feature-copy">
            <p class="feature-kicker">Feature</p>
            <h2 class="feature-title">設定缺點
              <br>誠實面對自己
            </h2>
            <p class="feature-text">
              大部分的交友軟體，都在展示自己的最好的一面。<br>
              但真正的我們，往往不是那樣。<br>
              也許你會遇到一個人，剛好不介意你的缺點，甚至理解它。
            </p>
            <!-- <button class="feature-cta" type="button">探索功能</button> -->
          </div>
          <div class="feature-device-wrap">
            <img src="../assets/images/phone_feature1.png" alt="流浪靈魂功能畫面" class="feature-device">
          </div>
        </article>
      </section>

      <section class="flaw-marquee">
        <h2 class="flaw-marquee-title">每個缺點，都在等待被理解</h2>
        <div class="flaw-marquee-rail">
          <div class="flaw-marquee-track">
            <div class="flaw-marquee-group">
              <span class="flaw-tag">固執</span>
              <span class="flaw-tag">玻璃心</span>
              <span class="flaw-tag">社交恐懼</span>
              <span class="flaw-tag">慢熟</span>
              <span class="flaw-tag">容易尷尬</span>
              <span class="flaw-tag">過度敏感</span>
              <span class="flaw-tag">容易想太多</span>
              <span class="flaw-tag">不擅長聊天</span>
              <span class="flaw-tag">害怕被拒絕</span>
              <span class="flaw-tag">選擇困難</span>
            </div>
            <div class="flaw-marquee-group" aria-hidden="true">
              <span class="flaw-tag">固執</span>
              <span class="flaw-tag">玻璃心</span>
              <span class="flaw-tag">社交恐懼</span>
              <span class="flaw-tag">慢熟</span>
              <span class="flaw-tag">容易尷尬</span>
              <span class="flaw-tag">過度敏感</span>
              <span class="flaw-tag">容易想太多</span>
              <span class="flaw-tag">不擅長聊天</span>
              <span class="flaw-tag">害怕被拒絕</span>
              <span class="flaw-tag">選擇困難</span>
            </div>
          </div>
        </div>
        <div class="flaw-marquee-rail">
          <div class="flaw-marquee-track reverse">
            <div class="flaw-marquee-group">
              <span class="flaw-tag">不主動</span>
              <span class="flaw-tag">怕尷尬</span>
              <span class="flaw-tag">容易冷場</span>
              <span class="flaw-tag">訊息回很慢</span>
              <span class="flaw-tag">情緒起伏大</span>
              <span class="flaw-tag">太理性</span>
              <span class="flaw-tag">完美主義</span>
              <span class="flaw-tag">害怕承諾</span>
              <span class="flaw-tag">慢熱</span>
              <span class="flaw-tag">容易焦慮</span>
            </div>
            <div class="flaw-marquee-group" aria-hidden="true">
              <span class="flaw-tag">不主動</span>
              <span class="flaw-tag">怕尷尬</span>
              <span class="flaw-tag">容易冷場</span>
              <span class="flaw-tag">訊息回很慢</span>
              <span class="flaw-tag">情緒起伏大</span>
              <span class="flaw-tag">太理性</span>
              <span class="flaw-tag">完美主義</span>
              <span class="flaw-tag">害怕承諾</span>
              <span class="flaw-tag">慢熱</span>
              <span class="flaw-tag">容易焦慮</span>
            </div>
          </div>
        </div>
        <div class="flaw-marquee-rail">
          <div class="flaw-marquee-track">
            <div class="flaw-marquee-group">
              <span class="flaw-tag">容易自責</span>
              <span class="flaw-tag">嘴硬心軟</span>
              <span class="flaw-tag">需要安全感</span>
              <span class="flaw-tag">想很多才回覆</span>
              <span class="flaw-tag">不會拒絕</span>
              <span class="flaw-tag">太在意細節</span>
              <span class="flaw-tag">常常內耗</span>
              <span class="flaw-tag">不太會表達</span>
              <span class="flaw-tag">害怕麻煩別人</span>
              <span class="flaw-tag">容易胡思亂想</span>
            </div>
            <div class="flaw-marquee-group" aria-hidden="true">
              <span class="flaw-tag">容易自責</span>
              <span class="flaw-tag">嘴硬心軟</span>
              <span class="flaw-tag">需要安全感</span>
              <span class="flaw-tag">想很多才回覆</span>
              <span class="flaw-tag">不會拒絕</span>
              <span class="flaw-tag">太在意細節</span>
              <span class="flaw-tag">常常內耗</span>
              <span class="flaw-tag">不太會表達</span>
              <span class="flaw-tag">害怕麻煩別人</span>
              <span class="flaw-tag">容易胡思亂想</span>
            </div>
          </div>
        </div>
      </section>

      <section class="faq">
        <p class="faq-kicker">FAQ</p>
        <h2 class="faq-title">常見問題</h2>
        <details class="faq-item" open>
          <summary class="faq-question">流浪靈魂是什麼樣的交友軟體？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              流浪靈魂是一個以缺點為主題的匿名交友軟體
              <br>
              你不需要展示完美形象，只要誠實放上自己的標籤，像是固執、玻璃心、社交恐懼。
            </p>
          </div>
        </details>

        <details class="faq-item">
          <summary class="faq-question">什麼是讓靈魂流浪？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              我們將使用者稱為「靈魂」，將配對稱爲「流浪」，並將他們隨機漂流至其他使用者身邊，等待被接納。
            </p>
          </div>
        </details>

        <details class="faq-item">
          <summary class="faq-question">什麼是接納跟跳過？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              當你的靈魂流浪到其他人身邊，對方可以選擇接納、或是跳過你的靈魂，接納後系統會替你們開啟聊天室。
              <br>
              若被跳過，你的靈魂會繼續流浪，直到被接納為止。
            </p>
          </div>
        </details>

        <details class="faq-item">
          <summary class="faq-question">每個人都可以接納或跳過別人的靈魂嗎？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              是的，流浪靈魂的設計理念是讓每個人都可以自由地接納或跳過別人的靈魂，
              <br>
              意味著每個人都能出門流浪、以及會隨機有靈魂流浪到你身邊。
            </p>
          </div>
        </details>

        <details class="faq-item">
          <summary class="faq-question">流浪有次數上限嗎？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              是的，每日的流浪次數上限為 3 次。
            </p>
          </div>
        </details>

        <details class="faq-item">
          <summary class="faq-question">目前 App 開放下載了嗎？</summary>
          <div class="faq-answer-wrap">
            <p class="faq-answer">
              目前還在準備上架中，首頁會先顯示尚未開放，等正式上線後會第一時間更新下載連結。
            </p>
          </div>
        </details>
      </section>
    </main>
  </div>
</template>

<style>
@scope (.ws) {
  :scope {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    color: #e5e7eb;
    background-color: #192955;
  }

  .main {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 6rem;
  }
}

@scope (.hero) {
  :scope {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 92vh;
    padding-top: 1.5rem;
  }

  .content {
    display: flex;
    flex-direction: column;
    gap: 1.75rem;
    align-items: center;
  }

  .visual {
    width: min(320px, 78vw);
    aspect-ratio: 1 / 1;
    display: grid;
    place-items: center;
  }

  .title {
    font-size: clamp(3rem, 4.2vw, 3.6rem);
    letter-spacing: 0.16em;
    font-weight: 700;
    text-align: center;
  }

  .tagline {
    font-size: 1rem;
    color: #9ca3af;
    text-align: center;
  }

  .stores {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 0.5rem;
  }

  .store {
    display: inline-flex;
    align-items: center;
    gap: 0.6rem;
    padding: 0.65rem 1.3rem;
    border-radius: 999px;
    border: 1px solid rgba(148, 163, 184, 0.5);
    background: rgba(15, 23, 42, 0.95);
    color: #f9fafb;
    cursor: pointer;
    box-shadow: 0 14px 30px rgba(15, 23, 42, 0.95);
    transition:
      transform 120ms ease-out,
      box-shadow 120ms ease-out,
      border-color 120ms ease-out,
      background 120ms ease-out;
  }

  .store:hover {
    transform: translateY(-1px);
    border-color: rgba(248, 250, 252, 0.9);
    background: #020617;
  }

  .disabled {
    opacity: 0.5;
    cursor: not-allowed;
    pointer-events: none;
    background-color: #192955;
    border-color: #192955;
    color: #9ca3af;
    box-shadow: none;
    transform: none;
    transition: none;
  }

  .store-icon {
    width: 32px;
  }

  .store-text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    line-height: 1.1;
  }

  .store-label {
    font-size: 0.6rem;
    text-transform: uppercase;
    color: #9ca3af;
    padding-bottom: 4px;
  }

  .store-brand {
    font-size: 0.95rem;
    font-weight: 600;
  }
}

@scope (.features) {
  :scope {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem 0 4rem;
  }

  .feature-showcase {
    position: relative;
    isolation: isolate;
    overflow: hidden;
    width: min(1060px, 100%);
    min-height: 500px;
    border-radius: 38px;
    padding: clamp(2rem, 4.5vw, 3.5rem);
    display: grid;
    grid-template-columns: 1.05fr 0.95fr;
    gap: clamp(1.4rem, 3vw, 3rem);
    align-items: center;
    background: linear-gradient(130deg, #f5f3ff 0%, #ebe8ff 48%, #d6d1ff 100%);
    color: #22144b;
    box-shadow: 0 26px 60px rgba(9, 6, 36, 0.28);
  }

  .feature-showcase::before {
    content: '';
    position: absolute;
    inset: auto -10% -28% -10%;
    height: 60%;
    background:
      repeating-linear-gradient(
        -25deg,
        rgba(168, 124, 255, 0.18) 0 14px,
        rgba(95, 67, 221, 0.2) 14px 28px
      ),
      linear-gradient(100deg, #7c6cff 0%, #8f6fff 42%, #6f66ff 100%);
    border-radius: 48% 52% 0 0 / 60% 60% 0 0;
    z-index: -1;
  }

  .feature-copy {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    max-width: 470px;
  }

  .feature-kicker {
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: #6d58e3;
  }

  .feature-title {
    font-size: clamp(2rem, 4.2vw, 3rem);
    line-height: 1.12;
    letter-spacing: 0.02em;
    color: #201649;
  }

  .feature-text {
    font-size: 1.02rem;
    line-height: 1.72;
    color: #4e4a73;
    max-width: 42ch;
  }

  .feature-cta {
    margin-top: 0.35rem;
    width: fit-content;
    border: 0;
    border-radius: 999px;
    padding: 0.78rem 1.35rem;
    background: linear-gradient(95deg, #a462f4 0%, #ff66c3 100%);
    color: #f8f4ff;
    font-weight: 700;
    letter-spacing: 0.02em;
    box-shadow: 0 12px 24px rgba(164, 98, 244, 0.35);
  }

  .feature-device-wrap {
    display: flex;
    justify-content: center;
    align-items: flex-end;
    min-height: 360px;
  }

  .feature-device {
    width: min(380px, 92%);
    object-fit: contain;
    filter: drop-shadow(0 20px 40px rgba(45, 24, 112, 0.28));
  }
}

@scope (.soul-story) {
  :scope {
    width: min(1060px, 100%);
    margin-inline: auto;
    position: relative;
    isolation: isolate;
    padding-block: 1rem;
  }

  :scope::before {
    content: '';
    position: absolute;
    left: -6%;
    top: 6%;
    width: 220px;
    height: 220px;
    border-radius: 999px;
    background: radial-gradient(circle, rgba(104, 119, 255, 0.22), rgba(104, 119, 255, 0));
    z-index: -1;
  }

  :scope::after {
    content: '';
    position: absolute;
    right: -4%;
    bottom: 0;
    width: 180px;
    height: 180px;
    border-radius: 999px;
    background: radial-gradient(circle, rgba(130, 180, 255, 0.2), rgba(130, 180, 255, 0));
    z-index: -1;
  }

  .soul-story-layout {
    position: relative;
    display: grid;
    grid-template-columns: minmax(0, 1.4fr) minmax(240px, 0.8fr);
    gap: clamp(1.2rem, 3vw, 2.4rem);
    align-items: start;
    padding: clamp(1.1rem, 2.6vw, 1.8rem) 0;
  }

  .soul-story-main {
    padding-right: clamp(0.2rem, 1.2vw, 0.9rem);
    border-right: 1px solid rgba(119, 182, 255, 0.2);
  }

  .soul-story-kicker {
    font-size: 0.74rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #84c5ff;
    font-weight: 700;
  }

  .soul-story-title {
    margin-top: 0.65rem;
    font-size: clamp(1.9rem, 3.9vw, 2.8rem);
    line-height: 1.2;
    color: #f6f8ff;
    max-width: 18ch;
  }

  .soul-story-text {
    margin-top: 0.95rem;
    font-size: 1rem;
    line-height: 1.78;
    color: #b6c3e5;
    max-width: 58ch;
  }

  .soul-story-side {
    align-self: center;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding-left: clamp(0.2rem, 1vw, 0.8rem);
  }

  .soul-story-quote {
    font-size: clamp(1.1rem, 2.3vw, 1.45rem);
    line-height: 1.4;
    color: #dfe8ff;
    letter-spacing: 0.02em;
  }

  .soul-story-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .soul-story-tags span {
    border-radius: 999px;
    border: 1px solid rgba(144, 181, 255, 0.35);
    background: rgba(31, 51, 106, 0.58);
    color: #d4e4ff;
    padding: 0.44rem 0.9rem;
    font-size: 0.84rem;
  }
}

@scope (.flaw-marquee) {
  :scope {
    width: min(1060px, 100%);
    margin-inline: auto;
    border-radius: 28px;
    padding: clamp(1.2rem, 2.8vw, 1.9rem);
  }

  .flaw-marquee-kicker {
    text-align: center;
    font-size: 0.73rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: #7cc2ff;
    font-weight: 700;
  }

  .flaw-marquee-title {
    margin-top: 0.5rem;
    text-align: center;
    font-size: clamp(1.6rem, 2.9vw, 2.1rem);
    color: #f4f8ff;
  }

  .flaw-marquee-rail {
    margin-top: 1.3rem;
    overflow: hidden;
    mask-image: linear-gradient(90deg, transparent, #000 8%, #000 92%, transparent);
  }

  .flaw-marquee-track {
    width: max-content;
    display: flex;
    align-items: center;
    gap: 0.85rem;
    animation: flaw-scroll 34s linear infinite;
  }

  .flaw-marquee-track.reverse {
    animation-name: flaw-scroll-reverse;
    animation-duration: 38s;
  }

  .flaw-marquee-group {
    display: flex;
    align-items: center;
    gap: 0.85rem;
  }

  .flaw-tag {
    flex: 0 0 auto;
    white-space: nowrap;
    border-radius: 999px;
    border: 1px solid rgba(122, 175, 255, 0.38);
    background: rgba(20, 41, 92, 0.88);
    color: #dce9ff;
    padding: 0.5rem 0.9rem;
    font-size: 0.9rem;
    line-height: 1;
    box-shadow: inset 0 1px 0 rgba(177, 209, 255, 0.18);
  }

  @keyframes flaw-scroll {
    from {
      transform: translateX(-50%);
    }

    to {
      transform: translateX(0);
    }
  }

  @keyframes flaw-scroll-reverse {
    from {
      transform: translateX(0);
    }

    to {
      transform: translateX(-50%);
    }
  }
}

@scope (.faq) {
  :scope {
    width: min(1060px, 100%);
    margin-inline: auto;
    padding: clamp(1.2rem, 2.8vw, 2rem) 0 4.5rem;
  }

  .faq-title {
    margin-top: 0.55rem;
    text-align: center;
    font-size: clamp(1.75rem, 3.2vw, 2.2rem);
    color: #f6f8ff;
  }

  .faq-kicker {
    text-align: center;
    font-size: 0.73rem;
    letter-spacing: 0.17em;
    text-transform: uppercase;
    color: #77b6ff;
    font-weight: 700;
  }

  .faq-item {
    margin-top: 0.9rem;
    border: 1px solid rgba(196, 210, 236, 0.5);
    border-radius: 14px;
    background: #f8fbff;
    color: #111827;
    overflow: hidden;
  }

  .faq-question {
    list-style: none;
    cursor: pointer;
    position: relative;
    text-align: left;
    padding: 1rem 3.3rem 1rem 1.1rem;
    font-size: 1rem;
    font-weight: 600;
    color: #1f2937;
  }

  .faq-question::-webkit-details-marker {
    display: none;
  }

  .faq-question::after {
    content: '+';
    position: absolute;
    right: 0.85rem;
    top: 50%;
    transform: translateY(-50%);
    width: 24px;
    height: 24px;
    border-radius: 999px;
    display: grid;
    place-items: center;
    background: #2f80ff;
    color: #fff;
    font-size: 1rem;
    font-weight: 700;
    line-height: 1;
  }

  .faq-item[open] .faq-question::after {
    content: '-';
  }

  .faq-answer-wrap {
    display: grid;
    grid-template-rows: 0fr;
    opacity: 0;
    overflow: hidden;
    transition:
      grid-template-rows 320ms ease,
      opacity 240ms ease;
  }

  .faq-item > .faq-answer-wrap {
    display: grid;
  }

  .faq-item[open] .faq-answer-wrap {
    grid-template-rows: 1fr;
    opacity: 1;
  }

  .faq-answer {
    min-height: 0;
    padding: 0 1.1rem;
    font-size: 0.93rem;
    line-height: 1.65;
    color: #4b5563;
    transition: padding 300ms ease;
  }

  .faq-item[open] .faq-answer {
    padding: 0.1rem 1.1rem 1rem;
  }
}

@media (max-width: 960px) {
  @scope (.ws) {
    .main {
      padding-inline: 1.5rem;
    }
  }

  @scope (.soul-story) {
    .soul-story-layout {
      grid-template-columns: 1fr;
      gap: 1rem;
    }

    .soul-story-main {
      border-right: 0;
      padding-right: 0;
    }

    .soul-story-side {
      padding-left: 0;
    }

    .soul-story-title {
      max-width: none;
    }
  }

  @scope (.faq) {
    :scope {
      padding-bottom: 3.2rem;
    }
  }
}

@media (max-width: 640px) {
  @scope (.hero) {
    :scope {
      min-height: auto;
      padding-top: 1rem;
      gap: 2.4rem;
    }

    .visual {
      width: min(260px, 74vw);
    }

    .stores {
      flex-direction: column;
      align-items: center;
    }
  }

  @scope (.features) {
    :scope {
      min-height: auto;
      padding: 0.5rem 0 2rem;
    }

    .feature-showcase {
      grid-template-columns: 1fr;
      min-height: auto;
      border-radius: 30px;
      padding: 1.6rem 1.2rem 2.2rem;
      text-align: center;
    }

    .feature-copy {
      max-width: none;
      align-items: center;
    }

    .feature-title {
      font-size: clamp(1.65rem, 8.2vw, 2.1rem);
    }

    .feature-text {
      font-size: 0.95rem;
      line-height: 1.68;
    }

    .feature-device-wrap {
      min-height: auto;
      margin-top: 0.3rem;
    }

    .feature-device {
      width: min(315px, 90%);
    }
  }

  @scope (.ws) {
    .main {
      padding-inline: 1.25rem;
    }
  }

  @scope (.soul-story) {
    :scope {
      padding-block: 0.3rem;
    }

    .soul-story-layout {
      gap: 0.85rem;
      padding: 0.7rem 0;
    }

    .soul-story-title {
      font-size: clamp(1.55rem, 8vw, 2rem);
    }

    .soul-story-text {
      font-size: 0.93rem;
      line-height: 1.7;
    }

    .soul-story-quote {
      font-size: 1.02rem;
    }
  }

  @scope (.flaw-marquee) {
    :scope {
      border-radius: 22px;
      padding: 1.2rem 0.95rem;
    }

    .flaw-marquee-title {
      font-size: clamp(1.45rem, 7vw, 1.9rem);
    }

    .flaw-marquee-rail {
      margin-top: 1rem;
    }

    .flaw-marquee-track,
    .flaw-marquee-group {
      gap: 0.65rem;
    }

    .flaw-tag {
      font-size: 0.84rem;
      padding: 0.45rem 0.78rem;
    }

    .flaw-marquee-track {
      animation-duration: 26s;
    }

    .flaw-marquee-track.reverse {
      animation-duration: 30s;
    }
  }

  @scope (.faq) {
    :scope {
      padding-bottom: 2.5rem;
    }

    .faq-title {
      font-size: clamp(1.45rem, 7vw, 1.9rem);
    }

    .faq-question {
      padding: 0.92rem 3rem 0.92rem 0.9rem;
      font-size: 0.95rem;
    }

    .faq-answer {
      padding: 0 0.9rem;
      font-size: 0.89rem;
    }

    .faq-item[open] .faq-answer {
      padding: 0.1rem 0.9rem 0.92rem;
    }
  }
}
</style>
