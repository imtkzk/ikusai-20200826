<template>
      <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">チーム学習受講時のお願い</h2>
        </div>
        <ul class="please">
          <li>
            <h3 class="mymain-subhead">チームメンバーで協力し合いながら、学習を進めましょう！</h3>
            <p>基本的に講義は40分の動画学習、20分の演習に分かれています。動画学習ではそれぞれインプットに務めましょう。<br>20分の演習では、チームとディスカッションしても、個人で考えて取り組んでも大丈夫です。<br>質問がある場合は気軽に質問し合いましょう。教えることは自分の知識の整理につながるので、積極的に学んだ内容をチーム内でアウトプットし、より効率よく学習を進めましょう。</p>
          </li>
          <li>
            <h3 class="mymain-subhead">チームメンバーで協力し合いながら、学習を進めましょう！</h3>
            <p>基本的に講義は40分の動画学習、20分の演習に分かれています。動画学習ではそれぞれインプットに務めましょう。<br>20分の演習では、チームとディスカッションしても、個人で考えて取り組んでも大丈夫です。<br>質問がある場合は気軽に質問し合いましょう。教えることは自分の知識の整理につながるので、積極的に学んだ内容をチーム内でアウトプットし、より効率よく学習を進めましょう。</p>
          </li>
          <li>
            <h3 class="mymain-subhead">チームメンバーで協力し合いながら、学習を進めましょう！</h3>
            <p>基本的に講義は40分の動画学習、20分の演習に分かれています。動画学習ではそれぞれインプットに務めましょう。<br>20分の演習では、チームとディスカッションしても、個人で考えて取り組んでも大丈夫です。<br>質問がある場合は気軽に質問し合いましょう。教えることは自分の知識の整理につながるので、積極的に学んだ内容をチーム内でアウトプットし、より効率よく学習を進めましょう。</p>
          </li>
          <li>
            <h3 class="mymain-subhead">チームメンバーで協力し合いながら、学習を進めましょう！</h3>
            <p>基本的に講義は40分の動画学習、20分の演習に分かれています。動画学習ではそれぞれインプットに務めましょう。<br>20分の演習では、チームとディスカッションしても、個人で考えて取り組んでも大丈夫です。<br>質問がある場合は気軽に質問し合いましょう。教えることは自分の知識の整理につながるので、積極的に学んだ内容をチーム内でアウトプットし、より効率よく学習を進めましょう。</p>
          </li>
        </ul>
      </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ---------------------------------- please */

.please {
  margin-bottom: vw-sp(20);
}

.please li {
  margin-bottom: vw-sp(20);
  padding: vw-sp(35);
  background-color: $color-base;
  p {
    line-height: 1.8em;
  }
}

.please li:last-child {
  margin-bottom: 0;
}

@media screen and (min-width: $breakpoint1) {

  .please {
    margin-bottom: vw-pc(10);
  }

  .please li {
    margin-bottom: vw-pc(10);
    padding: vw-pc(30);
  }
}

</style>
