<script setup lang="ts">
import { onMounted, ref, reactive } from 'vue'


const count = ref(0)


onMounted(()=> {
  console.log('마운트')
})

const onClick = (btn: string) => {
  if (btn === 'plus'){
    count.value++;
  }  else {
    count.value--;
  }
  

}


</script>

<template>
  <div class="box">
  <h1>{{ count }}</h1>
  <!-- <input v-model="testValue" />  -->
  <button @click="onClick('plus')" class="btn">증가 버튼 +</button>
  <button @click="onClick('minus')" class="btn">감소 버튼 -</button>
</div>
</template>

<style scoped lang="scss">

.box{
  // border: 1px solid yellow;

  .btn{
  width: 150px;
  height: 150px;
  color: darkgray;
  border : 1px solid darkorange;
  
}
}


</style>
