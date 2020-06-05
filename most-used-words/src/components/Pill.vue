<template>
    <div class="pill">
        <span class="name">{{ name }}</span>
        <span class="amount">{{ amount }}</span>
    </div>
</template>

<script>
export default {
    props: ['name', 'amount']
}
</script>

<style scoped>

    @keyframes shadow-fade {
        to {box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);}
    }

    .pill {
        background-color: teal;
        color: white;
        
        margin: 10px;
        height: 55px;
        border-radius:30px;
        
        font-size: 1.3rem;
        font-weight: bold;

        display: flex;
        align-items: center;
        
    }

    .pill:hover{
        animation-name: shadow-fade;
        animation-duration: 1s;
        animation-timing-function: ease-in-out;
        animation-fill-mode: both;
        animation-direction: alternate;
    }

    .pill .name{
        margin-left: 15px;
    }

    .pill .amount{
        margin: 10px;
        padding: 5px;
        height: 35px;
        width: 35px;
        border-radius: 18px;

        background-color: tomato;
        font-size: 14px;
        
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>