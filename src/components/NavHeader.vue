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
              <a href="javascript:;"  v-if="username"> {{username}}</a>
              <a href="javascript:;"  v-if="!username" @click="login">登录</a>
              <a href="javascript:;"  v-if="username">我的订单</a>
              <a href="javascript:;"  class="my-cart" @click="goToCart"><span class="icon-cart"></span>购物车</a>
             </div>
          </div>
         
      </div>
      <div class="nav-header">
          <div class="container">
              <div class="header-logo">
                  <a href="/#/index"></a>
              </div>
              <div class="header-menu">
                  <div class="item-menu">
                      <span>小米手机</span>
                      <div class="children">
                              <ul> 
                                  <li class="product" v-for="(item,index) in phonelist" :key="index">
                                      <a v-bind:href="'/#/product' + item.id"  target="_blank">
                                      <div class="pro-img"> 
                                          <img v-bind:src="item.mainImage" :alt="item.subtitle"></div>
                                      <div class="pro-name">{{item.name}}</div>
                                      <div class="pro-price">{{item.price | currency}}</div>
                                      </a>
                                  </li>
                                  
                              </ul> 
                      </div>
                  </div>
                  <div class="item-menu">
                      <span>红米</span>
                     
                  </div>
                  <div class="item-menu">
                      <span>电视</span>
                      <div class="children">
                            <ul> 
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-1.jpg"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li>
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-2.jpg"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li>
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-3.png"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li>
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-4.jpg"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li> 
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-5.jpg"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li>
                                  <li class="product">
                                      <a href=" " target="_blank">
                                      <div class="pro-img"> <img src="/imgs/nav-img/nav-3-6.png"></div>
                                      <div class="pro-name">CC9</div>
                                      <div class="pro-price">1799元</div>
                                      </a>
                                  </li>
                            </ul> 
                      </div>
                  </div>
              </div>
              <div class="header-search">
                  <div class="wrapper">
                      <input type="text" name="keyword">
                      <a href="javascript:;" ></a>
                  </div> 
              </div>
          </div>
      </div>
      
      
  </div>
      
      
</template>
<script>
export default {
     name:'nav-header',
     data(){
         return{
             username:'',
             phonelist:[]
         }
     },
     filters:{
         currency(val){
             if(!val)return 0.00;
             return '￥'+val.toFixed(2)+'元';
           

         }

     },
     mounted(){
          this.getProductlist();
     },
     methods:{
          login(){
             this.$router.push('/login');
         },
         getProductlist(){
             this.axios.get('/products',{
                 params:{
                     categoryId:'100012',
                     pageSize:6
                 }
             }).then((res)=>{
                 this.phonelist=res.list
             })

         },
         
         goToCart(){
             this.$router.push('/cart');
         }
     }
    
   
}
</script>
<style lang="scss">
@import './../assets/scss/base.scss';
.header{
    .topbar{
        width:contain;
        height: 39px;
        background-color: #333333;
        .container{
            font-size: 12px;
            height: 39px;
            display: flex;
            justify-content: space-between;
            align-items: center;
           a{
              
             color:#b0b0b0;
             margin-right: 17px;
            
           }
            .my-cart{
               display: inline-block;
               height: 39px;
               line-height: 39px;
               width:110px;
               text-align: center;
               background-color: #ff6600;
               .icon-cart{
                   display: inline-block;
                   width:14px;
                   height:12px;
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
            width:1226px;
            height: 112px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            .header-logo{
                display: inline-block;
                width:55px;
                height:55px;
                background-color: #ff6600;
               a{
                     display: inline-block;
                     width:110px;
                     height: 55px;
                     transition: margin .2s;
                     &:before{
                       content: ' ';
                       display: inline-block;
                       width:55px;
                       height:55px;
                       background: url('/imgs/mi-logo.png') no-repeat center;
                       background-size: 55px;
                      }
                     &:after{
                       content: ' ';
                       display: inline-block;
                       width:55px;
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
                 font-size: 16px;
                 font-weight: bold;
                .item-menu{
                    display: inline-block;
                    margin-left: 20px;
                    span{cursor: pointer;}
                    &:hover{
                         color: #ff6600;
                         .children{
                             opacity: 1;
                             height: 220px;}


                    }
                    .children{
                         position: absolute;
                         top:112px;
                         left: 0; 
                         width: 1226px;
                         height:220px;
                         border-top:1px solid #b0b0b0;
                         overflow: hidden;
                         opacity: 0;
                         transition: all .5s;
                        .product{
                            position: relative;
                            float: left;
                            width:16.6%;
                            height:220px;
                            text-align: center;
                            a{display: inline-block;}
                           .pro-img{
                               img{
                                   margin-top: 15px;
                                   width:auto;
                                   height:112px;
                               }
                           }
                           .pro-name{
                               margin-top:10px;
                               margin-bottom: 8px;
                               color:#333333;
                               font-weight: bold;
                           }
                           .pro-price{
                               color:#ff6600;
                               font-weight: bold;
                           }
                           &:before{
                               content: ' ';
                               position: absolute;
                               top:28px;
                               right:0;
                               width: 1px;
                               height: 90px;
                               border-right: 1px solid #d7d7d7;
                           }
                           &:last-child:before{display: none;}
                            
                        }

                      
                       
                   

                    }
                   
                    
                }

            }
            .header-search{
                 width:319px;
                 .wrapper{ 
                     height: 50px;
                     display: flex;
                     align-items: center;
                     border: 1px solid #d7d7d7;
                     input{
                     border:none;
                     box-sizing: border-box;
                     padding-left: 14px;
                     width: 264px;
                     border-right: 1px solid #d7d7d7;
                     height: 50px;
                     }
                     a{
                     display: inline-block;
                     width:18px;
                     height:18px;
                     background: url('/imgs/icon-search.png') no-repeat center;
                     background-size: contain;
                     margin-left:16px;
                     }
                 }

            }
        }
    }
}


</style>

