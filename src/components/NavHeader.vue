<template>
  <div class="header">
      <div class="topbar">
          <div class="container">
              <div class="topbar-menu">
              <a href="javascript:;">小米商城</a>
              <a href="javascript:;">MUI</a>
              <a href="javascript:;">云服务</a>
              <a href="javascript:;">协议规则</a>
              </div> 
              <div class="topbar-user">
              <a href="javascript:;">登录</a>
              <a href="javascript:;">注册</a>
              <a href="javascript:;" class="my-cart"><span class="icon-cart"></span>购物车</a>  
              </div>
          </div> 
      </div>
      <div class="nav-header">
          <div class="container">
              <div class="header-logo">
                  <a href="#index"></a>
              </div>
              <div class="header-menu">
                  <div class="item-menu">
                      <span>小米手机</span>
                      <div class="children">
                          <ul>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                              <li class="product">
                                  <a href=""  target="_blank">
                                      <div class="pro-img">
                                          <img src="https://imgservice3.suning.cn/uimg1/b2c/image/P2AXKJ-nvRjI7gQaXPNOLg.jpg_220w_220h_4e"  alt="">
                                      </div>
                                      <div class="pro-name">小米779</div>
                                      <div class="pro-price">1799元</div>
                                  </a>
                              </li>
                             
                          </ul>
                      </div>
                  </div> 
                  <div class="item-menu">
                      <span>红米</span>
                      <div class="children"></div>
                  </div>
                   <div class="item-menu">
                      <span>电视</span>
                      <div class="children"></div>
                  </div>
              </div>
              <div class="header-search">
                  <div class="wrapper">
                      <input type="text" name='keyword'>
                      <a href="javascript::"></a>
                  </div>
              </div>
          </div>
      </div>
      
  </div>
      
      
</template>
<script>
export default {
     name:'nav-header'
}
</script>
<style lang="scss">
@import './../assets/scss/base.scss';
.header{
    .topbar{
        height: 39px;
        line-height: 39px;
        background-color: #333333;
        .container{
            width: 1226px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            a{font-size: 12px;
             font-weight: bold;
             color: #B0B0B0;
             margin-right: 17px;
             }
             .my-cart{
                 display: inline-block;
                 width:110px;
                 height:39px;
                 line-height: 39px;
                 background-color: #FF6600;
                 text-align: center;
                 margin-right: 0px;
                 .icon-cart{
                     display: inline-block;
                     width:16px;
                     height: 12px;
                     background: url('/imgs/icon-cart.png') no-repeat center;
                     background-size: contain;
                     margin-right: 4px;

                 }
             }
        }
    }
    .nav-header{
        .container{ 
            position: relative;
            width: 1226px;
            height: 112px;
            display: flex;
            justify-content:space-between;
            align-items: center;
           .header-logo{
            display: inline-block;
            width:55px;
            height: 55px;
            background-color: #FF6600;
            a{
                display: inline-block;
                width:110px;
                height: 55px;
                transition: margin .2s;
              &:before{
                  content: ' ';
                  display: inline-block;
                  width: 55px;
                  height:55px;
                  background: url('/imgs/mi-logo.png') no-repeat center;
                  background-size: 55px;
              }
              &:after{
                  content: ' ';
                  display: inline-block;
                  width: 55px;
                  height:55px;
                  background: url('/imgs/mi-home.png') no-repeat center;
                  background-size: 55px;
              }
              &:hover{
                  margin-left: -55px;
                  transition: margin .2s;
              }

            }
           }
           .header-menu{
               display: inline-block;
               width:643px;
               
               .item-menu{
                   display: inline-block;
                   margin-left: 20px;
                   font-weight: bold;
                   font-size: 16px;
                   span{cursor: pointer;}
                   &:hover{
                       color: #FF6600;
                       .children{
                           height: 220px;

                       }
                   }
                   .children{
                       position:absolute;
                       top:112px;
                       left: 0;
                       width:1226px;
                       border-top:1px solid #e5e5e5;
                      
                       .product{
                           position: relative;
                           float: left;
                           width:16.6%;
                           height: 220px;
                           font-size: 12px;
                           line-height: 12px;
                           text-align: center;
                          
                          
                           a{
                               display: inline-block;
                           }
                           img{
                               height:111px;
                               width:auto;
                               margin-top:26px;
                           }
                           .pro-img{
                               height:137px;
                           }
                           .pro-name{
                               font-weight:bold;
                               margin-top: 19px;
                               margin-bottom:8px;
                               color:#333333;
                           }
                           .pro-price{
                               color:#ff6600;
                           }
                            &:before{
                               position: absolute;
                               content: ' ';
                               top:28px;
                               right:0px;
                               border-left:1px solid #d7d7d7;
                               height:100px;
                               width:1px;
                           }
                           &:last-child:before{display: none;}

                       }

                   }

               }
        
           }
           .header-search{
               .wrapper{
                   height: 50px;
                   width: 317px;
                   border: 1px solid #e0e0e0;
                   display: flex;
                   align-items: center;
                   input{
                       border:none;
                       height: 50px;
                       line-height: 50px; 
                       box-sizing: border-box;
                       width:263px;
                       border-right: 1px solid #e0e0e0;
                   }
                   a{
                       display: inline-block;
                       width: 18px;
                       height: 18px;
                       background: url('/imgs/icon-search.png') no-repeat center;
                       background-size: contain;
                       margin-left: 18px;
                   }


               }


           }
           
           
        }
       
    }
 


}
</style>

