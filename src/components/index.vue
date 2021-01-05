<template>
    <div class="root">
        <kinesis-container class="container">
            <kinesis-element :strength="30">
                <h1 class="title1">CONTINENTAL GT </h1>
            </kinesis-element>
            <kinesis-element :strength="60">
                <p class="content1">With its 6.0 litre, twin-turbocharged W12 engine, a step-change in technology<br> 
                and a truly stunning design language, the Continental GT is unmatched<br>
                in its class. This Bentley GT* coupé is the quintessential grand<br>
                tourer – phenomenally powerful, beautifully<br>
                designed and exquisitely crafted.</p>
            </kinesis-element>
        </kinesis-container>
    </div>
</template>

<script>
export default {
    name: 'index',
    data: () => ({

    })
}
</script>

<style scoped>
    .container {
        background-color: rgba(255, 255, 255, 0.7);
        color: black;
        padding: 50px;
    }
</style>