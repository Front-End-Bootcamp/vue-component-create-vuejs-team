<script setup>
import Popup from "./components/Popup.vue";
</script>

<template>
	<div class="container">
		<Popup
			class="TTA"
			text="default text"
			header="Başlık"
			buttonText="textWhite"
			buttonColor="green"
			:showClose="false"
			:showAccept="true"
		>
			<p>
				Lorem Ipsum is simply dummy text of the printing and typesetting
				industry. Lorem Ipsum has been the industry's standard dummy text ever
				since the 1500s, when an unknown printer took a galley of type and
				scrambled it to make a type specimen book.
			</p>
		</Popup>

		<Popup
			class="TIC"
			header="Başlık"
			buttonText="textBlack"
			buttonColor="red"
			:showClose="true"
			:showAccept="false"
		>
			<img src="/vite.svg" />
		</Popup>

		<Popup
			class="VTTC"
			text="default text"
			header="Başlık"
			buttonText="textBlack"
			buttonColor="red"
			:showClose="true"
			:showAccept="false"
		>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?
			</p>
			<video class="video" autoplay>
				<source src="/punisher.mp4" type="video/mp4" />
			</video>
			<img src="/vite.svg" />
		</Popup>

		<Popup
			class="ITTC"
			text="default"
			header="Başlık"
			buttonText="textBlack"
			buttonColor="red"
			:showClose="true"
			:showAccept="false"
		>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. At, adipisci?
			</p>

			<img src="/vite.svg" />
		</Popup>

		<Popup
			class="IA"
			text=""
			header=""
			buttonText="textBlack"
			buttonColor="green"
			:showClose="false"
			:showAccept="true"
		>
			<img src="https://picsum.photos/290/290" />
		</Popup>

		<Popup
			class="IAC"
			text=""
			header=""
			buttonText="textBlack"
			buttonColor="green"
			:showClose="false"
			:showAccept="true"
		>
			<img src="https://picsum.photos/290/290" />
		</Popup>

		<Popup
			class="TTAC"
			text=""
			header="TİTLE"
			buttonText="textBlack"
			buttonColor="red"
			:showClose="true"
			:showAccept="true"
		>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta,
				facilis? Ex, qui? Minima dolorum quisquam quas quod iste, nisi nemo
				rerum vitae ipsa illum quaerat tenetur temporibus amet deserunt fugit!
			</p>
			<img src="" />
		</Popup>

		<Popup
			class="TTC"
			text=""
			header="TİTLE"
			buttonText="textBlack"
			buttonColor="red"
			:showClose="true"
			:showAccept="false"
		>
			<p>
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta,
				facilis? Ex, qui? Minima dolorum quisquam quas quod iste, nisi nemo
				rerum vitae ipsa illum quaerat tenetur temporibus amet deserunt fugit!
			</p>
			<img src="" />
		</Popup>
	</div>
</template>

<style scoped>
.video {
	width: 70%;
	height: 70%;
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

.container::-webkit-scrollbar{
	background: #eee;
	width: 12px;
	height: 12px;
	border-radius: 4px 4px;
}

.container::-webkit-scrollbar-corner {
	background: #eee;

}

.container::-webkit-scrollbar-thumb{
	background: red;
	border-radius: 6px;
}
.VTTC {
	margin: auto;
	left: 1000px;
}
.ITTC {
	margin: auto;
	left: 600px;
}
.TTA {
	margin: auto;
	left: 180px;
}

.TIC {
	margin: auto;
	left: 1360px;
}

.IA {
	top: 90%;
	left: 180px;
}

.IAC {
	top: 90%;
	left: 600px;
}

.TTAC {
	top: 90%;
	left: 1000px;
}

.TTC {
	top: 90%;
	left: 1360px;
}
</style>
