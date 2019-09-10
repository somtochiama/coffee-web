<template>
    <button :class="[{'small': small},'btn', 'mt-5']">👉 {{ text}}</button>        
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: "Shop Now"
    },
    small: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.btn {
  background-color: #ffcf59;
  padding: 10px 40px;
  border-radius: 30px;
}

button.small {
  font-size: 15px;
  padding: 7px 30px;
  margin-top: 0 !important;
}
</style>