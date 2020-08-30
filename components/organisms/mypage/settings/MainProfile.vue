<template>
      <div class="profile-edit profile-edit--main">
        <div class="profile-edit-top">
            <UserProfileImage class="profile-edit-image" />
        </div>
        <div class="profile-edit-content">
          <div class="form">
            <dl class="form-input">
              <dt>プロフィール画像</dt>
              <dd class="form-mypage">
                <div class="profile-upload-btn">
                  <div class="myedit-btn myedit-btn--blue myedit-btn--low">
                    <div></div>
                    <span><button type="submit" name="" value="submit" class="form-edit-btn">画像をアップロード</button></span>
                  </div>
                </div>
              </dd>
            </dl>
            <dl class="form-input">
              <dt>ユーザー名</dt>
              <dd class="form-mypage">
                <div class="profile-update-btn-input">
                  <div><input type="text" placeholder="例）User Name"></div>
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
      </div>
</template>


<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";
    @import "~assets/scss/profile.scss";
    @import "~assets/scss/form.scss";

</style>

