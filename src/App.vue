<script setup>
import Popup from './components/Popup.vue';
</script>

<template>
  <div class="container">
    <Popup class="TTA"
      text="default text"
      header="Başlık"
      buttonText="textWhite" 
      buttonColor="green"
      :showClose="false"
      :showAccept="true">
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
    </Popup>

    <Popup class="TIC"
      header="Başlık"  
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">
      <img src="/vite.svg">
    </Popup>

    <Popup class="VTTC"
      text="default text"
      header="Başlık" 
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">

      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?</p>
			<video  class="video" autoplay>
  			<source src="/punisher.mp4" type="video/mp4">
  		</video>
      <img src="/vite.svg">
    </Popup>

    <Popup class="ITTC"
      text="default"
      header="Başlık" 
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">

      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?</p>
      
      <img src="/vite.svg">
    </Popup>
  </div>
</template>

<style scoped>

.video {
    width: 70%;
    height: 70%;
 }

 .VTTC{
  left: 1000px;
 }
.ITTC{
  left: 600px;
}
.TTA {
  left: 180px;
}

.TIC {
  left: 1360px;
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
