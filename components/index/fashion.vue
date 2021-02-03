<template>
  <section class="m-istyle">
    <dl @mouseover="over">
      <dt>猜你喜欢</dt>
      <dd
        :class="{active:kind==='all'}"
        kind="all"
        keyword="最合适">为你甄选最适合的</dd>
    </dl>
    <ul class="ibody">
      <li
        v-for="(item, index) in curList"
        :key="index">
        <el-card
          :body-style="{ padding: '0px' }"
          shadow="never">
          <img
            :src="item.img"
            class="image">
          <ul class="cbody">
            <li class="title">{{ item.title }}</li>
            <li class="pos"><span>{{ item.pos }}</span></li>
            <li class="price">￥<em>{{ item.price }}</em><span>/起</span></li>
          </ul>
        </el-card>
      </li>
    </ul>
  </section>
</template>
<script>
export default {
  data: () => {
    return {
      kind: 'all',
      curList:[{
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        },
        {
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        },{
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        },{
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        },{
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        },{
          title: '张三',
          pos: '保岱镇',
          price: 666,
          img: 'https://img.meituan.net/phoenix/14bc46b5740b7714df2dc3fbf27b542d1459696.jpg@1920w_1080h'
        }
        ],
      city: '北京',
      list: {
        all: [],
        part: [],
        spa: [],
        movie: [],
        travel: [],
      }
    }
  },
  computed: {
    cur: function () {
      return this.list[this.kind]
    }
  },
  async mounted(){
    let self=this;
    
  },
  methods: {
    over: async function (e) {
   
    }
  },

}
</script>
<style lang="scss" scoped>
    @import "@/assets/css/index/fashion.scss";
</style>
