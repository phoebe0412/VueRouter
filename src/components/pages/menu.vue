<template>
 <div>
  <ul class="nav">
  <li class="nav-item">
    <router-link class="nav-link" to="/page/">卡片 1</router-link>
  </li>
  <li class="nav-item">
    <router-link class="nav-link" to="/page/child2">卡片 2</router-link>
  </li>
  <li class="nav-item">
    <router-link class="nav-link" to="/page/child3">卡片 3</router-link>
  </li>
  <li class="nav-item">
    <a href="#" class="nav-link" @click.prevent="updataPath">切換頁面</a>
  </li>
</ul>
</div>
</template>

<script>
export default {
  
  data () {
    return {
     
    }
  },
  methods : {
    updataPath(){
      this.$router.push('/page/child2')
    }
  }
}
</script>


