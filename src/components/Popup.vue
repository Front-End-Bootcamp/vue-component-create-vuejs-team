<script setup>

const props = defineProps([
    "text",
    "header",
    "buttonColor",
    "buttonText",
    "showClose",
    "showAccept"
])

</script>

<template>
    <div class="card">
        <div class="card__label">
            <h1 :header="props.header">{{header}}</h1>
        </div>
        <div class="card__wrapper">
					<!-- Text , Image , Video vb. eklemeler yapilabilir. -->
            <slot>
                {{props.text}}
            </slot>
        </div>
        <div class="card__footer">
            <button v-if="props.showAccept" class="button" :class="[props.buttonColor, props.buttonText]">Accept</button>
            <button v-if="props.showClose" class="button" :class="[props.buttonColor, props.buttonText]">Close</button>
        </div>
    </div>
</template>


<style lang="scss" scoped>
.card {
    position: fixed;
    left: 50%;
    top: 40%;
    transform: translate(-50%, -50%);
    width: 100%;
    height: 100%;
    z-index: 999;

    &__label {
        position: absolute;
        width: 290px;
        height: 100px;
        display: flex;
        align-items: stretch;
        justify-content: space-around;
        left: 50%;
        top: 40%;
        padding: 5px;
        transform: translate(-50%, -50%);
        background-color: antiquewhite;
    }

    &__wrapper {
        position: absolute;
        width: 290px;
        height: 280px;
        background-color: antiquewhite;
        display: inline-block;
        left: 50%;
        top: 65%;
        transform: translate(-50%, -50%);
        padding: 5px;
        overflow: hidden;
        border-top: 1px dashed brown;
        margin-top: 12px;
    }

    &__footer {
        position: absolute;
        width: 290px;
        height: 40px;
        background-color: antiquewhite;
        border-top: 1px dashed brown;
        left: 50%;
        top: 86%;
        transform: translate(-50%, -50%);
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 5px;
        margin-top: 30px;
    }
}
.button {
    // Default
    background-color: #000000;
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
</style>