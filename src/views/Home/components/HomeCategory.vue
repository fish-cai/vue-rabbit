<script setup>
import { useCategoryStore } from "@/stores/category";
const categoryStore = useCategoryStore();
</script>
<template>
  <div class="home-category">
    <ul class="menu">
      <li v-for="item in categoryStore.categoryList" :key="item">
        <router-link to="/">{{ item.name }}</router-link>
        <router-link v-for="i in item.children.slice(0, 2)" :key="i" to="/">{{
          i.name
        }}</router-link>
        <div class="layer">
          <h4>分类推荐<small>根据您的购买或浏览记录推荐</small></h4>
          <ul>
            <li v-for="i in item.goods" :key="i">
              <router-link to="/">
                <img :src="i.picture" alt="" />
                <div class="info">
                  <p class="name ellipisis-2">
                    {{ i.name }}
                  </p>
                  <p class="desc ellipisis">{{ i.desc }}</p>
                  <p class="price"><i>¥</i>{{ i.price }}</p>
                </div>
              </router-link>
            </li>
          </ul>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped lang="scss">
.home-category {
  width: 250px;
  height: 500px;
  background: rgba(0, 0, 0, 0.8);
  position: relative;
  z-index: 99;
}
.menu {
  li {
    padding-left: 40px;
    height: 55px;
    line-height: 55px;

    &:hover {
      background: $xtxColor;
    }

    a {
      margin-right: 4px;
      color: #fff;
    
      &:first-child{
        font-size: 16px;
      }
    }
     .layer{
      width: 990px;
      height: 500px;
      background: rgba(255,255,255,0.8);
      position: absolute;
      left: 250px;
      top :0;
      display: none;
      padding: 0 15px ;
     }
    h4{
      font-size: 20px;
      font-weight: normal;
      line-height: 80px;

      small{
        font-size: 16px;
        color: #666;
      }
    }
  }
}
</style>
