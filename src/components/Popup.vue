<script setup>
import { ref } from "vue"

const close = ref(true)

const props = defineProps([
	"text",
	"header",
	"buttonColor",
	"buttonText",
	"showClose",
	"showAccept"
])


const closeHandler = () => {
	close.value = false
}

</script>

<template>
	<div class="mask" v-if="close"></div>
	<div class="card" v-if="close">

		<div class="card__label">
			<h1 :header="props.header">{{header}}</h1>
		</div>
		<div class="card__wrapper">
			<slot>
				{{props.text}}
			</slot>
		</div>
		<div class="card__footer">
			<button v-if="props.showAccept" @click="closeHandler" class="button"
				:class="[props.buttonColor, props.buttonText]">Accept</button>
			<button v-if="props.showClose" @click="closeHandler" class="button"
				:class="[props.buttonColor, props.buttonText]">Close</button>
		</div>

	</div>

</template>


