<template>
  <div>

    
    <group title="is-type传入function">
      <x-input title="必须输入2333" :is-type="be2333" placeholder="I'm placeholder"></x-input>
    </group>

    <group title="mask">
      <x-input title="手机号码格式化" mask="999 9999 9999" v-model="maskValue" :max="13" is-type="china-mobile"></x-input>
      <cell title="value" :value="maskValue"></cell>
      <x-input title="(99) 9-99" mask="(99) 9-99" v-model="maskValue2" :max="9"></x-input>
    </group>

    

  </div>
</template>

<script>
import { Group,} from 'vux'

export default {
  components: {  
    Group   
  },
  