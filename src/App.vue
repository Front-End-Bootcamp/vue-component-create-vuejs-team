<script setup>
import Popup from './components/Popup.vue';

</script>

<template>
  <div class="container">
    <Popup class="v1"
      text="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum"
      header="Bu bir başlık"
      srcImage="https://picsum.photos/200/300"
      buttonText="textBlack" 
      buttonColor="blue">
    </Popup>

    <Popup class="v2"
      text="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries."
      header="Başlık" 
      srcImage="https://picsum.photos/200/300" 
      srcVideo="" 
      heightVideo="" 
      widthVideo="" 
      typeVideo=""
      buttonText="textBlack" 
      buttonColor="red">
    </Popup>
  </div>
</template>

<style scoped>
.v1 {
  width: 600px;
  left: 350px;
}

.v2 {
  width: 600px;
  left: 1170px;
}

.container {
  width: 100%;
  height: 100%;
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  background-color: rgb(192, 192, 192);
}
</style>
