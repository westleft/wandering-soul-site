<template>
  <section class="faq">
    <p class="kicker">FAQ</p>
    <h2 class="title">常見問題</h2>
    <details class="item" open>
      <summary class="question">流浪靈魂是什麼樣的交友軟體？</summary>
      <div class="answer-wrap">
        <p class="answer">
          流浪靈魂是一個以缺點為主題的匿名交友軟體
          <br>
          你不需要展示完美形象，只要誠實放上自己的標籤，像是固執、玻璃心、社交恐懼。
        </p>
      </div>
    </details>

    <details class="item">
      <summary class="question">什麼是讓靈魂流浪？</summary>
      <div class="answer-wrap">
        <p class="answer">
          我們將使用者稱為「靈魂」，將配對稱爲「流浪」，並將他們隨機漂流至其他使用者身邊，等待被接納。
        </p>
      </div>
    </details>

    <details class="item">
      <summary class="question">什麼是接納跟跳過？</summary>
      <div class="answer-wrap">
        <p class="answer">
          當你的靈魂流浪到其他人身邊，對方可以選擇接納、或是跳過你的靈魂，接納後系統會替你們開啟聊天室。
          <br>
          若被跳過，你的靈魂會繼續流浪，直到被接納為止。
        </p>
      </div>
    </details>

    <details class="item">
      <summary class="question">每個人都可以接納或跳過別人的靈魂嗎？</summary>
      <div class="answer-wrap">
        <p class="answer">
          是的，流浪靈魂的設計理念是讓每個人都可以自由地接納或跳過別人的靈魂，
          <br>
          意味著每個人都能出門流浪、以及會隨機有靈魂流浪到你身邊。
        </p>
      </div>
    </details>

    <details class="item">
      <summary class="question">流浪有次數上限嗎？</summary>
      <div class="answer-wrap">
        <p class="answer">
          是的，每日的流浪次數上限為 3 次。
        </p>
      </div>
    </details>

    <details class="item">
      <summary class="question">目前 App 開放下載了嗎？</summary>
      <div class="answer-wrap">
        <p class="answer">
          目前還在準備上架中，首頁會先顯示尚未開放，等正式上線後會第一時間更新下載連結。
        </p>
      </div>
    </details>
  </section>
</template>

<style>
@scope (.faq) {
  :scope {
    width: min(1060px, 100%);
    margin-inline: auto;
    padding: clamp(1.2rem, 2.8vw, 2rem) 0 4.5rem;
  }

  .title {
    margin-top: 0.55rem;
    text-align: center;
    font-size: clamp(1.75rem, 3.2vw, 2.2rem);
    color: #f6f8ff;
  }

  .kicker {
    text-align: center;
    font-size: 0.73rem;
    letter-spacing: 0.17em;
    text-transform: uppercase;
    color: #77b6ff;
    font-weight: 700;
  }

  .item {
    margin-top: 0.9rem;
    border: 1px solid rgba(196, 210, 236, 0.5);
    border-radius: 14px;
    background: #f8fbff;
    color: #111827;
    overflow: hidden;
  }

  .question {
    list-style: none;
    cursor: pointer;
    position: relative;
    text-align: left;
    padding: 1rem 3.3rem 1rem 1.1rem;
    font-size: 1rem;
    font-weight: 600;
    color: #1f2937;
  }

  .question::-webkit-details-marker {
    display: none;
  }

  .question::after {
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

  .item[open] .question::after {
    content: '-';
  }

  .answer-wrap {
    display: grid;
    grid-template-rows: 0fr;
    opacity: 0;
    overflow: hidden;
    transition:
      grid-template-rows 320ms ease,
      opacity 240ms ease;
  }

  .item > .answer-wrap {
    display: grid;
  }

  .item[open] .answer-wrap {
    grid-template-rows: 1fr;
    opacity: 1;
  }

  .answer {
    min-height: 0;
    padding: 0 1.1rem;
    font-size: 0.93rem;
    line-height: 1.65;
    color: #4b5563;
    transition: padding 300ms ease;
  }

  .item[open] .answer {
    padding: 0.1rem 1.1rem 1rem;
  }
}

@media (max-width: 960px) {
  @scope (.faq) {
    :scope {
      padding-bottom: 3.2rem;
    }
  }
}

@media (max-width: 640px) {
  @scope (.faq) {
    :scope {
      padding-bottom: 2.5rem;
    }

    .title {
      font-size: clamp(1.45rem, 7vw, 1.9rem);
    }

    .question {
      padding: 0.92rem 3rem 0.92rem 0.9rem;
      font-size: 0.95rem;
    }

    .answer {
      padding: 0 0.9rem;
      font-size: 0.89rem;
    }

    .item[open] .answer {
      padding: 0.1rem 0.9rem 0.92rem;
    }
  }
}
</style>
