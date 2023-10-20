<script setup>
import MyBtn from '@/components/form-components/MyButton.vue'

</script>

<template>
  <form class="form">
    <div class="title">
      <slot name="title"> </slot>
    </div>
    <div class="input">
      <slot name="input"> </slot>
    </div>
    <div class="foo">
      <slot name="btn">
        
      </slot>
      <slot name="foo"> </slot>
    </div>
  </form>
</template>

<style scoped>
div {
  width: 100%;
}
.form {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 30px 16px;
  background: #fff;
  height: 430px;
  width: 358px;
  border-radius: 18px;
}
.title {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: start;
}

.input{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  flex: 0 1 33.333333%;
}

.foo{
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  flex: 0 1 33.333333%;
}

</style>
