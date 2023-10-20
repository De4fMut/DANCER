<script setup>
import MyForm from './components/form-components/MyForm.vue'
import MyInput from './components/form-components/MyInput.vue'
import MyBtn from '@/components/form-components/MyButton.vue'
</script>

<template>
  <main>
    <MyForm>
      <template v-slot:title>
        <h1>Личный кабинет</h1>
        <h6>Вход с помощью лицевого счёта</h6>
      </template>
      <template v-slot:input>
        <MyInput></MyInput>
        <MyInput></MyInput>
      </template>
      <template v-slot:btn>
        <MyBtn></MyBtn>
      </template>
      <template v-slot:foo>
        <h6>
          <a href="#">Не помните лицевой счет или пароль?</a>
        </h6>
        <h6>
          <a href="#">Вход по телефону</a>
        </h6>
      </template>
    </MyForm>
  </main>
</template>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
}
h1 {
  color: #373653;
  font-size: 20px;
  /* font-family: Montserrat; */
  font-weight: 700;
}
h6 {
  color: #626c77;
  font-size: 14px;
  /* font-family: Onest; */
  font-weight: 400;
}
a{
  text-decoration: underline;
  color: inherit;
}
</style>
