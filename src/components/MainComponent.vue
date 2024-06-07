<template>
  <div class="Main-container">
    <div class="card-model">
      <iframe :src="props.data.link" style="width: 100%; height: 100%; border: none;"/>
    </div>
    <div class="card-info">
      <div class="info-name">{{ props.data.name }}</div>
      <div class="info-desription">
        {{ props.data.description }}
      </div>
    </div>    
  </div>
</template>

<script setup lang="ts">
// eslint-disable-next-line no-undef
const props = defineProps<{data: {
  name: string,
  description: string,
  link: string
}}>()


</script>

<style scoped lang="scss">
.Main-container {
  max-width: 70vw;
  height: 28vh;
  border: 2px solid black;
  border-radius: 4px;
  padding: 16px;
  display: flex;
  background-color: rgba(255, 255, 255, 0.547);
  backdrop-filter: blur(9px);
  transition: ease 0.4s;
  &:hover{
  background-color: rgba(190, 190, 190, 0.547);
  /* backdrop-filter: blur(4px); */
  }
}

.card-model {
  position: relative;
  min-width: 30%;
  min-height: 100%;
  &::after {
    content: "";
    position: absolute;
    width: 1px;
    /* height: 100%; */
    height: calc(100% + 32px);
    top: -16px;
    right: -16px;
    background-color: black;
  }
}

.card-info {
  margin-left: 32px;
  text-align: left;
}

.info-name {
  font-weight: bold;
  margin-bottom: 10px;
  font-size: 1.3rem;
}

.info-desription {
  width: 100%;
  height: 100%;
  font-size: 1.1rem;
}


</style>
