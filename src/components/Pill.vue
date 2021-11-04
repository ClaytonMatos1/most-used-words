<template>
    <div class="pill">
        <span class="name">{{ name }}</span>
        <span class="amount">{{ amount }}</span>
    </div>
</template>

<script>
export default {
    name: "pill",
    props: {
        name: {
            type: String,
            default: '',
        },
        amount: {
            type: Number,
            default: 0,
        },
    },
};
</script>

<style lang="scss" scoped>
.pill {
    display: flex;
    align-items: center;
    margin: 10px;
    height: 55px;
    border-radius: 30px;
    font-size: 1.3rem;
    font-weight: bold;
    background-color: #dc143c;
    color: #ffffff;

    .name {
        margin-left: 15px;
    }

    .amount {
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 10px;
        padding: 5px;
        width: 35px;
        height: 35px;
        border-radius: 18px;
        font-size: 14px;
        background-color: #ffffff;
        color: #dc143c;
    }
}
</style>