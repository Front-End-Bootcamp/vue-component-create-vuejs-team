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
<style  scoped>

.red {
    background-color: red;
}

.blue {
    background-color: blue;
}

.green {
    background-color: green;
}

.textBlack {
    color: rgb(0, 0, 0);
}

.textWhite {
    color: rgb(255, 255, 255);
}

.button {
    border: none;
    color: white;
    padding: 10px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;

}

.mask {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(194, 141, 60, 0.5);

}

.card {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    background: rgb(237, 252, 196);
    background: linear-gradient(0deg, rgba(237, 252, 196, 1) 0%, rgba(253, 187, 45, 1) 100%);
    border: 1px solid red;
    text-align: center;
    padding: 5px;
    width: 300px;
    position: fixed;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
}
</style>

