<template>
  <div calss='box'>
    <!-- 首页上半部分 -->
    <el-row type='flex' class='row-bg' justify='space-between'>
      <div class='block marr10'>
        <el-carousel height='450px' arrow='always' :interval='3000'>
          <el-carousel-item v-for='(item, index) in imgList' :key='index'>
            <div @click='gonew(item.id)' class='cursor' style='width:590px; height:450px'>
              <!-- todo 10086 -->
              <img :src="'http://180.76.56.118:10086/' + item.picturePath" alt='' style='width:100%; height:90%' />
            </div>
          </el-carousel-item>
        </el-carousel>
      </div>
      <notice class='notice' />
    </el-row>
    <!-- 首页下半部分 -->
    <el-row type='flex' class='row-bg' justify='space-between'>
      <work class='work' />
      <school class='school' />
      <other class='other' />
    </el-row>

    <!-- 定位fixed -->
    <div class='fixed1'>
      <a @click="$router.push('Info')"><img src='../../assets/6.jpg' alt='' /></a>
    </div>
    <div class='fixed2'>
      <a @click="$router.push('/MapView')"><img src='../../assets/5.jpg' alt='' /></a>
    </div>
  </div>
</template>
<script>
import notice from '../../views/notice.vue'
import work from '../../views/work.vue'
import school from '../../views/school.vue'
import other from '../../views/other.vue'

import { getNewsList } from '../../api/api'

export default {
  components: { notice, work, school, other },
  name: 'index',
  data() {
    return {
      imgList: []
    }
  },
  created() {
    this.getnews()
  },
  methods: {
    getnews() {
      const data = {
        current: 1,
        newsCategoryId: 16,
        size: 3
      }
      getNewsList(data)
        .then(res => {
          console.log(res)
          if (res.code == 200) {
            this.imgList = res.data.records
          }
        })
        .catch(err => {
          console.log(err)
        })
    },
    gonew(id) {
      this.$router.push({ path: '/home/news', query: { id: id } })
    }
  }
}
</script>
<style lang='less' scoped>
.block {
  width: 50%;
}

.block div {
  img {
    width: 100%;
    height: 100%;
  }
}

.notice {
  width: 50%;
}

.work {
  width: 40%;
  margin-right: 10px;
}

.school {
  width: 40%;
}

.other {
  width: 20%;
  margin-left: 5px;
}

.fixed1 {
  position: fixed;
  top: 270px;
  right: 2px;
}

.fixed2 {
  position: fixed;
  top: 340px;
  right: 2px;
}
</style>
