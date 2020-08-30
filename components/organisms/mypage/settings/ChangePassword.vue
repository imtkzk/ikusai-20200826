<template>
      <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">パスワードの変更</h2>
        </div>
        <div class="profile-edit profile-edit--sub">
          <div class="form">
            <dl class="form-input">
              <dt>新規のパスワードを入力</dt>
              <dd class="form-mypage">
                <div class="profile-update-btn-input">
                  <div><input type="password" placeholder="新規パスワード"></div>
                  <div><input type="password" placeholder="再度新規パスワードを入力（確認用）"></div>
                </div>
                <div class="profile-update-btn">
                  <div class="myedit-btn myedit-btn--orange myedit-btn--low">
                    <div></div>
                    <span><button type="submit" name="" value="submit" class="form-edit-btn">更新</button></span>
                  </div>
                </div>
              </dd>
            </dl>
          </div>
        </div>
      </section>
</template>


<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";
    @import "~assets/scss/profile.scss";
    @import "~assets/scss/form.scss";

</style>
