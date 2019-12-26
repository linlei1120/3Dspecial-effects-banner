# 3Dspecial-effects-banner
miniorject 3D
<!--3D轮播图-->
<swiper class="imageContainer" bindchange="handleChange" previous-margin="50rpx" next-margin="50rpx" circular autoplay interval="2000">
  <block wx:for="{{3}}" wx:key="{{index}}">
    <swiper-item class="item">
      <image class="itemImg {{currentIndex == index ? 'active': ''}}" src="../../../image/3.jpg"></image>
    </swiper-item>
  </block>
  
  
  page{
  background: #f7f7f7f7;
}
.imageContainer{
  width: 100%;
  height: 500rpx;
  background: rgb(248, 247, 247);
}
.item{
  height: 500rpx;
}
.itemImg{
  position: absolute;
  width: 100%;
  height: 340rpx;
  border-radius: 15rpx;
  z-index: 5;
  opacity: 0.7;
  top: 13%;
}
.active{
  opacity: 1;
  z-index: 10;
  height: 430rpx;
  top: 7%;
  transition:all .2s ease-in 0s;
}

/*  */
</swiper
const app = getApp()

Page({

  data: {
    currentIndex: 0
  },

  onLoad: function (options) {

  },
  /* 这里实现控制中间凸显图片的样式 */
  handleChange: function (e) {
    this.setData({
      currentIndex: e.detail.current
    })
  },
})
