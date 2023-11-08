<template>
  <h1>{{isUppercase ? message.toUpperCase() : message}}</h1>
  <p v-if="true">{{ text }}</p>
  <h2 v-html="html"></h2>
  <a :href="link.url" :target="link.target" :tabindex="link.tabindex">{{link.title}}</a>
  <input v-model="name" />
</template>
<script setup>
  const message = 'some new message';
  const isUppercase = true;
  const text = 'v-text interpolation';
  const html = '<strong>v-html directive</strong>';
  const link = {
    title: "Go to Google",
    url: 'https://google.com',
    tabindex: 1,
    target: '_blank',
  };


</script>
<style></style>
