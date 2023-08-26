<template>
  <q-page class="column flex-center">
    <q-btn
      @click="onClickTimer()"
      label="스탑와치"
      color="green"
      icon="timer"
    />
    <q-btn
      @click="onClickCountDown()"
      label="카운트다운"
      color="red"
      icon="timer"
    />
  </q-page>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
const $router = useRouter();

const count = ref(0);

const min = -5;
const max = 5;

const onClickTimer = () => {
  //alert('timer');
  console.log('onClickTimer');
  $router.push('/stopwatch');
};
const onClickCountDown = () => {
  //alert('timer');
  console.log('onClickTimer');
  $router.push('/countdown');
};
</script>
