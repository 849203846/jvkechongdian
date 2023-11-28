<script>
export default {
	 globalData: {  
	            latitude: '' ,
				 longitude: ''
	    },
	onLaunch: function(options) {
		const {query = {}} = options
		if(query && getApp()) {
			getApp().globalData.code = query.name || query.qrCode ? query.qrCode.split('code=')[1] : ''
		}
	},
};
</script>

<style>
/* 解决头条小程序组件内引入字体不生效的问题 */
/* #ifdef MP-TOUTIAO */
@font-face {
	font-family: uniicons;
	src: url('/static/uni.ttf');
}
/* #endif */
</style>
