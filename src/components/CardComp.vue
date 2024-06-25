<template>
    <div :class="['card', genderClass]">
      <slot name="header"></slot>
      <slot></slot>
    </div>
  </template>
  <script>
  export default {
    props: {
      gender: {
        type: String,
        required: true
      }
    },
    computed: {
      genderClass() {
        return this.gender === 'male' ? 'red-border' : 'purple-border';
      }
    }
  }
  </script>
  <style scoped>
  .card {
    border: 1px solid;
    padding: 16px;
    margin: 16px;
  }
  .red-border {
    border-color: red;
  }
  .purple-border {
    border-color: purple;
  }
  </style>