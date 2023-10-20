<script setup>
import { ref, reactive } from 'vue'
import { vMaska } from 'maska'
import VuePincodeInput from 'vue3-pincode-input'
import Eye from '@/components/form-components/Eye.vue'

const props = defineProps({
  value: String,
  // МОЖНО ИСПОЛЬЗОВАТЬ БУЛЕВЫЕ ПРОПСЫ
  phoneFromDB: String
})

const personalAccount = ref('')
const userPassword = ref('')

const maskedValue = ref('')
const bindedObject = reactive({})
</script>

<template>
  <div>
    <!-- <input type="tel" readonly :value="phoneFromDB"> -->
    <fieldset class="wrap user-password">
      <legend>Номер телефона</legend>
      <!-- <input class="my-input" type="text" maxlength="8" placeholder="00000000" v-model="personalAccount"> -->
      <div style="display: flex; flex-wrap: nowrap; justify-content:space-between; align-items:center">
        <input
          class="my-input user-password"
          type="password"
          maxlength="24"
          v-model="userPassword"
          autocomplete="current-password"
        />
        <button><Eye></Eye></button>
      </div>
      <!-- <input
      v-if="props.value === 'inputPhone'"
      class="my-input"
      type="tel"
      v-model.trim="maskedValue"
      placeholder="+7"
      maxlength="19"
      v-maska="bindedObject"
      data-maska="+7 (###) ###-##-##"
    /> -->
    </fieldset>
    <!-- <VuePincodeInput v-model="pincode" /> -->
  </div>
</template>

<style scoped>
div {
  /* margin: 0 0 24px 0 ; */
  width: 100%;
}
.wrap {
  color: #919ba6;
  font-size: 16px;
  font-weight: 400;
  line-height: 13px;
  border-radius: 5px;
  height: 44px;
  width: 100%;
}
.my-input {
  border: none;
  display: block;
  color: #919ba6;
  font-size: 16px;
  font-weight: 400;
  line-height: 13px;
  height: 100%;
}
.my-input:focus {
  background-color: #fff;
  border-color: #bdbdbd;
  outline: 0;
}
</style>
