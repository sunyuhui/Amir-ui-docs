<docs-header :active="headerActive"></docs-header>

<div class="docs-container">
	<docs-sidebar :active="sidebarActive"></docs-sidebar>
	<div class="docs-content">

#### 使用示例

	<a-button @click="emitClick"></a-button>
	<a-button class="hot"></a-button>
	<a-button>好的</a-button> 
	<a-button class="disabled">好的</a-button> 
	<a-button class="big"></a-button>
	<a-button class="bigger"></a-button> 

	methods: {
		emitClick() {
			console.log('clicked')
		}
	}

#### Demo

<p>normal：<a-button @click="emitClick"></a-button> </p>
<p>normal hot：<a-button class="hot"></a-button> </p>
<p>normal 自定义文案：<a-button>好的</a-button> </p>
<p>normal disabled：<a-button class="disabled">好的</a-button> </p>
<p>big: <a-button class="big"></a-button></p>
<p>bigger: <a-button class="bigger"></a-button></p> 

#### Props

<a-table :tableData="propTableData" :tableHead="propTableHead"></a-table>

备注：button的样式使用class控制，可选class为：`big`、`bigger`、`disabled`、`hot`

#### Events

<a-table :tableData="eventTableData" :tableHead="eventTableHead"></a-table>




<script>
	import Head from '../../common/table.js'
	export default {
		data() {
			return {
				sidebarActive: '/#/docs/button',
				headerActive: 'docs',
				propTableData: [
					{
						name: "class",
						description: "按钮ClassName",
						type: "String",
						necessary: "否",
						double: "否",
						default: "''"
					}
				],
				propTableHead: Head.propHead,
				eventTableData: [
					{
						name: "click",
						description: "按钮点击之后触发的事件",
						param: "无"
					}
				],
				eventTableHead: Head.eventHead
			}
		},
		methods: {
			emitClick() {
				console.log('clicked')
			}
		}
	}
</script>

</div>
</div>