<template>
  <section class="story">
    <div class="layout">
      <article class="main">
        <p class="kicker">匿名交友新方式</p>
        <h2 class="title">從缺點開始，才有機會真正被接住</h2>
        <p class="text">
          流浪靈魂是一款從「缺點」開始的匿名交友配對 App。你不需要展示完美形象，只要誠實放上自己的標籤，像是固執、玻璃心、社交恐懼。
        </p>
        <p class="text">
          也許有人會喜歡你的優點，但更難得的是，有人願意理解你的不完美。
        </p>
      </article>

      <aside class="side">
        <p class="quote">「擁抱缺點，接受不完美」</p>
        <div class="tags">
          <span>匿名聊天</span>
          <span>交友配對</span>
          <span>找人說說話</span>
        </div>
      </aside>
    </div>
  </section>
</template>

<style>
@scope (.story) {
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

  .layout {
    position: relative;
    display: grid;
    grid-template-columns: minmax(0, 1.4fr) minmax(240px, 0.8fr);
    gap: clamp(1.2rem, 3vw, 2.4rem);
    align-items: start;
    padding: clamp(1.1rem, 2.6vw, 1.8rem) 0;
  }

  .main {
    padding-right: clamp(0.2rem, 1.2vw, 0.9rem);
    border-right: 1px solid rgba(119, 182, 255, 0.2);
  }

  .kicker {
    font-size: 0.74rem;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #84c5ff;
    font-weight: 700;
  }

  .title {
    margin-top: 0.65rem;
    font-size: clamp(1.9rem, 3.9vw, 2.8rem);
    line-height: 1.2;
    color: #f6f8ff;
    max-width: 18ch;
  }

  .text {
    margin-top: 0.95rem;
    font-size: 1rem;
    line-height: 1.78;
    color: #b6c3e5;
    max-width: 58ch;
  }

  .side {
    align-self: center;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding-left: clamp(0.2rem, 1vw, 0.8rem);
  }

  .quote {
    font-size: clamp(1.1rem, 2.3vw, 1.45rem);
    line-height: 1.4;
    color: #dfe8ff;
    letter-spacing: 0.02em;
  }

  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .tags span {
    border-radius: 999px;
    border: 1px solid rgba(144, 181, 255, 0.35);
    background: rgba(31, 51, 106, 0.58);
    color: #d4e4ff;
    padding: 0.44rem 0.9rem;
    font-size: 0.84rem;
  }
}

@media (max-width: 960px) {
  @scope (.story) {
    .layout {
      grid-template-columns: 1fr;
      gap: 1rem;
    }

    .main {
      border-right: 0;
      padding-right: 0;
    }

    .side {
      padding-left: 0;
    }

    .title {
      max-width: none;
    }
  }
}

@media (max-width: 640px) {
  @scope (.story) {
    :scope {
      padding-block: 0.3rem;
    }

    .layout {
      gap: 0.85rem;
      padding: 0.7rem 0;
    }

    .title {
      font-size: clamp(1.55rem, 8vw, 2rem);
    }

    .text {
      font-size: 0.93rem;
      line-height: 1.7;
    }

    .quote {
      font-size: 1.02rem;
    }
  }
}
</style>
