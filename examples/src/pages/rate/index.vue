<template>
  <div>
    <i-cell-group>
      <i-cell title="基本用法">
        <i-rate 
          @change="onChange1" 
          :value="starIndex1">
        </i-rate>
      </i-cell>
      <i-cell title="自定义星星个数">
        <i-rate
          @change="onChange5"
          :count="10"
          :value="starIndex5">
        </i-rate>
      </i-cell>
      <i-cell title="自定义星星大小">
        <i-rate 
          @change="onChange2" 
          :value="starIndex2" 
          size="32">
        </i-rate>
      </i-cell>
      <i-cell title="自定义文字说明">
        <i-rate 
          @change="onChange2" 
          :value="starIndex2"
          show-text="星">
        </i-rate>
      </i-cell>
      <i-cell title="手势touch选择星">
        <i-rate 
          @change="onChange3" 
          :value="starIndex3"
          show-text="星">
        </i-rate>
      </i-cell>
      <i-cell title="禁用点击和手势选择星">
        <i-rate 
          :disabled="true"
          :value="starIndex4"
          show-text="星">
        </i-rate>
      </i-cell>
    </i-cell-group>
  </div>
</template>
<script>
import cellGroup from '../../components/cell-group/cell-group'
import cell from '../../components/cell/cell'
import rate from '../../components/rate/rate'
export default {
  components: {
    'i-cell-group': cellGroup,
    'i-cell': cell,
    'i-rate': rate
  },
  data() {
    return {
      starIndex1 : 0,
      starIndex2 : 0,
      starIndex3 : 0,
      starIndex4 : 4,
      starIndex5 : 5
    }
  },
  methods: {
    onChange1(e) {
      this.starIndex1 = e.index
    },
    onChange2(e) {
      this.starIndex2 = e.index
    },
    onChange3(e) {
      this.starIndex3 = e.index
    },
    onChange5(e) {
      this.starIndex5 = e.index
    }
  }
}
</script>
