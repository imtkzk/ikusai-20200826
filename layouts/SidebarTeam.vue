<template>
        <aside id="sidebar" class="sidebar">
        <ul class="sidemenu">
            <li class="sidemenu-dashbord"><a href="index.html">ダッシュボード</a></li>
            <li class="sidemenu-team is-active"><a href="team.html">チーム学習</a></li>
            <li class="sidemenu-skill"><a href="skill.html">獲得スキル一覧</a></li>
            <li class="sidemenu-profile"><a href="profile.html">プロフィール</a></li>
        </ul>
        </aside>
</template>


<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ------------------------------------ sidemenu */
.sidemenu li a {
 position: relative;
 display: flex;
 align-items: center;
 color: #fff;
 font-size: 2.4vw;
 font-weight: 700;
}

.sidemenu li a:hover {
 background-color: #1a3f6d;
 color: #28d089;
}

.sidemenu li.is-active a {
 background-color: #1a3f6d;
}

.sidemenu li a:before {
 content: '';
 position: absolute;
 display: inline-block;
 background-size: contain;
 background-repeat: no-repeat;
}

.sidemenu li.sidemenu-dashbord a:before {
 width: 5.6vw;
 height: 5.6vw;
 background-image: url(~assets/img/mypage/dashbord.png);
}

.sidemenu li.sidemenu-team a:before {
 width: 6.93333vw;
 height: 5.33333vw;
 background-image: url(~assets/img/mypage/team.png);
}

.sidemenu li.sidemenu-skill a:before {
 width: 5.33333vw;
 height: 6.93333vw;
 background-image: url(~assets/img/mypage/skill.png);
}

.sidemenu li.sidemenu-profile a:before {
 width: 4.8vw;
 height: 5.86667vw;
 background-image: url(~assets/img/mypage/profile.png);
}

.sidemenu li.is-active a:after {
 content: '';
 position: absolute;
 width: 0;
 height: 0;
 border-style: solid;
}

@media screen and (max-width: 800px) {
 .sidemenu {
  display: flex;
  align-items: center;
  justify-content: space-between;
 }
 .sidemenu li {
  flex: 1 1 auto;
 }
 .sidemenu li a {
  justify-content: center;
  padding-top: 11.2vw;
  height: 16vw;
  border-right: 1px solid #2e476e;
 }
 .sidemenu li:last-child {
  border-right: none;
 }
 .sidemenu li a:before {
  bottom: 6vw;
  left: 50%;
  transform: translateX(-50%);
 }
 .sidemenu li.is-active a:after {
  top: 0;
  left: 50%;
  border-width: 2.66667vw 2.66667vw 0 2.66667vw;
  border-color: #f8f8f8 transparent transparent transparent;
  transform: translateX(-50%);
 }
}

@media screen and (min-width: 801px) {
 .sidemenu li a {
  padding-left: 4.375vw;
  height: 6.25vw;
  font-size: 1vw;
  border-bottom: 1px solid #2e476e;
 }
 .sidemenu li a:before {
  top: 50%;
  left: 1.75vw;
  transform: translateY(-50%);
 }
 .sidemenu li.sidemenu-dashbord a:before {
  width: 1.3125vw;
  height: 1.3125vw;
 }
 .sidemenu li.sidemenu-team a:before {
  width: 1.625vw;
  height: 1.25vw;
 }
 .sidemenu li.sidemenu-skill a:before {
  width: 1.25vw;
  height: 1.625vw;
 }
 .sidemenu li.sidemenu-profile a:before {
  width: 1.125vw;
  height: 1.375vw;
 }
 .sidemenu li.is-active a:after {
  top: 50%;
  right: 0;
  border-width: 0.625vw 0.625vw 0.625vw 0;
  border-color: transparent #f8f8f8 transparent transparent;
  transform: translateY(-50%);
 }
}

@media screen and (min-width: 1601px) {
 .sidemenu li a {
  padding-left: 70px;
  height: 100px;
  font-size: 16px;
  font-size: 1.6rem;
 }
 .sidemenu li a:before {
  top: 50%;
  left: 28px;
 }
 .sidemenu li.sidemenu-dashbord a:before {
  width: 21px;
  height: 21px;
 }
 .sidemenu li.sidemenu-team a:before {
  width: 26px;
  height: 20px;
 }
 .sidemenu li.sidemenu-skill a:before {
  width: 20px;
  height: 26px;
 }
 .sidemenu li.sidemenu-profile a:before {
  width: 18px;
  height: 22px;
 }
 .sidemenu li.is-active a:after {
  border-width: 10px 10px 10px 0;
 }
}

</style>