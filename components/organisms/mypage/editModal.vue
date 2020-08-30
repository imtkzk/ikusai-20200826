<template>
  <div id="buy-modal" class="modal modal--large is-test">
    <div class="modal__in">
      <div id="buy-close" class="close-btn"><span></span></div>
      <h2 class="modal-head">プロフィールを完成させ、<br class="br--sp">一緒に学ぶチームと<br class="br--sp">共有しましょう。</h2>
      <p class="modal-desc">チームはあなたの入力した情報を参考し、<br class="br--sp">構成されます。</p>
      <div class="form">
        <dl class="form-input">
          <dt>性別</dt>
          <dd>
            <div class="mypage-buy-type">
              <div><label><input type="radio" name="radio-sex"><span>男性</span></label></div>
              <div><label><input type="radio" name="radio-sex"><span>女性</span></label></div>
              <div><label><input type="radio" name="radio-sex"><span>答えない</span></label></div>
            </div>
          </dd>
        </dl>
        <dl class="form-input">
          <dt>年齢</dt>
          <dd>
            <div class="form-select">
              <select name="">
                <option value="20代">20代</option>
                <option value="30代">30代</option>
                <option value="40代">40代</option>
              </select>
            </div>
          </dd>
        </dl>
        <dl class="form-input">
          <dt>プログラミング歴</dt>
          <dd>
            <div class="mypage-buy-type">
              <div><label><input type="radio" name="radio-his"><span>未経験</span></label></div>
              <div><label><input type="radio" name="radio-his"><span>1年未満</span></label></div>
              <div><label><input type="radio" name="radio-his"><span>1年~2年</span></label></div>
              <div><label><input type="radio" name="radio-his"><span>2年以上</span></label></div>
            </div>
          </dd>
        </dl>
        <dl class="form-input">
          <dt>ご使用のPC（OS）</dt>
          <dd>
            <div class="mypage-buy-type">
              <div><label><input type="radio" name="radio-device"><span>Windows</span></label></div>
              <div><label><input type="radio" name="radio-device"><span>Mac</span></label></div>
              <div><label><input type="radio" name="radio-device"><span>その他</span></label></div>
            </div>
          </dd>
        </dl>
        <dl class="form-input">
          <dt>興味のある機械学習の領域（複数選択可）</dt>
          <dd>
            <div class="mypage-buy-check">
              <div><label><input type="checkbox" name="checkbox-interest"><span>画像処理</span></label></div>
              <div><label><input type="checkbox" name="checkbox-interest"><span>自然言語処理</span></label></div>
              <div><label><input type="checkbox" name="checkbox-interest"><span>表形式のデータの取り扱い</span></label></div>
            </div>
          </dd>
        </dl>
        <dl class="form-input">
          <dt>
            <p>自己紹介</p>
            <p class="form-dt-text">簡単な自己紹介、学習の目標や、受講のきっかけなどを記入しましょう。<br>この自己紹介は一緒に学習を進めるチームメンバーが閲覧することができます。</p>
          </dt>
          <dd><textarea></textarea></dd>
        </dl>
        <div class="form-btn">
          <div class="cmn-btn cmn-btn--main cmn-btn--short">
            <div></div>
            <p><button type="submit" name="" value="submit" class="form-submit-btn">プロフィールを登録する</button></p>
          </div>
        </div>
        <div class="form-revise">
          <a href="#">後でプロフィールを記入する</a>
        </div>
      </div>
    </div>
    <div id="buy-overlay" class="modal-overlay"></div>
  </div>
</template>