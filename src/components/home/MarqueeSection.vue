<template>
  <section class="marquee">
    <h2 class="title">每個缺點，都在等待被理解</h2>
    <div class="rail">
      <div class="track">
        <div class="group">
          <span class="tag">固執</span>
          <span class="tag">玻璃心</span>
          <span class="tag">社交恐懼</span>
          <span class="tag">慢熟</span>
          <span class="tag">容易尷尬</span>
          <span class="tag">過度敏感</span>
          <span class="tag">容易想太多</span>
          <span class="tag">不擅長聊天</span>
          <span class="tag">害怕被拒絕</span>
          <span class="tag">選擇困難</span>
        </div>
        <div class="group" aria-hidden="true">
          <span class="tag">固執</span>
          <span class="tag">玻璃心</span>
          <span class="tag">社交恐懼</span>
          <span class="tag">慢熟</span>
          <span class="tag">容易尷尬</span>
          <span class="tag">過度敏感</span>
          <span class="tag">容易想太多</span>
          <span class="tag">不擅長聊天</span>
          <span class="tag">害怕被拒絕</span>
          <span class="tag">選擇困難</span>
        </div>
      </div>
    </div>
    <div class="rail">
      <div class="track reverse">
        <div class="group">
          <span class="tag">不主動</span>
          <span class="tag">怕尷尬</span>
          <span class="tag">容易冷場</span>
          <span class="tag">訊息回很慢</span>
          <span class="tag">情緒起伏大</span>
          <span class="tag">太理性</span>
          <span class="tag">完美主義</span>
          <span class="tag">害怕承諾</span>
          <span class="tag">慢熱</span>
          <span class="tag">容易焦慮</span>
        </div>
        <div class="group" aria-hidden="true">
          <span class="tag">不主動</span>
          <span class="tag">怕尷尬</span>
          <span class="tag">容易冷場</span>
          <span class="tag">訊息回很慢</span>
          <span class="tag">情緒起伏大</span>
          <span class="tag">太理性</span>
          <span class="tag">完美主義</span>
          <span class="tag">害怕承諾</span>
          <span class="tag">慢熱</span>
          <span class="tag">容易焦慮</span>
        </div>
      </div>
    </div>
    <div class="rail">
      <div class="track">
        <div class="group">
          <span class="tag">容易自責</span>
          <span class="tag">嘴硬心軟</span>
          <span class="tag">需要安全感</span>
          <span class="tag">想很多才回覆</span>
          <span class="tag">不會拒絕</span>
          <span class="tag">太在意細節</span>
          <span class="tag">常常內耗</span>
          <span class="tag">不太會表達</span>
          <span class="tag">害怕麻煩別人</span>
          <span class="tag">容易胡思亂想</span>
        </div>
        <div class="group" aria-hidden="true">
          <span class="tag">容易自責</span>
          <span class="tag">嘴硬心軟</span>
          <span class="tag">需要安全感</span>
          <span class="tag">想很多才回覆</span>
          <span class="tag">不會拒絕</span>
          <span class="tag">太在意細節</span>
          <span class="tag">常常內耗</span>
          <span class="tag">不太會表達</span>
          <span class="tag">害怕麻煩別人</span>
          <span class="tag">容易胡思亂想</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
@scope (.marquee) {
  :scope {
    width: min(1060px, 100%);
    margin-inline: auto;
    border-radius: 28px;
    padding: clamp(1.2rem, 2.8vw, 1.9rem);
  }

  .kicker {
    text-align: center;
    font-size: 0.73rem;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: #7cc2ff;
    font-weight: 700;
  }

  .title {
    margin-top: 0.5rem;
    text-align: center;
    font-size: clamp(1.6rem, 2.9vw, 2.1rem);
    color: #f4f8ff;
  }

  .rail {
    margin-top: 1.3rem;
    overflow: hidden;
    mask-image: linear-gradient(90deg, transparent, #000 8%, #000 92%, transparent);
  }

  .track {
    width: max-content;
    display: flex;
    align-items: center;
    gap: 0.85rem;
    animation: flaw-scroll 34s linear infinite;
  }

  .track.reverse {
    animation-name: flaw-scroll-reverse;
    animation-duration: 38s;
  }

  .group {
    display: flex;
    align-items: center;
    gap: 0.85rem;
  }

  .tag {
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

@media (max-width: 640px) {
  @scope (.marquee) {
    :scope {
      border-radius: 22px;
      padding: 1.2rem 0.95rem;
    }

    .title {
      font-size: clamp(1.45rem, 7vw, 1.9rem);
    }

    .rail {
      margin-top: 1rem;
    }

    .track,
    .group {
      gap: 0.65rem;
    }

    .tag {
      font-size: 0.84rem;
      padding: 0.45rem 0.78rem;
    }

    .track {
      animation-duration: 26s;
    }

    .track.reverse {
      animation-duration: 30s;
    }
  }
}
</style>
