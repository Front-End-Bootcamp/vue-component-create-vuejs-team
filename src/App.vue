<script setup>
import Popup from './components/Popup.vue';
import { ref } from "vue"

const showvideoImage = ref(false)
const showtextTitle = ref(false)
const showtitleImage = ref(false)
const showtitletextImage = ref(false)

const showvideoimageHandler = () =>{
  showvideoImage.value = true
}

const showtexttitleHandler = () =>{
  showtextTitle.value = true
}

const showtitleimageHandler = () => {
  showtitleImage.value = true
}

const showtitletextimageHandler = () => {
  showtitletextImage.value = true
}

</script>


<template>
  <div class="container">
     <Popup v-if="showtextTitle" class="TTA"
      text="default"
      header="Title"
      buttonText="textWhite" 
      buttonColor="green"
      :showClose="false"
      :showAccept="true">
      <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
    </Popup>

    <Popup v-if="showtitleImage" class="TIC"
      header="Title"  
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">
      <img src="/vite.svg">
    </Popup> 

    <Popup v-if="showvideoImage" class="VTTC"
      text="default"
      header="Title" 
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">

      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?</p>
      <video class="video" controls autoplay>
        <source src="/punisher.mp4" type="">
      </video>
      <img class="img" src="/vite.svg">
    </Popup>

    <Popup v-if="showtitletextImage" class="ITTC"
      text="default"
      header="Title" 
      buttonText="textBlack" 
      buttonColor="red"
      :showClose="true"
      :showAccept="false">

      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?</p>
      
      <img src="/vite.svg">
    </Popup>


    <button @click="showvideoimageHandler">Show Video+Image+Text Popup</button>
    <button @click="showtexttitleHandler">Show Text+Title Popup</button>
    <button @click="showtitleimageHandler">Show Title+Image Popup</button>
    <button @click="showtitletextimageHandler">Show Title+Text+Image</button>

  </div>


</template>


