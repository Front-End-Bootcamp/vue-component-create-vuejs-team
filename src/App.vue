<script setup>
import Popup from './components/Popup.vue';
import { ref } from "vue"

const showvideoImage = ref(false)
const showtextTitle = ref(false)
const showtitleImage = ref(false)
const showtitletextImage = ref(false)
const showVideo = ref(false)
const showVideoAccept = ref(false)
const showvideoacceptClose = ref(false)



// Functions
const showvideoimageHandler = () => {
	showvideoImage.value = true
}

const showtexttitleHandler = () => {
	showtextTitle.value = true
}

const showtitleimageHandler = () => {
	showtitleImage.value = true
}

const showtitletextimageHandler = () => {
	showtitletextImage.value = true
}


const showvideoHandler = () => {
	showVideo.value = true
}

const showvideoacceptHandler = () => {
	showVideoAccept.value = true
}

const showvideoacceptcloseHandler = () => {
	showvideoacceptClose.value = true
}

</script>


<template>
	<!-- Popups Begin -->

	<div class="container">
		<Popup
		 v-if="showtextTitle"
		 text="default"
		 header="Title"
		 buttonText="textWhite" 
		 buttonColor="green"
		 :showClose="false" 
		 :showAccept="true">
			<p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's
				standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make
				a type specimen book.</p>
		</Popup>

		<Popup v-if="showtitleImage" 
			header="Title" 
			buttonText="textBlack" 
			buttonColor="red" 
			:showClose="true"
			:showAccept="false">
			<img src="/vite.svg">
		</Popup>

		<Popup v-if="showvideoImage"
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

		<Popup v-if="showtitletextImage" 
		 	text="default" 
		 	header="Title"
		  buttonText="textBlack" 
			buttonColor="red"
			:showClose="true" 
			:showAccept="false">

			<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?</p>

			<img src="/vite.svg">
		</Popup>

		<Popup v-if="showVideo" 
			buttonText="textBlack" 
			buttonColor="red" 
			:showClose="true" 
			:showAccept="false">
			<video class="video" controls autoplay>
				<source src="/punisher.mp4" type="">
			</video>
		</Popup>

		<Popup v-if="showVideoAccept"
			buttonText="textWhite"
		  buttonColor="green" 
			:showClose="false" 
			:showAccept="true">
			<video class="video" controls autoplay>
				<source src="/punisher.mp4" type="">
			</video>
		</Popup>

		<Popup v-if="showvideoacceptClose" 
			buttonText="textWhite" 
			buttonColor="green" 
			:showClose="true" 
			:showAccept="true">
			<video class="video" controls autoplay>
				<source src="/punisher.mp4" type="">
			</video>
		</Popup>
<!-- Popups End -->

		<!-- Butons Begin -->

		<button @click="showvideoimageHandler">Show Video+Image+Text Popup</button>
		<button @click="showtexttitleHandler">Show Text+Title Popup</button>
		<button @click="showtitleimageHandler">Show Title+Image Popup</button>
		<button @click="showtitletextimageHandler">Show Title+Text+Image</button>
		<button @click="showvideoHandler">Show Video Close Popup</button>
		<button @click="showvideoacceptHandler">Show Video Accept Popup</button>
		<button @click="showvideoacceptcloseHandler">Show Video Accept Close Popup</button>

		<!-- Butons End -->
	</div>


</template>

<style scoped>
.img {
	width: 50px;
}

.video {
	width: 300px;
	height: 200px;
}

button {
	background-color: #acd01e;
	border: 0 solid #E5E7EB;
	box-sizing: border-box;
	color: #000000;
	display: flex;
	font-family: ui-sans-serif, system-ui, -apple-system, system-ui, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol", "Noto Color Emoji";
	font-size: 1rem;
	font-weight: 700;
	justify-content: center;
	line-height: 1.75rem;
	padding: .75rem 1.65rem;
	position: relative;
	text-align: center;
	text-decoration: none #000000 solid;
	width: 100%;
	max-width: 460px;
	cursor: pointer;
	transform: rotate(-2deg);
	user-select: none;
	-webkit-user-select: none;
	touch-action: manipulation;
	top: 150px;
}

button:focus {
	outline: 0;
	color: #ffffff;
}

button:after {
	content: '';
	position: absolute;
	border: 1px solid #000000;
	bottom: 4px;
	left: 4px;
	width: calc(100% - 1px);
	height: calc(100% - 1px);
}

button:hover:after {
	bottom: 2px;
	left: 2px;
}

button:hover {
	transform: translate(30px, -20px);
	transition: all 0.3s ease;
}

@media (min-width: 768px) {
	button {
		padding: .75rem 3rem;
		font-size: 1.25rem;
	}
}
</style>


