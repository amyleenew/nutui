<template>
    <div>
      <nut-docheader 
        :name="$route.name" 
        :chName="$route.params.chnName" 
        type="Component" 
        desc="步骤条。" 
        :showQrCode="true"></nut-docheader>
        <h5>示例</h5>
        <h6>默认用法</h6>
        <nut-codebox :code="demo1" :imgUrl="['../asset/img/demo/step1.png']"></nut-codebox>
        <h6>可配置活动数值，显示进度数字以及title具体每个进度条的高度</h6>
        <nut-codebox :code="demo2" :imgUrl="['../asset/img/demo/step2.png']"></nut-codebox>
        <h6>可以设置进度条为图片</h6>
        <nut-codebox :code="demo3" :imgUrl="['../asset/img/demo/step3.png']"></nut-codebox>
        <h5>Props</h5>
        <div class="tbl-wrapper">
        <table class="u-full-width">
          <thead>
            <tr>
              <th>参数</th>
              <th>说明</th>
              <th>类型</th>
              <th>默认值</th>
              <th>可选值</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>stepsId</td>
              <td>当同一页面有多个进度条时，需设置每个进度条组件单独的stepsId，如只有一个进度条组件，则无需设置该属性</td>
              <td>String</td>
              <td>''</td>
              <td>--</td>
            </tr>
            <tr>
              <td>stepTitle</td>
              <td>每个进度条的标题</td>
              <td>string</td>
              <td>--</td>
              <td>--</td>
            </tr>
            <tr>
              <td>active</td>
              <td>每个进度条组件激活的个数</td>
              <td>Number</td>
              <td>0</td>
              <td>--</td>
            </tr>
            <tr>
              <td>showNum</td>
              <td>是否显示进度条左侧的数字</td>
              <td>boolean</td>
              <td>false</td>
              <td>true/false</td>
            </tr>
            <tr>
              <td>titleTop</td>
              <td>进度条标题距离顶部的距离，单位为rem</td>
              <td>Number</td>
              <td>0.3</td>
              <td>--</td>
            </tr>
            <tr>
              <td>icon</td>
              <td>左侧进度条的图片地址</td>
              <td>String</td>
              <td>--</td>
              <td>--</td>
            </tr>
          </tbody>
        </table>
        </div>
    </div>
</template>

<script>
import Vue from 'vue';
export default {
    data(){
        return{
          demo1:
`<nut-steps stepsId="step1">
  <nut-step stepTitle="您的订单已经发往北京"><p>2017-12-12</p></nut-step>
  <nut-step stepTitle="您的订单已经到达上海"><p>2017-12-11</p></nut-step>
  <nut-step stepTitle="快递公司已揽件"><p>2017-12-10</p></nut-step>
</nut-steps>`,
          demo2:
`<nut-steps stepsId="step2" :active="2" :showNum='true' :titleTop="0.4">
  <nut-step stepTitle="您的订单已经发往北京"><p>2017-12-12</p></nut-step>
  <nut-step stepTitle="您的订单已经到达上海"><p>2017-12-11</p></nut-step>
  <nut-step stepTitle="快递公司已揽件"><p>2017-12-10</p></nut-step>
</nut-steps>`,
demo3:
`<nut-steps stepsId="step3" :active="1">
  <nut-step stepTitle="您的订单已经发往北京" icon="图片地址1"><p>2017-12-12</p></nut-step>
  <nut-step stepTitle="您的订单已经到达上海" icon="图片地址2"><p>2017-12-11</p></nut-step>
  <nut-step stepTitle="快递公司已揽件" icon="图片地址2"><p>2017-12-10</p></nut-step>
</nut-steps>`
        }
    },
    methods:{
    }
}
</script>

<style lang="scss" scoped>

</style>


