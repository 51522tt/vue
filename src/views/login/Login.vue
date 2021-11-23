<template>
  <div class="login">
    <img class='login__img' src="http://www.dell-lee.com/imgs/vue3/user.png" alt="">
    <div class='login__input'>
        <input class='login__input__content' type="text" placeholder='请输入手机号'>
    </div>
    <div class='login__input'>
        <input class='login__input__content' type="text" placeholder='请输入密码'>
    </div>
    <div class='login-button'>登录</div>
    <div class='login-link'>立即注册</div>
    <!-- <div>忘记密码</div> -->
  </div>
</template>

<script>
export default {
  name: 'login'
}
</script>

<style lang='scss' scoped>
.login{
    position:absolute;
    top:50%;
    left:0;
    right: 0;
    transform: translateY(-50%);
    &__img{
        display: block;
        width: .66rem;
        height: .66rem;
        margin:0 auto .4rem auto;
    }
    &__input{
        margin: 0 auto .16rem ;
        width: 2.95rem;
        height: .48rem;
        border: 0.01rem solid rgba(0,0,0,0.10);
        border-radius: .06rem;
        &__content{
            width: 100%;
            height: 100%;
            border: none;
            outline: none;
            background-color: #F9F9F9;
            font-size: .16rem;
            border-radius: 6px;
            &::placeholder {
                color: #777;
            }
        }
    }
    &-button{
        margin: 0 auto .16rem ;
        width: 2.95rem;
        height: .48rem;
        line-height: .48rem;
        text-align: center;
        background: #0091FF;
        box-shadow: 0 4px 8px 0 rgba(0,145,255,0.32);
        border-radius: 4px;
        color: #FFFFFF;
        font-size:.16rem;
    }
    &-link {
        text-align: center;
        font-size: .14rem;
        color: #777;
    }
}
</style>
