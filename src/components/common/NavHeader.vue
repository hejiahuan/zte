<template>
  <div class="nav_header">
    <div class="nav_header_top">
      <div class="container">
        <div class="nav_header_top_left">
          <a href="javascript:;">
            <img src="~/assets/img/zte_logo.png" alt />
          </a>
        </div>
        <div class="nav_header_top_right">
          <div class="nav_header_top_righ_left">
            <input type="text" />
            <a class="search_icon" href="javascript:;">
              <i class="iconfont">&#xe782;</i>
            </a>
          </div>
          <div class="nav_header_top_righ_right">
            <span class="maopao">99</span>
            <a href="javascript:;" class="iconfont">
              &#xe658;
              <span>购物车</span>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="nav_header_menu">
      <div class="container">
        <div class="nav_header_menu_left">
          <div class="nav_header_menu_left_menu">
            <div class="nav_header_menu_left_menu_title">
              <a href="javascript:;">全部商品分类</a>
            </div>
            <div class="nav_header_menu_left_menu_body">
              <ul>
                <li>
                  <span>智能手机</span>
                  <div class="children">3434</div>
                </li>
                <li>
                  <span>智能终端</span>
                  <div class="children">wwww</div>
                </li>
                <li>
                  <span>影音娱乐</span>
                  <div class="children">11111</div>
                </li>
                <li>
                  手机充电
                  <div class="children">99999</div>
                </li>
                <li>手机配件</li>
                <li>服务/其他</li>
              </ul>
            </div>
          </div>
          <div class="nav_header_menu_left_title">
            <div class="nav_header_menu_left_title_left">
              <div>
                <a href="javascript:;">首页</a>
              </div>
              <div>
                <a href="javascript:;">天机</a>
               
              </div>
              <div>
                <a href="javascript:;">星星</a>
               
              </div>
            </div>
            <div class="nav_header_menu_left_title_right">
              <a href="javascript:;">ZTE年货盛宴</a>
            </div>
          </div>
        </div>
        <div class="nav_header_menu_right">
          <a href="javascript:;">ZTE春节年会大促销</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavHeader"
};
</script>
<style lang="scss" scoped>
@import "assets/scss/basic.scss";
@import "assets/scss/config.scss";
@import "assets/scss/mixin.scss";

.nav_header {
  height: 140px;
  .nav_header_top {
    height: 100px;
    .container {
      height: 100%;
      @include flex($align: space-around);
      .nav_header_top_left {
        //felx-grow/在felx占比
        flex-grow: 6;
        img {
          width: 65%;
        }
      }
      .nav_header_top_right {
        flex-grow: 2;
        width: 680px;
        height: 50px;
        display: flex;
        @include flex($align: space-between);
        .nav_header_top_righ_left {
          position: relative;
          border: 1px solid $navinputcolor;
          height: 99%;
          width: 550px;
          display: flex;
          align-items: center;
          input {
            border: none;
            border-right: 1px solid $navinputcolor;
            width: 460px;
            height: 100%;
          }
          .search_icon {
            width: 100px;
            height: 50px;
            background-color: $navinputcolor;
            position: relative;
            border: 1px solid $navinputcolor;
            text-align: center;
            i {
              color: #fff;
              font-size: 40px;
            }
          }
        }

        .nav_header_top_righ_right {
          width: 140px;
          height: 100%;
          display: flex;
          justify-content: center;
          align-items: center;
          background: $carButton;
          position: relative;
          .maopao {
            position: absolute;
            width: 16px;
            height: 15px;
            display: flex;
            justify-content: center;
            left: 50px;
            top: 3px;
            background: #fff;
            font-weight: 750;
            border-radius: 50%;
            border: 1px solid #fff;
          }
          a {
            font-size: 35px;
            font-weight: 500;
            color: $navfontColor;
            display: flex;
            justify-content: center;
            align-items: center;
            span {
              margin-left: 15px;
              font-size: 18px;
            }
          }
        }
      }
    }
  }
  .nav_header_menu {
    height: 46px;
    background-color: $navinputcolor;
    position: relative;
    .container {
      height: 100%;
      font-size: $fontF;
      font-weight: 500;
      @include flex($align: space-between);
      .nav_header_menu_left {
        height: 100%;
        width: 620px;
        display: flex;
        .nav_header_menu_left_menu {
          width: 242px;
          height: 556px;
          z-index: 100;
          .nav_header_menu_left_menu_title {
            width: 100%;
            height: 8.2%;
            text-align: center;
            background-image: linear-gradient(
              to right,
              #4facfe 0%,
              #00f2fe 100%
            );
            a {
              line-height: 45px;
              color: #fff;
            }
          }
          .nav_header_menu_left_menu_body {
            width: 100%;
            height: 91.5%;
            background-color: #fff;
            position: relative;
            opacity: 0.7;
            ul {
              li {
                font-size: $fontJ;
                color: $navfontColor;
                cursor: pointer;
                line-height: 82px;
                padding-left: 60px;
                font-weight: 600;
                &::after {
                  position: absolute;
                  content: "";
                  margin-top: 34px;
                  right: 18px;
                  height: 8px;
                  width: 8px;

                  /* //画箭头之前讲过 */
                  border-top: 2px solid #aaa;
                  border-left: 2px solid #aaa;

                  /* 顺时针旋转 旋转45度*/
                  transform: rotate(135deg);
                }
                &:hover {
                  color: $navinputcolor;
                  .children {
                    display: block;
                    // transition: all 0.5s;
                  }
                  &::after {
                    position: absolute;
                    content: "";
                    margin-top: 34px;
                    right: 18px;
                    height: 8px;
                    width: 8px;

                    /* //画箭头之前讲过 */
                    border-top: 2px solid $navinputcolor;
                    border-left: 2px solid $navinputcolor;

                    /* 顺时针旋转 旋转45度*/
                    transform: rotate(135deg);
                  }
                }
                .children {
                  display: none;
                  position: absolute;
                  top: 0;
                  left: 240px;
                  width: 990px;
                  height: 510px;
                  background-color: yellow;
                }
              }
            }
          }
        }
        .nav_header_menu_left_title {
          width: 385px;
          height: 100%;
          @include flex($align: space-between);
          .nav_header_menu_left_title_left {
            width: 250px;
            @include flex($align: space-around);
            a{
              color: #fff;
            }
           
            
          }
          .nav_header_menu_left_title_right {
            a {
              color: #fff;
            }
          }
        }
      }
      .nav_header_menu_right {
        a {
          color: #fff;
        }
      }
    }
  }
}
</style>