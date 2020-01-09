<template>
  <div class="plotInfo">
  <div class="common-header">
    <span id="btnList" class="title-img">
        <span v-for="(item, i) in content" class="btnIcon">
            <img :src="i === index ? '../static/images/ring2.gif' : '../static/images/ring.png'" @click="toPage(i)" alt="">
        </span>
    </span>
  </div>
 <div class="contentTable">
     <div class="contentTable2" id="offsetBox" :style="{'marginLeft':  '-' + offset}">
        <table class="content" v-for="table in content2">
            <tr class="title">
                <th class="t1">[ 序号 ]</th>
                <th class="t2">[ 小区名称 ]</th>
                <th class="t3">[ 户数 ]</th>
                <th class="t4">[ 监控点位 ]</th>
                <th class="t5">[ 本日出入人数 ]</th>
            </tr>
            <tr v-for="(item, i) in table">
                <td class="line1">{{item.num}}</td>
                <td class="line2">{{item.name}}</td>
                <td class="line3">{{item.pNum}}</td>
                <td class="line4">{{item.points}}</td>
                <td class="line5">{{item.out}}</td>
            </tr>
        </table>
     </div>
 </div>
 </div>
</template>
<script>
export default {
    name: 'PlotInfo',
    props: {
    	width: {
    		type:String,
    		default:'484'
        },
        height: {
    		type:String,
    		default:'484'
        },
        speed: {
    		type: Number,
    		default: 500
        },
        content: {
            type: Array,
            default: [[{
                num: 'NUM.1',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.2',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.3',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.4',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.5',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.6',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.7',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.8',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.9',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.10',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            }],[{
                num: 'NUM.11',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.12',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.13',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.14',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.15',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.16',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.17',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.18',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.19',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.20',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            }],[{
                num: 'NUM.21',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.22',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.23',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.24',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.25',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.26',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.27',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.28',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.29',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            },{
                num: 'NUM.30',
                name: '蜀风花园兰苑',
                pNum: 789,
                points: 18,
                out: '6,000'
            }]]
        },
    },
    data() {
        return {
            margin: [],
            offset: undefined,
            length: null,
            index: null,
            content2: [],
            timer: undefined,
        };
    },
    created() {
        let _this = this;
        _this.initPage();
    },
    methods: {
        initPage() {
            let _this = this;
            window.onload = function () {
                var offsetBox = document.getElementById('offsetBox')
                for (let i in _this.content) {
                    _this.content2.push(_this.content[i]);
                }
                _this.content2.push(_this.content[0]);
                _this.length = _this.content.length;
                for (let i = 0; i < _this.length + 1; i++) {
                    _this.margin.push(i*100+'%')
                }
                _this.index = -1;
                function ring() {
                    _this.length = _this.content.length;
                    if (_this.index === _this.length - 1) { //转到最后一列
                        _this.index = 0;
                        _this.offset = _this.margin[_this.length];
                        setTimeout(() => {
                            offsetBox.style.transition = "all 0ms ease 0s";
                            _this.index = 0;
                            _this.offset = _this.margin[_this.index];
                        }, 300)
                    } else {
                        offsetBox.style.transition = "all 300ms ease 0s";
                        _this.index ++
                        _this.offset = _this.margin[_this.index];
                    }
                    return ring;
                }
                _this.timer =  setInterval (ring(), _this.speed)
            }
        },
        toPage(index) {
            let _this = this;
            if (_this.index !== index) {
                clearInterval(_this.timer);
                _this.index = index - 1;
                _this.offset = _this.margin[_this.index];
                var offsetBox = document.getElementById('offsetBox');
                function ring() {
                    _this.length = _this.content.length;
                    if (_this.index === _this.length - 1) { //转到最后一列
                        _this.index = 0;
                        _this.offset = _this.margin[_this.length];
                        setTimeout(() => {
                            offsetBox.style.transition = "all 0ms ease 0s";
                            _this.index = 0;
                            _this.offset = _this.margin[_this.index];
                        }, 300)
                    } else {
                        offsetBox.style.transition = "all 300ms ease 0s";
                        _this.index ++
                        _this.offset = _this.margin[_this.index];
                    }
                    return ring;
                }
                _this.timer =  setInterval (ring(), _this.speed)
            }
        },
        handleAnimation(anim){
            this.anim = anim
        }
    }
};
</script>