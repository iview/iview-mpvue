<template>
  <div>
    <i-panel title="基础用法">
    <i-input :value="value1" title="收货人" autofocus="true" placeholder="名字" />
    <i-input :value="value2" type="number" title="联系电话" placeholder="请输入手机号" />
    <i-input :value="value3" type="textarea" title="详细地址" placeholder="请输入详细地址(最多50字)" maxlength="50" />
    <i-input :value="value4" title="用户信息" disabled="true" />
  </i-panel>

  <i-panel title="无标题输入框">
    <i-input :value="value5" placeholder="请输入收货人姓名" />
  </i-panel>

  <i-panel title="圆角输入框">
    <i-input :value="value6" type="number" right="true" title="消费总额" mode="wrapped" placeholder="询问收银员后输入" />
    <i-input :value="value7" type="number" right="true" error="true" title="不参与优惠金额" mode="wrapped" placeholder="询问收银员后输入" />
  </i-panel>
  </div>
</template>
<script>
import panel from '../../components/panel/panel'
import input from '../../components/input/input'
export default {
  components: {
    'i-panel': panel,
    'i-input': input
  },
  data() {
    return {
      value1: '',
      value2: '',
      value3: '',
      value4: '输入框已禁用',
      value5: '',
      value6: '',
      value7: ''
    }
  }
}
</script>
