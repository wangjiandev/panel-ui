<template>
	<view class="content">
		<view class="map"></view>
		<epx-panel>
			<view class="news">
				<image src="http://p1.img.cctvpic.com/photoworkspace/contentimg/2020/07/17/2020071707561351548.jpg" mode="aspectFill"></image>
				<p>去年6月，储先生被一名陌生女孩添加了微信好友，经交流后发现，对方竟是某网络直播平台的美女主播。储先生按照这名女孩的指引，登录进入了女孩所在的网络平台直播间，并慢慢成了女孩的忠实粉丝。随后，这位“美女主播”竟在线下通过微信向自己主动示好，两人很快通过微信谈起了恋爱。接下来，已经成为自己“网恋女友”的美女主播却频频遭遇不幸，业绩不好被领导批评、妹妹学费不够、母亲癌症需要手术……痴情的储先生大动怜香惜玉之心，每次都有求必应，多次在“女友”直播时慷慨打赏，共计花费9.7万余元。</p>
				<p>然而，当“女友”又以类似理由向储先生要求援助时，储先生已囊中羞涩。这时的“女友”却没有了与他继续聊天的耐心，直接将其微信拉黑。最终，怀疑被骗的储先生选择向警方报案。</p>
				<p>接到报案后，警方立即组织对该直播平台注册信息、受害人充值资金流向等进行深入研判，成功锁定并于今年1月赴外地抓获该网络女主播褚某（女，22岁），同时顺线发现，该案借助网络直播平台的合法外衣实施团伙作案，存在上、下游多个犯罪窝点，涉及受害人众多。</p>
				<image src="http://p3.img.cctvpic.com/photoworkspace/contentimg/2020/07/17/2020071707592249307.png" mode="aspectFill"></image>
				<p>
					对此，青岛市公安局迅速成立由刑警支队牵头的专案组，在山东省反电信网络诈骗中心的指导和青铁公安处、当地公安机关的配合下，深入侦查研判，精心扩线布网，于近日组织警力辗转千里赶赴该诈骗团伙所在地，为实施全面收网做好了充分准备。
				</p>
				<p>
					7月14日下午4点整，随着现场指挥部一声令下，布控在8个诈骗窝点的近500名警力同时收网，将总计151名窝点成员（其中30名已移交当地警方处理）悉数抓获，并依法扣押涉案电脑、手机、银行卡、账目材料等物品一宗。
				</p>
			</view>
		</epx-panel>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	page {
		height: 100%;
		display: flex;
	}

	.content {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100vw;
		overflow: hidden;
		background-color: #E8ECF3;
		position: relative;
	}
	.news{
		width: 100%;
		image{
			width: 100%;
			height: 300rpx;
		}
		p {
			margin: 20rpx 0;
			font-size: 28rpx;
		}
	}
</style>
