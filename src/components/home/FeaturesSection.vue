<template>
  <section class="features">
    <article class="showcase">
      <div class="copy">
        <p class="kicker">Feature</p>
        <h2 class="title">設定缺點<br>誠實面對自己</h2>
        <p class="text">
          大部分的交友軟體，都在展示自己的最好的一面。<br>
          但真正的我們，往往不是那樣。<br>
          也許你會遇到一個人，剛好不介意你的缺點，甚至理解它。
        </p>
        <!-- <button class="cta" type="button">探索功能</button> -->
      </div>
      <div class="device-wrap">
        <img src="../../assets/images/phone_feature1.png" alt="流浪靈魂功能畫面" class="device">
      </div>
    </article>
  </section>
</template>

<style>
@scope (.features) {
  :scope {
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem 0 4rem;
  }

  .showcase {
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

  .showcase::before {
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

  .copy {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    max-width: 470px;
  }

  .kicker {
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: #6d58e3;
  }

  .title {
    font-size: clamp(2rem, 4.2vw, 3rem);
    line-height: 1.12;
    letter-spacing: 0.02em;
    color: #201649;
  }

  .text {
    font-size: 1.02rem;
    line-height: 1.72;
    color: #4e4a73;
    max-width: 42ch;
  }

  .cta {
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

  .device-wrap {
    display: flex;
    justify-content: center;
    align-items: flex-end;
    min-height: 360px;
  }

  .device {
    width: min(380px, 92%);
    object-fit: contain;
    filter: drop-shadow(0 20px 40px rgba(45, 24, 112, 0.28));
  }
}

@media (max-width: 640px) {
  @scope (.features) {
    :scope {
      min-height: auto;
      padding: 0.5rem 0 2rem;
    }

    .showcase {
      grid-template-columns: 1fr;
      min-height: auto;
      border-radius: 30px;
      padding: 1.6rem 1.2rem 2.2rem;
      text-align: center;
    }

    .copy {
      max-width: none;
      align-items: center;
    }

    .title {
      font-size: clamp(1.65rem, 8.2vw, 2.1rem);
    }

    .text {
      font-size: 0.95rem;
      line-height: 1.68;
    }

    .device-wrap {
      min-height: auto;
      margin-top: 0.3rem;
    }

    .device {
      width: min(315px, 90%);
    }
  }
}
</style>
