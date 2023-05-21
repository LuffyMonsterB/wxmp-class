<template>
  <scroll-view>
    <Main v-if="page==='main'"/>
		<Search v-if="page==='search'"/>
		<My v-if="page==='my'"/>
    <!-- tabbar -->
    <view class='cu-tabbar-height'></view>
    <view class="footer">
      <Tabbar :pageList="pageList" :activePage="page"  @changePageTo="handleChangePageTo"/>
    </view>
  </scroll-view>
</template>

<script>
import Tabbar from "components/Tabbar/Tabbar";
import Main from "components/Main/Main";
import Search from "components/Search/Search";
import My from "components/My/My";
export default {
  components: { Tabbar,Main,Search,My },
	data(){
		return{
			page:'main',
      pageList:[
        {page:'main',text:'首页',icon:'cuIcon-homefill',isCenter:false},
        {page:'search',text:'搜索',icon:'cuIcon-discover',isCenter:true},
        {page:'my',text:'我的',icon:'cuIcon-myfill',isCenter:false},
      ]
		}
	},
	methods:{
		handleChangePageTo(page){
			this.page=page
		}
	}
};
</script>

<style scoped>
.Page{
  width: 100%;
}
.footer{
  position: fixed;
}
</style>
